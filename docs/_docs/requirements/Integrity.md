---
title: Integrity
permalink: /docs/integrity/
---
<style>body {text-align: justify}</style>

#### Definition of Integrity:
*Guarding against improper information modification or destruction, and includes ensuring information non-repudiation and authenticity.*

Integrity in the mobile network ensures that traffic is not changed or destroyed. When you send a message to a loved one saying “I love you”, an attacker can not change the traffic packet changing it to something else. But it also includes an attacker who can not change the address, making the message go to someone else. Often this is achieved through a checksum on the packets.

<img src="{{ "/assets/img/sec/Int.png" | relative_url }}" alt="5G Overview" class="img-responsive center">

| Mobile network aims              | Explanation | What they combat          | 3GPP Specifications |
| -------------                    | ----------- |-------------              | --------- |
| Correct Charging Service         | By having integrity protection for the charging service, the correct customer gets charged the correct amount for their usage. | Interception of Internet traffic | |
| Traffic Integrity                | By ensuring traffic integrity, no one will be able to change  / delete the traffic that is send over the network. | Eavesdropping Phone Calls | |
| Mutual Authentication            | With mutual authentication, the UE and 5G network, both know they are talking to each other and not to a third (malicious) party| Interception of text messages / RCS | |
| Software and Hardware Integrity  | The integrity of software and hardware makes sure they both are legit and doing what they should do. | User localization | |


