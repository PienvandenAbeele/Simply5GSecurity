---
title: User Data Repository (UDR)
permalink: /docs/udr/
---
<style>body {text-align: justify}</style>

### Description

<div class="row">
    <div style="text-align: justify" class="col-md-5">
        The UDR (Unified Data Repository) is a central database that stores data about the network and its subscribers. It is used by various network functions for authentication, authorisation, billing, and policy management. The UDR is closely related to UDM, which is responsible for the generation of the authentication token. Further, the UDM stores important information about the registered network functions at the NRF. 
    </div>
    <div class="col-md-7">
        <img src="{{ "/assets/img/5gbasics/udr_sba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

<div class="row">
    <div style="text-align: justify" class="col-md-6">
        <h3>Interaction with other NFs</h3>
        <h5> Consumes services from:</h5>
        NRF
        <h5> Provides services to:</h5>
        UDM, NRF
        <br>
        <br>
        <br>
        <p><a class="btn btn-info btn-sm centerbut" href="https://www.etsi.org/deliver/etsi_ts/129500_129599/129504/17.08.00_60/ts_129504v170800p.pdf" target="_blank" rel="noopener noreferrer">3GPP Specifications</a></p>
    </div>
    <div class="col-md-6">
    <br>
        <img src="{{ "/assets/img/5gbasics/udr_rba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

### Security importance
With the role of a central data repository for the core network, the UDR is vital for the network's security. Under any conditions, the confidentiality and integrity of the data stored in the UDR must be ensured. Any leakage of the data would have severe consequences. For example, if an attacker obtains a user's shared keys, the trust anchor is compromised. This could result in the interception of connections or the impersonation of a user.