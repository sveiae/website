---
title: "Critical Security Tests Part 2: Intrusion Detection and Monitoring Tests"
last_modified_at: 2021-03-10T14:42:02-05:00
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

TLDR: Learn how to test network monitoring and detection to improve your security beyond the very basics.

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

![test all the security things](/assets/images/2021-03-08/test-all-the-things.png){:class="img-responsive"}  
*Test. The. Important. Things.*

# Example IDS/IPS + SIEM tests.

**Sending command-and-control traffic:**  
Run command below:
```bash
printf "GET /kU2QLsNB6TzexJv5vGdunVXT.php HTTP/1.1\r\n\r\nUser-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/74.0.3729.169 Safari/537.36\r\nHost: 107.23.248.210\r\nAccept: */*\r\n\r\n" | nc -v 107.23.248.210 80
# should create an IDS event alerting of a Microsoft Spyware called Strong Pity.
# you will get a flag back which you can see if you actually are able to detect with deep packet inspection.
```
Then see what hosts you're able to connect to.

**Sending shell to a server:**  
Run command below:
```bash
to be continued...
# iterate through list of evil domains, trying to resolve them.
```
Then see what domains are actually resolved.

**Sending exploit kit traffic**  
Run command below:
```bash
printf "GET /a.php?e=2884 HTTP/1.1\r\n\r\nUser-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/74.0.3729.169 Safari/537.36\r\nHost: 107.23.248.210\r\nAccept: */*\r\n\r\n" | nc -v 107.23.248.210 80
# should create an IDS event alerting of a Teletubbies Adobe Flash exploit indication.
# you will get a flag back which you can see if you actually are able to detect with deep 
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