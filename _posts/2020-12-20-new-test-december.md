---
title: "New Tests - December"
date: 2020-12-28
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

## Check Intrusion Detection/Prevention is ON and reporting
**CIS 8:** Malware Defenses  
**From:** Brian  
Implemented in platform: :heavy_check_mark:  
>This is a very crude test of IDS, and I hope you can create a better test. But for what it's worth this little test checks if the IDS is listening and reporting.

### Manual test:
```bash
# From a computer you want to test from:
# open a cmd prompt, go to where you downloaded the file, 
# then simply run:
ping -c 3 -p 2b2b2b415448300d scanme.nmap.org
# your IDS should detect this. 
# Now check your SIEM and see how your security responds.
```
### Automated - Using our platform:
We built a few hundred IDS tests that tests shell and payload traffic to simulate attack traffic.  

![app image](/assets/images/monthly-tests/intrusion-detection.png){:class="img-responsive"}

## Want more tests? Register below!  
<script charset="utf-8" type="text/javascript" src="//js.hsforms.net/forms/shell.js"></script>
<script>
  hbspt.forms.create({
	portalId: "8898112",
	formId: "2b1cfdb3-6618-4dd8-86e4-4786274c0d38"
});
</script>



[create account]: #want-more-tests-register-below