---
title: User Data Repository (UDR)
permalink: /docs/udr/
---
<style>body {text-align: justify}</style>

### Description
The UDR is the database of the 5G Core. It is used by NFs to store their data. It offers storage for subscription, authentication, application, etc in a unified database.

<img src="{{ "/assets/img/5gbasics/udr_sba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

### Interaction with other NFs:

| Consumes services from    | Provides services to  | 
| -------------             |-------------          |
| NRF                       | UDM, NRF              |

<img src="{{ "/assets/img/5gbasics/udr_rba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

### Link to the specifications
<a href="https://www.etsi.org/deliver/etsi_ts/129500_129599/129504/17.08.00_60/ts_129504v170800p.pdf">3GPP Specifications</a>

### Security importance
Since the UDR stores all the information about the other NFs, it has to store this information safely so it can not be tampered with.
