---
title: Authentication Server Function (AUSF)
permalink: /docs/ausf/
---
<style>body {text-align: justify}</style>

### Description
The AUSF authenticates the UE. It stores the keys exchanged between the 5G network and the UE. When the AMF needs to authenticate the UE connected to the network, it will ask the AUSF.

<img src="{{ "/assets/img/5gbasics/ausf_sba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

### Interaction with other NFs:

| Consumes services from            | Provides services to  | 
| -------------                     |-------------          |
| UDM, AMF                          | NRF                   |

<img src="{{ "/assets/img/5gbasics/ausf_rba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

### Link to the specifications
<a href="https://www.etsi.org/deliver/etsi_ts/129500_129599/129509/17.07.00_60/ts_129509v170700p.pdf">3GPP Specifications</a>

### Security importance
Since the AUSF is responsible for verifying the identity of devices connecting with the Core Network, it is an essential part of the security since it will detect devices which are not allowed to connect for example.
In addition to its role in access control and authentication, the AUSF also helps to protect against potential security threats by implementing various security measures such as encryption, firewalls, and intrusion detection systems. These measures help to protect against attacks such as man-in-the-middle attacks, denial-of-service attacks, and other types of cyber threats.