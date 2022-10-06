# dig

`dig` provides a lot of query options and even allows specifying a different DNS server to use. For example, we can 
use Cloudflare's DNS server: `dig @1.1.1.1 tryhackme.com`.

## host

`host` is another useful alternative for querying DNS servers for DNS records.

    host clinic.thmredteam.com

```text
clinic.thmredteam.com has address 104.21.93.169
clinic.thmredteam.com has address 172.67.212.249
clinic.thmredteam.com has IPv6 address 2606:4700:3034::ac43:d4f9
clinic.thmredteam.com has IPv6 address 2606:4700:3034::6815:5da9
```
