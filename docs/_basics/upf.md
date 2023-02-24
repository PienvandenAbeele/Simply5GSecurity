---
title: User Plane Function (UPF) 
permalink: /docs/upf/
---
<style>body {text-align: justify}</style>

### Description

<div class="row">
    <div style="text-align: justify" class="col-md-5">
        The UPF (User Plane Function) is the key component of the 5G user plane.  It acts as a bridge between the <a href="{{ "/docs/ue/" | relative_url }}">UE</a> and the data network, i.e., the Internet, forwarding data packets between them and applying routing and forwarding policies as needed. For doing so it is configured by the <a href="{{ "/docs/smf/" | relative_url }}">SMF</a> via the N4 interface.      
    </div>
    <div class="col-md-7">
        <img src="{{ "/assets/img/5gbasics/upf_sba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

<div class="row">
    <div style="text-align: justify" class="col-md-6">
        <h3>Interaction with other NFs</h3>
        <h5> Consumes services from:</h5>
        <a href="{{ "/docs/smf/" | relative_url }}">SMF</a>
        <h5> Provides services to:</h5>
        -
        <br>
        <br>
        <br>
        <p><a class="btn btn-info btn-sm centerbut" href="https://www.etsi.org/deliver/etsi_ts/133500_133599/133513/17.00.00_60/ts_133513v170000p.pdf" target="_blank" rel="noopener noreferrer">3GPP Specifications</a></p>
    </div>
    <div class="col-md-6">
    <br>
        <img src="{{ "/assets/img/5gbasics/upf_rba.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

### Security importance
The UPF handles the actual user data, e.g., the IP traffic. A compromised UPF implies that the user data of the customers can be intercepted or manipulated. Ensuring the UPF’s integrity shall be the highest priority.  
