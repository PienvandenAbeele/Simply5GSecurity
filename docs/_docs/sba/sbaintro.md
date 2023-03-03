---
title: Introduction
permalink: /docs/sbaintro/
---
<style>body {text-align: justify}</style>

In general, there are three security protocols followed to ensure secure communication between two parties:
* There has to be authentication between the two communication endpoints. This is to prevent a spoofing attack.
<img src="{{ "/assets/img/Sec/SBA_1.png" | relative_url }}" alt="5G Overview" class="img-responsive centernas">

* Protection of the communication, which includes <a href="{{ "/docs/confidentiality/" | relative_url }}">confidentiality</a>, <a href="{{ "/docs/integrity/" | relative_url }}">integrity</a> and replay protection. To mitigate tampering, repudiation and information disclosure of messages.
<img src="{{ "/assets/img/Sec/SBA_2.png" | relative_url }}" alt="5G Overview" class="img-responsive centernas">

* Authorisation of the request from both sides to mitigate the elevation of privilege
<img src="{{ "/assets/img/Sec/SBA_3.png" | relative_url }}" alt="5G Overview" class="img-responsive centernas">

In SBA domain security, these three measures are realised through two principles, <a href="{{ "/docs/tls/" | relative_url }}">TLS</a> and <a href="{{ "/docs/oauth/" | relative_url }}">OAuth 2.0</a>. <a href="{{ "/docs/tls/" | relative_url }}">TLS</a> ensures mutual authentication and transport security. <a href="{{ "/docs/oauth/" | relative_url }}">OAuth 2.0</a> ensures the authorisation of the requests.

