---
title: "Obstacles to security clarity"
last_modified_at: 2021-03-02T16:52:02-05:00
description: "The main reason why security efforts often are ineffective and expensive"
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

![compliance](/assets/images/2021-02-23/featureimage.jpg){:class="img-responsive"}  

If you're wondering why your security efforts don't seem to pay off that much in terms of actually securing your system, you're not alone. Security professionals, and company leaderships, [feel ill equipped to manage security](https://www.isc2.org/-/media/B7E003F79E1D4043A0E74A57D5B6F33E.ashx), and have been feeling this way for a long time. 

<!-- ## Data breaches everywhere -->
Year after year, we see data breaches in companies with plenty of information security funding. It's not a secret that **well-funded security teams also have a hard time implementing effective security controls, and an even harder time doing effective security testing** of said controls. Even when these controls have been known for a very long time and are fairly easy to implement. Teams lacking funding are usually doing even worse. Too many times simple controls are failing - like managing what outbound ports are allowed, tuning the IDS to detect obvious hacking, or even ensuring the antivirus is turned 'ON'. Furthermore security teams are surprised when they learn they fail such simple security controls. On the other hand, many of these same organizations don't have any problems passing a security audit.

<!-- Why are there breaches in companies that have great security tools, funding, and pass security compliance audits year after year? -->

This post will point out many of the hinders to effective cyber security, while outlining the remedy for some of the pains associated with securing an organization's IT systems.

# Sources of confusion
![compliance](/assets/images/2021-02-23/paper-stack.jpg){:class="img-responsive"}  
*NIST 800-53 anyone?*

Let's go over the main reasons why our attention isn't geared towards solving the basics of information security.

## 1. We're compliant, not secure
Being compliant simply means auditors found you to have sufficient controls in place. In practice, this means that someone, with *even less* understanding of your systems than the security team, tries to figure out if it is secure. For the most part, this becomes an exercise in creating paperwork which says "we do this, and we do that". At the end the auditor will usually give their blessing, along with a list of things to improve. 

The problem with audits is that it is in everyone's interest to pass a security audit; both the auditor and the employees of the organization under audit have a financial incentive to pass the audit. And so the incentive for passing the audit is far stronger than finding the truth. This is why audits do not give clarity on an organization's security - it usually only creates paperwork.

## 2. We're caught up in the hype
We spend lots of time and resources focusing on specific vulnerabilities which are oftentimes hyped up in the news. The fact is that you can spend days fixing ONE vulnerability, or you can put in place basic security controls that mitigate that one vulnerability, plus hundreds of other vulnerabilities. This happens all the time. We're playing whack-a-mole with vulnerabilities instead of handling vulnerabilities holistically. This exact same thing happens in terms of other types of security hypes - like shiny new security tools or training promising to solve our problems once and for all. 

## 3. We're slow
There is another problem that might be even more striking in certain cases - security teams work like development teams worked 10 years ago: slow iterations, very little testing (except for patch management). And the feedback loop relies on real failures and an occasional audit.

![compliance and hype driven process](/assets/images/2021-03-01/static-security.png){:class="img-responsive"}  
*Typical compliance- and hype-driven process*

## Bad results over time
This, in turn, leads to a significant lag time in effective security controls implementations — from small business to large enterprises and government organizations.

# Solution: Test Driven Security
The solution is to test important security controls as quickly and often as possible. This is what's referred to as test driven security. If you're interested in learning more, read on the method of [test driven security](https://www.securiful.com/blog/why-test-driven-security/), or check out posts on how to actually do the testing, starting with [network tests](https://www.securiful.com/blog/network-security-tests-guide/)

![test driven security](/assets/images/2021-03-01/test-driven-security.png){:class="img-responsive"}  
*Test driven security*

If you like this article, please share using the buttons below!

Thanks!

## Create an account and start testing!  
<script charset="utf-8" type="text/javascript" src="//js.hsforms.net/forms/shell.js"></script>
<script>
  hbspt.forms.create({
	portalId: "8898112",
	formId: "2b1cfdb3-6618-4dd8-86e4-4786274c0d38"
});
</script>

[create account]: #create-an-account-and-start-testing