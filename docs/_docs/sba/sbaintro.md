---
title: Introduction
permalink: /docs/sbaintro/
---
<style>body {text-align: justify}</style>

In general, there are three security protocols followed to ensure secure communication between two parties:
* There has to be authentication between the two communication endpoints. This is to prevent a spoofing attack.
<img src="{{ "/assets/img/Sec/SBA_1.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

* Protection of the communication, which includes confidentiality, integrity and replay protection. To mitigate tampering, repudiation and information disclosure of messages.
<img src="{{ "/assets/img/Sec/SBA_2.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

* Authorisation of the request from both sides To mitigate the elevation of privilege
<img src="{{ "/assets/img/Sec/SBA_3.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

In SBA domain security, these three measures are realised through two principles, TLS and OAuth. TLS ensures mutual authentication and transport security. OAuth ensures the authorisation of the requests.

