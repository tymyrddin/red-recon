# Catching web infrastructure

## Attack tree

```text
1 Do a whois
2 Nmap domains
```

## Notes

* Most internet resources on cloud providers, like load balancers, content distribution networks, S3 buckets, 
etc., regularly rotate their IP addresses. If the nmap takes too long, the addresses will have 
been assigned to another customer and the results will no longer be relevant. Scan domain names, not IP addresses.

## Examples

    # nmap -F -sV -iL domains.txt -oA fast_results