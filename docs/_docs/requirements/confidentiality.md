---
title: Confidentiality
permalink: /docs/confidentiality/
---
<style>body {text-align: justify}</style>

#### Definition of Confidentiality:
*The protection of data, provides access for those who are allowed to see it while disallowing others from learning anything about its content.*

In the mobile network, confidentiality is important to ensure no one but the required parties can see the information. For example, when enter your password to log into your bank account, if an attacker were to snoop around on the network, they can see the traffic, but do not know what it says or who it is for, and thus they can not see your password. This is established by encrypting the traffic data.

<img src="{{ "/assets/img/Sec/Conf.png" | relative_url }}" alt="5G Overview" class="img-responsive center">


| Mobile network aims                          | Explanation     | What they combat          | 3GPP Specifications |
| -------------                                | ---------       |-------------              | -------------- |
| Confidentiality of User Data Traffic (UDT)        |  By ensuring the confidentiality of the UDT (the UDT is the metadata of the packets send, thus not the content of the messages), only the people/systems who are allowed to, will be able to see the data traffic of a user. For everyone else, this data (e.g. how much the user sends) will be encrypted and unavailable.                | Interception of Internet traffic | Network Access Security 33.501 - 6.6.2 |
| Confidentiality of Voice/Video Calls         | By ensuring the confidentiality of voice/video calls, these calls will be encrypted; thus, only the receiver and sender will be able to see and hear the information being exchanged.                | Eavesdropping Phone Calls | |
| Confidentiality of text messages (SMS) / RCS | By ensuring the confidentiality of the text messages / RCS, only the people who are allowed to, will be able to see the messages. For everyone else, these messages will be encrypted.               | Interception of text messages / RCS | |
| Location privacy                             | By ensuring the confidentiality of the location of the user, the location will be encrypted and not for everyone to see.               | User localization | |
| Identity privacy                             | By ensuring the confidentiality of the identity of the user, the identity will be encrypted and/or unlink-able which will give the user the option to use the 5G network, without everyone knowing who they are.               | User identification & tracking | |
