---
title: Introduction
permalink: /docs/reqintro/
---
<style>body {text-align: justify}</style>

Security requirements are based on the CIA triad, which stands for Confidentiality, Integrity and Availability. 
These three categories are used to find vulnerabilities and to create solutions. The reason the CIA triad is used in (almost) all security specifications of systems, is that it splits up the possible threats. For each of the three categories, one can decide if it is needed for the specific system. 

<img src="{{ "/assets/img/Sec/CIA_TRIAD.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

For example, the distribution of a software update by the mobile network operator. Integrity is very important since the content of the update send over the network, can not be tampered with or it will not work anymore. However, confidentiality is not as important, since it is a publicly available update, which the provider wants everyone to have.

Therefore CIA is also used in the <a href="https://www.etsi.org/deliver/etsi_ts/129500_129599/129509/17.07.00_60/ts_129509v170700p.pdf">3GPP Specifications</a> to define which security properties each component of the 5G network needs to have. For example, the UE needs to have integrity and availability, and for each of the NFs, it is defined which of the CIAs they need to provide.


