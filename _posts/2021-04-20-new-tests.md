---
title: "New Tests - April"
date: 2021-04-28
# last_modified_at: 2021-01-05T09:42:00-05:00
description: "User submitted tests implemented in application"
categories:
  - Monthly-Security-Tests
tags:
  - Security Testing
image:
  path: /assets/images/monthly-tests/featureImage.jpg
  # height: 100
  # width: 100
---
<!-- Google analytics -->
{% include googleAnalytics.html %}
<!-- leadfeeder analytics -->
<!-- {% include leadfeederAnalytics.html %} -->

![feature image](/assets/images/monthly-tests/featureImage.jpg){:class="img-responsive"}

# This months implemented tests:

**Test requirements**
* Can be done from a single computer
* We can expect to get similar results on similar systems in the organization.
* Does not need special software or hardware

## 1. Assess average listening services per host
**CIS 9:** Limitation and Control of Network Ports, Protocols, and Services  
**From:** Brice  
Implemented in platform: :heavy_check_mark:  
>Unfortunately most attacks come from a small set of countries, because of this we've started blocking entire IP blocks from the worst offenders (we use pfBlocker for this). In order to test that this control is implemented we do ongoing nmap of a random set of IPs within these blocks. You can get the IP blocks from: https://lite.ip2location.com/ip-address-ranges-by-country

```bash
# From a computer on the network:
# open a cmd prompt, then simply run:
nmap -Pn --top-ports 100 192.168.0.0/24 -oG result
# This will write the output to a file "result"
# Then count the number of services and sort by highest occurance:
cat result | grep -i open | grep -oE [0-9]\{1,4}/open | sort | uniq -c | sort -r
```

## 2. Assess diversity of services inside your network
**CIS 4:** Limitation and Control of Network Ports, Protocols, and Services   
**From:** Ash  
Implemented in platform: :heavy_check_mark:  
>Check for privileges on your own computer. If you find yourself being admin (and your job is not being a system administrator) it's a good indicator that you need to look deeper into your organizations privilege management.

```bash
# From the computer(s) under test:
# Check if we are running elevated:
whoami /groups | find "S-1-16-12288" && Echo I am running elevated, so I must be an admin
# Check if we belong to local administrators:
whoami /groups | find "S-1-5-32-544" && Echo I am a local admin
# Check if we belong to domain admins:
whoami /groups | find "-512 " && Echo I am a domain admin
# Track changes and audit for unnecessary privileges.
```

## 3. Test connectivity from other countries to your organization
**CIS 12:** Boundary Defense  
**From:** Jason  
Implemented in platform: :x:  
>The network team has on multiple times configured our endpoints VPN client run with split tunneling, practically bypassing most of our firewalls, IDSes, and URL filters. We have made the helpdesk team run this command at random times a day on about a quarter of our endpoints to ensure we don't run split tunneling anywhere.

```bash
# From a remote client:
# open a cmd prompt, 
# then simply run:
Invoke-RestMethod ifconfig.me
# capture the data and run reports. 
```

This list was compiled from answers to our monthly questionnaire on what security leaders throughout the world vote on being the most important in order to test an organization's security defenses. 

Thank you to everyone one that contributed!

## Want more tests? Register below!  

<script charset="utf-8" type="text/javascript" src="//js.hsforms.net/forms/shell.js"></script>
<script>
  hbspt.forms.create({
	portalId: "8898112",
	formId: "2b1cfdb3-6618-4dd8-86e4-4786274c0d38"
});
</script>



[create account]: #want-more-tests-register-below