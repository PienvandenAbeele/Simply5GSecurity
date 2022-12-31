---
title: Identification
permalink: /docs/identification/
---
<style>body {text-align: justify}</style>

IMSI: International Mobile Subscriber Identity

SUPI: Subscriber Permanent Identifier

SUCI: Subscriber Concealed Identifier

With the introduction of 5G, there came a big improvement against man-in-the-middle attacks which used “IMSI catchers”. IMSI catchers are used as fake base stations and can be bought in several countries. They are used to collect data, for example, to see if a certain UE is in an area.

<img src="{{ "/assets/img/Sec/IMSI_Chatcher.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

Every UE has an IMSI value, which it sends to base stations, to identify and show it is in the area. The reason IMSI Catchers work is that the IMSI data was always sent unencrypted over the network. 

5G tackles this issue with the introduction of SUPI, which is the successor of the IMSI. The SUPI is encrypted and sent over the network as a one-time temporary identifier called the SUCI.
The SUPI is encrypted with an Elliptic Curve Integrated Encryption Scheme (ECIES) using the public key of the home network. From that point on it is a SUCI and can be safely sent over the air.
At the 5G Core, the UDM will decrypt the SUCI to the SUPI again.


<div class="row">
    <div style="text-align: center" class="col-md-6">
        <p><dt>IMSI</dt></p>
        <img src="{{ "/assets/img/Sec/IMSI.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
    <div style="text-align: center" class="col-md-6">
        <p><dt>SUCI</dt></p>
        <img src="{{ "/assets/img/Sec/SUCI.png" | relative_url }}" alt="5G Overview" class="img-responsive center">    
    </div>
</div>

