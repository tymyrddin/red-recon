# Assets discovery

Obtain all the companies owned by a main company and then all the assets of these companies:

* Find the acquisitions of the main company, this will give the companies inside the scope.
* Find the ASN (if any) of each company, this will give the IP ranges owned by each company.
* Use reverse whois lookups to search for other entries (organisation names, domains...) related to the first one 
(recursively).
* Use other techniques like shodan org and ssl filters to search for other assets (the ssl trick can be done recursively).

## Discover acquisitions

* [CrunchBase](https://www.crunchbase.com/)
* [Wikipedia](https://www.wikipedia.org/)

## ASNs

If the target organisation has an [ASN](../dns/asn.md), it is possible to test all the hosts inside the scope for vulnerabilities, 
and look for domains inside these IPs. Search by company name, by IP or by domain using the 
[Hurricane Electric BGP Toolkit](https://bgp.he.net/). 

## Continue

Use [shodan](../dns/passive-enum.md) to find open ports and depending on finds pentest possible services running.