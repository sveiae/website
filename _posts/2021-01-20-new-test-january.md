---
title: "New Tests - January"
date: 2021-01-19
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

## Assess density of listening services in network
**CIS 9:** Limitation and Control of Network Ports, Protocols, and Services  
**From:** Brice  
Implemented in platform: :heavy_check_mark:  
>When it comes to listening services in the client network, I like to run a tight ship. We had an attacker in our network that was able to pivot wayyy to easy because our users stood up any server they wanted. Not anymore. The command below allow you to quickly see if there are any services that are anomalies in your network.
### Manual test:
```bash
# From a computer on the network:
# open a cmd prompt, then simply run:
nmap -Pn --top-ports 100 192.168.0.0/24 -oG result
# This will write the output to a file "result"
# Then count the number of services and sort by highest occurance:
$ cat result | grep -i open | grep -oE [0-9]\{1,4}/open | sort | uniq -c | sort -r
      53 22/open
      53 443/open
      1 21/open      <- anomaly
      1 3389/open    <- anomaly
```      
### Automated - Using our platform:
![app image](/assets/images/monthly-tests/network-ports.png){:class="img-responsive"}

## Want more tests? Register below!  
<script charset="utf-8" type="text/javascript" src="//js.hsforms.net/forms/shell.js"></script>
<script>
  hbspt.forms.create({
	portalId: "8898112",
	formId: "2b1cfdb3-6618-4dd8-86e4-4786274c0d38"
});
</script>



[create account]: #want-more-tests-register-below