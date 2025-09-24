---
title: "Is Software Development Hard? Or, We are making it complicated?"
author: Siva
images: ["/images/mind.png"]
type: post
draft: false
date: 2024-06-19T04:59:17+05:30
url: /is-software-development-hard
toc: false
categories: [Thoughts]
tags: [Thoughts]
---

You started your career as a software developer. Learned some basics and learning many more as you go on.
As a responsible developer who wants to be good at your craft, you read the highly recommended books 
such as **"Clean Code"**, **"Refactoring"**, **"Growing Object-Oriented Software Guided by Tests"**, etc.

You also try to improve your craft by learning **TDD(Test Driven Development)**, **DDD(Domain Driven Design)**,
**Clean/Hexagonal/Onion/Ports&Adapter** Architecture. You definitely feel you are getting better at software development.

<!--more-->

While you can clearly see the benefits of some of these techniques, you are still not very sure about some of the practices.
You think maybe it's because of your lack of understanding or not yet matured enough to understand those great ideas.
But you never gave up. Every few weeks/months later, you keep trying those ideas again to see if you understand them now.
But still, you are not very sure about the benefits of some of those practices or techniques.

Again, you think it's your lack of skills because of which you are not able to see the benefits of those practices.
Years pass by...you keep trying to understand, but keep failing...decades pass by...you keep trying to understand, but keep failing.

You ask the experts, and they told you **"Your question is wrong"** or **"Your pet-project is not complex enough to see the benefits"**.
**You wonder, though it's a pet project, the usecases are the same as many usecases you worked in real projects.!!!**

One fine day, you thought maybe some of those practices were not really that great or not applicable to the work I am doing.
Then you start taking a closer look at those practices and realize that many
(over)enthusiasts conveniently forgot telling when to apply them and when not to.

And, some idealists take those ideas to extremes telling there is only one "right way" to do it, 
and if you are not following those said practices, then you are not a professional developer.

But you are too afraid to say this out loud because of the risk of people seeing you as stupid.
But there is a limit to everything, and finally one day you said, "I don't like some of those practices".
I am not going to blame myself for not seeing the benefits of using some of those practices 
when I am not seeing the benefits even after trying them for years.

**Feels familiar? This is my current state of mind.**

And, guess what? It's not just you who are feeling this way.
Many others also feel the same way, but too afraid to say it out loud because people are very eager to judge you 
if you are not part of their "elite circle" of echo-chamber.
But again, you reached to a point where you don't give a shit about how people judge you based on their 
"strong opinions" and their "there is only one right way" narrow mindset.


-------------------------------

Okay, let's see what exactly I am talking about.

**Let's talk about TDD.**

I love automated testing. I prefer running an automated test to verify whether some functionality is working or not rather than 
starting the application, navigating through a bunch of screens, submitting a form by filling out a bunch of fields manually everytime.

But "You should always write test first before writing production code, otherwise you are not doing TDD" is something I disagree with.

When I am implementing a feature, I read the task, analyze it, get a high-level thought about how I am going to implement it and then start coding.
I create a class (production code), write a method with arguments based on my current understanding and implementing very basic functionality.
It would typically take 30 seconds to 2 minutes. Then I use my IDE shortcut **Cmd + Shift+ T** to create a test and write a basic test.
Then I enhance the implementation with more code and parallelly extend the test(s) or create new tests.

At the end of an hour or so, I have the feature implemented with proper test suite.

My goal is to implement the feature, well tested with automated test suite.

Creating an instance of class that doesn't exist, calling a method that doesn't exist and then 
using your IDE shortcuts to create those classes/methods work for you, great.

But creating the class or method first and then using IDE shortcut to create test(s) works for me.
A common argument against this is, if you write production code first, then your tests depend on implementation details.

If I am writing a unit test that needs some mock setup then whichever approach I follow, my tests will depend on implementation details.
If I am writing an integration test, then irrespective of the approach I can write the test without depending on implementation details.

I am not writing the entire production code for few hours, test it manually and then writing tests for the sake of coverage.
The production code and tests evolve parallelly step by step in incremental way. This worked great for me.

Now, can I say I am doing TDD? Many TDD enthusiasts disagree hysterically.

You might often see the tweets **"Its unfortunate that even in {year} you need to tell you should write test first in TDD"** by some popular people.
When so-called "thought leaders" say this, it makes an impression that "everyone agreed this is the only right way to follow TDD".
This implicit assumption stops people even asking questions about following slight variations of TDD.

Anyway, as I said, my approach works great for me. I don't need to convince anybody. So it's all good.

**What about Clean/Hexagonal/Onion/Ports&Adapters Architecture?**

