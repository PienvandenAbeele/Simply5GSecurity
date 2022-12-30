---
title: Session Management Function (SMF)
permalink: /docs/smf/
---

### Description
The SMF collects the information related to all sessions and manages them. The SMF gets information from different NFs and orchestrates those network components based on the requests from the AMF.

<img src="{{ "/assets/img/5gbasics/smf_sba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

### Interaction with other NFs:

| Consumes services from    | Provides services to  | 
| -------------             |-------------          |
| UDM, NRF                  | AMF, UPF              |

<img src="{{ "/assets/img/5gbasics/smf_rba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

### Link to the specifications
<a href="https://www.etsi.org/deliver/etsi_ts/129500_129599/129502/17.06.00_60/ts_129502v170600p.pdf">3GPP Specifications</a>

### Security importance
The SMF handles the information between sessions, and thus also checks the security of sessions. Therefore it is essential for the security of the network that the SMF works.