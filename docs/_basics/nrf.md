---
title: Network Repository Function (NRF)
permalink: /docs/nrf/
---

### Description
The Network Repository Function (NRF) keeps track of all the NFs. NFs will register at the NRF and then when a NF needs to talk to another NF, the NRF allows them to discover each other.

<img src="{{ "/assets/img/5gbasics/nrf_sba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

### Interaction with other NFs:

| Consumes services from            | Provides services to  | 
| -------------                     |-------------          |
| UDM, AMF, SMF, UDR, AUSF, UPF     | UDR                   |

<img src="{{ "/assets/img/5gbasics/nrf_rba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

### Link to the specifications
<a href="https://www.etsi.org/deliver/etsi_ts/129500_129599/129510/17.07.00_60/ts_129510v170700p.pdf">3GPP Specifications</a>

### Security importance
The NRF is important for security since it makes sure the correct NFs communicate and validates if the correct NFs are registered.
It is responsible for storing and managing the security policies and configurations that govern access to network resources and services, as well as for enforcing these policies to prevent unauthorised access or tampering with network information.