---
title: "Top Tests - January"
date: 2021-01-31
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

# Best tests for January
* Outbound ports to the Internet
* Check AV is on and reporting
* Test SSL on Websites

## 1. Check outbound ports to the Internet
**CIS 9:** Limitation and Control of Network Ports, Protocols and Services  
**From:** James  
Implemented in platform: :heavy_check_mark:  
>Unneded outbound ports are constantly used by attackers to call home. Simply scan scanme.nmap.org from your office computer. Any unneded ports is a failure.

```bash
# From a computer your own network:
nmap -p1-65535 scanme.nmap.org
# Any unneeded, open, port is a failure.
```

## 2. Check antivirus is ON and reporting
**CIS 8:** Malware Defenses  
**From:** Brian  
Implemented in platform: :heavy_check_mark:  
>Run Eicar. It's a test virus, and doesn't harm your computer. I let helpdesk run it on multiple endpoints and then see if it's alerted in our central AV system. I also use it to see if my SIEM picks up the alert, and that security team responds.
Simply download eicar here: https://secure.eicar.org/eicar.com

```bash
# From a computer you want to test from:
# open a cmd prompt, go to where you downloaded the file, 
# then simply run:
eicar.com
# your antivirus should detect this. 
# Now check your SIEM and see how your security responds.
```

## 3. Test SSL on company websites
**CIS 3:** Continuous Vulnerability Management  
**From:** Samir  
Implemented in platform: :x:  
>I started test my websites' SSL score myself after paying way too much for a 'pentester' to only find SSL flaws in a security audit.
Simply put in your website urls here: https://www.ssllabs.com/ssltest/ and then run the test.
You can also script this with nmap, which is what I do:

```bash
# From a computer on the Internet:
# open a cmd prompt, then simply run:
nmap -sV --script ssl-enum-ciphers -p 443 your-websites
# The test will output a grading of your SSL configuration.
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