---
title: "Why test driven security?"
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

# What gets tested, gets done.
TLDR: Get control of your security. Jump into improving your security posture by seeing which important security controls you fail. This gives you immediate feedback on what you need to improve on, instead of going through the process of "dreaming up" ideal architectures, being overwhelmed by hundreds of pages of compliance documents, or worrying about the latest security news.

If you want to start testing immediately, [download][create account] a free trial of our testing software.

## Problem: compliance- and-hype driven security.
![compliance](/assets/images/2021-03-01/paper-stack.jpeg){:class="img-responsive"}  
*NIST 800-53 anyone?*

**Data breaches everywhere**  
Year after year, we see data breaches in companies with plenty of information security funding. It's not a secret that well-funded security teams have a hard time implementing **effective security controls**, and an even harder time doing **effective security testing** of said controls. Even when these controls have been known for a very long time and are easy to implement. Teams lacking funding are usually doing even worse. Too many times simple controls are failing - like managing what outbound ports are allowed, tuning the IDS to detect shellcode, or ensuring the antivirus is turned ON. Furthermore security teams are surprised to fail these kinds of simple tests. It's just not something we're focusing on. On the other hand, many of these same organizations don't have any problems passing a security audit.

Why are there breaches in companies that have great security tools, funding, and pass security compliance audits year after year?

**We're compliant, not secure...**  
It happens because being compliant simply means an auditor found you to have sufficient controls in place. Having the newest security tech simply means just that, having new security tech. And having people working on security means you got people. We have to get away from thinking this equals effective security controls. The truth is **we’re not prioritizing** controls which are effective and easy to implement. The good news is that it's easy to do something about.

**We're caught up in the hype**  
We spend lots of time and resources focusing on specific vulnerabilities which are reported in the news. The problem with this is that you can spend days fixing ONE vulnerability, or you can put in place the security control that mitigates the vulnerability + hundreds/thousands of other vulnerabilities. This happens all the time. We're playing whack-a-mole with vulnerabilities instead of putting in place simple security controls that handle vulnerabilities holistically. This exact same thing happens in terms of any hype - like shiny new security tools promising to solve our problems once and for all.

**We're slow**  
There is another problem that might be even more striking in certain cases - security teams work like development teams worked 10 years ago: slow iterations, very little testing (except for patch management), and the feedback loop seems to rely on real failures and an occasional audit.

![compliance and hype driven process](/assets/images/2021-03-01/static-security.png){:class="img-responsive"}  
*Typical compliance- and hype-driven process*

**Bad results over time**  
This, in turn, leads to a significant lag time in effective security controls implementations — from small business to large enterprises and government organizations.


## Solution: Test critical controls - often
> What gets measured gets done —supposedly not Peter Drucker after all.

**What we need to do is:**  
* Know **what** to test.
* Know **how** to test.
* **Automate** testing.
* Test often.

**Build, test, fix, repeat:**  
Similar to test driven development; a security team chooses the most important/effective controls that must be passed, writes tests that verifies its effectiveness. Then whatever they fail on, they improve. Instead of slow and expensive iterations, we can get short and affordable iterations, with actionable feedback loops. Like below:

![test driven security](/assets/images/2021-03-01/test-driven-security.png){:class="img-responsive"}  
*Test driven security*

**Security controls requirements:**
* Effective.
* Easy to implement.
* Measurable.

If at some point we have met all of these criteria, we could expand the scope to include controls that are either less effective, or harder to implement. We still need them to be measurable however.

## Basic security test examples:
![test all the security things](/assets/images/2021-03-01/test-all-the-things.png){:class="img-responsive"}  
*Test. The. Important. Things.*

**List of all tests (more to come):**  
* connecting to known malware download sites.
* connecting to botnets and known attack networks.
* connecting to all the countries in the world (three are many I have no interest in connecting to).
* resolving known malicious domains.
* checking outbound ports to the Internet.
* checking inbound ports from the Internet.
* checking open ports and services inside my network.
* check if VPN is running ‘split tunnel’ and bypassing a bunch of controls (important in these times).
* checking if my antivirus actually detects malware.
* ensuring security and event logs are generated and sent to my central server.
* testing all kinds of traffic that the IDS should detect on, and see if the IDS analyst reacts to it.

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