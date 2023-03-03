---
title: Introduction
permalink: /docs/nasintro/
---
<style>body {text-align: justify}</style>

Network Access Security can be seen as the “realisation” of the network. Almost all communication inside and outside the <a href="{{ "/docs/core/" | relative_url }}">5G Core</a> uses this protocol. It is based on the measure already used in 4G called “air interface encryption”. This measure ensures <a href="{{ "/docs/confidentiality/" | relative_url }}">confidentiality</a> and with 5G, Network Access Security also supports <a href="{{ "/docs/integrity/" | relative_url }}">integrity</a> protection. Thus providing full-fledged protection for the communication happening over the air in the <a href="{{ "/docs/core/" | relative_url }}">User Plane</a>.
Network Access Security can be split up into three different areas: <a href="{{ "/docs/identification/" | relative_url }}">Identification</a>, <a href="{{ "/docs/aka/" | relative_url }}">Authentication and Key Agreement</a> and <a href="{{ "/docs/sa/" | relative_url }}">Security Activation</a>. On the left image below, you can see the flow of the communication in a simplified way. The right image shows how the communication lays between the <a href="{{ "/docs/ue/" | relative_url }}">UE</a>, <a href="{{ "/docs/ue/" | relative_url }}">gNodeB</a> and <a href="{{ "/docs/core/" | relative_url }}">Core Network</a>.

<div class="row">
    <div style="text-align: justify" class="col-md-5">
        <img src="{{ "/assets/img/Sec/I_AKA_SA.png" | relative_url }}" alt="5G Overview" class="img-responsive centernas"> 
    </div>
    <div class="col-md-7" >
        <img src="{{ "/assets/img/Sec/nasintro.png" | relative_url }}" alt="5G Overview" class="img-responsive center">            
    </div>
</div>

