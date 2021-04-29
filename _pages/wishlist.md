---
permalink: /requested-tests/
title: "Requested Tests"
---

<!-- Google analytics -->
{% include googleAnalytics.html %}
<!-- leadfeeder analytics -->
<!-- {% include leadfeederAnalytics.html %} -->

![feature image](/assets/images/requested-tests/crash-test-1620591_640.jpg){:class="img-responsive"}

These are the most highly ranked tests, that people have been recommending we implement into our testing platform through our email list.

**Test requirements**
* Can be done from a single computer
* We can expect to get similar results on similar systems in the organization.
* Does not need special software or hardware


## Test connectivity out to other countries
**CIS 12:** Boundary Defense  
**From:** Eion  
Implemented in platform: :heavy_check_mark:  
>Unfortunately most attacks come from a small set of countries, because of this we've started blocking entire IP blocks from the worst offenders (we use pfBlocker for this). In order to test that this control is implemented we do ongoing nmap of a random set of IPs within these blocks. You can get the IP blocks from: https://lite.ip2location.com/ip-address-ranges-by-country  

```bash
# From a computer on the Internet:
# open a cmd prompt, then simply run:
nmap -Pn --top-ports 10 bad-IPs-list
# The test will output a grading on your SSL configuration.
```

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

## Asess density of listening services in network
**CIS 9:** Limitation and Control of Network Ports, Protocols, and Services  
**From:** Brice  
Implemented in platform: :heavy_check_mark: 
>When it comes to listening services in the client network, I like to run a tight ship. We had an attacker in our network that was able to pivot wayyy to easy because our users stood up any server they wanted. Not anymore. The command below allow you to quickly see if there are any services that are anomalies in your network.  
```bash
# From a computer on the network:
# open a cmd prompt, then simply run:
nmap -Pn --top-ports 100 192.168.0.0/24 -oG result
# This will write the output to a file "result"
# Then count the number of services and sort by highest occurance:
$ cat result | grep -i open | grep -oE [0-9]\{1,4}/open | sort | uniq -c | sort -r
      53 22/open
      53 443/open
      1 21/open      <- anomaly
      1 3389/open    <- anomaly
```

## Check outbound ports to the Internet
**CIS 9:** Limitation and Control of Network Ports, Protocols and Services  
**From:** James  
Implemented in platform: :heavy_check_mark:  
>Unneded outbound ports are constantly used by attackers to call home. Simply scan scanme.nmap.org from your office computer. Any unneded ports is a failure.  

### Manual test:
```bash
# From a computer your own network:
nmap -p1-65535 scanme.nmap.org
# Any unneeded, open, port is a failure.
```

## Check antivirus is ON and reporting
**CIS 8:** Malware Defenses  
**From:** Brian  
Implemented in platform: :heavy_check_mark: [november 2020](https://www.securiful.com/monthly-security-tests/new-test-november/)
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

## Test SSL on company websites
**CIS 3:** Continuous Vulnerability Management  
**From:** Samir  
Implemented in platform: :x:  
### Manual Test:
>I started test my websites' SSL score myself after paying way too much for a 'pentester' to only find SSL flaws in a security audit.
Simply put in your website urls here: https://www.ssllabs.com/ssltest/ and then run the test.
You can also script this with nmap, which is what I do:  

```bash
# From a computer on the Internet:
# open a cmd prompt, then simply run:
nmap -sV --script ssl-enum-ciphers -p 443 your-websites
# The test will output a grading of your SSL configuration.
```

## Check user privileges
**CIS 4:** Controlled Use of Administrative Privileges  
**From:** Lindsey  
Implemented in platform: :x:  
>Check for privileges on your own computer. If you find yourself being admin (and your job is not being a system administrator) it's a good indicator that you need to look deeper into your organizations privilege management.  

```bash
# From the computer(s) under test:
# Check if we are running elevated:
whoami /groups | find "S-1-16-12288" && Echo I am running elevated, so I must be an admin
# Check if we belong to local administrators:
whoami /groups | find "S-1-5-32-544" && Echo I am a local admin
# Check if we belong to domain admins:
whoami /groups | find "-512 " && Echo I am a domain admin
# Track changes and audit for unnecessary privileges.
```

## Check for VPN split tunneling
**CIS 11:** Secure Configuration for Network Devices, such as Firewalls, Routers and Switches  
**From:** Anonymous  
Implemented in platform: :x:  
>The network team has on multiple times configured our endpoints VPN client run with split tunneling, practically bypassing most of our firewalls, IDSes, and URL filters. We have made the helpdesk team run this command at random times a day on about a quarter of our endpoints to ensure we don't run split tunneling anywhere.  

```bash
# From a remote client:
# open a cmd prompt, 
# then simply run:
Invoke-RestMethod ifconfig.me
# capture the data and run reports. 
```

## Assess average listening services per host
**CIS 9:** Limitation and Control of Network Ports, Protocols, and Services  
**From:** Brice  
Implemented in platform: :heavy_check_mark:  
>Unfortunately most attacks come from a small set of countries, because of this we've started blocking entire IP blocks from the worst offenders (we use pfBlocker for this). In order to test that this control is implemented we do ongoing nmap of a random set of IPs within these blocks. You can get the IP blocks from: https://lite.ip2location.com/ip-address-ranges-by-country  

```bash
# From a computer on the network:
# open a cmd prompt, then simply run:
nmap -Pn --top-ports 100 192.168.0.0/24 -oG result
# This will write the output to a file "result"
# Then count the number of services and sort by highest occurance:
cat result | grep -i open | grep -oE [0-9]\{1,4}/open | sort | uniq -c | sort -r
```

## Assess diversity of services inside your network
**CIS 4:** Limitation and Control of Network Ports, Protocols, and Services   
**From:** Ash  
Implemented in platform: :heavy_check_mark:  
>Check for privileges on your own computer. If you find yourself being admin (and your job is not being a system administrator) it's a good indicator that you need to look deeper into your organizations privilege management.  

```bash
# From the computer(s) under test:
# Check if we are running elevated:
whoami /groups | find "S-1-16-12288" && Echo I am running elevated, so I must be an admin
# Check if we belong to local administrators:
whoami /groups | find "S-1-5-32-544" && Echo I am a local admin
# Check if we belong to domain admins:
whoami /groups | find "-512 " && Echo I am a domain admin
# Track changes and audit for unnecessary privileges.
```

## Test connectivity from other countries to your organization
**CIS 12:** Boundary Defense  
**From:** Jason  
Implemented in platform: :x:  
>The network team has on multiple times configured our endpoints VPN client run with split tunneling, practically bypassing most of our firewalls, IDSes, and URL filters. We have made the helpdesk team run this command at random times a day on about a quarter of our endpoints to ensure we don't run split tunneling anywhere.  

```bash
# From a remote client:
# open a cmd prompt, 
# then simply run:
Invoke-RestMethod ifconfig.me
# capture the data and run reports. 
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