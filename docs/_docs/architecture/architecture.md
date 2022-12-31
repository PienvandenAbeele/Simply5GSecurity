---
title: 5G Security Architecture
permalink: /docs/architecture/
---
<style>body {text-align: justify}</style>

 <img src="{{ "/assets/img/Sec/Arch.png" | relative_url }}" alt="5G Overview" class="img-responsive center"/> 

ME: Mobile Entity

HE: Home environment

SN: Serving Network

AN: Access Network

USIM: User Subscription Identity Module

In the image, you can see the SN which is the 5G Core and the ME which is the User Equipment. The HE is the home environment, so the 5G entity to which the SN provides services. How these components should communicate is defined by the 3GPP and those are to ensure security in the network. The most important one, which is also used the most, is Network Access Security (I) in the picture. In the words of the 3GPP, it is defined as:

**Network access security (I):** *the set of security features that enable a UE to authenticate and access services via the network securely, including the 3GPP access and Non-3GPP access, and in particular, to protect against attacks on the (radio) interfaces. In addition, it includes the security context delivery from SN to AN for access security.*

Then you also have the SBA Domain Security which is used in the communication with the SN and the HE. This security implementation is important as it defines in what why NFs should communicate with each other inside the SN but also with other network domains. It is defined by the 3GPP as follows:

**SBA domain security (V):** *the set of security features that enables network functions of the SBA architecture to securely communicate within the serving network domain and with other network domains. Such features include network function registration, discovery, and authorisation security aspects, as well as the protection for the service-based interfaces.*

