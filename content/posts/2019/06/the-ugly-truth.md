+++
date = "2019-06-26"
draft = false
title = "The ugly truth"
type = "post"
images = ["/images/odd-man.jpg"]
categories = [ "Thoughts", ]
tags = [ "Thoughts"]
thumbnail = "static/images/odd-man.jpg"
+++

I am so excited to meet my old friend Vinay after a long time. It has been almost one and half year we spoke to each other. We worked together in one of my previous organizations and he is a close friend and kind of mentor to me too.
We both got busy in our lives, and we are not in touch lately. I am so happy to meet him after a long time.

**Vinay:** Hey Rahul, how are you? 

**Rahul:** Fine Vinay, how are you?

**Vinay:** I am fine too. I think it's more than a year we met last time.

**Rahul:** Yeah, almost one and half year.

**Vinay:** When did you come back from Germany?

**Rahul:** Almost 4 months back. 

**Vinay:** Nice, so how are things going on? Did you write any new books?

**Rahul:** Things are fine. No, I didn't write any new books. I am bit occupied with other things. 

**Vinay:** So, how was your Germany experience?

**Rahul:** It's very good. The company work culture is good, facilities are nice. Made some good friends. Of course there are some problems like cold weather, food problem etc, but overall its a wonderful experience.

**Vinay:** Oh cool. So did you work on anything interesting?

**Rahul:** Ah, nothing much. Pretty standard stuff. Java, SpringBoot, JPA, some messaging systems etc.. the usual suspects. I didn't learn anything new from technical stand point, but learned a little bit about different cultures, importance of open communication, being compassionate etc.

**Vinay:** That's very nice. (after a pause of 10 seconds) hey, I am sensing a bit of change in you. Earlier whenever we meet within few minutes you start talking about some new technical stuff that you learned with so much excitement. But now even I am asking about it you are not showing much enthusiasm to talk about tech. What's going on?

**Rahul:** Hmmm...you are right Vinay. I am not really enjoying the technology as much as I used to. Things changed a lot. I feel the tech landscape is not getting any better, in fact I feel it's getting worse and worse.

**Vinay:** Why do you think so?

**Rahul:** You remember when we started our careers as Java developers, we primarily worked with Java 5, Servlets or Struts, JSPs, some home grown ORM or Hibernate and some frontend stuff like HTML, CSS, JavaScript and jQuery. Things were not great but we could get things done. Then came along new frameworks like Spring which simplifies a lot of things.

When we adopt those new technologies like Spring, Hibernate etc I could clearly see the benefits. Instead of writing 100 lines of code we could leverage those frameworks high-level abstractions and implement the same functionality say within 30 lines of code and they make testing much easier as well.

But I feel most of the recent frameworks or libraries or architectural approaches are not making anythings simpler, in fact they are making things unimaginably complex.

These days everyone wants to implement their application using microservices, serverless functions, want to use Docker, Kubernetes and deploy on some cloud. What they want to build, does that application needs microservices architecture all these are secondary. First decide on tech stack with all the latest bells and whistles irrespective of scaling needs and complexity of the system they want to build.

I can't explain how horrible it feels when the team spend 70% of the time fighting with this modern infrastructure setup and 30% of the time on actual business logic.

Did you ever see a Kubernetes YAML configuration file? Don't look at it if you have a choice. And the funny thing is people complain about "Oh Java is old, too much XML configuration, complex web.xml blah blah blah but they are fine with 23670 lines of YAML configuration files.

The current situation is now like just to setup a couple of microservices you need to setup a project with some new JVM language like Kotlin (if you use Java then you will considered as a legacy developer), then setup SpringBoot, Spring Cloud Config server, Eureka Server, Gateway service, of course you should use some messaging systems like RabbitMQ or Kafka, then central logging system like ELK or Splunk, distributed tracing using Zipkin, Hystrix CircuitBreaker, Retry mechanisms, docker based local development setup, Kubernetes deployment pipelines, Terraform or CloudFormation for infrastructure setup and the list goes on and on.

If the application that we are building truly requires it then it is okay to take the pain of managing all this complexity. But the reality is many organizations have complex systems that are built over a decade and it got complex and complex over the years and it reached to a point that enhancing it with new features is painful. Now they want to rebuild their system.

Their scaling needs might not change, they might not have the need for each sub-system to go to production independently,their current data center infrastructure might be more than enough for their scaling needs. 

Now they want to make things better. Instead of saying "we have a screwed up, but working, system in place and we want to clean it up and make it more maintainable" they ask for "we want you to do Digital Transformation of our systems or re-architect with modern software technologies". 

That's it. All the CTOs who born to do the digital transformations, all the architects who want to experiment with latest cool architectural styles, all the developers who want to get their hands on latest frameworks jump on to the situation and give a helping hand.

The worst thing is if some honest person tells the business folks that your business doesn't need all this complex high scaling needs, they don't like it. They like to see themselves as next Google or next Facebook. 

Actually for a while I thought maybe I am looking at all these as complex things because they are complex to learn and implement properly. So, I spent good amount of time to understand and how to implement them. Still I feel most of it is an unnecessary complexity, not worth the effort.

> I strongly believe that our IT industry is constantly trying to find an alternative to "Discipline" and in this process making things much worse.

**Vinay:** Oh my god, I thought it's just me who got overwhelmed with all these new things. Recently we started working on a new application and the architecture board decided to use ReactJS as frontend and SpringBoot on backend. 

