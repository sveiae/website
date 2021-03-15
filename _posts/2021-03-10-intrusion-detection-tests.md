---
title: "Critical Security Tests Part 2: Intrusion Detection and Monitoring Tests"
last_modified_at: 2021-03-10T14:42:02-05:00
categories:
  - Blog
tags:
  - Post Formats
  # - readability
  - standard
  - link
---
<!-- Google analytics -->
{% include googleAnalytics.html %}
<!-- leadfeeder analytics -->
{% include leadfeederAnalytics.html %}

TLDR: Testing Network Detection and Monitoring controls isn't easy, but is incredibly important if you want to improve your security beyond the very basics.

If you want to start testing immediately, [register][create account] for a free trial of our testing software.

# Testing detection and monitoring controls.
![compliance](/assets/images/2021-03-10/snort-ids.jpeg){:class="img-responsive"}  
*Test your snort*


**Controls**  
Many business networks run appliances with unused or underutilized IDS and SIEM controls:
* Home: Open source or dedicated firewalls usually have an IDS and basic event monitoring
* Enterprise IDSes and SIEMs firewalls can do deep packet inspection, SSL proxying, and other lot of other network monitoring.

**Tests**  
We'll be testing basic aspects of our controls by:
* Sending command-and-control traffic to a server we control on the Internet.
* Sending a shell to a server we control on the Internet.
* Sending exploit kit traffic to a server we control on the Internet.
* Sending other indications of compromise type traffic.

![test all the security things](/assets/images/2021-03-08/test-all-the-things.png){:class="img-responsive"}  
*Test. The. Important. Things.*

# Example IDS/IPS + SIEM tests.

**Connecting to botnets and known attack networks:**  
Use the EDROP list from [Spamhaus](https://www.spamhaus.org/drop/), which "include netblocks controlled by spammers and cybercriminals". Scan a few of these networks to see if your traffic is able to route to networks that you should never be able to route to.
```bash
nmap --top-ports 5 "91.200.81.0/24" "208.12.64.0/19" "176.119.7.0/24"
# scans networks on 5 most common ports.
```
Then see what hosts you're able to connect to.

**Resolving known malicious domains (DNS):**  
Get domain lists from [Urlhaus](https://urlhaus.abuse.ch/api/#retrieve), which has attacker domains that should not be resolved. Create a shortened list which is easier to iterate to. These domain lists change all the time so it makes no sense for me to recommend specific domains.  
```bash
for i in $(cat short-list-of-urlhaus-domains.txt) | do host $i; done
# iterate through list of evil domains, trying to resolve them.
```
Then see what domains are actually resolved.

**Checking outbound ports to the Internet:**  
Simply scan scanme.nmap.org
```bash
nmap --top-ports 1000 scanme.nmap.org
# Testing top 1000 ports for outbound connections.
```
Then see which ports are open outbound to the Internet.

**Want a tool that does it all for you?**
These tests need to be done securely. If you're unsure, or don't have the time to compile your own tests, register to use our tool below.

# Create an account and start testing!  
Available tests for intrusion detection, prevention, and monitoring controls:

<style>
.tablelines table, .tablelines td, .tablelines th {
        border: 1px gray;
        }
</style>
|                       |  **Intrusion Detection** | **Intrusion Prevention**   | **Security Event Monitoring** |
| malware               | :heavy_check_mark:       | :heavy_check_mark:         | :heavy_check_mark:            |
| exploits              | :heavy_check_mark:       | :heavy_check_mark:         | :heavy_check_mark:            |
| shellcode             | :heavy_check_mark:       | :heavy_check_mark:         | :heavy_check_mark:            |
| c2c traffic           | :heavy_check_mark:       | :heavy_check_mark:         | :heavy_check_mark:            |
| browser attacks       | :heavy_check_mark:       | :heavy_check_mark:         |                               |
| web app attacks       | :heavy_check_mark:       | :heavy_check_mark:         |                               |
{: .tablelines}


<script charset="utf-8" type="text/javascript" src="//js.hsforms.net/forms/shell.js"></script>
<script>
  hbspt.forms.create({
	portalId: "8898112",
	formId: "2b1cfdb3-6618-4dd8-86e4-4786274c0d38"
});
</script>



[create account]: #create-an-account-and-start-testing