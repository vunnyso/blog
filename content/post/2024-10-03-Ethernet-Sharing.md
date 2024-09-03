+++
author = "Vunny Sodhi"
title = "Ethernet Sharing"
date = "2024-10-03"
description = "Ethernet Sharing"
tags = [
    "Ethernet"
]
+++

Steps to share ethernet
<!--more-->
### Steps on machine from where you want to share Network
1. Open Network Manager and Create "Wired Ethernet" connection.
2. Under "Wired" select "Restrict to device" as "enp0s31f6"
3. Under "IPv4" select "Method" Manual and choose "Address" as "192.168.1.1" and "Netmask" as "255.255.255.0"
4. sudo ip link set enp0s13f0u3u1 down
5. sudo ip link set enp0s13f0u3u1 up

### Steps for target machine 
1. sudo ip addr add 192.168.1.150/24 dev enp0s20f0u1
2. sudo ip link set enp0s20f0u1 down
3. sudo ip link set enp0s20f0u1 up