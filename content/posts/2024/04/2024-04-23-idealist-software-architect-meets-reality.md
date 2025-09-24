---
title: When Idealist Software Architect Meet Reality
author: Siva
images: ["/images/shocked-man.png"]
type: post
draft: false
date: 2024-04-23T04:59:17+05:30
url: /2024/04/idealist-software-architect-meets-reality/
categories: [IT, Career, Fun]
tags: [IT, Career, Fun]
---

My name is **Vishwas**. I am a software architect. I recently joined this new organization.
Actually, they hired me because they were impressed with my work in the tech community.

It seems they are going to get a big client project soon, and they want to make sure that the project is successful.
I am also excited to work on this project.

<!--more-->

I know there is another architect (**Syam**) in the team who is working there for the last five years. 
I don't know how much he will cooperate with me. But I am sure that I can handle it.
I suspect he is going to try hard to lead this project as an architect.

--------------------------------------------
Finally, the day has come. The client project has been awarded to us.
Our offshore delivery manager arranged a meeting with all the leads, architects and managers to discuss the project plan.
The manager announced that the project is going to be led by me, and everyone congratulated me.
Surprisingly, **Syam** was also looking very happy with this decision. 
He also came to me and congratulated me. I thought I wrongly judged him.

--------------------------------------------
The project kick-off meeting was scheduled and I prepared a detailed project plan.
I told the offshore delivery manager that I need a team of 12 people with at least 5 senior experienced developers
who have hands-on experience with Microservices, DDD, Spring Boot, JPA, Clean Architecture, etc.

He said, shall we hire [Vaughn Vernon](https://twitter.com/VaughnVernon) and [Oliver Drotbohm](https://twitter.com/odrotbohm) for this project?
They have excellent experience in DDD and Architecture Design.

I said, "Really??, that would be great".

He said, "Come on man. I am just kidding, we can't afford them. But we already kind of prepared a team for you. We brought some experienced developers from other projects."

I said, "Okay, let me see the team."

--------------------------------------------
The team was introduced to me. I was shocked to see the team.
The team consists of 8 people, but only 2 people have experience with Spring Boot and JPA.
The rest of the team members are freshers who just completed their training in Java.

One of the "experienced team members" recently written code as follows:

```java
@Component
@Controller
@Configuration
public class OrderController {
    @Autowired
    private OrderService orderService;
    
    public void setOrderService(OrderService orderService) {
        this.orderService = orderService;
    }

    @RequestMapping("/createOrder")
    public String createOrder(Order order) {
        ...
    }
}
```

After watching this code snippet, I took a break and went to the restroom to cry.

![Shocked](https://media1.tenor.com/m/ze0zHtVXPEIAAAAd/shocked-brahmi-gifs.gif "Shocked")

After crying for 15 minutes, I came back to my seat and started thinking about how to handle this situation.

I had a lot of ideas on how to design the system properly by strictly following **DDD**, **Clean Architecture**, etc.
I also thought about how to use **Immutable** objects, wherever possible, to avoid side effects.
I was thinking of having 100% code coverage with complete End-To-End automation.

But now I realized that I can't implement all these ideas with this team.
Forget about following my ideas, I have to teach them how to write a simple Spring Boot application.
On top of it, I have to deliver the project within the shot deadline.

Nevertheless, we started development. The team is doing the best they can.
But the code quality is worse than I ever imagined.

**Forget about Immutability, these people are adding random annotations 
until it works without knowing what they are doing also.**

![Irritation](https://media1.tenor.com/m/dASlzSl-YmoAAAAd/brahmi-king.gif "Irritation")

--------------------------------------------

After a few days, I met **Syam** at cafeteria.

**Syam**: How is the project going on?

**Vishwas**: It's moving slowly. But the team is not up to the mark. I have to teach them everything from scratch.

**Syam**: You had a lot of ideas on how to design the system perfectly when you join the project. Isn't it?

**Vishwas**: Yes, but I can't implement them with this team.

**Syam**: Can I tell you something if you don't mind?

**Vishwas**: Sure

**Syam**: You are an excellent architect. I have seen your articles, your conference talks, etc. 
You have a lot of ideas on how to design the system properly.

It looks like you have been working with bright minds throughout your career.
Also, you were in a position to take decisions on who should be in your team, 
what technology stack you should use, etc.

Is it correct?

**Vishwas**: Yes, you are right.

**Syam**: I thought so.

**You are one of those very few lucky champs to have such a great career. 
But you are also a victim of your own success.
Because you have been working with bright minds all the time and have the decision-making power,
you are ignorant of the challenges faced by normal people who had to get things done with an average skilled team.**

You think that everyone is passionate about following the best practices, design patterns, etc.
But in reality, many developers don't give a damn about these things. They only care about getting things done.
But you expect them to be as passionate as you are about software development.

Do you think you are the first one who has those bright ideas?

When I joined this company, I also had a lot of ideas on how to design the system properly.
But I am nowhere as skilled as you are though.

**Being idealist is not going to help you. You have to understand the reality.
You know, many so-called excellent consultants come to the company and give a lot of 
idealistic suggestions on how to perfectly design the system.
Then they take their fee and leave. If they have to implement those ideas with the given team, 
they will also face the same challenges you are facing now.
But they don't face those challenges because they are not going to implement those ideas.**

As you are facing the ground reality, you can understand what many team leads and architects go through.
But if I were to tell about these problems before you join here, you would have thought that I am making excuses for my incompetence.
You may also give suggestions on how to train the team effectively, how to improve the hiring process, etc.
But now that you are in this situation, you understand that there is no time to change our hiring process or train the team effectively.
We have to deliver the project within the given deadline with the given team.

Do you think the world is running based on the software developed by the idealist developers by strictly following DDD, Clean Architecture, Pure Functional Programming, Immutability, etc etc?
Go take a look at some of the biggest banks software systems. You will be shocked to see how they are working.

I am not saying that you should not follow the best practices. 
After all, if we are passionate about software development, that's where we try to draw our professional satisfaction, right.

I don't know how long you are going to stay in this company.
Everyone has a certain value system and no matter what, they can't go beyond that.
I can only imagine how hard it is for you to let this project go as it is.

**But I guess, now you know being idealistic when you have decision-making power is different from dealing with reality when you don't have decision-making power.**

**Vishwas**: Thank you for sharing your thoughts. Yes, I have been a consultant for a long time,  
and I deliver training on DDD, Clean Architecture, etc. I have been blind to the reality.
Every time a client comes with a technical problem, we give technical solutions. 
Never thought about those problems may not be technical at all. 
Sometimes they are cultural problems, sometimes they are political problems, etc.
But I never take those things into account when I give suggestions.

I always thought if we follow those architectural styles, best practices, etc rigorously, then we can solve any problem.
But now I realize that it's not the case.

**Syam**: Well, you are a smart guy. You will figure it out. All the best.

**Vishwas**: Thank you.

