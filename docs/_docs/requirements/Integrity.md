---
title: Integrity
permalink: /docs/integrity/
---
<style>body {text-align: justify}</style>

**Definition of Integrity:**
*Guarding against improper information modification or destruction, and includes ensuring information non-repudiation and authenticity.*

<div class="row">
    <div style="text-align: justify" class="col-md-5">
        <br>
        Integrity in the mobile network ensures that traffic is not changed or destroyed. When you pay for something online, an attacker can not change the traffic packet changing it to something else, for example changing amount you're paying. But it also includes an attacker who can not change the address, making the message go to someone else. Often this is achieved through a checksum on the packets. 
    </div>
    <div class="col-md-7">
        <img src="{{ "/assets/img/Sec/Int.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>


| Name                              | Explanation                                                   | 3GPP Specifications |
| -------------                     | -----------                                                   | --------- |
| Correct Charging Service          | By having integrity protection for the charging service, the correct customer gets charged the correct amount for their usage.           | |
| Traffic Integrity                 | By ensuring traffic integrity, no one will be able to change  / delete the traffic that is send over the network.               | 5.3.3 in <a href="https://www.etsi.org/deliver/etsi_ts/133500_133599/133501/17.07.00_60/ts_133501v170700p.pdf" target="_blank" rel="noopener noreferrer">33.501</a>|
| Mutual Authentication             | With mutual authentication, the <a href="{{ "/docs/ue/" | relative_url }}">UE</a> and 5G network, both know they are talking to each other and not to a third (malicious) party      | 5.3.4 in <a href="https://www.etsi.org/deliver/etsi_ts/133500_133599/133501/17.07.00_60/ts_133501v170700p.pdf" target="_blank" rel="noopener noreferrer">33.501</a>|
| Software and Hardware Integrity   | Integrity of software and hardware ensures that the system does what the original intent was. Attackers can not change the content.    | 5.3.4 in <a href="https://www.etsi.org/deliver/etsi_ts/133500_133599/133501/17.07.00_60/ts_133501v170700p.pdf" target="_blank" rel="noopener noreferrer">33.501</a> |
