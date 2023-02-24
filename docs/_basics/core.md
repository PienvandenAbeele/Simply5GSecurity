---
title: 5G Core Network
permalink: /docs/core/
---
<style>body {text-align: justify}</style>

The 5G Core Network (5GC) is the next-generation core network for 5G network. An important aspect of the design of the 5G core is the separation into control-plane and user-plane. The **control-plane** carries all signalling traffic, which is used to *build up and maintain* a user-plane connection, e.g., an Internet connection. In contrast, the **user-plane** data carries all user traffic, e.g., the actual IP traffic that is generated when visiting a website. 



<div class="row">
    <div style="text-align: justify" class="col-md-4">
    <br>
        In both planes the core consist of so-called <strong>network functions</strong> (NF) to support a wide range of services to other network functions. A common perspective on the core network architecture is the service-based architecture. In this architecture each of the network functions offer a service end point and the network functions communicate via a message bus to the services end points accordingly. 
    <br>
    </div>
    <div class="col-md-8">
        <img src="{{ "/assets/img/5gbasics/planes.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

Both the user-control plane separation and the use of the network functions have the advantage to build up a fully software defined 5G network. This is brings more flexibility and scaling options to the network. Scaling up and changing configurations becomes much easier that way. For example, the network operator can easily add more resources when needed by to a specific area. This idea is often realised by cloud native deployments which use virtualisation technologies such as Kubernetes.


While this gives more flexibility and scaling options, it also brings security concerns. Since the control-plane is now software-based, if something is misconfigured or there is a vulnerability in the Core, attackers can now access the core from a distance, instead of having to be at the hardware. To avoid this, we want to educate people on the security risks, see <a href="{{ "/docs/reqintro/" | relative_url }}">5G Security</a>, for more details.

For now, we move on to the network functions and what each of them does!
