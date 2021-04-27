---
title: "New Tests - March"
date: 2021-03-27
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

## Test connectivity out to other countries
**CIS 12:** Boundary Defense  
**From:** Eion  
Implemented in platform: :heavy_check_mark:  
>Unfortunately most attacks come from a small set of countries, because of this we've started blocking entire IP blocks from the worst offenders (we use pfBlocker for this). In order to test that this control is implemented we do ongoing nmap of a random set of IPs within these blocks. You can get the IP blocks from: https://lite.ip2location.com/ip-address-ranges-by-country

### Manual test:
```bash
# From a computer on the Internet:
# open a cmd prompt, then simply run:
nmap -Pn --top-ports 10 bad-IPs-list
# The test will output a grading on your SSL configuration.
```
### Automated - Using our platform:
![app image](/assets/images/monthly-tests/geo-fencing.png){:class="img-responsive"}

## Want more tests? Register below!  

<script charset="utf-8" type="text/javascript" src="//js.hsforms.net/forms/shell.js"></script>
<script>
  hbspt.forms.create({
	portalId: "8898112",
	formId: "2b1cfdb3-6618-4dd8-86e4-4786274c0d38"
});
</script>



[create account]: #want-more-tests-register-below