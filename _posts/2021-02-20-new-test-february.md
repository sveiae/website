---
title: "New Tests - February"
date: 2021-02-24
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

## Check outbound ports to the Internet
**CIS 9:** Limitation and Control of Network Ports, Protocols and Services  
**From:** James  
Implemented in platform: :heavy_check_mark:  
>Unneded outbound ports are constantly used by attackers to call home. Simply scan scanme.nmap.org from your office computer. Any unneded ports is a failure.

### Manual test:
```bash
# From a computer your own network:
nmap -p1-65535 scanme.nmap.org
# Any unneeded, open, port is a failure.
```
### Automated - Using our application:
![app image](/assets/images/monthly-tests/outbound-ports.png){:class="img-responsive"}

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