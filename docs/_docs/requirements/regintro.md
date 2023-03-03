---
title: Introduction
permalink: /docs/reqintro/
---
<style>body {text-align: justify}</style>

<div class="row">
    <div style="text-align: justify" class="col-md-5">
        <br>
        The CIA triad is a widely-applicable model for defining security requirements. It is based on three fundamental principles: Confidentiality, Integrity, and Availability. These principles are essential for ensuring the security of any system also the 5G network. We will use this model to structure the 5G security requirements which are more loosely defined by the specification.  
    </div>
    <div class="col-md-7">
        <img src="{{ "/assets/img/Sec/CIA_TRIAD.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

One example of how the CIA triad can be applied in a 5G network is as follows:
* **Confidentiality:** In a 5G network, confidentiality might be ensured by encrypting all communication between the UE and the network, which ensures that unauthorized individuals cannot intercept and read sensitive information.
* **Integrity:** To ensure the integrity of data transmitted over a 5G network, cryptographic checksums shall be used to verify that the data has not been altered in transit.
* **Availability:** To ensure the availability of the 5G network, redundant infrastructure and failover mechanisms could be put in place to ensure that the network remains online and functional even in the event of a hardware/software failure or coordinated Denial-of-Service attack.

With CIA, one can decide if it is needed for the specific system. For example, the distribution of a software update by the mobile network operator. Integrity is very important since the content of the update send over the network, can not be tampered with or it will not work anymore. However, confidentiality is not as important, since it is a publicly available update, which the provider wants everyone to have.

Therefore CIA is also used in the <a href="https://www.etsi.org/deliver/etsi_ts/129500_129599/129509/17.07.00_60/ts_129509v170700p.pdf" target="_blank" rel="noopener noreferrer">3GPP Specifications</a> to define which security properties each component of the 5G network needs to have. For example, the <a href="{{ "/docs/ue/" | relative_url }}">UE</a> needs to have integrity and availability, and for each of the <a href="{{ "/docs/core/" | relative_url }}">NFs</a>, it is defined which of the CIAs they need to provide.

