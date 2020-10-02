---
title: 2020-09-29-inception
date: 2020-09-29 16:21:15
tags:
---

So how do different roles contribute?
Eugene and TC have shared lots of great things about inception. I feel I have learnt new things too. So, I’d like to summarize my learning and give a brief summary of the whole inception journey. So that we can link up what we have learnt. Also I think it will be interesting to share some first hand experience from a developer perspective. 

To prepare for this session, I’ve interviewed some people from different roles to ask about their experience and opinions.

Inception can be in different formats or different flavors. It doesn't have to be exactly the same. But the process is very similar.

Ideal Products
To start with the inception, we ask questions. When we talk with clients or product owners, there are usually two possible situations. One is that they don't know what exactly they want, while the other is that they know what they want but they don’t know how large the project would be, or how long it might take.

If they don’t know what exactly they want, we will ask questions about their pain points. So that we can put up what they want. When the product owners know what they want, but don’t know how long it will take. We will ask questions about risks, dependencies. Like what service is ready, which is not ready. What are we depending on? What can be a trade-off? Time, cost, scope, user experience. Like Eugege & TC mentioned previously.

Also, we can ask what their ideal product is. This can help us clarify the direction.

Product Roadmap
When building the product roadmap mentioned previously, everyone can help with the process, including developers, QAs, designers, and BAs.

This process could help us find out some really good features. These awesome ideas will be noted down. And after recording those brilliant ideas, people will vote for the features. Usually all the teammates, like UI/UX designers, BAs, product owners, devs and QAs can vote. And usually the business and product people should take a larger percentage for the vote. 

Features
Then these features will be clustered into “Must have”, “Should have” , “Could have”, and “wouldn't have”. For example here is a feature to consider, our level up cafe app could email customers on what they’ve ordered and what time it will be delivered. It’s nice to have this feature, but customers can still order without this feature. So this feature will be a “could have” feature. (ask people)

Understand the tech environment
Tech people at this time will also ask questions like 
What’s the current tech stack? This will impact the technology selection.
What’s the system integration points in the existing system? How many users are we going to support? Is this feature something other departments of our company already built, or some 3rd party service we should purchase? Any dependencies, and tech challenges?
Any risks to delivery of the project? 

Then we will forecast the technical architecture to achieve technical goals.

During this process, we will have facilitators to write down the key questions and answers. Anyone can be the facilitator. One tip here is that, if you are a facilitator, make sure everyone is sticking to the topic. Do bring people back when the discussion is out of topic for quite some time. 

Breaking into stories & Estimation
The important features will be breaking down into small stories. And developers and QAs will think about the implementation details at a high level. And estimate the stories. Give each story a rough point. What we did previously in real cases: We will have many physical cards. We will write the brief story description on the card, and write the estimated story points at the back of the card.

Usually we will take 3 iterations as an example. Usually one iteration is two week. The team, especially developers and QAs will pick the stories to fill in each iteration without looking at the point on the stories. Just by thinking how many cards can be finished within one iteration, given e.g. we have 4 developers and 1 QA in the team. After doing this, we will flip over the cards, to add up together the stories points of each iteration. We will do this 3 times for 3 iterations. Then we make an average. Then we will know how many points can be finished by each dev pair. 

Then with how many people we have, we can calculate an estimated timeline.

Also, we will add an overall buffer to the estimated timeline, in case anything unexpected or missed.

Then a delivery plan will be there. Just keep in mind that story points usually represent the complexity of a task not how many days. As we are applying an agile process, the delivery plan is flexible too when the market changes. Story point is just one of the tools that helps predict team velocity. We learn and adjust the plan reactively as the project goes. If you want to know more details about breaking into user stories, our next episode will cover more details on it. Welcome to join if you think that’s interesting.

MVP
The timeline for a full feature product can be very long. Very often, Product owners would prefer to build the MVP(minimum viable product) to prove their concept, test the market, or have a quicker feedback cycle. Take our level up cafe app as an example: selecting delivery time could be a nice feature, but in MVP, we can default that the food will be delivered once it is ordered. And in future releases, this feature could be included then. By doing these cut offs ,we can have our MVP. And we will estimate a date for finishing the MVP. Then for all the stories together, we’ll estimate another time for full release.

Till now, we will have a plan. We will showcase to the related people and departments and get some more feedback. 

Summary
By working collaboratively between different roles, we will achieve a very good plan and accomplish a successful inception.

