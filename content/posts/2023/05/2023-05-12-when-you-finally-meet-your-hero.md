---
title: When you finally meet your hero
author: Siva
images: ["/images/superhero.png"]
type: post
draft: false
date: 2023-05-12T04:59:17+05:30
url: /2023/05/when-you-finally-meet-your-hero/
categories: [Life]
tags: [Life]
---

It's already 8.50am. I got stuck in the traffic, and I doubt I would be on time for the meeting by 9.30am.
Somehow, I managed to reach the office by 9.35am, and it looks like the meeting is not yet started.
Oh, I didn't tell you why I am so excited for this meeting, right. 
It's actually a workshop, and it's going to be conducted by **Mr Vinod**. **THE AWESOME VINOD**.

<!--more-->

Vinod joined our organization 7 months ago as an enterprise architect and oh man, he is just awesome.
I didn't have the opportunity to work with him directly, but I have attended some of the meetings he was in, and he is a legend.
The way he presents his ideas, how good he is with software architectural concepts...he is just charismatic.

Luckily, we got approval from business to rewrite one of the old applications and 
Vinod will be the architect for this stream of work. That's why I am super excited to attend this workshop where Vinod will walk us 
through the new architecture for this application. I am sure I am going to learn a lot from Vinod.

---------------------
The workshop started at 9:45am and Vinod is presenting his thoughts on the application's new architecture.
He said we will be following **Microservices architecture**, and in each service we will follow 
**Hexagonal Architecture, CQRS and Event Sourcing**.

I have read a lot about these Hexagonal Architecture, CQRS and Event Sourcing concepts, but when it comes to actual implementation, I see a lot of challenges.
I don't think I fully understand those concepts, and I hope I can get more clarity on these concepts from Vinod.

Around 10:15am, somebody opened the door and came to attend the workshop, and he is none other than **Mr Ajay**.
I never worked with him closely, but based on what I heard about this guy, he is good for nothing but to maintain old legacy applications, 
fixing small bugs, he has no interest in learning new things etc etc.

Vinod continued explaining at a high level how this application architecture would look like, what are the technologies we are going to use, etc.

I was taking notes and recollecting various questions I had on Hexagonal Architecture, CQRS and Event Sourcing concepts but never found satisfying answers.

---------------------

The first day workshop was over by 4.45pm, and I went to Vinod to see if he has some free time and ask the questions I had about 
Hexagonal Architecture, CQRS and Event Sourcing concepts.

**Me:** Hi Vinod, I am Siva.

**Vinod:** Hey Siva

**Me:** Today's workshop was really good. I am super excited to work on this project.

**Vinod:** Thanks. I am also very excited to work on this project. 

**Me:** You mentioned we will use Hexagonal Architecture, CQRS and Event Sourcing. I read about these concepts, but I feel I don't fully understand them well enough.
If you don't mind, can I ask you a few questions?

**Vinod:** Sure, why not.

Then I started asking various questions about Hexagonal Architecture. 
Then Vinod starts explaining what is Hexagonal Architecture, how it helps in decoupling core domain from infrastructure, etc.

But I am familiar with all this theory at high level, so I wanted to go a little bit more implementation level details.
So, I gave a specific example scenario and asked him how Hexagonal Architecture will actually help here.

Then again Vinod started giving high-level theoretical explanations about Hexagonal Architecture.

I thought maybe I am not able to grasp what he is saying. I don't want to push beyond this today, so I thanked him and left for the day.

---------------------

After going home, I was wondering maybe I wasn't clearly explaining to him the questions I had.
It would be better if I create a sample application and ask the questions with code examples.
So, I created a sample application with my understanding of Hexagonal Architecture and written down a series of questions.

I hope Vinod will understand my questions clearly now as I am showing practical challenges with code examples.

---------------------

Next day again after the workshop, I went to Vinod, showed him the sample application and asked a couple of questions on this scenario how to handle this problem.

To my surprise and disappointment, he again started giving high-level theoretical explanations about Hexagonal Architecture.

