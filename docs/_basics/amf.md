---
title: AMF
permalink: /docs/amf/
redirect_from: /docs/amf.md
---

The 5G architecture is based on a service-based architecture. The network is build upon Network Functions communicating with each other through a message bus. When a NF needs information from another NF, it will communicate with said function through the message bus and exchange information. An important aspect of SBA is the separation of the control-plane and user-plane. Lets take a look at what that means:

The network planes all carry different types of traffic data. The user-plane carries traffic from the network user, which are packets from and to the user. The control-plane carries the signalling traffic, which are packets from and to the router. What they did in 5G compared to other generations of networks, is move the control-plane to a software based architecture, instead of having the user and control plane together. By doing so, they enable more freedom to network managers, since they can now change the control plane configuration, without having to touch the user-plane. As you can see in the image (REF), the 5G Core Network is the control plane, and the user-plane is the UPF function between the RAN and the DN. This is a big performance and implementation improvement compared to 4G. Since the control-plane is now software based, everyone can deploy a 5G Core Network now, since it is software instead of hardware now. Scaling up and changing configurations become much easier that way.

While this gives more flexibility and scaling options, it also bring security concerns. Since the control-plane is now software based, if something is misconfigured or there is a vulnerability in the Core, attackers can now access the Core from a distance, instead of having to be at the hardware. To avoid this, we want to educate people on the security risks, see 5G Security, for more details.

For now we move on to the Network Functions and what each of them does!

