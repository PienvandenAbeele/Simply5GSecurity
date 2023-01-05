---
title: 5G Security Architecture
permalink: /docs/architecture/
---
<style>body {text-align: justify}</style>

The security architecture of 5G can be shown in the following way:

<img src="{{ "/assets/img/Sec/Arch.png" | relative_url }}" alt="5G Overview" class="img-responsive center"/> 

Some definitions of the acronyms:

ME: Mobile Entity

HE: Home environment

SN: Serving Network

AN: Access Network

USIM: User Subscription Identity Module

Then you also have 3GPP AN and Non-3GPP AN. These two are both Access Networks, but the Non-3GPP is an access network which does not follow 3GPP specifications.

In the image you can see the SN which is the 5G Core and the ME which is the User Equipment. The HE is the home environment, so the 5G entity to which the SN provides services to. How these components should communicate is defined by the 3GPP and those are to ensure security in the network. We will explain (I) (link) and (V) (link) in more depth, but first lets see what they all do:

The most important one, which is also used to most, is Network Access Security (I) in the picture. In the words of the 3GPP it is defined as: 

- Network access security (I): the set of security features that enable a UE to authenticate and access services via the network securely, including the 3GPP access and Non-3GPP access, and in particularly, to protect against attacks on the (radio) interfaces. In addition, it includes the security context delivery from SN to AN for the access security.
- Network domain security (II): the set of security features that enable network nodes to securely exchange signalling data and user plane data.
- User domain security (III): the set of security features that secure the user access to mobile equipment.
- Application domain security (IV): the set of security features that enable applications in the user domain and in the provider domain to exchange messages securely. Application domain security is out of scope of the present
document.

Then you also have the SBA Domain Security which is used in the communication with the SN and the HE. This security implementation is also important as it defines in what why NFs should communicate with each other inside the SN but also to other network domains. It is defined by the 3GPP as follows:

- SBA domain security (V): the set of security features that enables network functions of the SBA architecture to securely communicate within the serving network domain and with other network domains . Such features include network function registration, discovery, and authorisation security aspects, as well as the protection for the service-based interfaces.

(IV) is not shown on the image, and the reason for this is that (IV) is the communication between User Application and Server Application, which is the high level, but what happens underneath is what is interesting and those are the things we see in the image shown. 

<a href="https://www.etsi.org/deliver/etsi_ts/133500_133599/133501/17.07.00_60/ts_133501v170700p.pdf">3GPP Specifications</a> of the security architecture.