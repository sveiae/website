---
title: "Security tests that stand the test of time"
last_modified_at: 2021-03-01T16:52:02-05:00
categories:
  - Blog
tags:
  - Post Formats
  - readability
  - standard
  - link
---
<!-- Google analytics -->
{% include googleAnalytics.html %}
<!-- leadfeeder analytics -->
{% include leadfeederAnalytics.html %}

# Let's test our network security.
TLDR: Testing your most important security controls is easy and incredibly important if you want to improve your security.

If you want to start testing immediately, [register][create account] for a free trial of our testing software.

## Test all things network security.
![compliance](/assets/images/2021-03-01/paper-stack.jpeg){:class="img-responsive"}  
*NIST 800-53 anyone?*

**Leave no network behind!**  
All networks have unused security opportunities:
* Home routers have firewall rules and can chose to use secure DNS servers.
* Home firewalls have VLANs, URL filtering, and sometimes even Intrusion Detection/Prevention.
* Enterprise firewalls can do deep packet inspection, SSL proxying, and other lot of other network monitoring.

**What we'll be testing**
* connecting to botnets and known attack networks.
* resolving known malicious domains (DNS).
* checking outbound ports to the Internet.
* checking inbound ports from the Internet.
* Test detection of a remote shell (IDS)

## Testing time:
![test all the security things](/assets/images/2021-03-01/test-all-the-things.png){:class="img-responsive"}  
*Test. The. Important. Things.*

### Connecting to botnets and known attack networks:
Difficulty: Easy  
Use the EDROP list from [Spamhaus][https://www.spamhaus.org/drop/], which "include netblocks controlled by spammers and cybercriminals". Scan a few of these networks to see if your traffic is able to route to networks that you should never be able to route to.
```bash
nmap --top-ports 5 91.200.81.0/24 208.12.64.0/19 176.119.7.0/24
# scans network on 5 most common ports.
```
### Resolving known malicious domains (DNS):
Difficulty: Easy  




These tests need to be done securely. If you're unsure, or don't have the time to compile your own tests, register to use our tool below.


# Create an account and start testing!  
<script charset="utf-8" type="text/javascript" src="//js.hsforms.net/forms/shell.js"></script>
<script>
  hbspt.forms.create({
	portalId: "8898112",
	formId: "2b1cfdb3-6618-4dd8-86e4-4786274c0d38"
});
</script>

[create account]: #create-an-account-and-start-testing