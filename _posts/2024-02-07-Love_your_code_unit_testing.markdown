---
layout: post
title:  "Love Your Code: Unit Testing – Why Should You Care?"
date:   2024-02-23 10:00:00 +0100
img: unit-tests-1.png
categories: blog
comments: true
published: true
--- 
In the paradigm of modern software development, the concept of unit testing stands as a pivotal cornerstone, ushering in a shift-left approach to code quality and reliability. Unit testing encompasses the systematic examination of individual components, or units, of software code in isolation, propelling developers towards a mindset that prioritizes code quality from the outset. These tests meticulously verify that each unit performs as expected, adhering to specified requirements and exhibiting the desired behavior. By embracing unit testing early in the development process, development teams foster a culture of proactive quality, paving the way for swift feedback loops, seamless integration, and enhanced software robustness.

Unit testing serves as the first quality gate in the software development lifecycle. A robust suite of unit tests ensures that code changes meet the required specifications before progressing further in the development pipeline. In fact, some development teams adopt the practice of not even initiating code reviews until unit tests have passed, thereby enforcing a stringent standard of quality from the outset.

The integration of unit testing facilitates a fast feedback loop, enabling developers to receive immediate validation of their code changes. This rapid feedback mechanism empowers developers to iterate with confidence and agility, addressing issues promptly and minimizing the risk of defects propagating further downstream.

Moreover, well-crafted unit tests build confidence in code changes, serving as a litmus test for the acceptability of merges between branches of code. When unit tests provide sufficient coverage and validation, developers can proceed with merging code changes between branches with confidence, knowing that the integrity and functionality of the software remain intact.

Let's dive in into unit tests a litle bit more and start with a typical question, who is responsible for unit tests?

# Responsibility and Ownership: Who's in Charge?
While developers traditionally spearhead the creation of unit tests, the responsibility for ensuring comprehensive test coverage transcends individual roles. Software testers play a pivotal role in advocating for rigorous unit testing practices, collaborating with developers to identify test scenarios, validate assumptions, and validate edge cases.
There is no doubt that you need technical knowledge to be able to write unit tests or adapt the code to be able to add unit tests. But unit tests are just the trigger to elevate quality, everyone should contribute to code reviews and with that understand the intent of the test and the underlying code. 
All the measures that we can extract with that should be everyone responsibility, if the code coverage drops
Beware to take those measurements as exactly that: measurements, not a goal that we need to blindly reach or be evaluated with. 
In summary, more technical persons must write the unit tests but the conception and review is shared amongst those technical persons and the ones with a sharp quality view of the product.

## Why Should Testers Care About Unit Testing?
Unit testing plays a crucial role in the software development lifecycle by verifying the correctness of individual units of code. It helps identify defects early in the development process, making it easier and more cost-effective to fix them. As testers, we should care about unit testing because it provides an additional layer of assurance that our code behaves as expected and meets the defined requirements. 
It also builds up the confidence of the team regarding changes made, for example if the team needs to refactor some code, the fact that they have unit tests defined will help in understanding if the changes have minimal quality in an automated way.

## How Can Non-Technical Testers Help in This Effort?
While unit testing may seem technical at first glance, non-technical testers can still contribute to the effort in several ways:

* **Reviewing Unit Test Cases**

    Non-technical testers can review unit test cases for clarity, completeness, and alignment with requirements.
    Providing Test Data: Testers can assist in identifying relevant test data and edge cases for unit testing scenarios.

* **Analyzing Test Results and Metrics**

    Testers can help analyze unit test results and identify patterns or trends that may indicate areas of concern.
    In the same way, caring about metrics can help directing effort into more critical areas or even discussing if those metrics and results are relevant.

# Advantages and Disadvantages: Unveiling the Duality
Unit testing bestows a myriad of advantages upon software development teams, they are the first barrier up to enhance quality but they need to be seen as another tool in your belt of quality tools that we must use but that are not enough by themselves.

> Unit tests are another tool in your quality belt, use it but be aware that you need all the other tools in your belt to achieve higher quality.

