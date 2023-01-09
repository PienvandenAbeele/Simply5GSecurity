---
title: Access and Mobility Management Function (AMF)
permalink: /docs/amf/
---
<style>body {text-align: justify}</style>

### Description

<div class="row">
    <div style="text-align: justify" class="col-md-5">
        The AMF is responsible for the mobility and connection management of the UE. The AMF performs functions such as authentication, authorisation, and mobility management to ensure that UEs can securely access the network and maintain their connections as they move between different coverage areas. 
    </div>
    <div class="col-md-7">
        <img src="{{ "/assets/img/5gbasics/amf_sba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

<div class="row">
    <div style="text-align: justify" class="col-md-6">
        <h3>Interaction with other NFs</h3>
        <h5> Consumes services from:</h5>
        NRF, AUSF, UDM, SMF
        <h5> Provides services to:</h5>
        SMF, AMF
        <br>
        <br>
        <br>
        <p><a class="btn btn-info btn-sm centerbut" href="https://www.etsi.org/deliver/etsi_ts/129500_129599/129518/17.07.00_60/ts_129518v170700p.pdf" target="_blank" rel="noopener noreferrer">3GPP Specifications</a></p>
    </div>
    <div class="col-md-6">
        <img src="{{ "/assets/img/5gbasics/amf_rba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

### Security importance

The AMF is the core network's point of contact for the UE, which puts the AMF in an essential role in securing the connection between the UE and the network. During the <a href="{{ "/docs/aka/" | relative_url }}">authentication and key agreement (AKA)</a>, the AMF checks the authentication of the UE and derives subsequent keys for securing the connection. The AMF also chooses which security algorithms are used for encryption and integrity protection on the NAS layer during the <a href="{{ "/docs/sa/" | relative_url }}">security activation</a>.