I tried countless times to really like these architectural styles. 
But in the end, I fail to see any benefit. 
After converting a module from my [preferred approach](https://github.com/sivaprasadreddy/tomato-architecture) to these styles, 
the code looks unnecessarily complicated.

I have mostly worked on data-centric applications throughout my career.
I am not a big fan of Clean/Hexagonal/Onion/Ports&Adapters Architecture, especially for data-centric applications.
The key advertised benefit of those architectural styles is the ability to isolate infrastructure concerns 
from core domain logic.

In most of the business applications there will be low-to-medium complex business logic but heavily relies on 
infrastructure of databases, message brokers, external API integrations, etc. 
For such applications, the ability to test core domain logic isolating the infrastructure is not very beneficial. 
Rather, I love to eliminate the unnecessary indirections(interfaces) and be able to test the logic with 
infrastructure components using tools like [Testcontainers](https://testcontainers.com/).

In most of the business (data-centric) applications that I worked on, the usual tasks are:

* Receive user input as REST API call, a form submitted or a message from message broker
* Validate basic things like required fields, min/max/regex checks
* Validate against existing data like email already exists
* Save or update the data
* Retrieve the data from multiple sources(tables)
* Return the only necessary data for that specific usecase
* Optionally, publish events to a message broker to be consumed by other systems

Most of the data-centric business applications involve these tasks.

Many people suggest DDD as the golden standard for building applications.
I like some aspects of DDD such as:

* Using ubiquitous language
* Defining Bounded Context
* Modelling value objects, entities, repositories, application services, etc

But the key aspect of DDD is Aggregate.

I know the difference between entity and aggregate. Usually, a unit of work is applied at the Aggregate level.

Some DDD proponents suggest following some strict rules of how (not)to access an aggregate/entity directly and everything should go through Aggregate only.
That is all well and good until an usecase comes around where it requires accessing a list of entities 
(You know my classic example of Post and Comment and the usecase ofAdmin need to view list comments of all posts).
Based on the usecase, DDD rules get relaxed and entity is promoted to become an Aggregate.
So, I prefer to directly model the domain based on usecases than arbitrary rules suggested by purists.

After trying to understand the nuances of all these concepts, 
I settled for the following approach for data-centric applications.

* Create separate classes to handle different UseCases
* Create separate request and response models for each usecase. This might result in some classes having same fields, but that's ok.
* Follow CQRS (you don't have to separate read DB and write DB). Using a single model representation for both reads and writes complicate things.
* Write unit tests for testing any business logic that involves calculations, etc using mocks if necessary
* Write integration tests for testing APIs using real infrastructure components

It is as simple as that.

This is my experience and opinions after working on data-centric applications for many years.

If you are going to tell me that **Anemic domain model** with the **Transaction Script Pattern** is bad, 
tell that to the entrepreneurs who run multi million-dollar business by just using google sheets. 

If Clean/Hexagonal/Onion/Ports&Adapters Architecture works for you, that's great.

But, as I already said, I don't see much benefit of using these styles for data-centric applications.
And, I am happy that I put this "maybe I couldn't see the greatness of Hexagonal/Onion/Ports&Adapters Architecture" 
lingering thought hanging over my head for years to the rest.

## Do we(developers) love complexity?
If you read this far, you might be thinking I am blaming those visionary thought leaders for software development complexity.
Well, not really. I actually think, we(software developers) also like to complicate things.

Let me tell you a simple story.

I started programming using Windows OS, and I didn't use Linux at least for 5 years after I started my career as a software developer.
Then a friend introduced me to the Linux and I installed Ubuntu with dual boot mode.

Formatting the drive, installing OS, installing a bunch of software from the terminal is fun.
When Wi-Fi or Bluetooth doesn't work, fishing thru linux forums, running random linux commands and finally fixing the issue felt great.
The very next day I update the system, and a lot of things get broken again. And I repeat the same processing of running various commands suggested in forums and fixing the issues feels geeky.

One time I bought a new model laptop for which Wi-Fi drivers are not yet released, but there is a GitHub repository with the drivers implementation.
I cloned that repo, build the drivers using Make file and install them, and it worked. That day I felt like an uber-geek.

After doing all this, do you think I used Linux as my daily driver? Nope.
Once linux is updated and fixed, I switched to Windows and did my regular work.
Then why on earth I spend all the time and effort in fixing those linux driver issues?

I want to feel like a geek by doing complex things. I love solving complex problems.

I used to read open-source projects code on GitHub to learn how others do things.
If the code is simple, I skip it and find the next one.
I wanted to see the code that uses reflection and do some crazy things.
I want to read the code that uses strategy pattern than a simple Enum or if-else even though 
there will never be a need for another strategy. Ohhhh, that craving for complexity in the initial years...

Some developers love "to hate PHP".
Can we find more extensible CMS than WordPress written in PHP?
Why there are not many Laravel like more productive framework in your favourite non-PHP language?
Who has time to find out. We are busy copying bean properties from layer to layer endlessly!!!

I am 100% sure that it's just not me. Many people can correlate to this.
If there are no complex things to do, then what we do? We make the simple things complicated and then solve it. Isn't it?
We, developers, love complexity, at least for some time.

Now I am in my 40's and I greatly appreciate simplicity.
I want my application code as boring as possible so that I can finish my work and take care of things at home.
I like challenges, but not every day.

I re-watch this [RailsConf 2014 - Keynote: Writing Software by David Heinemeier Hansson](https://www.youtube.com/watch?v=9LfmrkyP81M)
 now and then to remind myself about the beauty of keeping things simple and avoiding cargo-cult mindset.

**Conclusion**

We are lucky that today we have an enormous amount of material available at our fingertips to learn how to build complex systems.
Just because some thought leaders said something is great, don't need to follow them blindly.
Most importantly, don't need to hesitate to question the status quo if something doesn't feel right.

Not everyone is building the next facebook or google or netflix.
Just because you prepared for System Design interviews, don't need to apply all those creative and complex solutions 
to your business application, which has a max of 5000 users at any given time.

If anyone tries to tell you "just in case if you want to use a different database...", RUN as fast as you can.
