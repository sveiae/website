---
title: "New Tests - April"
date: 2021-04-29
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

# This months implemented test:

**Test requirements**
* Can be done from a single computer
* We can expect to get similar results on similar systems in the organization.
* Does not need special software or hardware

## Test ability to interact with Malware and Cybercrime controlled services
**CIS 9:** Malware Defense  
**From:** Phil  
Implemented in platform: :heavy_check_mark:  
>I try finding lists of URLs for malware sites and services, then test if I can use curl (a commandline web client) to hit those sites. It gives me an indication of how well my URL filter is working at blocking malware downloads and drive by attacks.  

I use the malware list from the [blocklists project](https://blocklistproject.github.io/Lists/)
### Manual test:
```bash
# From a computer on the network:
# make or download a file with malware URLs.
# download a malware url file:
wget https://blocklistproject.github.io/Lists/malware.txt
# get a few domains from the file (from line 20 to 120, total of 100 tests),
# saved to 'sample.txt'
sed -n '20,120p' malware.txt | awk '{print $2}' > sample.txt
# open a cmd prompt, then simply run:
for i in $(cat out); do curl --max-time 2 -k $i -I -L; done
# HTTP 200 means either you hit the actual malware domain, or some sort of blackhole.
```
You will need to inspect the HTTP responses further to sort out any false positives.  

### Automated - Using our platform:
![app image](/assets/images/monthly-tests/malicious-website.png){:class="img-responsive"}


## Want more tests? Register below!  

<script charset="utf-8" type="text/javascript" src="//js.hsforms.net/forms/shell.js"></script>
<script>
  hbspt.forms.create({
	portalId: "8898112",
	formId: "2b1cfdb3-6618-4dd8-86e4-4786274c0d38"
});
</script>



[create account]: #want-more-tests-register-below