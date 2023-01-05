---
title: Integrity
permalink: /docs/integrity/
---
<style>body {text-align: justify}</style>

#### Definition of Integrity:
*Guarding against improper information modification or destruction, and includes ensuring information non-repudiation and authenticity.*

Integrity in the mobile network ensures that traffic is not changed or destroyed. When you pay for something online, an attacker can not change the traffic packet changing it to something else, for example changing amount you're paying. But it also includes an attacker who can not change the address, making the message go to someone else. Often this is achieved through a checksum on the packets.

<img src="{{ "/assets/img/Sec/Int.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

| Mobile network aims              | Explanation | What they combat          | 3GPP Specifications |
| -------------                    | ----------- |-------------              | --------- |
| Correct Charging Service         | By having integrity protection for the charging service, the correct customer gets charged the correct amount for their usage. | Fraud attacks | |
| Traffic Integrity                | By ensuring traffic integrity, no one will be able to change  / delete the traffic that is send over the network. | Modification of traffic | |
| Mutual Authentication            | With mutual authentication, the UE and 5G network, both know they are talking to each other and not to a third (malicious) party| Impersonation attack| |
| Software and Hardware Integrity  | Integrity of software and hardware ensures that the system does what the original intent was. Attackers can not change the content. | Malware and Hardware Trojan | |
