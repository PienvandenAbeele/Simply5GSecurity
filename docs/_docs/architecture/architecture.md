---
title: 5G Security Architecture
permalink: /docs/architecture/
---
<style>body {text-align: justify}</style>

The 5G security architecture consists of different components. As can be seen in the image you have the different networks and environments. You also have 3GPP AN and Non-3GPP AN. These two are both Access Networks, but the Non-3GPP is an access network which does not follow 3GPP specifications.
<div class="row">
    <div style="text-align: justify" class="col-md-4">
        <br>
        <br>
        <ul>
        <li>ME: Mobile entity</li>
        <li>HE: Home environment</li>
        <li>SN: Serving network</li>
        <li>AN: Access network</li>
        <li>USIM: User subscription identity module</li>
        </ul>
    </div>
    <div class="col-md-8">
        <img src="{{ "/assets/img/Sec/Arch.png" | relative_url }}" alt="5G Overview" class="img-responsive center"/> 
        <br>
    </div>
</div>

In the image you can see the SN which is the 5G Core and the ME which is the <a href="{{ "/docs/ue/" | relative_url }}">User Equipment</a>. The HE is the home environment, so the 5G entity to which the SN provides services to. How these components should communicate is defined by the 3GPP and those are to ensure security in the network. We will explain <a href="{{ "/docs/nasintro/" | relative_url }}">Network Access Security (I)</a> and <a href="{{ "/docs/sbaintro/" | relative_url }}">SBA domain security (V)</a> in more depth, but first lets see what they all do:

The most important one, which is also used to most, is <a href="{{ "/docs/nasintro/" | relative_url }}">Network Access Security (I)</a> in the picture. In the words of the 3GPP it is defined as: 

- <a href="{{ "/docs/nasintro/" | relative_url }}">Network Access Security (I)</a>: the set of security features that enable a <a href="{{ "/docs/ue/" | relative_url }}">UE</a> to authenticate and access services via the network securely, including the 3GPP access and Non-3GPP access, and in particularly, to protect against attacks on the (radio) interfaces. In addition, it includes the security context delivery from SN to AN for the access security.
- Network domain security (II): the set of security features that enable network nodes to securely exchange signalling data and user plane data.
- User domain security (III): the set of security features that secure the user access to mobile equipment.
- Application domain security (IV): the set of security features that enable applications in the user domain and in the provider domain to exchange messages securely. Application domain security is out of scope of the present
document.

Then you also have the <a href="{{ "/docs/sbaintro/" | relative_url }}">SBA domain security (V)</a> which is used in the communication with the SN and the HE. This security implementation is also important as it defines in what why <a href="{{ "/docs/core/" | relative_url }}">NFs</a> should communicate with each other inside the SN but also to other network domains. It is defined by the 3GPP as follows:

- <a href="{{ "/docs/sbaintro/" | relative_url }}">SBA domain security (V)</a>: the set of security features that enables network functions of the SBA architecture to securely communicate within the serving network domain and with other network domains . Such features include network function registration, discovery, and authorisation security aspects, as well as the protection for the service-based interfaces.

Application domain security (IV) is not shown on the image, and the reason for this is that (IV) is the communication between User Application and Server Application, which is the high level, but what happens underneath is what is interesting and those are the things we see in the image shown. For the full specifications, <a href="https://www.etsi.org/deliver/etsi_ts/133500_133599/133501/17.07.00_60/ts_133501v170700p.pdf" target="_blank" rel="noopener noreferrer">click here</a>.
