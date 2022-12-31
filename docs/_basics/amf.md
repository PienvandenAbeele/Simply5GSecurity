---
title: Access and Mobility Management Function (AMF)
permalink: /docs/amf/
---
<style>body {text-align: justify}</style>

### Description
The AMF is responsible for the connection and management between the 5G core network, and the UE. The AMF will keep track of who is allowed to connect with the 5G network, where the UE is during the connection and if the UE is still reachable. These 4 responsibilities are called (respectfully) Registration Management, Connection Management, Mobility Management and Reachability Management.
<img src="{{ "/assets/img/5gbasics/amf_sba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

### Interaction with other NFs:

| Consumes services from    | Provides services to      | 
| -------------             |-------------              |
| SMF, AMF                  | AMF, SMF, NRF, UDM, AUSF  |

<img src="{{ "/assets/img/5gbasics/amf_rba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

### Link to the specifications
<a href="https://www.etsi.org/deliver/etsi_ts/129500_129599/129518/17.07.00_60/ts_129518v170700p.pdf">3GPP Specifications</a>

### Security importance
The AMF is the point where the UE gets a connection with the 5G Core. It keeps track of who is connected and tries to detect and avoid any suspicious behaviour from UEs.