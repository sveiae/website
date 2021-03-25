---
title: "Test driven security"
last_modified_at: 2021-03-15T16:52:02-05:00
description: "The reason why test driven security is the future of security testing"
categories:
  - Blog
tags:
  - Post Formats
  - readability
  - standard
  - link
image:
  path: /assets/images/2021-03-01/featureimage.jpg
  height: 100
  width: 100
---
{% include og.html %}
<!-- Google analytics -->
{% include googleAnalytics.html %}
<!-- leadfeeder analytics -->
<!-- {% include leadfeederAnalytics.html %} -->

![test driven security](/assets/images/2021-03-01/featureimage.jpg){:class="img-responsive"}  

Have you ever asked yourself if all your hard work and investments in security will pay off in stopping a cyber attack? You probably have, especially if you're in IT or in a leadership position. As a security professional for many years, I found myself asking this question a lot. I also asked others the same question. The answers I got was usually "I hope so" or "I think so". Usually the answer was followed up with "I wish I knew". 

# The need to know
The current state we're in is that information security professionals know --that they don't know-- how secure their own systems are, and [feel I'll equipped to manage security](https://www.isc2.org/-/media/B7E003F79E1D4043A0E74A57D5B6F33E.ashx). This extends to how [private citizens'](https://www.pewresearch.org/internet/2017/01/26/1-americans-experiences-with-data-security/) view companies' ability to manage security. There is little confidence accross the board.

The proven way to get more confidence is to **test whether what we're doing works, or if we need to improve on something**. This line of thinking ties into the methodology of failing fast.

It's like most other things in life - such as sports, personal health, and dating: You need to test to know.

## We're effective when we have clarity on our security gaps
The times we understand we have a significant security gap, we are able to put resources into fixing the problem: IT organizations, which usually are fairly stagnant, summon the troops, poor in resources, and quickly fix problems to reduce risk. Unfortunately this usually happens when news break about some exploitable vulnerability, after a annual penetration test, or when the organization fails a compliance requirement.

The main problem with this type of learning is that it is reactive and unstructured. In addition, the information we get is sometimes  irrelevant and over emphasized relative to other gaps, which results in a slow progression towards clarity. We need to find ways to learn about what is relevant to us, and to do it as fast as possible. This can be achieved through **methodic testing of relevant security controls and then analyzing the results.**

<!-- It's easy to sit and dream up ideal architectures
TLDR: Get control of your security. Jump into improving your security posture by seeing which important security controls you fail. This gives you immediate feedback on what you need to improve on, instead of going through the process of "dreaming up" ideal architectures, being overwhelmed by hundreds of pages of compliance documents, or worrying about the latest security news. -->


<!-- # Obstacles to clarity on security
Let's go over the main reasons why our attention isn't geared towards doing this in the first place...

![compliance](/assets/images/2021-03-01/paper-stack.jpeg){:class="img-responsive"}  
*NIST 800-53 anyone?*

## Data breaches everywhere
Year after year, we see data breaches in companies with plenty of information security funding. It's not a secret that **well-funded security teams also have a hard time implementing effective security controls, and an even harder time doing effective security testing** of said controls. Even when these controls have been known for a very long time and are fairly easy to implement. Teams lacking funding are usually doing even worse. Too many times simple controls are failing - like managing what outbound ports are allowed, tuning the IDS to detect shellcode, or ensuring the antivirus is turned ON. Furthermore security teams are surprised when they learn they fail such simple security controls. On the other hand, many of these same organizations don't have any problems passing a security audit.

Why are there breaches in companies that have great security tools, funding, and pass security compliance audits year after year?

## We're compliant, not secure... 
Being compliant simply means auditors found you to have sufficient controls in place. Having the newest security tech simply means just that, having new security tech. And having people working on security means you got people paid to do the job. We have to get away from thinking this equals effective security. 

## We're caught up in the hype
We spend lots of time and resources focusing on specific vulnerabilities which are oftentimes hyped up in the news. The fact is that you can spend days fixing ONE vulnerability, or you can put in place basic security controls that mitigate the vulnerability + hundreds/thousands of other vulnerabilities. This happens all the time. We're playing whack-a-mole with vulnerabilities instead of handling vulnerabilities holistically. This exact same thing happens in terms of any hype - like shiny new security tools promising to solve our problems once and for all.

## We're slow
There is another problem that might be even more striking in certain cases - security teams work like development teams worked 10 years ago: slow iterations, very little testing (except for patch management), and the feedback loop relies on real failures and an occasional audit.

![compliance and hype driven process](/assets/images/2021-03-01/static-security.png){:class="img-responsive"}  
*Typical compliance- and hype-driven process*

## Bad results over time
This, in turn, leads to a significant lag time in effective security controls implementations — from small business to large enterprises and government organizations. -->

# Solution: Test Driven Security
> What gets measured gets done —supposedly not Peter Drucker after all.

What we need in order to gain clarity, quickly, is to perform tests, and get quick and actionable feedback. This is a much better way than dreaming up ideal architectures, being overwhelmed by hundreds of pages of compliance documents, or worrying about the latest security news.

**Testing requirements:**  
* Know what is critical to test.
* Know how to test.
* Test often.

**Build, test, fix, repeat:**  
Similar to test driven development; a security team chooses the most important/effective controls which must not fail, writes tests that verifies whether they do - then whatever fails, is improved. Instead of slow and expensive iterations, we can get short and affordable iterations, with actionable feedback loops. Like below:

![test driven security](/assets/images/2021-03-01/test-driven-security.png){:class="img-responsive"}  
*Test driven security*

**Security controls requirements:**  
* Effective.
* Easy(ish) to implement.
* Measurable.

If at some point we have met all of these criteria, we could expand the scope to include controls that are either less effective, or harder to implement. We still need them to implement the controls in such a way that they can be measured.

**In the next articles we'll take a look at how we can run test driven [network security](https://www.securiful.com/blog/network-security-tests-guide/) and test driven [intrusion detection and monitoring](https://www.securiful.com/blog/intrusion-detection-tests-guide/)**

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