---
layout: post
title:  "Automation Guild 2022"
date:   2022-03-17 16:00:00 +0100
img: automationguild2022.png
categories: blog
comments: true
published: true
---
Hey, I attended [Automation Guild 2022](https://guildconferences.com/automation-guild-2022/) and I was so pumped up that I had to put it in words!
 
It was my first time ever attending the TestGuild conferences, 5 days of test awesomeness, quoting [Joe Colantonio](https://twitter.com/joecolantonio) :)
 
As expected from great conferences it picked my brain and got me energized to make changes or investigate further some of those subjects.
 
I felt that it was a very well balanced conference, with talks spread between technical and non technical subjects, keeping the interest of the participants day in and out. Also recognizing that soft skills go hand to hand with automation, there is not one without the other because at the end of the day we need to convince people that automation is valuable and work with them to make it great and helpful.
 
The participants (a.k.a. Guild) are realy awesome, a bunch of people eager to learn, smart and most of all participating a lot! Giving another spin to this online conference.
 
The format was fully online and we have a central site to check the live events, a slido to post questions that will be answered in a live QA after each session and a slack channel per day to focus the conversations where everyone was interacting during the event.
At first I felt overwhelmed with so much going on, looking at the live event, reading what was being said in slack and reviewing questions in slido to make sure mine was not already posted. 

For me, my best configuration is to have, at least, two screens, one with the live feed and the slido questions and a second one with slack and a browser. In the screen with the live feed I can follow along what is happening and check the slido questions already posted or post my own. On the second screen I interact in slack with the guild, believe me there is always a conversation happening there about what we are seeing or just seen :) This way I feel on top of everything that is happening and of course I know that I can always view again or with more detail everything that is happening (I will miss the live interactions but still) which is a great advantage of having online conferences.

## Host
Joe Colantonio is a force of nature, well adapted to the streaming, it is noticeable that this is not his first rodeo, he conducts the live streaming doing the intros, engaging with the audience, reading slack entries and making sure all is running fine. Even in the face of a Vimeo crash that interrupted the videos, he reacted very fast and shifted to the youtube channel making adjustments to the live site in real time!
 
How do I know all of that, because he was transparent about it, showing that those super gurus online are persons just like the rest of us that makes things work when they need to work with one or another trick up their sleeve. This transparency also makes the guild more engaged with the conference because it really seems that we are there to make it work, together.
 
At the end of the day I am proud to be a tester, we can anticipate what can go wrong and be prepared to deliver, even with issues.
 
In the first three days I felt that there was a good balance between soft and technical talks, all focusing on automation and on how to reach it from all the angles and difficulties you can think of. On the last two days we saw an increase of focus in the technical part (oh yeah).
 
## Day 1
On the first day, the talk that got my brain pumped up was the first one presented by [Marcus Merrell](https://twitter.com/mmerrell) and [James Walker](https://twitter.com/automationjames) called "Stop Over-Testing! Taming the Combinatorial Explosion" focused on how to focus on your primary workflows and balance risk with coverage.
 
![Combinatorial Explosion](/assets/img/combinatorial_explosion.png){: .center-image}
 
They start talking about how difficult it is to have the right tests to cover the risks of a given application, and how misguided coverage is sometimes more harmful than helpful.
In fact on a lot of occasions I remember asking myself if we had the right coverage of tests to prevent major risks to reach production. There was no data to support my decision at the time and it was based merely on my experience from using the application.
They showed a modeling approach that will uncover the major workflows from your application and auto-generate tests based on risk profiles that in their case correspond to environments. In this approach we model our application in order to have all workflows represented, checkout, add to bag, or whatever is that you define as your workflows.
The application will then use the model to generate new tests to cover the model, now you can imagine the amount of possible combinations that this approach may generate, millions!
 
In their words:
```note
There are more combinations of things going on in our software development landscape than the stars in the universe.
```
 
We also know that, from those millions, some tests are not necessary or valuable, so we need to balance that out with risk profiles that will dictate what are the tests that matter and what are the tests that we do not need. With this approach we will reduce the amount of tests that we need to generate. In the example they are using [testmodeller](https://testmodeller.io/) as the modeling tool that will generate tests based on the model and saucelabs that will execute tests and return the results back. 
 
They even go further and connected neo4j, a graph database, to all tools used, such as Jira, Xray, source repo, etc, to be able to connect all informations in one place. This will allow them to extract powerful conclusions such as: we can inquire what are the commits that are linked to requirements, expanding on the last query we can extract what are the tests that are linked to the requirements and so that are covering the commits.
 
A great demonstration that if we manage to have one source of truth, connecting different tools and artifacts from different phases of the SDLC we can extract valuable conclusions and be more accurate in performing the right amount of actions.
 
Testing is hard and automation even harder, reaching to test everything is impossible! So having tools that can assist in choosing what to test and to automate are vital nowadays.
 
## Day 2
My favorite for the second day was the roundtable. There is something about talking with other great professionals such as [Darrel Farris](https://twitter.com/djbfarris), [Chris de Steuben](https://twitter.com/chrisdesteuben), [Laveena Ramchandani](https://twitter.com/Laveena_18) and Pradgnya Kulkarni, sharing the does and don'ts, the challenges and understanding different points of view and different experiences.
 
![Roundtable 2](/assets/img/roundtable_2.png){: .center-image}
 
The theme was: "The journey to quality Engineering" and the panel opened up with questions from the guild, from how they end in testing or what they should advise their past selves if they had the opportunity or if AI will replace testers in the future. A lot of great insights from leaders in the industry sharing their experiences.
 
Really good to see that we share the same difficulties, similar journeys and we are all here sharing to help each other. It is the real focus of the conference, helping each other with knowledge we have acquired along the years.
 
## Day 3
Day 3 was in and from all the amazing talks, one lure me in because I think that automation in testing is really an activity that need the same foundations as development, and as so, seeing Manpreet Singh talking about Design Patterns in Test Automation was refreshing, we have a lot to learn from using patterns that are well validated in development. Sometimes we think testing does not need such things as design patterns, it is this type of thinking that creates automation hard to maintain, to extend and overall to share with other teammates. Manpreet did a great job explaining those and the benefit of using them.
 
![Design Patterns](/assets/img/designpattern.png){: .center-image}
 
She went over SOLID principles (Single Responsibility, Open, Liskov Substitution, Interface Segregation and Dependency Inversion) and explained the concepts of singleton, factory design pattern and builder design pattern. We went over each of them with proper examples and pros and cons for each of them. The examples provided were clear and easy to understand.
 
I particularly liked this talk because it is putting test coding on the same level as development, where it should be, and not like something that anyone can do. At the end of the day we are programming, test indeed, but programming and for that we must have capable persons and follow best practices to produce maintainable and stable code.
Why not using validated patterns to make our automation life more easy?
 
In the next two days, more dedicated to technical talks, I was thrilled, what an amazing week it has been so far and now we are going to get to the serious things :)
 
## Day 4
On the fourth day I could not choose only one talk, so I want to refer three:
* How To Run Automated Testing For Audio And Video Applications from Nikolai Varlamov
* OpenTelemetry in Your Tests from Manuel de la Peña
* How to Minimize And Optimize Regression Set from Dmitriy Gumeniuk
 
Let me go over each so that I can explain what I liked in each :)
 
### First
**How To Run Automated Testing For Audio And Video Applications from Nikolai Varlamov** I always was curious to see how far we can get in automating tests for Audio and Video due to the challenge they represent (other challenges worth mentioning are validating machine learning or artificial intelligence applications). As I suspected it is not an exact science, we work with intervals, intervals to assess if the video quality is as expected or how far can we get in reducing quality to save disk space and bandwidth without losing video quality. It all comes out to how much the human eye can detect combined to how much you are disposed to lose in terms of quality to save space or increase communication.
 
![Design Patterns](/assets/img/audioandvideo.png){: .center-image}
 
Nikolai has shown different approaches he uses in his daily work and the presentation was packed with information that really opened my eyes to the different challenges present in such a demanding area. If you can check it as he goes over techniques and tools relevant to address those challenges.
 
### Second
**OpenTelemetry in Your Tests from Manuel de la Peña**, using [opentelemetry](https://opentelemetry.io/) to gather test metrics.
He starts by going over what is Observability, defining Observability as a collection of data from production (from logs, metrics and APM (Application Performance Monitoring)). It comes with tools for visual exploration of data so that it is possible to analyze, react and respond after an unexpected behavior.
 
By using telemetry to collect the data, but what is telemetry? Open Telemetry is the collection of vendor neutral tools, PAI and SDKs used to instrument, generate, collect and export  telemetry data, matrix, logs and traces to help you analyze your software performance and behavior.
 
He showed us how he used these tools to observe the CI/CD systems in production (this will help identifying issue in plugins used in the tools or credentials that were not rotated when they should) and how they help regarding notification and ownership of tests in the pipeline (he identified a process gap between test failing in the CI/CD process and the ownership of those failures by product teams, more so when we have tests that span between different products or teams). 
 
He shows why he has chosen to use XML as the base to exchange information between different systems, for testing tools almost all produce results in XML format which gives it an, almost, universal support. His presentation is heavily focused on Jenkins as it is their main tool used to support CI/CD processes.
 
At the time of the presentation he was still gathering data and did not have any report to show but expects to be able to identify flakiness of tests in the time window for example. This and other possible applications come to mind if we manage to have all that information connected, one question come to my mind:
![Open Telemetry](/assets/img/question1.png){: .center-image}
 
Manuel answered that he did not think in this possibility but given the data available it should be possible and he will, hopefully, follow this idea.
Hope he does :)

In his journey he managed to contribute back to the open telemetry plugin, well done!
 
 
### Third
**How to Minimize And Optimize Regression Set from Dmitriy Gumeniuk**, to finalize all of these my personal favorite of the three because it touches a subject that is close to my heart :) A tool ([drill4J](https://drill4j.github.io/)) that has the ability to gather coverage from e2e tests automation and from manual tests and with that information plus information about the source code of the release is able to know what tests we need to run if one piece of the code changes or if code is added it can suggest to add tests.
 
Understanding the impact of the changes, and because it has the information of the existent tests and their execution results, can define which tests must be executed to cover those changes instead of executing all the tests all the time.
 
![drill4j.png](/assets/img/drill4j.png){: .center-image}
 
I know I know it is not magical and we need to have agents in the environments to gather the data and sure they can have between 3-15% impact on the performance of the application but the gains justifies the means.
 
It got me thinking of the potentiality of such tool, imagine that we can execute it in production and understand, because we are monitoring real users, what are the areas of our application most used, understand the workflows of the users, in order to cross that with the actual tests we have, are we missing something or spending too much time in validating a feature that is almost never used?
 
Oh boy, the fourth day really got my brain thinking about the future and what incredible enhancements we can reach with automation.
 
## Day 5
The final day was upon us sadly, just now that I was getting the grip on the conference and my brain was sparkling with ideas, but hey this day was still packed with great talks, and what better ending that having an Ask Us Anything About E2E Automation in CI/CD panel? In fact, with most organizations shifting or wanting to shift towards DevOps, and with it, the implementation of CI/CD it is a conversation that has a lot of potential.
 
![cicd.png](/assets/img/cicd.png){: .center-image}
 
And again the guild did not let us down :) Questions around what was the panel opinion of having CI without CD or using production data in a non production environment, or even what to do with tests suits that take 1 hour to run and how they fit in the CI/CD process? Great conversation packed with opinions of persons with a lot of experience that really shed some light on their take on such important issues.
 
 
## Dealing with conference withdrawing
After being invested into the conference for 5 days you start to build a rhythm, I got excited to see the conference and to interact with the rest of the guild over great subjects. Having the videos on demand is great to be able to catch up whenever we have the possibility (not everyone is able to take one week from work to be present in such a conf), but I will advise everyone to be present in the live conference otherwise you will be missing one of the better features of this conference: interaction with other professionals. It is all about the sharing of experiences.
 
Great conversations were happening during the conference, around great day to day topics. It is always incredible hearing others sharing the same pain and showing how they tackle it, planting ideas on our minds for the future.
 
```note
"conferences like this one gets me fuel for the remainder of the year."
```

More than anything, conferences like this one gets me fuel for the remainder of the year, packed with experiences sharing, tooling and innovative approaches to challenges we are facing or will eventually. It is hard to come back to reality after such a great week! Miss the enlightenment, the conversations, the sharing!


## Wrapping up
I just want to thank Joe Colantonio and his team for putting together a conference focused on automation testing that is really packed with interesting content and speakers! More than that, he has managed to build a community around him that is full of people wanting to learn more and to help others, with no fear of participating. I went to some conferences where the level of participation is low and that only leaves us with the talks. In this one everyone engages with the speakers and with each other in the channels, it was a really good surprise, keep it going Joe!
 
If I was asked to summarize in one sentence what I have learned from this conference I would say:
Automation lives on! And it's here to serve us, we live in an era of data, so we need to find innovative ways to connect all information in order to be more efficient in all our actions by using the right tools for the job with the right technique (right for your challenge and context).

My final advise is to consider this conference a must go each year, I know I will :)
 
See you in my next article ;)
 
 
 
 

