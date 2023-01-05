---
title: Network Basics
permalink: /docs/ue/
---
<style>body {text-align: justify}</style>

## User Equipment (UE):
Any device connected to the 5G network, which is usually a mobile phone together with a SIM card. The UE connects with the RAN. Often the UE requests a service that the 5G network will transfer to where ever it needs to go. Like a Whatsapp message to a loved one.
<img src="{{ "/assets/img/5gbasics/ue_ran.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
## Radio Access Network (RAN): 
The RAN is a radio tower, to which the UE connects when it wants to use the mobile network. The RAN connects with the 5G Core Network and will transfer data from and to the UE and the 5G Core. For example, the Whatsapp message, which the UE sent to the RAN, and the RAN will send it to the 5G Core Network.
<img src="{{ "/assets/img/5gbasics/ran_core.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
## 5G Core Network (5G Core): 
<a href="{{ "/docs/core/" | relative_url }}">The Core Network</a> is the brains behind the 5G network. It consists of different Network Functions  communicating with each other through a message bus. See the Core page for more detailed information. The Core connects to RAN. To follow the previous example, the Whatsapp message received by the Core from the RAN will be sent back to the RAN to then be sent to the DN by the RAN.
<img src="{{ "/assets/img/5gbasics/core_ran.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
## Data Network (DN): 
The Data Network is the service to which the traffic will be distributed. Often this is to the internet. The Core network will send its traffic to the DN, such that the DN can further transfer it to possibly another 5G Network.
<img src="{{ "/assets/img/5gbasics/ran_dn.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