Then I interrupted Vinod and said, I understand the high-level conceptual idea about Hexagonal Architecture.
But, I am not able to find the proper way to handle this scenario. 
So, putting aside the theory, my question is, how **exactly** you would implement this specific feature following Hexagonal Architecture?

Then I noticed Vinod is getting uncomfortable, I can see that in his face. Then he gave a sassy answer. 

> **That my friend is a low-level implementation detail that I want you to figure out instead of me giving away the answer.**

And he took his laptop and left.

It took me a couple of minutes to absorb what just happened. 

If he doesn't know the answer, that's absolutely fine. Nobody knows everything.
But the way he escaped by throwing "It's a low-level implementation detail that I want you to figure out instead of me giving away the answer" 
on my face and just left felt very rude to me.

I don't know what just happened. I don't know whether I did anything wrong or he is just one of those 
**"buzzword throwing bullshitters"**.
Whatever it is, I thought tomorrow I will meet him and apologize if I was rude and move on.

---------------------

Next day I went to the office a little early and went to the cafeteria to have breakfast.
There I see Vinod and a few of his close friends(colleagues) sitting. 
I wished Vinod and his friends good morning and sat at a nearby table and having my breakfast.

One of Vinod's friends loudly said to the person who served them coffee, 

> Hey, coffee is very tasty today. How **EXACTLY** you mixed sugar and coffee powder?

And the whole Vinod and his 6 other friends burst into laughter.

I understand what just happened. He was mocking me the way I asked Vinod: **how exactly you would implement this specific feature following Hexagonal Architecture**.

I looked at Vinod, and he looked at me and gave a smirk.

