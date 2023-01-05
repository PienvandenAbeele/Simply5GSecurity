---
title: Access and Mobility Management Function (AMF)
permalink: /docs/amf/
---
<style>body {text-align: justify}</style>

### Description
The AMF is responsible for the connection and management between the 5G core network, and the UE. The AMF will keep track of who is allowed to connect with the 5G network, where the UE is during the connection and if the UE is still reachable. These 4 responsibilities are called (respectfully) *registration management*, *connection management*, *mobility management* and *reachability management*.
<img src="{{ "/assets/img/5gbasics/amf_sba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

### Interaction with other NFs:

| Consumes services from    | Provides services to      | 
| -------------             |-------------              |
| SMF, AMF                  | AMF, SMF, NRF, UDM, AUSF  |

<img src="{{ "/assets/img/5gbasics/amf_rba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

### Link to the specifications
<a href="https://www.etsi.org/deliver/etsi_ts/129500_129599/129518/17.07.00_60/ts_129518v170700p.pdf">3GPP Specifications</a>

### Security importance
The AMF is the point where the UE gets a connection with the 5G Core. It keeps track of who is connected and tries to detect and avoid any suspicious behaviour from UEs. The AMF checks (with information it gets from other NFs) if the UE that is connecting, is a legit customer and what services they can use. If an UE asks for a service it has no access to, the AMF will detect this, by checking the information it gets from the <a href="{{ "/docs/ausf/" | relative_url }}">AUSF</a>.
