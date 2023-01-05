---
title: TLS
permalink: /docs/tls/
---
<style>body {text-align: justify}</style>

With everything being send over channels and over the network, it is important there are secure channels connecting two systems/people. That's where TLS comes in: TLS is a cryptographic protocol which ensures the security of data from one end-point to another when send over the internet. In 5G TLS should be used to ensure safe connections. TLS does not secure data once it has been delivered to an endpoint. However, it does provide confidentiality and integrity of the data sent over the internet. Thus attacks like eavesdropping or alteration of the content are not possible.

For authentication TLS supports three models:
* Two-way authentication: authentication of both parties. In this mode, both the server and the client will be authenticated.
* One-way authentication: server authentication with an unauthenticated client. That means only the server is authenticated by the client, and the client won’t be authenticated by the server.
* Total anonymity: the server and client won’t authenticate each other.

As decided by the 3GPP in the specifications, all NFs need to use two-way authentication, to make sure both parties are who they say they are.
Therefore, TLS is of uttermost importance to ensure a secure network, as it will protect the data that is being sent around and it will ensure only legit parties are involved. Thus the information NFs send each other is protected against attackers who want to see what is happening, possibly changing this data for their advantage or attackers who pretend to be a NF.
<img src="{{ "/assets/img/Sec/TLS.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
