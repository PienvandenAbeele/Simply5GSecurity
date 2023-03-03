---
title: Authentication and Key Agreement
permalink: /docs/aka/
---
<style>body {text-align: justify}</style>
To achieve secure communication over the network, AKA is used. AKA stands for Authentication and Key Management which is a protocol that involves mutual authentication between the user and the network, and, it also derives crypto keys which in turn protect the data transferred over the <a href="{{ "/docs/core/" | relative_url }}">Control and User plane</a>.

On top of the AKA features which also exist in 4G (User authentication for the network and network authentication for the user, and deriving a common communication crypto key), in 5G AKA introduces new features:

* Increased home control: home network obtains Authentication confirmation
* Serving network authentication by key binding
* Ensuring correct user identity by <a href="{{ "/docs/identification/" | relative_url }}">IMSI</a>/NAI key binding
* Anti-Bidding down Between Architectures by ABBA parameter binding

To achieve this, the 3GPP has defined three different authentication methods, namely:
* 5G-AKA: 5G-Authentication and Key Management
* EAP-AKA: Extensible Authentication Protocol – Authentication and Key Management
* EAP-TLS: Extensible Authentication Protocol – Transport Layer Security

5G-AKA will be explained later on, but first, why do we need these new AKA procedures?

One of the main reasons for designing and deploying a new generation of mobile networks is to address and fix known security issues in the previous generation. For 5G this is no different, as there were multiple security vulnerabilities in 4G regarding AKA. A well-known example is network spoofing: An attacker would deploy a fake base station with a stronger signal than the legitimate base station in that area. This would then lure <a href="{{ "/docs/ue/" | relative_url }}">UE</a> to register at the fake base station instead of the legitimate base station, giving the attacker information about the <a href="{{ "/docs/ue/" | relative_url }}">UEs</a>.

### 5G-AKA
<div class="row">
    <div style="text-align: justify" class="col-md-4">
    <br>
        The 5G-AKA procedure happens the moment the <a href="{{ "/docs/amf/" | relative_url }}">AMF</a> receives a signalling message from the <a href="{{ "/docs/ue/" | relative_url }}">UE</a>. This is done with the <a href="{{ "/docs/identification/" | relative_url }}">SUCI</a>.
        As can be seen in the image, the <a href="{{ "/docs/amf/" | relative_url }}">AMF</a> then starts to authenticate the <a href="{{ "/docs/ue/" | relative_url }}">UE</a> by sending an authentication request to the <a href="{{ "/docs/ausf/" | relative_url }}">AUSF</a>, which will first check if the serving network requesting the authentication service is also authorised. 
    </div>
    <div class="col-md-8">
        <img src="{{ "/assets/img/Sec/SUPI_ENCR.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
        <br>
    </div>
</div>
If successful, the <a href="{{ "/docs/ausf/" | relative_url }}">AUSF</a> will then send an authentication request to the <a href="{{ "/docs/udm/" | relative_url }}">UDM</a>. The <a href="{{ "/docs/udm/" | relative_url }}">UDM</a> will then get the <a href="{{ "/docs/identification/" | relative_url }}">SUPI</a> from the <a href="{{ "/docs/identification/" | relative_url }}">SUCI</a> using the SIDF (the SIDF is a function which the <a href="{{ "/docs/udm/" | relative_url }}">UDM</a> uses to decrypt the <a href="{{ "/docs/identification/" | relative_url }}">SUCI</a>). The <a href="{{ "/docs/identification/" | relative_url }}">SUPI</a> is then used to select the authentication method configured for the subscriber, in this case, 5G-AKA.

The <a href="{{ "/docs/udm/" | relative_url }}">UDM</a> will start the 5G-AKA by sending the authentication response back to the <a href="{{ "/docs/ausf/" | relative_url }}">AUSF</a>. This response contains an AUTH Token, <a href="{{ "/docs/identification/" | relative_url }}">SUPI</a>, Crypto token (XRES) (REF), AUSF Key (KAUSF) and some extra data.

The <a href="{{ "/docs/ausf/" | relative_url }}">AUSF</a> will then compute the hash of the expected response token (HXRES) and stores the KAUSF. Next, the authentication response will be sent to the <a href="{{ "/docs/amf/" | relative_url }}">AMF</a>, along with the AUTH Token and the HXRES. Only when the <a href="{{ "/docs/ue/" | relative_url }}">UE</a> Authentication is successful, the <a href="{{ "/docs/identification/" | relative_url }}">SUPI</a> is sent to the <a href="{{ "/docs/amf/" | relative_url }}">AMF</a>.

The <a href="{{ "/docs/amf/" | relative_url }}">AMF</a> stores the HXRES and sends the AUTH token in an authentication request to the <a href="{{ "/docs/ue/" | relative_url }}">UE</a>. The <a href="{{ "/docs/ue/" | relative_url }}">UE</a> can then validate the AUTH token with the secret key it shares with the home network. When successful, the UE will consider the network to be authenticated. However, the <a href="{{ "/docs/ue/" | relative_url }}">UE</a> will continue the authentication by computing and sending the <a href="{{ "/docs/amf/" | relative_url }}">AMF</a> a RES token to the <a href="{{ "/docs/amf/" | relative_url }}">AMF</a>. The <a href="{{ "/docs/amf/" | relative_url }}">AMF</a> will send this RES token to the <a href="{{ "/docs/ausf/" | relative_url }}">AUSF</a> for validation. As mentioned above, if this validation is successful, the <a href="{{ "/docs/ausf/" | relative_url }}">AUSF</a> will send the <a href="{{ "/docs/identification/" | relative_url }}">SUPI</a> of the <a href="{{ "/docs/ue/" | relative_url }}">UE</a> to the <a href="{{ "/docs/amf/" | relative_url }}">AMF</a>.

<div class="row">
    <div style="text-align: justify" class="col-md-5">
        <h3>Algorithms</h3>
        To derive keys certain cryptographic algorithms are used. The 3GPP has defined which algorithms should be used for which services.
    </div>
    <div class="col-md-7">
        <h3>Key Hierarchy</h3>
        See image. The reason there is a key hierarchy is the fact keys are derived from other keys and thus further protecting the master key. If one key gets leaked, it does not reveal the secret key, as it is a derivation. With a deeper key hierarchy, this security feature is even stronger.
    </div>
</div>

<!-- <img src="{{ "/assets/img/Sec/SUCI_Flow.png" | relative_url }}" alt="5G Overview" class="img-responsive center"> -->

<!-- ## Home Control (for the AKA page)

Home control is a new 5G security feature for the AKA that is used to verify the location of a device when it is roaming, i.e., connected to a "visited network". During the Authentication and Key Agreement in the roaming scenario, the home network is able to verify if a UE is actually in the visited network when it receives a request from a visited network. 

Home control was added to address vulnerabilities of 3G and 4G. These vulnerabilities allow attackers to send false messages to the home network, pretending to be visiting the network. These fake messages were used to request sensitive information such as authentication tokens and derived keys. That information could then be used to intercept voice calls and text messages. -->