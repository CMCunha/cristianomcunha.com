---
layout: post
title:  "There are NO Flaky Tests!"
date:   2025-04-15 10:00:00 +0100
img: 
categories: blog
comments: true
published: true
---

Hey there, glad to see you keep coming back ;)

This time I want to talk a bit about a subject that is impacting a lot of teams out there and sometimes I see them not approaching it the better way.
Let's talk about Flaky tests or, in my opinion, the fact that 
```note
there are not falky tests! 
```

# What is a Flaky Test?
First things firs, what is a Flaky Test anyway?
A flaky test is a test that both passes and fails periodically without any code changes.

Humm, so the code of the test do not change, the application also remains the same and we are using the same tool to run the tests but in some excutions they will pass and in another they will fail? On top of that we are saying that the problem is on the test...interesting.

```note
Have you ever heard of flaky apps or environments?
```

In fact I have never heard of flaky environment or flaky applications, can you imagine? Using an application that sometimes work and other times dont? It will not go that far...

At the end of the day tests are code, like applications, but we never heard of falky applications, why?
Well because we solve those issues when they rise intstead of just keep restarting the app (in my mind it is what would match the re-run scenarios of tests).

Let that sink in for a moment and let's see when have you experienced Flakyness?

# Have you experienced Flakyness?
When did it appeared? Have you, since the first approach to automation being hit by Flakyness? Probably not, with few tests that run in one machine they seem pretty stable and reliable.

In my experience there are a few reasons for their apperance, the one my top list is **poor code**, automated tests are code, and if you fail in producing good code you will end up with Flakyness. Sometimes I see that automated checks are given to less experienced developers as a punishment, would you give one of the most important feature of your product to them also? Automated checks are not easy, you need to understand the application, environment and users in order to deliver automated checks that are valuable. And do not forget that the code produced for these automated checks must be of high quality as they will be executed multiple times.

The other reason is having a **high number of web tests**, long and unreliable tests that will lead to Flakyness. This usually happens when we are converting all those manual tests into automated checks. We cannot just create automated checks for all the manual validations we had, this will for sure lead to a flaky behavior.

The testing strategy in some companies will demand **multiple environments**, one for dev, one for QA, one for staging, etc. But producing a lot of environments is not easy, and we all know that they will not have the same capacity of production, so having multiple environments means that we will maintain multiple applications/products in more limited environments and we expect that the tests will be successfull in all of them with so much possible failing points? 

The necessity of multiple environments implies that we are able to deploy our applications with **multiple configurations** and execute the automated checks also with different configurations, don't get me wrong it is not impossible but there is a lot of assumptions going on, and we all know that assumptions are the mother of all major fuck ups.

Last but not the least, **software architecture complexity**, how many layers do you have in your product/application? Do you use cache? How complex is the database? Is it distributed? Are you using messaging? Are you lost in the web of micro services? Does your system uses APIs? (internal and external).

And there can be others but at the end of the day this will
```note 
block a release.
```

Do not think that this is something that will only happen to  others, this will appear and most of the time when we least need it, when everyone is just waiting on automated chekcs to promote a build to production, BAM flaky behavior happens and we are just entering the retry mode until it work or we will just remove those tests from the execution, been there, was not pretty :()

# Risks of (not solving) flakiness
I started lifting the veil on some risks that encontering a flaky behavior may produce, beeing the most obvious one **delays in the delivery**, but here are lot of other impacts that sometimes we forget like **losing the confidence on thet tests**, how can we trust something that just fails from time to time without explanation? For me this is the worst of them all because once we lose the confidence in something it is really hard to reinstate it.

We were so fats in blaming the tests that we forget that that falky behavior is actually caused by something, and by automatically associating it to the test we may be **hiding problems** (in the architecture, Infrastructure or the code itself).

All of the above will lead to **cost of money**, time taken from our engineers is costly for the company and delays in the deliver also as a high impact in the company.

# Let’s deconstruct the ‘flaky test’

Why do we automatically blame the tests/checks?
Tests have found a Flaky behavior of the system



## Systems?

## Flakiness is (valuable) information
The system is telling you something….we need to listen

Performance/concurrence issues
Memory leaks
Incorrect configurations
Actual problems that are hard to replicate

## Cause of flaky behavior
Socio-technical systems are composed by hardware, software, physical surroundings, people, procedures, laws and regulation and data and data structure.
In our case we have considered:
Tests
Infrastructure
Target application


### Tests
Wrong approach/Mentality
Rely on test order
Data
Poor code quality
Lack of collaboration

### Infrastructure
Network configuration
Accesses
Authorization
Data manipulation (ex: Masking) 
Sizing (not enough MEM, CPU, DISK)


### Target Application
Memory leak
Deployment issue
Actual issues in the targeted app!

## (Our) Approach to deal with flakiness

### Invest in Information
Meaningful logs
Test
Application
Infra
Available

Add Information
Screenshots
Videos
Traces

Insightful reports
Enough to pinpoint the issue

### Invest in code
Review the test code
Incorrect assertions
Poorly coded tests
Active waits
Search methods

Generate good practices handbook
Examples with how flaky tests were solved
Work with development teams
Increase testability
Sharing sessions
All teams

### Create a quarantine strategy
Create a quarantine/quarantine_fix tag
Tag the tests that have detected the flaky behavior
Assure that the area is covered manually (if hurts it will not be forgotten)
Have a job that execute the quarantine tests in loop and register results (it is hard to know if we have corrected a flaky test)

### Rethink your testing approach
Too many end to end tests
Rethink your testing approach 
Layered approach	
Atomic tests
Shift left

Re-Run tests - NEVER


# Final considerations
The tests have found a flaky behavior in the system - They are not flaky!
Tests
Code quality
Information
Shift left
Layered approach

Infra
Data
Connections
Users
Information

Application
Bullet proof deploy
Collaboration
Testability


 
See you in my next article ;)
 
 