![Smirk](https://media.tenor.com/Dh6mA-6Q43sAAAAd/supernatural-you-know-it.gif)

Here is the thing about certain people. For some, self-respect is at most important.
When you insult them beyond certain limit, then they don't hesitate to hit back, no matter the consequences.
It may impact their career, or next salary hike... it doesn't matter.

Vinod did what he could, and now it's my turn.

---------------------

The first 2 days of workshop went smooth because everyone has an overwhelmingly positive opinion on Vinod.
Everyone is so amazed at Vinod's charismatic presentation skills that people forget to ask the right questions.
Today as usually, Vinod started his presentation, throwing all the fancy buzzwords that managers and business folks love to hear, 
throwing all the latest cool technology names that developers love to hear.

Giving a break to his mesmerizing presentation, Vinod asked does anyone have any questions.

I have been working at this company for 4 years, and I know a little bit more about the business domain, how different systems interact with each other,
how much time it may take for making a tiny change in one service, etc...which Vinod has no clue about.

I raised my hand indicating I have questions, and I started asking: 

The proposed architecture doesn't seem to take into the consideration of integration with other systems and made some assumptions about their APIs.

**Me:** Hey Sunil (tech lead of another application that we need to integrate with), is your application exposes REST APIs already?

**Sunil:** No, currently we are processing the data using a scheduler job and data shared via FTP.

**Me:** Vinod, you mentioned we are going to implement process all the data using Event Driven Architecture in async fashion. 
If I am not wrong, currently the fraud-detection service is implemented in such a way that it performs preliminary checks synchronously.
Is that service going to update to fit with our new proposed design? Are our estimates taking that effort into account? 

Then there was a pin drop silence for about 1 minute.

A moment ago it was like **"Vinod's proposed architecture is awesome"** and now it became 
**"it looks like the proposed architecture didn't take many ground realities into account"**.

In addition to that, various other team managers and tech leads start asking questions about how this design is going to affect their services, 
does he know how the current integration happens between their service and the existing implementation, etc.

People started talking among themselves, discussing will this new proposed design actually work or not, 
whether the estimated timelines are achievable at all or not.

Finally, breaking the silence, Vinod said evidently there are few things that need to be revised in the proposed architecture.
Thanks Siva for bringing it up, I appreciate it. We will continue the workshop tomorrow.

**Raj(another team manager):** Should we continue tomorrow, or is it better to understand how various systems interact with each other currently and come up with a new proposal later?

After 30 seconds of silence, Vinod said, I will let you know by EOD today.

After the workshop ended abruptly, I was at water cooler drinking water and coincidentally, Vinod came there.
Then I gave the badass Clint Eastwood look.

![Ever noticed how every once in a while you come across someone you shouldn't be fucking with?, That's me](/images/clint-eastwood-quotes-fucked-with.jpeg)

Later that day we get email that workshop is postponed for a few weeks.

---------------------

2 days later....

We got a P1 production issue that our batch jobs are failing under high-load, and we are not able to replicate that issue in any other lower environments.
We did some guess work and tried various fixes, but nothing worked.

My manager, who still thinks Vinod is awesome, suggested us to talk to Vinod and using his vast experience fix this bug ASAP.

As I don't want to waste time on hearing theoretical lectures at that moment, I sent another developer to talk to Vinod, just to obey my manager's suggestion.

While we are banging our heads on how to solve this high-priority issue, 
**Ajay** walked to me and said "I overheard that you are facing the database connection intermittent failure issues".

**Do you remember Ajay, the guy who came to workshop late, and nobody has any good opinion on him...yeah the same guy.**

I don't have any hope that he will be of any help for us, but anyway, I explained the problem we are facing and what we have already tried.

Then he took a minute and suggested to change the database setting on AWS RDS configuration and append some flag as part of JDBC URL.

As we don't have any other better solution, we tried Ajay's suggestion and to my surprise, it worked. 
After that change, we are not getting those errors even under the peak load.

I thanked Ajay for helping us, but we all have that ego right. 

How come I couldn't find that solution? 
How come he, a guy who is good for nothing but to maintain old legacy applications, could solve this so easily???

> After fighting with my ego for 5 minutes, my manners kicked in and inner myself told me that 
"Fuck your ego and don't be an asshole. Go and talk to Ajay and learn from him how that fix actually works".

---------------------

Next day I saw him at the cafeteria and went to him and introduced myself and once again thanked him for helping us out.

**Me:** I was searching on stackoverflow and read a lot of blogs etc and nowhere I could find any clue what is causing the issue and how to fix it.
How do you know about this issue and fix it?

**Ajay:** Sometime back we got a similar issue in our application too, and it took me 5 days to figure out the root cause and fix it.

after 2 minutes of silence...

**Ajay:** You didn't think I could solve this issue, right? I could see that on your face yesterday.

**Me:** Sorry, but yes. Based on what I heard, I didn't think you will solve it so easily.

**Ajay:** Don't worry. Most of the people here think I am not a skilled developer, and I am way past being offended by that. 

**Me:** If you don't mind, can you explain what is the root cause of that problem and how that configuration actually fix it?

In the next 15 minutes, Ajay explained to me what is the root cause and how this RDS config change internally works to prevent that problem.

I was blown away by his explanation. I am not a genius but I can recognize a genius when I see one.

**Me:** That was awesome Ajay. Once again I am sorry for misjudging you.

**Ajay:** Don't worry about it. See you later.

---------------------

Next day, after lunch, I was going for a walk and I saw Ajay sitting alone.
I went to him, and after some casual conversation:

**Me:** Can I ask you something, if you don't mind.

**Ajay:** Sure.

**Me:** Why many people think you are not a very skilled developer?

**Ajay:** Hahaha, maybe you need to ask them.

**Me:** Sorry if I am offending you, but I am really surprised why many people feel that way about you while you are clearly super talented.

**Ajay:** Siva, I know I am not dumb and I don't feel like I need to prove it to everyone.

You know, these days most of the developers are chasing all the shiny new technologies 
and learning only the basics of 100 different things without having deeper knowledge on any one of them.

On the other hand, I like to gain deeper knowledge on few things than jumping on every hyped technology.
I am not really familiar with many new technologies that are created in recent years.
But I have strong knowledge on running production grade highly-scalable applications and what kind of problems occurs during peak loads and how to handle them.

I know how to tune Java Garbage Collection configuration, how to handle database connection starvation, how to configure server level thread pools,
what kind of file system is better for I/O heavy applications.

But, nowadays people hardly care about them. They would say my cloud provider can auto-scale the application based on load.
They don't care about tuning the application or how much fat the AWS bill will become.

I don't know how to scaffold the "SPA of the week" frontend application. I don't know what is the fancy name people are giving to write modular applications.

So, when people find out that I don't know about `npx create-react-app`, 
they think I am only good for maintaining legacy applications.

Thankfully, my manager knows that the only person who knows how this system actually works is me.
So, they are not going to fire me and I won't be getting any recognition awards or good salary hikes.

**Me:** Doesn't that bother you?

**Ajay:** In the beginning it does. But not anymore.

In fact, the way people think about me is actually helping me to maintain work-life balance.
Nobody has high expectations from me. Nobody asks me to motivate anyone else. 
Nobody asks me to give a presentation on how to improve productivity.
I come to the office at 10am and leave by 6pm sharp. Once in a while, we get some tricky production issues, and I need to spend a little bit more time.
Apart from it, I would say I am the only person who has work-life balance in this company :-)

