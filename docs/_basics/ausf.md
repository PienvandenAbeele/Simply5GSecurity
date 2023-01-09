---
title: Authentication Server Function (AUSF)
permalink: /docs/ausf/
---
<style>body {text-align: justify}</style>

### Description

<div class="row">
    <div style="text-align: justify" class="col-md-5">
        The AUSF is a 5G core network component responsible for authenticating the UE in coordination with the UDM and AMF. Therefore, the AUSF provides services to the AMF, allowing it to request an authentication token. The UDM gives the AUSF temporary keys and authentication data during this process. On the <a href="{{ "/docs/aka/" | relative_url }}">authentication and key agreement (AKA)</a> page, you can find more information on this process. 
    </div>
    <div class="col-md-7">
        <img src="{{ "/assets/img/5gbasics/ausf_sba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

<div class="row">
    <div style="text-align: justify" class="col-md-6">
        <h3>Interaction with other NFs</h3>
        <h5> Consumes services from:</h5>
        NRF
        <h5> Provides services to:</h5>
        UDM, AMF
        <br>
        <br>
        <br>
        <p><a class="btn btn-info btn-sm centerbut" href="https://www.etsi.org/deliver/etsi_ts/129500_129599/129509/17.07.00_60/ts_129509v170700p.pdf" target="_blank" rel="noopener noreferrer">3GPP Specifications</a></p>
    </div>
    <div class="col-md-6">
        <img src="{{ "/assets/img/5gbasics/ausf_rba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

### Security importance
In its function for managing the authentication of the UE, the AUSF is very important for the security of the network. The AUSF is responsible of implement increased home control when performing the <a href="{{ "/docs/aka/" | relative_url }}">authentication and key agreement</a> procedure.