Q&A
So this will be our main content today. We are very happy to answer questions in the Q&A column

					





















MC
Start
Hello, everyone! Welcome to level up, Episode 2. First of all, thank you for taking the time to join the event. I believe we’re gonna have a fun evening full of knowledge and inspiration. I’m Alice. Tonight I’ll be your MC. I’m a software developer, a consultant from ThoughtWorks in Melbourne. 

Housekeeping
To start with, let’s share some housekeeping stuff. Questions for presenters. Feel free to put them in the Q&A column down there. You can see them. And you can vote for them. Don’t worry. There are no stupic questions. But if you feel like you don't want to be known who’s asking, you can ask them anonymously. 

You can also see on the bottom, there is a button called chat. In there, the presenters may ask questions that you can interact with. You can put your answers in the chat. You are also welcome to turn it in to all panelists and attendees. So that everyone else can see the answers there. Have a chat or have a discussion there if you like. We cannot hear or see you. So the chat is a good way to get some interaction with us. 

Towards the end of the session, we're gonna send a link to the feedback form. There will be an email coming out a little bit afterwards to collect feedback too. We really love your feedback. About this session, about the content, about the presentation. Your feedback means a lot to us. It can help us to improve and make our next session and season even better.

Launch the poll
I’ll also quickly launch a poll right now. Just one question poll, for getting a little bit feel on who’s here. What is your level of experience now? Just take a few seconds to answer it now. Don’t worry. It’s anonymous. Hopefully this gonna give us to understand what sort of experience level you have, so that we can tailor our examples and explanations on that.

(I’m gonna end the poll in 5 seconds.)

About LevelUp
Also, just wanna give a brief introduction to level up. It’s a program that has been running since 2013. Designed to help people to get a better start in IT career. We noticed there is a gap between what traditional education like bootchamps, and university courses, and the skills you are gonna need when you get your first job. So level up is a program designed to address that gap. 

Why LevelUp now?
Earlier this year, we had to cancel our planned in-personal events in Melbourne and Sydney. However,  by responding to change, applying agile thinking, we are able to bring you this new format of the level up. We had our first season earlier this year. And this is season 2. 

For this season, we have 6 episodes. The first episode was accomplished with great success last Tuesday. And today is Episode 2. Today we are going to hear great people from ThoughtWorks sharing their experience about one of the most important parts of the agile development process, which is Inception! 

During this season, we’re gonna follow a sort of agile development process and cover topics from Discovery to Delivery. It’s okay if you missed the first episode. I believe you will learn a lot from each episode. You can find the links for all these events on our website. Levelup.thoughtworks.com

And similar with this one, you can just simply click to register. (7min 35s)

Introduce presenters
Today we’ve also invited Eugege and TC as our presenters.

Eugene
It’s my pleasure to introduce Eugene. Eugene is our senior business analyst from ThoughtWorks. Eugene is good at helping teams realise their full potential and deliver great results. He is a pragmatic leader who can sharpen a team's focus, bring disciplined approach to software development. He has years of delivery experience in different roles (Presales, IM, PO, Solution Architect). During his career,  Eugene has worked in telecom, fintech, entertainment, real estate industries. And he has delivered complex solutions across the globe.

TC
We also have our lovely TC. TC is our lead experience designer. She has been designing usable, useful and engaging interfaces for a variety of clients in Australia and around the world since 1994. She has a passion for good design and seeks to understand human behaviour and how to support it through technology. She creates innovative and effective solutions. She has deep analytical and design skills. She has powerful communication techniques and the ability to share. She has also been mentoring a number of juniors within ThoughtWorks.

Let’s get started
So without further ado, let’s get started. I’ll hand it over to Eugene.
Eugene, can you please share with us what’s the focus of today.

Questions for Eugene
Can anything go wrong? And how to mitigate proactively?
How would we know if it’s successful?
what do you struggle with? What you miss?

Questions for TC
Can you please show us how to plan out inceptions briefly?
Can you please give us some examples of building roadmaps?

Ending
Thank you for spending this wonderful evening together with us! Our next episode is about iterating and user stories. We'll be discussing how to manage requirements in agile projects and why high performing teams involve quality analysts early in the process, often before any code has been written.It will be very interesting too. 

Also, thanks to the awesome people that put huge effort on preparing the events. Most importantly, thank you for attending the event today. We love to hear some feedback from you. Also, hope everyone got inspired! And, see you next time!
