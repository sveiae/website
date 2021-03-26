---
title: "Top 3 - February"
date: 2021-02-28
# last_modified_at: 2021-01-05T09:42:00-05:00
description: "Our user survey's best security tests for January"
categories:
  - Monthly Security Tests
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

# Highest voted tests for January
This list was compiled from answers to our monthly questionnaire on what security leaders throughout the world vote on being the most important in order to test an organization's security defenses. 

A big thanks to everyone one that contributed!

## 1. Test connectivity out to other countries
CIS 12: Boundary Defense
**From Eion:**
>Unfortunately most attacks come from a small set of countries, because of this we've started blocking entire IP blocks from the worst offenders (we use pfBlocker for this). In order to test that this control is implemented we do ongoing nmap of a random set of IPs within these blocks. You can get the IP blocks from: https://lite.ip2location.com/ip-address-ranges-by-country

```bash
# From a computer on the Internet:
# open a cmd prompt, then simply run:
nmap -Pn --top-ports 10 bad-IPs-list
# The test will output a grading on your SSL configuration.
```
Implemented in platform: :heavy_check_mark:

## 2. Check user privileges
CIS 4: Controlled Use of Administrative Privileges
**From Lindsey:**
>I check for windows privileges on user login, for all the endpoints, to have a good overview of how many priveleged accounts are running out there.

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
Implemented in platform: :x:

## 3. Check endpoint VPN state
CIS 11: Secure Configuration for Network Devices, such as Firewalls, Routers and Switches
**From Anonymous:**
>We've started to have some serious VPN issues on the east-coast, starting mid-January. As a consequence our remote users (basically everyone) have lost VPN multiple times per day. To track this we're checking endpoints routable IPs from time to time, and push this information to a secret service that we control.

```bash
# From a remote client:
# open a cmd prompt, go to where you downloaded the file, 
# then simply run:
Invoke-RestMethod ifconfig.me
# send this information through channels you can control and analyze the data. 
```
Implemented in platform: :X:

## Want more tests? Register below!  

<script charset="utf-8" type="text/javascript" src="//js.hsforms.net/forms/shell.js"></script>
<script>
  hbspt.forms.create({
	portalId: "8898112",
	formId: "2b1cfdb3-6618-4dd8-86e4-4786274c0d38"
});
</script>



[create account]: #want-more-tests-register-below