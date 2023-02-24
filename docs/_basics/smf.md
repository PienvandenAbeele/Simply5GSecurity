---
title: Session Management Function (SMF)
permalink: /docs/smf/
---
<style>body {text-align: justify}</style>

### Description
The SMF, or Session Management Function, is responsible for managing the sessions, e.g., IP data connections of end-user devices in the 5G network. This includes tasks such as establishing, modifying, and releasing individual sessions and allocating IP addresses for each session. 
<div class="row">
    <div style="text-align: justify" class="col-md-5">
        The SMF communicates indirectly with end-user devices through the <a href="{{ "/docs/amf/" | relative_url }}">AMF</a>, which forwards session-related messages between the devices and the SMF via the NAS protocol. 
        In addition, the SMF interacts with other network functions through its service-based interface and controls the different <a href="{{ "/docs/upf/" | relative_url }}">UPF</a> (User Plane Function) network functions in the network through the N4 network interface. This control includes configuring traffic steering and traffic enforcement for individual sessions in the <a href="{{ "/docs/upf/" | relative_url }}">UPF</a>. 
    </div>
    <div class="col-md-7">
        <img src="{{ "/assets/img/5gbasics/smf_sba.png" | relative_url }}" alt="5G Overview" class="img-responsive center center-vertical">
    </div>
</div>

<div class="row">
    <div style="text-align: justify" class="col-md-6">
        <h3>Interaction with other NFs</h3>
        <h5> Consumes services from:</h5>
        <a href="{{ "/docs/udm/" | relative_url }}">UDM</a>, <a href="{{ "/docs/nrf/" | relative_url }}">NRF</a>
        <h5> Provides services to:</h5>
        <a href="{{ "/docs/upf/" | relative_url }}">UPF</a>, <a href="{{ "/docs/amf/" | relative_url }}">AMF</a>
        <br>
        <br>
        <br>
        <p><a class="btn btn-info btn-sm centerbut" href="https://www.etsi.org/deliver/etsi_ts/129500_129599/129502/17.06.00_60/ts_129502v170600p.pdf" target="_blank" rel="noopener noreferrer">3GPP Specifications</a></p>
    </div>
    <div class="col-md-6">
        <img src="{{ "/assets/img/5gbasics/smf_rba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

### Security importance
In its role, the SMF manages the user-plane <a href="{{ "/docs/core/" | relative_url }}">(UP)</a> security policy of the session. The UP security policy typically includes measures to protect user data via integrity over the radio network. 
