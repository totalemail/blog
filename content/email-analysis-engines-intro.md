---
title: "Introduction to Email Analysis Engines"
date: 2019-07-12
description: "A brief introduction to what an email analysis engine is, how we use them within TotalEmail, and how you can get the most out of the results."
tags: ["Email Scoring", "Analysis Engines"]
---

#### What is an email analysis engine?

An email analysis engine is a system that takes an email as input and performs some analysis on the email to determine if the email is malicious, spam, contains malicious attachments, or a number of other suspicious characteristics.

#### How does TotalEmail use email analysis engines?

Within the context of TotalEmail, email analysis engines are used to influence an email's [score](https://blog.totalemail.io/email-scoring-0/). If an analysis engine diagnoses an email as malicious, that diagnosis will increase an email's score. You can learn more about how analysis engines fit into TotalEmail [here](https://blog.totalemail.io/what-happens-in-totalemail/).

#### What analysis engines is TotalEmail currently using?

TotalEmail uses a combination of custom and open-source (e.g. [spam assassin](https://spamassassin.apache.org/)) analysis engines. Some analysis engines use natural language processing techniques to predict if an email is malicious, others check to see if the email contains anything matching certain regexes, while still others look for specific headers and combinations of headers which may indicate an email is malicious. TotalEmail currently has 10+ analysis engines and we will keep adding new engines over time.

#### Why use multiple analysis engines? Isn't one enough?

There are at least two benefits of having multiple analysis engines which focus on different aspects of an email:

1. It allows you to compare analysis engines and techniques to determine which one(s) are most effective. Moving forward, we (the TotalEmail team) will be using machine learning algorithms to rate techniques over time and determine which analysis engines/techniques are most trust-worthy.
2. It makes it more likely that you will catch a malicious email because you are looking at the email from many, different perspectives. Emails can be complex and there are a lot of little details one could focus on. Using multiple analysis engines provides insight into many different details that a single analysis engine may not catch.

<img src='https://drscdn.500px.org/photo/245669323/m%3D900/v2?user_id=23113227&webp=true&sig=1fef9927003eac2de96dd241281d57885e5a33876c700707a7c6c5047ee6a938' alt='Tracks over Valley by Floyd Hightower on 500px.com'>

*Photo by [Floyd Hightower](https://hightower.space/) on [500px](https://500px.com/photo/245669323/tracks-over-valley-by-floyd-hightower)*

#### Have a good idea for an analysis engine?

If you have any suggestions for an email analysis engine that you would like us to use please <a href="mailto:info@totalemail.io">let us know</a>! Also, if you have an idea for a *new* email analysis engine you would like to create and test, we would be happy to help you do that too.

[Keep calm](https://totalemail.io/email/3680fcfb6544fe685d1a261cb95b9b9ef5435e74c47fcd32a6535134311f1647) and [check out our voting page](https://totalemail.io/vote/)!