I still can't get my head around this ReactJS ecosystem. There are billions things to stitch together to build a frontend application. There is **react, react-dom, redux, react-redux, react-router, react-router-dom, react-router-redux, redux-thunk, connected-react-router, react-reduct-myass-router-dom-redux**...I can't even remember the names of those npm modules for the god's sake.

**Rahul:** The dangerous thing is many people actually know that we don't actually need all this complexity but they don't risk saying it aloud.

All this new cool tech stuff craziness is one side of the coin only. The other size is even more ugly. 

I understand that we all want to feel what we do is important, but I don't understand this obsession of **I want to change the world**...**I want to make world a better place**. And they are planning to achieve this mission by implementing Enterprise Data Management CRUD applications...with some messaging queues in between.

**Vinay:** Enterprise Data Management CRUD applications....LOL

**Rahul:** Seriously Vinay, I don't understand this at all. If you work on something that would **improve the health of people, reduce pollution, decrease crime rate, reduce global warming, improve the food quality** then it makes sense to say I am making the world a better place. 

But honestly how many of us are working on such projects. Most of the projects that we work on is actually providing some sort of cozy comforts without which people can happily live too. In fact I strongly believe 60% of the features that we build are kind of nice to have features and most of the people don't even care about them.

In one of my previous projects, We were doing Inception for our new feature. Our mission is to **"Improve the quality of life of our users by reminding them about their future upcoming payment dues so that they don't end up paying penalties and can live with peace of mind"**.

While most of the people in the room are nodding their heads to the great mission of our new feature, I was thinking 


![Whaaat??!!!](https://media.giphy.com/media/3o7527pa7qs9kCG78A/giphy.gif)

**If the user is a responsible person they would pay their bills on time. If not they might pay the penalty one time and then onwards they will be careful. If they are not careful even after that then the user is an irresponsible person and we are planning to bring peace of mind to such irresponsible person using a reminder feature...wow!!!**

**Vinay:** LOL...making world a better place and bringing peace of mind with a Reminder feature..hehehe

**Rahul:** Along with **World Changers**, we also have **Thinkers**.

**Vinay:** Thinkers??

**Rahul:** Yes, Thinkers. 

![Thinkers](https://media.giphy.com/media/d3mlE7uhX8KFgEmY/giphy.gif)

Some people proudly badge themselves as a "Thinker" as if there are people who don't think. As far as I know all people think and do things. I don't know when it became necessary to explicitly tell the world that they "Think".

**Vinay:** Weird.

**Rahul:** One more weird thing I noticed in recent times is you got to trash some of well established tools and practices to look like a geek. 

When you see someone using Eclipse IDE you should immediately say **"OMG, I can't believe you are still using Eclipse in 2019...dude, grow up...use Intellij IDEA or become a real developer using Vim"**... 

![](https://media.giphy.com/media/xUOxf7BoJ9L9f5dR5K/giphy.gif)

You should look at somebody using Java and start saying **"Oh man, you are still using OO language...I can't imagine myself writing code in java...that's horrible...I prefer to code in Puuuuuuuuuuuuuure Functional programming languages like Haskel or Clojure"**.

**Vinay:** Yeah, we also have such people in my team. They didn't actually use Functional language on any production application so far but they keep talking about why should we use FP instead of OO language. The reality is all they know is how to generate Fibonacci series without any side effects and mutable state.

**Rahul:** Not only that, if you want to be part of the modern tech tribe you need to preach **"Live to code"**, **"Eat, Sleep, Code, Repeat"** anthem and participate in **#NoCode** movement and rally with **"Everyone should code"** placards.

What the hell is this "Everyone should code" madness anyway!!??? I am very glad that the great people like **Ilayaraja**, **SP Balasubrahmanyam**, **Sachin Tendulkar**, **ViswanathanAnand** etc were born before this dumbass internet age..otherwise they might have also turned into Functional Programmers, React Developers or DevOps engineers.

> I can't believe that after millions of years of human evolution we come to the conclusion of the purpose of life is to **"Live for code"**!!!

And by the way, are you aware of **#100DaysOfCode** yagam?

**Vinay:** What is **#100DaysOfCode** yagam?

**Rahul:** In the ancient Indian times saints and rushis do yagams for 9 days or 14 days for the wellbeing of kingdom. Nowadays software developers do [#100DaysOfCode](https://twitter.com/search?q=%23100DaysOfCode) yagam to make world a better place.

![100DaysOfCode Yagam](/images/yagam.jpg)

**Vinay:** Dude, stop..I can't laugh anymore. 

If you don't mind me saying, it seems you are going to have hard time to cope up with all this drama.

**Rahul:** Yeah. After seeing all this bullshit I really lost interest in learning any new things unless it is necessary for my job.

**Vinay:** I don't have any solution for your problems but let me tell you one simple trick that worked for me.

Few years ago I realized Job and Career are two different things. Job is something we do for money and Career is something we do for our soul satisfaction. Unfortunately many of us confuse between these two and try to find happiness in Job. Very very few lucky people only get soul satisfaction at job. 

When it is clearly evident that the job is not giving you that satisfaction but you are getting paid nicely then try to find happiness outside of work.

If I remember correctly you love reading books, watching movies and writing short stories. Spend more time on these activities.

**Rahul:** Yeah, I should find my passion somewhere else. Hey, talking about movies I saw a couple of wonderful movies recently. **12 Angry Men**, **It's a wonderful Life**, **My dinner with andre**, **To Kill a Mockingbird**...wonderful movies.

**Vinay:** Oh nice...I will try to watch them. 

As always it's wonderful talking to you. I need to go now, will see you soon.

**Rahul:** Sure...see you.
