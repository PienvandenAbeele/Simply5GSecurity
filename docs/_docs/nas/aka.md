---
title: Authentication and Key Agreemanagemnt
permalink: /docs/aka/
---
<style>body {text-align: justify}</style>
To achieve secure communication over the network, AKA is used. AKA stands for Authentication and Key Management which is a protocol that involves mutual authentication between the user and the network, and, it also derives crypto keys which in turn protect the data transferred over the Control and User plane.

On top of the AKA features which also exist in 4G (User authentication for the network and network authentication for the user, and deriving a common communication crypto key), in 5G AKA introduces new features:

* Increased home control: home network obtains Authentication confirmation
* Serving network authentication by key binding
* Ensuring correct user identity by IMSI/NAI key binding
* Anti-Bidding down Between Architectures by ABBA parameter binding

To achieve this, the 3GPP has defined three different authentication methods, namely:
* 5G-AKA: 5G-Authentication and Key Management
* EAP-AKA: Extensible Authentication Protocol – Authentication and Key Management
* EAP-TLS: Extensible Authentication Protocol – Transport Layer Security

5G-AKA will be explained later on, but first, why do we need these new AKA procedures?

One of the main reasons for designing and deploying a new generation of mobile networks is to address and fix known security issues in the previous generation. For 5G this is no different, as there were multiple security vulnerabilities in 4G regarding AKA. A well-known example is network spoofing: An attacker would deploy a fake base station with a stronger signal than the legitimate base station in that area. This would then lure UE to register at the fake base station instead of the legitimate base station, giving the attacker information about the UEs.

### 5G-AKA

The 5G-AKA procedure happens the moment the AMF receives a signalling message from the UE. This is done with the SUCI (ref to SUCI).
As can be seen in the image, the AMF then starts to authenticate the UE by sending an authentication request to the AUF, which will first check if the SN requesting the authentication service is also authorised.

If successful, the AUSF will then send an authentication request to the UDM. The UDM will then get the SUPI from the SUCI using the SIDF (!!!!!!!). The SUPI is then used to select the authentication method configured for the subscriber, in this case, 5G-AKA.

The UDM will start the 5G-AKA by sending the authentication response back to the AUSF. This response contains an AUTH Token, SUPI, Crypto token (XRES) (REF), AUSF Key (KAUSF) and some extra data.

<img src="{{ "/assets/img/sec/SUCI_Flow.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

The AUSF will then compute the hash of the expected response token (HXRES) and stores the KAUSF. Next, the authentication response will be sent to the AMF, along with the AUTH Token and the HXRES. Only when the UE Authentication is successful, the SUPI is sent to the AMF.
The AMF stores the HXRES and sends the AUTH token in an authentication request to the UE. The UE can then validate the AUTH token with the secret key it shares with the home network. When successful, the UE will consider the network to be authenticated. However, the UE will continue the authentication by computing and sending the AMF a RES token to the AMF. The AMF will send this RES token to the AUSF for validation. As mentioned above, if this validation is successful, the AUSF will send the SUPI of the UE to the AMF.

<!-- Small side note about ABBA:
The parameter that provides anti-bidding down protection of security features against security features introduced in a higher release to a lower release and indicates the security features that are enabled in the current network. -->

### Algorithms
To derive keys certain cryptographic algorithms are used. The 3GPP has defined which algorithms should be used for which services.

### Key Hierarchy
See image. The reason there is a key hierarchy is the fact keys are derived from other keys and thus further protecting the master key. If one key gets leaked, it does not reveal the secret key, as it is a derivation. With a deeper key hierarchy, this security feature is even stronger.

<img src="{{ "/assets/img/sec/SUPI_ENCR.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

