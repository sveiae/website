---
title: "Test Driven Security"
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

# If attackers can do it, you can test it.
TLDR: Use standard tests to see how your security posture is doing, instead of reading up on hundreds of pages of compliance documents or worrying about the latest security news. If you just want to start testing, head over to [landing page][securiful-landing] to register for a free trial of our testing software.

## Problem: compliance- and-hype driven security
->![compliance](/assets/images/2021-03-01/paper-stack.jpeg){:class="img-responsive"}<-
->*NIST 800-53 anyone?*<-

Year after year, we see data breaches in companies with plenty of information security funding. It's not a secret that well-funded security teams have a hard time implementing **effective security controls**, and an even harder time doing **effective security testing** of said controls. Even when these controls have been known for a very long time and are easy to implement. Teams lacking funding are usually doing even worse. Too many times simple controls are failing - like managing what outbound ports are allowed, tuning the IDS to detect shellcode, or ensuring the antivirus is turned ON. Furthermore security teams are surprised to fail these kinds of simple tests. It's just not something we're focusing on. On the other hand, many of these same organizations don't have any problems passing a security audit.

Why are there breaches in companies that have great security tools, funding, and pass security compliance audits year after year?

It happens because being compliant simply means an auditor found you to have sufficient controls in place. Having the newest security tech simply means just that, having new security tech. And having people working on security means you got people. We have to get away from thinking this equals effective security controls. The truth is **we’re not prioritizing controls which are effective and easy to implement**. The good news is that it's easy to do something about.

There is another problem that might be even more striking - security teams work like development teams worked 10 years ago: slow iterations, very little testing (except for patch management), and the feedback loop seems to rely on real failures and an occasional audit.

In summary there are three problems:
* We don't know **how** to test.
* we don't know **what** to test.
* We don't automate testing.

This, in turn, lead to a significant lag time in effective security controls implementations — from small business to large enterprises and government organizations.

![compliance and hype driven process](/assets/images/2021-03-01/static-security.png){:class="img-responsive"}
*Typical compliance- and hype-driven process*

## Solution: test-driven security
> What doesn’t get measured doesn’t get done —supposedly not Peter Drucker after all.

**Build, test, fix, repeat:**
The solution was to make something similar to test driven development; a security team chooses the most important/effective controls that must be passed, writes tests that verifies its effectiveness. Then whatever they fail on, they improve. Instead of slow and expensive iterations, we can get short and affordable iterations, with sensible feedback loops. At least that’s the idea. Like below:

![test driven security](/assets/images/2021-03-01/test-driven-security.png){:class="img-responsive"}

**Security controls requirements:** 
* Effective.
* Easy to implement.
* Measurable.
If at some point we have met all of these criteria, we could expand the scope to include controls that are either less effective, or harder to implement. We still need them to be measurable however.

## Basic security test examples:
![test all the security things](/assets/images/2021-03-01/test-all-the-things.png){:class="img-responsive"}

We're compiling more and more tests that you NEED to perform on your environment - whether it's for home office users, or in enterprise networks. Here are a few:
**List of all tests so far (more to come)**
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















[securiful-landing]: https://www.securiful.com