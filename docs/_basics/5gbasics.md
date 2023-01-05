---
title: 5G Introduction
permalink: /docs/5gbasics/
redirect_from: /docs/5gbasics.md
---
<style>body {text-align: justify}</style>

5G is the successor of 4G and the next mobile network generation. With the introduction of 5G, the mobile network improves in a lot of areas:

* Lower latency

    Latency is the time it takes a data packet to travel across the network towards its destination. With lower latency, the time for a packet to arrive, goes down which makes the network faster.

* Better reliability

    Reliability measures the ability of a system to function correctly, including avoiding data corruption. With better reliability there are less packets being corrupted or not delivered.
    
* More network capacity

    More network capacity means more devices will be able to connect to the network and communicate with each other. Think about a highway with 4 lanes instead of 2 lanes, here more cars can pass in the same amount of time, just like with more network capacity, more network packets can pass through.

* Higher availability

    Availability measures how often the system is available for use. With a higher availability, the network will have less down time.


This also introduces more complexity to the network, which introduces more possible security risks. With more complexity, there are more possibilities something goes wrong. If a system manager needs to implement a lot of different steps, there is a greater risk they missed something, which can lead to security risks. Therefore services like <a href="{{ "/docs/identification/" | relative_url }}">SUCI</a> and <a href="{{ "/docs/oauth/" | relative_url }}">OAuth 2.0</a> are there to combat these risks and create a secure network.
But first, we will focus on explaining the 5G Architecture, and the function of all the components.

# 3GPP explanation

- Je hebt bij elke NF die link to specifications staan, wat ik nog een beetje mis is een uitleg ergens van wat 3GPP doet en dat zij dus die specifications maken die iedereen in principde kan implementeren en dat het dan goed samenwerkt met elkaar.