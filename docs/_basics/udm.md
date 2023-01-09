---
title: Unified Data Management (UDM)
permalink: /docs/udm/
---
<style>body {text-align: justify}</style>

### Description
In a 5G network, the UDM (Unified Data Management) generates authentication tokens used during the <a href="{{ "/docs/aka/" | relative_url }}">authentication and key agreement (AKA)</a> procedure. 
<div class="row">
    <div style="text-align: justify" class="col-md-5">
        The generation is based on user subscription data, which it retrieves from the <a href="{{ "/docs/udr/" | relative_url }}">User Data Repository (UDR)</a>. Often co-located with the UDM is the Subscription Identifier De-concealing function (SIDF) that is used during the identification phase to resolve the Subscription Permanent Identifier (SUPI) from the Subscription Concealed Identifier (SUCI), this is explained in <a href="{{ "/docs/aka/" | relative_url }}">AKA</a> as well.
    </div>
    <div class="col-md-7">
        <img src="{{ "/assets/img/5gbasics/udm_sba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

<div class="row">
    <div style="text-align: justify" class="col-md-6">
        <h3>Interaction with other NFs</h3>
        <h5> Consumes services from:</h5>
        NRF, UDR, AUSF
        <h5> Provides services to:</h5>
        SMF, AMF
        <br>
        <br>
        <br>
        <p><a class="btn btn-info btn-sm centerbut" href="https://www.etsi.org/deliver/etsi_ts/129500_129599/129503/17.08.00_60/ts_129503v170800p.pdf" target="_blank" rel="noopener noreferrer">3GPP Specifications</a></p>
    </div>
    <div class="col-md-6">
    <br>
        <img src="{{ "/assets/img/5gbasics/udm_rba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

### Security importance
The UDM implements an essential security role in the 5G during the identification procedure as it implements the SIDF and also during the authentication and key agreement procedure as it generates the authentication tokens for the UE authentication.  