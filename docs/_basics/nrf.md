---
title: Network Repository Function (NRF)
permalink: /docs/nrf/
---
<style>body {text-align: justify}</style>

### Description

<div class="row">
    <div style="text-align: justify" class="col-md-5">
        <br>
        The Network Repository Function (NRF) keeps track of all the NFs. NFs will register at the NRF and then when a NF needs to talk to another NF, the NRF allows them to discover each other.
    </div>
    <div class="col-md-7">
        <img src="{{ "/assets/img/5gbasics/nrf_sba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

<div class="row">
    <div style="text-align: justify" class="col-md-6">
        <h3>Interaction with other NFs</h3>
        <h5> Consumes services from:</h5>
        UDM, AMF, SMF, UDR, AUSF, UPF
        <h5> Provides services to:</h5>
        UDR
        <br>
        <br>
        <br>
        <p><a class="btn btn-info btn-sm centerbut" href="https://www.etsi.org/deliver/etsi_ts/129500_129599/129510/17.07.00_60/ts_129510v170700p.pdf" target="_blank" rel="noopener noreferrer">3GPP Specifications</a></p>
    </div>
    <div class="col-md-6">
        <img src="{{ "/assets/img/5gbasics/nrf_rba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

### Security importance
The NRF is important for security since it makes sure the correct NFs communicate and validates if the correct NFs are registered.
It is responsible for managing access to network resources and prevent unauthorised access.  

Besides managing the network functions, the NRF manages the OAuth (Open Authorisation) process. OAuth is a standard for authorisation that allows a network function to grant third-party access to their services without sharing the credentials. In the 5G core network, OAuth is a central part of the security measures, and the NRF acts as the central OAuth server, which manages the process of granting.
When a network function wants to access a service from another network, it must first request authorisation from the NRF. The NRF will based on the security policies, issue an access token, which the network function can use to access the protected service on another resource. See <a href="{{ "/docs/oauth/" | relative_url }}">OAuth 2.0</a> for more information about OAuth 2.0.