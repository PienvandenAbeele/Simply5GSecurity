---
title: Confidentiality
permalink: /docs/confidentiality/
---
<style>body {text-align: justify}</style>

**Definition of Confidentiality:**
*The protection of data, provides access for those who are allowed to see it while disallowing others from learning anything about its content.*


<div class="row">
    <div style="text-align: justify" class="col-md-5">
        <br>
        In the mobile network, confidentiality is important to ensure no one but the required parties can see the information. For example, when enter your password to log into your bank account, if an attacker were to snoop around on the network, they can see the traffic, but do not know what it says or who it is for, and thus they can not see your password. This is established by encrypting the traffic data. 
    </div>
    <div class="col-md-7">
        <img src="{{ "/assets/img/Sec/Conf.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

Confidentiality is a principle of information security that refers to protecting information from unauthorised access or disclosure. Confidentiality is often achieved through the use of encryption. In a 5G network, there may be a wide range of sensitive information that needs to be protected against unauthorised, such as your permanent identity or user data. In general, we have the following requirements for confidentiality.

| Name                      | Explanation                                                                       | 3GPP Specifications |
| -------------             | ---------                                                                         | -------------- |
|Identity confidentiality   |  Identity confidentiality ensures that the user's identity is not revealed to an external attacker. Identity confidentiality is a privacy feature of 5G and is related to the location confidentiality requirement. It prohibits a user from being identified or tracked (in combination with location confidentiality). With 5G, new security features are implemented to ensure identity confidentiality, such as <a href="{{ "/docs/identification/" | relative_url }}">SUCI</a> encryption or increased home control. | 5.2.5 in <a href="https://www.etsi.org/deliver/etsi_ts/133500_133599/133501/17.07.00_60/ts_133501v170700p.pdf" target="_blank" rel="noopener noreferrer">33.501</a> |
|Location confidentiality   | Location confidentiality protects the individual's location information, including their whereabouts and movements. It is vital for the 5G mobile system as our mobile devices (phones or smart watches) are our constant companions. 5G uses improved security features to ensure location (and identity) confidentiality, such as prohibiting the <a href="{{ "/docs/identification/" | relative_url }}">SUPI</a> / IMSI paging. | 5.2.5 in <a href="https://www.etsi.org/deliver/etsi_ts/133500_133599/133501/17.07.00_60/ts_133501v170700p.pdf" target="_blank" rel="noopener noreferrer">33.501</a>|
|Control data confidentiality |  Ensuring the confidentially of the control data confirms that an attacker can not gain any crucial information transported in the control data. This essential information can vary depending on the protocol and network functions and might incorporate key material or user identifiers. 5G uses different measurements to ensure the control data confidentiality depending on the domain and protocol. For example, in the core network, 5G uses the <a href="{{ "/docs/tls/" | relative_url }}">TLS</a> protocol to ensure the confidentiality of control data. The confidentiality of the control data sent over the air can be provided by using RRC-signalling and NAS-signalling encryption. | 5.2.2 & 13.1.0 in <a href="https://www.etsi.org/deliver/etsi_ts/133500_133599/133501/17.07.00_60/ts_133501v170700p.pdf" target="_blank" rel="noopener noreferrer">33.501</a>|
User data confidentiality   | The user data is the data the user sends; this usually includes text messages, phone calls, internet browsing, and app traffic. The 5G system protects the user data through the optional use of encryption on the radio layer transmission. | 5.2.2 in <a href="https://www.etsi.org/deliver/etsi_ts/133500_133599/133501/17.07.00_60/ts_133501v170700p.pdf" target="_blank" rel="noopener noreferrer">33.501</a> |
