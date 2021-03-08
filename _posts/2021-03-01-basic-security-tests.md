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

# Implement fast, test fast, improve fast, repeat fast.
TLDR: Build, test, fix, repeat. Use standard tests to see how your security posture is doing, instead of reading up on hundreds of pages of compliance documents or worrying about the latest security news. If you don’t want to read the reasoning of why I’m doing all of this you can **just skip to “examples of tests and what they measure”**, or head over to our [landing page][securiful-landing] to start testing.

## Problem: compliance- and-hype driven security
During my career, working in info sec, I’ve realized that security teams have a hard time implementing **effective security controls**, and an even harder time doing **effective security testing** of said controls. Even when these controls have been known for a very long time and are easy to implement.

Too many times I’ve tested a simple control, like checking what outbound ports are allowed, and the security team had no idea they would fail this simple test— or they had no idea this was an important security control.

Coming from application development, application security and penetration testing, the problem is probably more striking to me: security teams work like development teams worked 10 years ago: slow iterations, very little testing (except for patch management), and the feedback loop seems to rely on real failures and an occasional audit.

Blame time: I blame it on security marketing and security news (which are the same thing in many cases), overly complex security frameworks (from NIST usually), and a lack of willingness to do root cause analysis.

The end result is that **we’re not prioritizing controls which are effective and easy to implement**. This, in turn, has led to a significant lag time in effective security controls implementations — from small business to large enterprises and government organizations.

![compliance and hype driven process](/assets/images/2021-03-01/static-security.png){:class="img-responsive"}



## Solution: test-driven security
> What doesn’t get measured doesn’t get done —supposedly not Peter Drucker after all.

**Test driven security:**
The solution was to make something similar to test driven development; a security team chooses the most important/effective controls that must be passed, writes tests that verifies its effectiveness. Then whatever they fail on, they improve. Instead of slow and expensive iterations, we can get short and affordable iterations, with sensible feedback loops. At least that’s the idea. Like below:

![test driven security](/assets/images/2021-03-01/test-driven-security.png){:class="img-responsive"}

**Security controls requirements:** 
* Effective.
* Easy to implement.
* Measurable.
If at some point we have met all of these criteria, we could expand the scope to include controls that are either less effective, or harder to implement. We still need them to be measurable however.



## Basic security test examples:
![test all the security things](/assets/images/2021-03-01/test-all-the-things.png){:class="img-responsive"}
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