---
title: "Top 3 Security - January"
last_modified_at: 2021-01-05T09:42:00-05:00
description: "Learn how to test your security controls in firewall and routers using your command line"
categories:
  - Monthly Top 3 Security Tests
tags:
  - Security Testing
  - Network Security
image:
  path: /assets/images/2021-01-05/featureimage.jpg
  # height: 100
  # width: 100
---
<!-- Google analytics -->
{% include googleAnalytics.html %}
<!-- leadfeeder analytics -->
<!-- {% include leadfeederAnalytics.html %} -->

![feature image](/assets/images/2021-01-05/featureimage.jpg){:class="img-responsive"}  

# Thank you for contributing!
This list was compiled from answers to our monthly questionnaire on what security leaders throughout the world vote on being the most important in order to test an organization's security defenses.

## 1. Check outbound ports to the Internet: 
From James:
>"Simply scan scanme.nmap.org from your office computer. Any unneded ports is a failure. I'm amazed of how many don't do this more often."
```bash
# from a computer your own network:
nmap -p1-65535 scanme.nmap.org
# Any unneeded, open, port is a failure.
```
Implemented in platform: :heavy_check_mark:
## 2. Check antivirus related controls:
From Brian:
>"Try to run Eicar. It's a test virus, and doesn't harm your computer. I use it to see if my SIEM picks up antivirus detection, and that security team responds."
Simply download eicar here: https://secure.eicar.org/eicar.com
```bash
# from a server on your own network:
# open a cmd prompt, go to where you downloaded the file, 
# then simply run:
eicar.com
# your antivirus should detect this. 
# Now check your SIEM and see how your security responds.
```
Implemented in platform: :heavy_check_mark:
## 3. Test SSL on company websites:
From Samir:
>"I started test my websites' SSL score myself after paying way too much for a 'pentester' to only find SSL flaws in a security audit"
Simply put in your website urls here: https://secure.eicar.org/eicar.com and then run the test.
You can also script this with nmap, which is what I do:
```bash
# from a computer on the Internet:
# open a cmd prompt, then simply run:
nmap -sV --script ssl-enum-ciphers -p 443 your-website
# The test will output a grading on your SSL configuration.
```
Implemented in platform: :x:
## Want more tests? Register below!  
Available tests for routers and firewalls:

<style>
.tablelines table, .tablelines td, .tablelines th {
        border: 1px gray;
        }
</style>
|                       |  **Secure Routing and DNS** | **URL Filtering**   | **Port filtering**  |   **Network Monitoring**
| malware websites      |                             | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark:  |
| attack networks       | :heavy_check_mark:          | :heavy_check_mark:  | :heavy_check_mark:  | :heavy_check_mark:  |
| ports and protocols   | :heavy_check_mark:          |                     | :heavy_check_mark:  | :heavy_check_mark:  |
| malicious dns         | :heavy_check_mark:          |                     | :heavy_check_mark:  | :heavy_check_mark:  |
| c2c traffic           |                             |                     | :heavy_check_mark:  | :heavy_check_mark:  |
{: .tablelines}

<script charset="utf-8" type="text/javascript" src="//js.hsforms.net/forms/shell.js"></script>
<script>
  hbspt.forms.create({
	portalId: "8898112",
	formId: "2b1cfdb3-6618-4dd8-86e4-4786274c0d38"
});
</script>



[create account]: #want-more-tests-register-below