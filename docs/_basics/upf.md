---
title: User Plane Function (UPF) 
permalink: /docs/upf/
---
<style>body {text-align: justify}</style>

### Description
The User Plane Function (UDF) interconnects the Data Network with the 5G core.
The UDF sends traffic packets forward and makes sure they are sent to the correct place. It also inspects said packets and makes sure the Quality of Service is upheld (QoS).

<img src="{{ "/assets/img/5gbasics/upf_sba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

### Interaction with other NFs:

| Consumes services from    | Provices services to  | 
| -------------             |-------------          |
| SMF                       | ??                    |

<img src="{{ "/assets/img/5gbasics/upf_rba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

### Link to the specifications
<a href="https://www.etsi.org/deliver/etsi_ts/133500_133599/133513/17.00.00_60/ts_133513v170000p.pdf">3GPP Specifications</a>

### Security importance
It ensures the QoS of internet packets that are sent. It has to protect the messages being sent between the Core, DN and UE.
