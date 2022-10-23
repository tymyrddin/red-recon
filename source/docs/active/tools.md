# Tools

## theHarvester

Use theHarvester to collect information such as names, email addresses, subdomains, hosts, and IP addresses for 
`target.com`:

    theharvester -d target.com -b all

## Recon-ng

Get started with a target by creating a workspace for it:

```text
recon-ng
workspaces add <target>
```

Add the domain names and company names to the recon-ng database tables for use in further commands:

```text
add domains target.com
add domains www.target.com
add domains othertarget.com
add domains www.othertarget.com

add companies Target Name~A whatever company
add companies Target Subsidiary~A subsidiary company
add companies Product Target ~A whatever company product line
```

To view the domains and company tables:

```text
show companies
show domains
```

Collect the points of contact from Whois databases:

```text
use recon/domains-contacts/whois_pocs
run
```

Discover other domain names and hosts on the Internet related to the target by using a Bing search and a Google search:

```text
use recon/domains-hosts/bing_domain_web
run
use recon/domains-hosts/google_site_web
run
```

Load the reporting module and specify the creator of the report, the customer, and the report filename to generate:

```text
use reporting/html
set CREATOR 'Pentester name'
set CUSTOMER 'Target Name'
set FILENAME /root/Desktop/target_recon.html
run
```

If we had used other modules to collect additional information, that information would have been included in the 
report. As shown in the help menu the Marketplace: Interfaces with the module marketplace to pick and choose 
modules you want. 

```text
marketplace
marketplace install modulename
modules load modulename
[modulename] > show options
[modulename] > options set option
[modulename] > info
[modulename] > input
[modulename] > run
```

## Maltego

Maybe it comes up with something extra. Use built-in transformers of Maltego, for example:

### Gathering info about an organisation

1. Enter website, company 
2. Discover entities associated with target
   * Domain info and associated emails
   * Hosting company, support and admin emails
   * Files, related links, websites, and other companies
3. Display on a graph
4. Come up with a strategy

### Gathering info about a person

1. Enter person
2. Discover entities associated with target
   * Websites, links, social networking accounts
   * Social media friends and associated accounts
   * Emails of friends
3. Display on a graph
4. Come up with a strategy

## Resources

* [Maltego](https://www.maltego.com)
* [Recon-ng](https://tools.kali.org/information-gathering/recon-ng)
* [Infosec institute: Awesome modules of Recon-ng used for Web Recon testing](https://resources.infosecinstitute.com/topic/awesome-modules-of-recon-ng-used-for-web-recon-testing/)
