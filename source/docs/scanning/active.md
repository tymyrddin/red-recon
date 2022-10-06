# Active scanning

With active scanning packets are sent to the target systems to discover the operating systems and the services
running on the systems.

* Try a ping sweep across the network with Nmap to identify what IP addresses have live systems up and
running.
* Try a TCP full connect scan, UDP scan or SYN scan. Disable ping in these scans to stop Nmap from doing a ping sweep first to determine if the IP address is up and
running.
* Do a Service identification and OS fingerprinting on single hosts.
* Craft packets to bypass firewalls.