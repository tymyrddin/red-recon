# Active DNS enumeration

DNS enumeration is for finding more information about all DNS components in a target. It is useful for 
identifying usernames, DNS record names, DNS domain names, and IP addresses of a target, increasing the attack 
surface of a target.

Different tools are required for DNS enumeration. Also see [passive enumeration](passive-enum.md).

## nslookup

`nslookup` is a command line utility useful for identifying DNS infrastructure.

    # nslookup 
    > set type=any 
    > ls -d <domain>

It uses the default DNS server to get the `A` and `AAAA` records related to a domain. For example:

    nslookup clinic.thmredteam.com

```text
Server:		127.0.0.53
Address:	127.0.0.53#53

Non-authoritative answer:
Name:	clinic.thmredteam.com
Address: 104.21.93.169
Name:	clinic.thmredteam.com
Address: 172.67.212.249
Name:	clinic.thmredteam.com
Address: 2606:4700:3034::ac43:d4f9
Name:	clinic.thmredteam.com
Address: 2606:4700:3034::6815:5da9
```

## nmap

Nmap is a port scanner used to identify open ports. Click Here for Nmap Cheatsheet

    # nmap -sC -sV -p53 192.168.x.0/24

## dig

dig is a command line tool for querying DNS servers. `dig` provides a lot of query options and even allows specifying a different DNS server to use. For example, we can 
use Cloudflare's DNS server with: `dig @1.1.1.1 tryhackme.com`.

    # dig axfr <domain> @<ns-domain>

## host

`host` is another useful alternative for querying DNS servers for DNS records.

    # host <domain>

For example:

    host clinic.thmredteam.com

```text
clinic.thmredteam.com has address 104.21.93.169
clinic.thmredteam.com has address 172.67.212.249
clinic.thmredteam.com has IPv6 address 2606:4700:3034::ac43:d4f9
clinic.thmredteam.com has IPv6 address 2606:4700:3034::6815:5da9
```

## fierce

Reconnaissance tool that quickly scans a target domain for DNS related vulnerabilities.

    # fierce -dns <domain>

## AltDNS

AltDNS is useful for identifying subdomains through alteration and permutation.

    git clone https://github.com/infosec-au/altdns.git 
    cd altdns 
    pip install -r requirements.txt

## DNSenum

DNSenum is perl script identifying DNS information of target.

    # dnsenum --noreverse <domain>

## DNSrecon

Reconnaissance tool that can be used to perform automatic recon of target. To get subdomains from the DNS records: 

    # dnsrecon -d <domain>