Let's look into some advantages:
* **Early Defect Detection** - Unit tests uncover defects at the earliest stages of development, minimizing the risk of costly rework and fostering code stability.
* **Reduced Time to Market** - Unit testing accelerates the development cycle by catching defects early, leading to faster time-to-market for software products.
* **Enhanced Code Quality** - By enforcing modular design principles and facilitating code refactoring, unit tests elevate code quality and maintainability. 
* **Accelerated Feedback Loops** - Swift execution of unit tests enables rapid iteration, empowering developers to iterate with confidence and agility.
* **Cost Savings** - Detecting and fixing defects early in the development process is more cost-effective than addressing them later in the life cycle.
* **Regression Prevention** - Unit tests act as a safety net, preventing regression issues when making code modifications or enhancements.

However, unit testing is not without its challenges. As in any practice there are advantages and disadvantages to using them. Next we will look into possible challenges that may arise when using unit tests:
* **Maintenance Overhead** - As codebases evolve, maintaining and updating unit tests can become arduous, requiring diligent attention to prevent test decay.
* **False Sense of Security** - While comprehensive unit test coverage is desirable, it does not guarantee flawless software. Unit tests must be supplemented by integration, system, and acceptance tests to ensure holistic quality assurance.

# Measurements for Tracking Evolution
As in any adoption we need ways to understand if we are going in the right direction, this is often achieved by using metrics. For unit tests there are some available metrics to track the evolution of unit testing efforts, but bare in mind that the ultimate goal is to raise the overall quality and the confidence of the team in changing code. 

> Fixating solely on metrics without comprehending their significance or the team's context can lead to an overemphasis on metrics, diverting attention from quality concerns.

Teams can monitor key metrics such as:

* **Code Coverage**
Measure the percentage of code covered by unit tests to ensure adequate test coverage. But there is a lot of ways you can calculate the coverage, namely:
    * **Statement Coverage** - measures the percentage of statements in your code that your tests execute. At first glance, you might wonder, “isn’t this the same as line coverage?” Indeed, statement coverage is similar to line coverage but takes into account single lines of code that contain multiple statements. If you always write one statement per line, your line coverage will be similar to your statement coverage.
    * **Branch Coverage** - measures the percentage of executed branches or decision points in the code, such as if statements or loops. It determines whether tests examine both the true and false branches of conditional statements.
    * **Line Coverage** - measures the percentage of executable code lines that your test suite executed. If a line of code remains unexecuted, it means that some part of the code hasn't been tested.
    * **Function Coverage** - is a straightforward metric. It captures the percentage of functions in your code that your tests call.

    Most code coverage tools include these four types of common code coverage. Choosing which code coverage metric to prioritize depends on specific project requirements, development practices, and testing goals.
* **Test Case Pass Rate**
Track the percentage of unit test cases that pass successfully to gauge the effectiveness of the testing strategy.

* **Defect Density**
Monitor the rate of defects identified through unit testing to assess the quality of the codebase. This is a little harder to achieve if you do not have tooling that allows the link between tests and defects but consider it as it is valuable information to have.

# Metrics and Pitfalls: Navigating the Terrain
Metrics serve as barometers of unit testing effectiveness, encompassing parameters such as code coverage, test suite execution time, and test failure rates. While these metrics provide valuable insights into the health of unit testing practices, they must be interpreted judiciously to avoid misinterpretation and misalignment with organizational goals.

Pitfalls abound in the realm of unit testing, including:

1. **Over-reliance on Code Coverage**
    While code coverage metrics offer visibility into test completeness, they do not guarantee test effectiveness or reliability.

2. **Brittle Tests**
    Fragile unit tests, characterized by excessive dependencies and tight coupling, are prone to failure and hinder code refactoring efforts.

Take metrics as they are, just that: Metrics. Use them to help you understand if the initial effort in investing in unit tests is maintained or to see if the unit tests are effective, but do not use them as measures for developer productivity, if you cross that bridge people will focus on reaching targets and not in enhancing quality.

# How Hard Is It to Achieve Unit Testing?
Achieving effective unit testing demands unwavering dedication, discipline, and a shared commitment to quality from both developers and testers. It encompasses crafting thorough test cases, maintaining robust code coverage, and continually refining the test suite as the codebase evolves.

More than a mere numbers game, successful unit testing requires a concerted effort to cultivate a testable application. While initially perceived as additional overhead, this investment is integral to enriching the value of unit tests. Though it may seem daunting initially, integrating unit testing seamlessly into daily workflows yields substantial benefits, serving as the first line of defense for quality assurance.

