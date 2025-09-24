+++
date = "2020-03-06"
draft = true
title = "Life is too short to waste at toxic workplaces"
type = "post"
images = ["/images/businessman-1.jpg"]
categories = [ "Thoughts", ]
tags = [ "Thoughts"]
thumbnail = "static/images/businessman-1.jpg"
+++


# "Never give up"..."Fight till you die"...


Yesss...Never give up. Yes, these are the things that we keep hearing all the times, in movies, 
in self-help books, in motivational speeches.

But over the time I have a different perspective to it. 

> We should not give up so easily...but at the same time **it is very important to know when to give up and walk away**.

We all want to work in a good companies with healthy working environment. But sometimes we may end up working at not-so-good places.
Yeah, that's life. We don't always get what we want and we may have to compromise on few things. 

But what will happen if you stay at toxic work environment for long time?
What kind of impact it will have on your career and health?

Before discussing all that, first let me elaborate what I mean by **Toxic Work Environment**.

### Toxic Work Environment:
Suppose you are working at a place where the following things happen regularly and is considered quite normal.

* You work on a feature and implemented unit/integration tests and committed the code. 
Next day you want to make some change and when you open the test classes you noticed that all your tests are commented out or **@Ignored**.
When you ask why they did it, they say they change some common functionality and tests are failing due to that change so they commented out.

* When there is a change in functionality some tests are failing throwing **NullPointerException**. 
The awesome developers simply fixed it by adding **@Test(expected = NullPointerException.class)**.

<p align="center">
<img src="/images/cat-why.jpg" width="396" height="406.8" alt="How could you do that??!!!" />
</p>

* There is a mandatory process that there should be a minimum SonarQube code coverage of 80% before going to deployment. Fair enough.
How the awesome folks achieve it? Simple. Just add whatever the packages/classes that are not covered to ignore list.

<p align="center">
<img src="/images/jack-nicolson.gif" width="396" height="406.8" alt="Who is the boss??" />
</p>

* The awesome dev team don't bother to write tests, but as there is min 80% code coverage requirement, 
one fine day a new JIRA task will be created **"Make code coverage minimum 80%"** and assigned it to someone.
A ninja fullstack developer then used http://www.evosuite.org/ to generate tests and bang...in just 30 minutes we have 100% code coverage.

    **CAUTION NOTE:** If you are not strong minded person, don't dare to look at the generated tests hoping they are useful.

<p align="center">
<img src="https://i.imgflip.com/3rq6tc.jpg" title="made at imgflip.com"/>
</p>

* As per the TownHall meeting presentation by Senior Tech Leadership, we have great DevOps culture and we rigorously follow DevOps practices.
Automation is in our blood.

    **And the reality is:** We have a single repository for multiple microservices and a single Jenkins build pipeline. 
    Whenever we make changes to any services and want to deploy we should go to DevOps engineer and ask him to trigger the build.
    Then he will update jenkins file with **modulesToBuild = ["service-1", "service-4"]** and trigger the build. 
    If you want to build different set of modules you need to visit the DevOps guru and he will do the ritual.

    If someone honestly didn't know this is what is called CI/CD in that company and 
    updated Jenkins build pipeline by parameterizing the modules to build, environment to deploy etc so that 
    they don't have to change all the times.
    The poor guy tested it in multiple environments and everything is working fine. 
    And, when he come back next day and see the build pipeline everything is reverted.
    When he ask DevOps dude why they reverted, the answer is **We are the owners of CI/CD pipelines, who are you to change it!!!**.
    When he discuss this with manager the answer is **Why don't you focus on the application development 
    and leave the build pipeline issues to DevOps team**.

* Every once in a while there will be a **Agile Assessment Survey** (a.k.a Corporate Agile Drama) where the entire team sit in a room and have to nod head for everything Agile Coach/Manager says.
If you disagree with any point, good luck talking to them.

* QA team raise a defect and asks developer to check what is desired behaviour with BA. Developer pings BA to get what is expected behaviour.
BA pings another developer to check how it is implemented currently. Then BA says that is the expected behaviour. 
And developer conveys the same to QA. QA closes the defect. To put is simply "Nobody has a fucking clue on what they are doing".

* As per the leadership folks the company is an amazing place to work and they want to conduct 2 days Hackathon as a hiring process.
Guess what is the selection criteria??!!! **Select whoever worked all night**. 
I must really appreciate the selection committee for their clarity on what they want!!

* You will be given a 2001 year model laptop, without any privileges, you can't even set JAVA_HOME environment variable by yourself.
You need to go to admin team and stand in a queue for about 1 hour for such things. 
If your laptop is randomly restarting don't complain...that's not even a problem...just learn to be patient.

* A poor QA guy want to share knowledge on how they implemented automation testing using Selenium. 
    A bunch of senior devs, leads started asking him 
    
    * Does the tests automatically generated based on requirements? 
    * If you are writing tests manually then what is the guarantee that there isn't any bugs in tests?
    * Whenever there is a change in requirement we should update tests also which takes more time
    * Can we 100% rely on these automation tests and deploy to production? if not, why should we bother to write tests?
    etc etc
        
    And those awesome senior devs, leads finally convinced the QA guy who came to share his knowledge 
    that **Automation Testing is not very useful**.

