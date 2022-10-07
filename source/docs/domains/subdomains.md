# Subdomains

To get subdomains from the DNS records: 

    dnsrecon -d target.com

Also try a Zone Transfer:

    dnsrecon -a -d target.com

👉 If zone transfers are not refused, make sure to document that in the report.

## Resources

* [dnsrecon](https://www.kali.org/tools/dnsrecon/)