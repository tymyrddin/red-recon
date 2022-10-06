# Certificates

When a certificate authority issues a certificate, these are entered into a central repository called a certificate log. 
This repository keeps a binary tree of all certificates, where each node is the hash of its child nodes, thereby 
guaranteeing the integrity of the entire chain. All issued TLS certificates should be publicly published to detect 
domain spoofing, typo-squatting, homograph attacks, and other mischievous ways to deceive and redirect users. These 
logs can be searched.

Secret applications with little security hiding behind proxies can be exposed, and minimally subdomain enumeration 
is way faster.

Note: Wildcard certificates are a single point of failure. If we stumble upon the private key while roaming the
network, we could intercept the communication flow of ***all*** applications using that same parent domain.

## Tools

* [Censys](https://censys.io/)
* [crt.sh](https://crt.sh/)
* [Sublist3r](https://github.com/aboul3la/Sublist3r)
* [Amass](https://github.com/OWASP/Amass/)
* [Fernmelder](https://github.com/stealth/fernmelder/)