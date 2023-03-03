---
title: Security Activation
permalink: /docs/sa/
---
<style>body {text-align: justify}</style>

<div class="row">
    <div style="text-align: justify" class="col-md-5">
        Once <a href="{{ "/docs/aka/" | relative_url }}">Authentication and Key Agreement (AKA)</a> has been completed, both the <a href="{{ "/docs/ue/" | relative_url }}">UE</a> and the <a href="{{ "/docs/core/" | relative_url }}">Core Network</a> have a shared key. From this point on, all communication between the <a href="{{ "/docs/ue/" | relative_url }}">UE</a> and the <a href="{{ "/docs/core/" | relative_url }}">Core Network</a> will be done over NAS and all communication between the <a href="{{ "/docs/ue/" | relative_url }}">UE</a> and the <a href="{{ "/docs/ue/" | relative_url }}">gNodeB</a> will done over RRC. If you take a look at the image, you see the flow between the <a href="{{ "/docs/ue/" | relative_url }}">UE</a>, <a href="{{ "/docs/ue/" | relative_url }}">gNodeB</a> and <a href="{{ "/docs/core/" | relative_url }}">Core Network</a>. Here you see the Access Stratum and Non-Access Stratum as well, showing the division of NAS and RRC.     
    </div>
    <div class="col-md-7" >
        <img src="{{ "/assets/img/Sec/sa.png" | relative_url }}" alt="5G Overview" class="img-responsive center">       
    </div>
</div>
At the NAS communication, NAS Security Mode Command ensures confidentiality and there is integrity protection, at the <a href="https://www.etsi.org/deliver/etsi_ts/133500_133599/133501/17.07.00_60/ts_133501v170700p.pdf" target="_blank" rel="noopener noreferrer">3GPP Specifications</a> at 6.7.2, information can be found on which algorithms should be used. Then at the AS communication, RRC Security Mode Command offers the same security features as NAS, namely confidentiality and integrity, which can be found in <a href="https://www.etsi.org/deliver/etsi_ts/133500_133599/133501/17.07.00_60/ts_133501v170700p.pdf" target="_blank" rel="noopener noreferrer">3GPP Specifications</a> at 6.7.4.