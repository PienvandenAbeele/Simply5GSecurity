---
title: Network Basics
permalink: /docs/ue/
---
<style>body {text-align: justify}</style>

<div class="row">
    <div style="text-align: justify" class="col-md-5">
    <br>
        A 5G network consits of the User Equipment (UE), Radio Access Network (RAN), Core Networks (CN) and the Data Network (DN). To understand how these interact with eachother, lets imagine you would like to send a Whatsapp message to a loved one. You will type it on your phone (UE) which will transmitted it via the radio connection to the base station, which will then emulate it and forward it to data network.
    </div>
    <div class="col-md-7">
        <img src="{{ "/assets/img/5gbasics/basics.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

<div class="row">
    <div style="text-align: justify" class="col-md-6">
        <br>
        <h4>User Equipment (UE):</h4>
        Any device connected to the 5G network, which is usually a mobile phone together with a SIM card. The UE connects with the RAN. Often the UE requests a service that the 5G network will transfer to where ever it needs to go.
    </div>
    <div class="col-md-6">
        <img src="{{ "/assets/img/5gbasics/ue.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

<div class="row">
    <div style="text-align: justify" class="col-md-6">
        <h4>Radio Access Network (RAN):</h4>
        The RAN is the Radio Access Network which allows UEs to connect to the network. The RAN is responsible for handling the radio link between devices and the core network, transmitting and receiving signals over the air, and performing various tasks such as modulation, demodulation, and error correction. In 5G networks, the RAN is often distributed over a larger area and consists of a larger number of cells, which  allows for increased capacity and coverage, as well as support for higher data rates. 
    </div>
    <div class="col-md-6">
    <br>
        <img src="{{ "/assets/img/5gbasics/ran.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

<div class="row">
    <div style="text-align: justify" class="col-md-6">
        <h4>5G Core Network (CN):</h4>
        <a href="{{ "/docs/core/" | relative_url }}">The Core Network</a> is the brains behind the 5G network. It consists of different Network Functions  communicating with each other through a message bus. See the Core page for more detailed information. The Core connects to RAN. To follow the previous example, the Whatsapp message received by the Core from the RAN will be sent back to the RAN to then be sent to the DN by the RAN.
    </div>
    <div class="col-md-6">
        <img src="{{ "/assets/img/5gbasics/core1.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>

<div class="row">
    <div style="text-align: justify" class="col-md-6">
        <br>
        <h4>Data Network (DN):</h4>
        The Data Network is the service to which the traffic will be distributed. Often this is to the internet. The Core network will send its traffic to the DN, such that the DN can further transfer it to possibly another 5G Network.
    </div>
    <div class="col-md-6">
        <img src="{{ "/assets/img/5gbasics/core.png" | relative_url }}" alt="5G Overview" class="img-responsive center">
    </div>
</div>




