---
title: Security Activation
permalink: /docs/sa/
---
<style>body {text-align: justify}</style>

Once AKA has been completed, both the UE and the CN have a shared key. From this point on, all communication between the UE and the CN will be done over NAS and all communication between the UE and the gNodeB will done over RRC. If you take a look at the image, you see the flow between the UE, gNodeB and CN. Here you see the Access Stratum and Non-Access Stratum as well, showing the division of NAS and RRC. At the NAS communication, NAS Security Mode Command ensures confidentiality and there is integrity protection, at the <a href="https://www.etsi.org/deliver/etsi_ts/133500_133599/133501/17.07.00_60/ts_133501v170700p.pdf">3GPP Specifications</a> at 6.7.2, information can be found on which algorithms should be used. Then at the AS communication, RRC Security Mode Command offers the same security features as NAS, namely confidentiality and integrity, which can be found in <a href="https://www.etsi.org/deliver/etsi_ts/133500_133599/133501/17.07.00_60/ts_133501v170700p.pdf">3GPP Specifications</a> at 6.7.4.

<img src="{{ "/assets/img/Sec/sa.png" | relative_url }}" alt="5G Overview" class="img-responsive center">       
