---
title: "New Tests - November"
date: 2020-11-28
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

## Check antivirus is ON and reporting
**CIS 8:** Malware Defenses  
**From:** Brian  
Implemented in platform: :heavy_check_mark:  
>Run Eicar. It's a test virus, and doesn't harm your computer. I let helpdesk run it on multiple endpoints and then see if it's alerted in our central AV system. I also use it to see if my SIEM picks up the alert, and that security team responds.
Simply download eicar here: https://secure.eicar.org/eicar.com

### Manual test:
```bash
# From a computer you want to test from:
# open a cmd prompt, go to where you downloaded the file, 
# then simply run:
eicar.com
# your antivirus should detect this. 
# Now check your SIEM and see how your security responds.
```
### Automated - Using our platform:
![app image](/assets/images/monthly-tests/antivirus.png){:class="img-responsive"}

## Want more tests? Register below!  
<script charset="utf-8" type="text/javascript" src="//js.hsforms.net/forms/shell.js"></script>
<script>
  hbspt.forms.create({
	portalId: "8898112",
	formId: "2b1cfdb3-6618-4dd8-86e4-4786274c0d38"
});
</script>



[create account]: #want-more-tests-register-below