I can go on and on..but I guess you get the point.

If you closely notice there are some common themes in all these instances:

* They are not very skilled and they don't want to learn either
* They are highly insecure about the job and they will make sure nothing is changed so that they can keep their jobs
* They create lot of problems to anyone trying to improve the situation until they become one among them

> Over all they create a culture where a good developer is the one who stay late nights and work on weekends.
They celebrate working on weekends, they feel proud of it and management also appreciate it.

 
If you are like me then you also may feel like this is a toxic place to work at. 
But what happen if you end up working in such environment for whatever reason?

### Consequences of working at toxic workplaces

When I started my career as a software developer I have one simple goal: **To make a living**.
I didn't have any aspirations of **Changing the world** or **Put a dent in the universe**.

But along the way I find software development very interesting and I keep learning the things to 
make myself a better developer than yesterday.
I read a lot of material on **Clean Code**, **Design Patterns**, **different architectural styles** etc and try to put it in practice as much as possible.

> End of the day it is a job and I do it to make a living. But some of us take pride in what we do and how good we do it.

What happen if you end up working in such a toxic workplace as I described above??
Instead of getting appreciation for the efforts you are putting to improve the situation, you will be facing problems with lot of people.
Especially if you have to deal with shitty developers, managers and architects at the same time it is not easy and most likely you may give up sooner or later.
Then you may start blending with them to get the ball rolling.

You start compromising on the code quality, don't bother to write tests because you know they most likely get commented out.
You stop asking for requirements clarification because you know whatever you implement may become the requirement.
You also don't give a damn about sharing knowledge because you know what happened to people who tried sharing their knowledge.

Even worse you may start feeling that having good technical skills is only good to give conference talks, 
write blog posts etc but literally of no use in day to day work.

Yes, I know software development is not all about coding. Soft skills and effective communication is very important to build applications successfully.
But no amount of soft skills can help you to improve something when they don't want to improve.

The very valuable skill of being a good developer that you feel proud of, suddenly becomes nothing.
Nothing makes you happy anymore. You start waking up at 2.30 AM and couldn't sleep. 
If you don't know what does it means waking up at 2.30AM regularly, it is an indication that you are 1 step away from depression.

You don't need this, you deserve better. There is no shame in walking away from this kind of shitty environment.

### Don't hesitate to walk away
I usually feel guilty if I have to walk away from a problem. But what could I possibly do in this kind of toxic workplace?
Is it even worth it? Even if you stay and try to improve the situation, assuming you have the power/designation, then there is slight chance of making things better over time.
But at the cost of what? Your mental health get screwed up, you may lost precious family time.

> **Remember one thing:** You can't bring change by force unless people truly believe in it. 
Otherwise things go back to the way they are in the very second you take eyes off of them. 

We have one life and by god's grace we are blessed with health and family. There is no need to sacrifice them for a job.
Walk away from such toxic places and there is no shame in it.

When you think of leaving job at such a bad workplace what could possibly make you stay? May be good salary or big brand.
When you are so unhappy that you don't even have motivation to spend that money then it is not worth it.
Brand...yeah...let me tell you something about brand.

### Don't fall into the trap of big Brands
It feels so good to say "I am working at Apple" or "I am working at Google" rather than "I am working at Xyz India Pvt Limited". Isn't it?

Working at such a big branded companies have many benefits...better pay..better credibility etc etc. 
But I am not sure working there would make you happy!!??
I can't comment on such top tier companies because I never working at such companies. 
But there are many "Next best thing" type popular companies which claims to be thought leaders, pioneers of "insert your favourite buzzwords here".

Let me tell you a simple story.

**A girl fall in love with a guy and then they got married. And then on the very first night he shows his true character by selling the girl to a brothel house.**

Another small story:

**You went to a famous restaurant for breakfast and they gave you food from street side stall**.

How do you feel in such scenario? Its cheating..right?

Be careful while joining some popular companies looking at their past glory. 
They might have turned into a mere **Outsourcing consulting company** and 
they may send you as a contractor/consultant to the companies with toxic work culture as I described above.
While joining they might smartly mention it in a polished way that "You might have to work at client location to closely work with business stakeholders". Look out for such traps.

Don't blindly believe what you see on social media. You can't even imagine how different their projection on social media and the reality is.
Looking at their wild popularity in the community if you join in that organization, when you see how things actually are you may go like 
**MY EYES...MY EYES...**

<img src="/images/my-eyes-phoeby.gif" width="396" height="406.8" alt="My Eyes Oh My GIF - MyEyes OhMy Phoebe GIFs" />

There are many not so well known small ir medium sized companies which are also good. Try them. 
There might be a good chance to prove yourself in such small companies.

### Summary
Life is too short to waste in such a toxic work environments. Try if you can influence and make things better.
You may feel like when everyone else is adjusting to such environment why can't I? But think about is it worth the struggle?
If you are sure that the environment can't be changed then move on. The longer you stay at such places the more damage will happen to your mental health and career.
After all YOLO :-)
