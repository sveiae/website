---
title: "Top Tests - February"
date: 2021-02-28
# last_modified_at: 2021-01-05T09:42:00-05:00
description: "Our user survey's best security tests for January"
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

# Run these security tests today!

## What is this list?
These are tests submitted to our monthly email newsletter. All the tests are submitted by people with extensive information security experience. Members of the list can vote on which tests should be implemented in our security testing platform.

If you want to get a hold on all tests, please subscribed to our email newsletter: **Security tests to put your worries to rest**. 

**Test requirements**
* Can be done from a single computer
* Does not need special software or hardware
* We can expect to get similar results on similar systems in the organization.

# February:

## 1. Test connectivity out to other countries
**CIS 12:** Boundary Defense  
**From:** Eion  
Implemented in platform: :heavy_check_mark:  
>Unfortunately most attacks come from a small set of countries, because of this we've started blocking entire IP blocks from the worst offenders (we use pfBlocker for this). In order to test that this control is implemented we do ongoing nmap of a random set of IPs within these blocks. You can get the IP blocks from: https://lite.ip2location.com/ip-address-ranges-by-country

```bash
# From a computer on the Internet:
# open a cmd prompt, then simply run:
nmap -Pn --top-ports 10 bad-IPs-list
# The test will output a grading on your SSL configuration.
```

## 2. Check user privileges
**CIS 4:** Controlled Use of Administrative Privileges  
**From:** Lindsey  
Implemented in platform: :x:  
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

## 3. Check for VPN split tunneling
**CIS 11:** Secure Configuration for Network Devices, such as Firewalls, Routers and Switches  
**From:** Anonymous  
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