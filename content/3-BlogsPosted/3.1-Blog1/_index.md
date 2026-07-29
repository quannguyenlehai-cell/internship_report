---
title: "Blog 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

What I Learned After 2 Months of "Exploring" AWS
Lambda
As a student who's just started learning Cloud less than 2 months ago, honestly, I found AWS quite challenging at first. Hundreds of services with a lot of complex English terminology overwhelmed me. However, when I started doing exercises with AWS Lambda, everything gradually became much easier to understand.

Below are the most basic lessons I learned after a few weeks of self-study.

1. Serverless
Normally, when working on large projects, we often have to run a server on our local machine and leave it running continuously 24/7 waiting for applications to call it.

But with AWS Lambda, you just need to throw your code onto the cloud. AWS will take care of the underlying server. You don't need to install an operating system, you don't need to worry about system vaping or server overload.

2. Code only runs when an event occurs (Trigger)
Lambda functions don't run indefinitely. They only "wake up" when a specific event triggers them:
- Someone uploads a file to the system.

- Someone clicks a button on the web/app interface.

- Data is added to the database.
As soon as the event occurs, Lambda will run your code, return the result, and then automatically shut down.

3. Extremely budget-friendly for students
Because lambda only runs when an event occurs, you only pay for the exact number of milliseconds the code actually runs.
- If no one uses your app, the cost is 0.

- AWS also offers a free tier for free trials every month, so you can work on projects comfortably without worrying about unnecessary charges.
4. Personal Experience - Don't Write Too Much Code
When I first started learning, my mistake was cramming the entire backend into a single Lambda function, making the code slow and difficult to fix.
After two months, I realized I should break down the work:
- One function for account registration
- One function for data storage
- ...
In short...
If you're new to Cloud and only have a short time to prepare, AWS Lambda is well worth trying. You don't need to be an expert in network infrastructure or servers; just focus on writing the right code - with Lehaiquan Nguyen.

[Article Link](httpshttpswww.facebook.com/groups/awsstudygroupfcj/permalink/2225735151524778/?rdid=LGtwaQotLkeDI1a7#)