**Me:** Oh man, you are a gold mine of knowledge. Not just about tech but also life in general.

---------------------

Next day, again we are taking a walk after lunch...

**Ajay:** Hey Siva, can I ask you something?

**Me:** Sure

**Ajay:** What happened between you and Vinod during that workshop? I kind of felt you were pissed off at Vinod.

I told him the whole story of what happened.

**Ajay:** Oh, he should have handled it in a nicer way.

You know, companies need these kinds of people who throw fancy buzzwords with American accent.
While talking to potential customers, these are the people who get clients to the company by saying all those fancy buzzwords.
So, company management always feels they are more important than a developer like you and me. 
So, if you want to grow, then you should not mess with those folks.

**Me:** Who said I want to grow?

**Me & Ajay:** hahaha

**Ajay:** Welcome to the club!!

---------------------

A Few weeks later, we had annual appraisal meetings...

**Ajay:** How was your appraisal discussion?

**Me:** I got "Meets Expectation" rating with a special note of I need to improve my team collaboration skills.
And as I guessed, I was moved to a different project so that Vinod doesn't have to deal with me anymore.
How was yours?

**Ajay:** Same "Meets Expectation", just like the past 6 years. 

---------------------

It's 9pm, I just had my dinner and leaned on my bed staring at the ceiling.

It's funny how each of us see the world very differently.

**My manager thinks Vinod is great. I think Vinod is a buzzword-throwing bullshitter. 
Vinod thinks I am an asshole. I think Ajay is a hardcore techie. Many people in our company think Ajay is unnecessary baggage.
Me and Ajay think we both are awesome.**

So many angles, so many perspectives.

While all these thoughts are flowing through my mind, my wife just walked in to the room.

Then I asked my wife, **what do you think of me? Am I a good software developer or not?**

**My wife:** I think you are an over thinker who forgets to bring a milk packet in the evening even after reminding it for 10 times.

**Me:** You know, a wise man once said, 

> **You can convince the whole world that you are a genius, but you can never be as good as your wife expects you to be.**

**My wife:** Looks like that wise man hasn't got married yet because a wise husband never says such quotations.

**Me:** Good night

---------------------
## When you finally meet your hero...

It's sad that we judge people that we hardly know, based on what others said.

It's also very interesting, how we admire some people knowing very little about them, consider them as our role models, 
take everything they say as a fact, worship them as our heroes.

**Talking about heroes, here comes my hero.** 

* Not the hero that throws buzzwords and gets away with it.
* Not the hero who insults his admirer for asking questions. 

But,

* The hero who enjoys solving the real hard problems.
* The hero who is matured enough to not care about what others think about him. 
* The hero who has a big heart to offer help even after knowing they don't have a good opinion on him.

**Ajay:** Hey Siva

*************************** THE END *******************************
