---
title: 5G Basics
permalink: /docs/5gbasics/
redirect_from: /docs/5gbasics.md
---

5G is the successor of 4G and the next mobile network generation. With the introduction of 5G, the mobile network improves in a lot of areas:

- Higher data speeds
- Lower latency
- More reliability
- More network capacity
- More availability

This also introduces more complexity to the network, which introduces more possible security risks. Services like SUCI (link to page) and Oauth (link to page) are there to ensure more security on the network. 

But first we will focus on explaining the 5G Architecture, and the function of all the components.

UE: User Equipment. Any device connected to the 5G network, which is usually a mobile phone together with a SIM card. The UE connects with the RAN. Often the UE requests a service which the 5G network will transfer to where ever it needs to go. Like a Whatsapp message to a loved one.

RAN: Radio Access Network. The RAN is tower (often called the gNodeB), to which the UE connects when it wants to use the mobile network. The RAN has a connection with the 5G Core Network and will transfer data from and to both the UE and the 5G Core. For example, the Whatsapp message, which the UE sent to the RAN, and the RAN will send it to the 5G Core Network.

5G Core Network: The Core Network is the brains behind the 5G network. It consists out of different Network Functions (link to page) communicating with each other through a message bus. See Core page for more detailed information. The Core connects the RAN and the DN. To follow the previous example, the Whatsapp message received by the Core from the RAN, will be send to the DN by the Core.

DN: Data Network. The Data Network is the service to which the traffic will be distributed. Often this is to the internet. The Core network will send its traffic to the DN, such that the DN can further transfer it to possibly another 5G Network.

