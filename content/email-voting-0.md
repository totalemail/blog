---
title: "Introduction to Email Voting"
date: 2019-06-01
description: "A brief introduction to our email voting system."
tags: ["Email Scoring", "Voting", "Vue.js", "Django", "Django Rest Framework", "Javascript"]
---

If you are the adventurous type, you can skip the prose and explore our voting system [here](https://totalemail.io/vote/).

#### Why did we create the email voting feature?

Let's face it: in life, it seems all the valuable actions are hard to do while all the worthless actions are easy to do. And the internet only exacerbates the problem. As part of TotalEmail's mission to help you determine if an email is malicious, we wanted to address this problem; namely, **we wanted to create a system which allows visitors to do meaningful actions quickly and easily**. To this end, we've created a system that makes it easy for you to tell the TotalEmail community whether you think an email is malicious based on certain characteristics.

#### What is email voting?

Email voting is a system for telling the TotalEmail community whether you think an email is malicious. The idea is that we list a data point from some emails (for example, the subject line or a domain name) and let you classify the data point as likely good or likely bad. For example, if you go to the [voting page](https://totalemail.io/vote/) you will see a list of subject lines. You can vote on whether a given subject line looks bad or not - which we then take into account in the [email scoring system](https://blog.totalemail.io/email-scoring-0/). If the subject line of an email is voted malicious a number of times, we increase the email's score (email scores are described in depth [here](https://blog.totalemail.io/email-scoring-0/)).

<img src='https://drscdn.500px.org/photo/240748705/m%3D900/v2?user_id=23113227&webp=true&sig=7c8f1b3131be83839bfcc83dc6efc116dd0c76ef04a5279496cb4e38a7deee54' alt='Just a Number? by Floyd Hightower on 500px.com'>

*Photo by [Floyd Hightower](https://hightower.space/) on [500px](https://500px.com/photo/240748705/just-a-number-by-floyd-hightower)*

#### How did we create the email voting feature?

As with most of TotalEmail, we are using [Django](https://www.djangoproject.com/) and the [Django Rest Framework](https://www.django-rest-framework.org/) to manage the database, logic, and display of content for the email voting feature. We are using [Vue.js](https://vuejs.org/), a javascript framework, to make the interaction more dynamic and with a better user-experience (e.g. when a visitor classifies a subject line, that subject line gets removed from the screen). This is our first time introducing a javascript framework to TotalEmail. We chose Vue.js because it does everything we need and is easy to learn (if you know javascript, it shouldn't take you more than 20 minutes to get a basic understanding of Vue.js from the [guide](https://vuejs.org/v2/guide/)).

[Happy exploring](https://totalemail.io/email/b6f821a724719e09d168a683f99b2c8b9ff35a3aef1651a0af6af69c6a82fb41)!
