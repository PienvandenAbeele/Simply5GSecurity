---
title: Unified Data Management (UDM)
permalink: /docs/udm/
---
<style>body {text-align: justify}</style>

### Description
The UDM stores the security credentials for the users and additional subscription information. Using that information, the UDM provides service for the authentication of subscribers, e.g., ensuring that customers only have access to their subscribed services.

<img src="{{ "/assets/img/5gbasics/udm_sba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

### Interaction with other NFs:

| Consumes services from    | Provides services to  | 
| -------------             |-------------          |
| NRF, UDR, AUSF            | AMF, SMF              |

<img src="{{ "/assets/img/5gbasics/udm_rba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

### Link to the specifications
<a href="https://www.etsi.org/deliver/etsi_ts/129500_129599/129503/17.08.00_60/ts_129503v170800p.pdf">3GPP Specifications</a>

### Security importance
The UDM plays a critical role in ensuring the security and privacy of user data, as it is responsible for storing, processing, and protecting sensitive user information such as subscriber profiles, usage records, and authentication data.