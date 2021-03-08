---
title: "Critical security controls testing"
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

TLDR: I found a way to test critical security controls and significantly improve the security of a wide range of security architectures.

If you don’t want to read the reasoning of why I’m doing all of this you can **just skip to “examples of tests and what they measure”**, or head over to our [landing page][securiful-landing] to start testing.


# Problem: compliance- and-hype driven security

During my career, working in info sec, I’ve realized that security teams have a hard time implementing effective security controls, and an even harder time doing effective security testing of said controls. Even when these controls have been known for a very long time and are easy to implement.

Too many times I’ve tested a simple control, like checking what outbound ports are allowed, and the security team had no idea they would fail this simple test— or they had no idea this was an important security control.

Coming from application development, application security and penetration testing, the problem is probably more striking to me: security teams work like development teams worked 10 years ago: slow iterations, very little testing (except for patch management), and the feedback loop seems to rely on real failures and an occasional audit.

Blame time: I blame it on security marketing and security news (which are the same thing in many cases), overly complex security frameworks (from NIST usually), and a lack of willingness to do root cause analysis.

The end result is that we’re not prioritizing controls which are effective and easy to implement. This, in turn, has led to a significant lag time in effective security controls implementations — from small business to large enterprises and government organizations.




[securiful-landing]: https://www.securiful.com