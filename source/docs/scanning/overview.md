# Overview

## Passive scanning

With passive scanning there is no interaction with the target hosts, but traffic
on the target network is captured to see what can be picked up.

* Monitor network traffic for source and destination IP addresses to understand the hosts that exist on the network.
* Inspect packets to discover usernames and passwords, or other confidential information, and layer-2 addresses
(MAC addresses).

👉 MAC addresses of valid clients can possibly be spoofed to bypass security controls.

## Active scanning

With active scanning packets are sent to the target systems to discover the operating systems and the services
running on the systems.

* Try a ping sweep across the network with Nmap to identify what IP addresses have live systems up and
running.
* Try a TCP full connect scan, UDP scan or SYN scan. Disable ping in these scans to stop Nmap from doing a ping sweep first to determine if the IP address is up and
running.
* Do a Service identification and OS fingerprinting on single hosts.
* Craft packets to bypass firewalls.