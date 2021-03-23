---
title: "Obstacles to security clarity"
last_modified_at: 2021-05-01T16:52:02-05:00
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
{% include leadfeederAnalytics.html %}

If you're wondering why your security efforts don't seem to pay off that much in terms of actually securing your system, you're not alone. Security professionals, and company leaderships, [feel I'll equipped to manage security](https://www.isc2.org/-/media/B7E003F79E1D4043A0E74A57D5B6F33E.ashx), and have been thinking this for a long time. 

<!-- ## Data breaches everywhere -->
Year after year, we see data breaches in companies with plenty of information security funding. It's not a secret that **well-funded security teams also have a hard time implementing effective security controls, and an even harder time doing effective security testing** of said controls. Even when these controls have been known for a very long time and are fairly easy to implement. Teams lacking funding are usually doing even worse. Too many times simple controls are failing - like managing what outbound ports are allowed, tuning the IDS to detecting obvious hacking, or even ensuring the antivirus is turned 'ON'. Furthermore security teams are surprised when they learn they fail such simple security controls. On the other hand, many of these same organizations don't have any problems passing a security audit.

<!-- Why are there breaches in companies that have great security tools, funding, and pass security compliance audits year after year? -->

This post will point out many of the hinders to effective cyber security, while outlining the remedy for some of the pains associated with securing your organizations IT systems.

# Sources of confusion
Let's go over the main reasons why our attention isn't geared towards doing this in the first place...

![compliance](/assets/images/2021-03-01/paper-stack.jpeg){:class="img-responsive"}  
*NIST 800-53 anyone?*

## 1. We're compliant, not secure
Being compliant simply means auditors found you to have sufficient controls in place. Having the newest security tech simply means just that, having new security tech. And having people working on security means you got people paid to do the job. We have to get away from thinking this equals effective security. 

## 2. We're caught up in the hype
We spend lots of time and resources focusing on specific vulnerabilities which are oftentimes hyped up in the news. The fact is that you can spend days fixing ONE vulnerability, or you can put in place basic security controls that mitigate the vulnerability + hundreds/thousands of other vulnerabilities. This happens all the time. We're playing whack-a-mole with vulnerabilities instead of handling vulnerabilities holistically. This exact same thing happens in terms of any hype - like shiny new security tools promising to solve our problems once and for all.

## 3. We're slow
There is another problem that might be even more striking in certain cases - security teams work like development teams worked 10 years ago: slow iterations, very little testing (except for patch management). And the feedback loop relies on real failures and an occasional audit.

![compliance and hype driven process](/assets/images/2021-03-01/static-security.png){:class="img-responsive"}  
*Typical compliance- and hype-driven process*

## Bad results over time
This, in turn, leads to a significant lag time in effective security controls implementations — from small business to large enterprises and government organizations.

# Solution: Test Driven Security
The solution is to test important security controls as quickly and often as possible. This is what's referred to as test driven security. If you're interested in learning more, read on the method of [test driven security]({% post_url 2021-03-01-why-test-driven-security.md}), or check out posts on how to actually do the testing, starting with [network tests]({% _posts/2021-03-08-network-security-tests-guide)

![test driven security](/assets/images/2021-03-01/test-driven-security.png){:class="img-responsive"}  
*Test driven security*

If you like this article, please share using the buttons below!

Thanks!

## Create an account and to use our test app!  
<script charset="utf-8" type="text/javascript" src="//js.hsforms.net/forms/shell.js"></script>
<script>
  hbspt.forms.create({
	portalId: "8898112",
	formId: "2b1cfdb3-6618-4dd8-86e4-4786274c0d38"
});
</script>

[create account]: #create-an-account-and-start-testing