Embracing techniques like Test-Driven Development (TDD) and complementing with Behavior-Driven Development (BDD) offers a structured approach. With TDD emphasizing test-first methodology and BDD focusing on behavior-driven testing, both methodologies synergize to elevate code quality. By leveraging this combined approach, teams can effectively enhance the overall quality of their codebase.

# How AI Will Change Unit Testing
The advent of artificial intelligence (AI) is set to transform unit testing, automating test case generation, discerning patterns in test failures, and streamlining test execution. AI-driven testing tools hold promise in enhancing testers' capabilities, boosting test coverage, and expediting the testing process, heralding a new era of efficiency and innovation in software development.
Similar to other domains, I view AI's impact as a valuable companion—an assistant capable of providing insights and aiding progress towards objectives. While it's not yet at the stage of autonomously crafting unit tests without human oversight, it unquestionably serves as a potent ally to kickstart the process.

# Practical Example: Harnessing the Power of Copilot
Consider a scenario where a development team leverages GitHub Copilot, an AI-powered code completion tool, to streamline unit testing workflows. By analyzing code snippets and suggesting test cases in real-time, Copilot accelerates the creation of unit tests, fosters collaboration between developers and testers, and promotes code quality and consistency.

After installing [Copilot](https://docs.github.com/en/copilot/about-github-copilot) on my IDE (I'm using VScode) and it unlocks two possible usages to assist in my coding:

1. **Using Copilot Chat**
    Copilot Chat appears in the IDE as a chat window where we can interact with Copilot, one of the possible interactions is to create unit tests for a class or method. 

    To do so, open the chat area and write: */tests*, this will analyse the code in your workspace and generate unit tests for it.

    ![Copilot Chat](/assets/img/Copilot_chat.png){: .center-image}

    As you can see it suggested three tests:
    * 'should return an empty array when no books are provided'
        * Validating that when passing an empty array the result should be empty.

    * 'should return an empty array when an empty array is provided'
        * Validating that when an empty array is passed it should return an empty array back.

    * 'should correctly extract book information'
        * This one is really interesting, it is suggesting injecting information and has created a sample (remember that this was totally generated by Copilot). It inserts the data and then validates that when extracting it the values match.

    You can continue the interaction with it asking more specific questions or any code change.
    Once you are ok with the suggestions you can create a new test class.

2. **Using  Copilot Suggestions**
    Another way to use Copilot is integrated in your IDE when you are writing code, it is an upgrade of the autocomplete feature. Autocomplete was amazing, let me tell you, not having to know from heart all the methods and variables available for a language was a breeze. But actually having an entity advising, based on what you are writing, what code it thinks that you want to write is amazing!

    In fact, in the following example I just wrote the method name and it automatically suggested a series of tests based on the name given and on the knowledge of the code available.

    ![Copilot Suggestion](/assets/img/Copilot_suggestion.png){: .center-image}

    While it may not be entirely accurate or occasionally encounter failures, it serves as a sufficient foundation and saves valuable time.

    Imagine that one day it nails 100% of the suggestions, is it ready to write code and unit tests autonomously?

# Conclusion: Embracing the Unit Testing Imperative
Unit testing plays a pivotal role in fostering a culture of quality and reliability within development teams. By embracing unit testing as a shift-left practice, teams can accelerate feedback loops, enforce quality standards, and build confidence in code changes, ultimately delivering high-quality software products that meet end-user expectations. Embracing unit testing principles empowers testers to uphold code integrity, bolster software quality, and deliver value to stakeholders with unwavering confidence, making them catalysts for positive change in the ever-evolving landscape of software development.

Let us embark on this transformative journey, where unit testing reigns supreme, innovation thrives, and software excellence knows no bounds. Together, we shape the future of software testing, one unit test at a time.

You have now taken the first two steps towards increasing the quality of your overall SDLC with:
* [The Critical Role of Testing in Requirement Gathering: Building a Solid Foundation for Software Development](https://cristianomcunha.com/12Months_Journey_to_production/)

And now this article focuses on Unit Tests, the next step will be 'Testing in Agile: Strategies for Continuous Delivery'.

 See you in my next article ;)
