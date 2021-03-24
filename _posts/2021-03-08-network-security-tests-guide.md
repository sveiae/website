---
title: "Critical Security Tests Part 1: Network Security Tests Guide"
last_modified_at: 2021-03-09T16:52:02-05:00
description: "Learn how to test your security controls in firewall and routers using your command line"
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
<!-- {% include leadfeederAnalytics.html %} -->

![feature image](/assets/images/2021-03-08/featureImage.jpg){:class="img-responsive"}  

TLDR: Learn how to test basic network security controls to ensure you got the basics down when it comes to nework security.

If you don't want to spend time writing your own tests, just download our app instead. [Register][create account] for a free trial of our testing software.

# Testing network security.
![compliance](/assets/images/2021-03-08/network.jpg){:class="img-responsive"}  
*securing connectivity between devices*

**Controls**  
Almost all networks have unused security controls:
* Home routers have firewall rules and can chose to use secure DNS servers.
* Home firewalls have VLANs, URL filtering, and sometimes even Intrusion Detection/Prevention.
* Enterprise firewalls can do deep packet inspection, SSL proxying, and advanced network monitoring.

Our testing will show if these controls are working.

**Tests**  
We'll be testing basic aspects of our controls by:
* Connecting to botnets and known attack networks.
* Resolving known malicious domains (DNS).
* Checking outbound ports to the Internet.
* Checking inbound ports from the Internet.
* Testing detection of remote shells (IDS)

![test all the security things](/assets/images/2021-03-08/test-all-the-things.png){:class="img-responsive"}  
*Test. The. Important. Things.*

## Example Network Security tests.

**Connect to botnets and known attack networks:**  
Use the EDROP list from [Spamhaus](https://www.spamhaus.org/drop/), which "include netblocks controlled by spammers and cybercriminals". Scan a few of these networks to see if your traffic is able to route to networks that you should never be able to route to.
```bash
nmap --top-ports 5 "91.200.81.0/24" "208.12.64.0/19" "176.119.7.0/24"
# Scan spamhaus networks on 5 most common ports and see what you're able to connect to. 
# Any accessible IP is a failure.
```

**Resolve known malicious domains (DNS):**  
Get domain lists from [Urlhaus](https://urlhaus.abuse.ch/api/#retrieve), which has attacker domains that should not be resolved. Create a shortened list which is easier to iterate to. These domain lists change all the time so it makes no sense for me to recommend specific domains.  
```bash
for i in $(cat short-list-of-urlhaus-domains.txt) | do host $i; done
# Iterate through list of evil domains, trying to resolve them.
# Any domain which resolves to a routable IP is a failure.
```

**Check outbound ports to the Internet:**  
Simply scan scanme.nmap.org.
```bash
nmap --top-ports 1000 scanme.nmap.org
# Testing top 1000 ports for outbound connections.
# Any unneeded, open, port is a failure.
```

**Check inbound ports from the Internet:**  
Simply scan scanme.nmap.org from a cloud host.
```bash
# from a server outside your own network:
nmap --top-ports 1000 "your IP"
# Any unneeded, open, port is a failure.
```

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



[create account]: #create-an-account-and-start-testing