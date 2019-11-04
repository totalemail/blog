---
title: "TotalEmail v0.2: Andromeda"
date: 2019-04-10
description: "Version 0.2 is released! Named 'Andromeda' after the constellation representing a princess from Greek mythology, this release greatly simplifies and improves email parsing. In this blog post, we'll discuss a few of the new things we are most excited about."
tags: ["Release Notes", "Import", "Database", "Email Structure", "Network Data"]
---

![This release is named "Andromeda" after the constellation representing chained princess from Greek mythology](/imgs/andromeda-art.png)

#### Why we did it: Our objectives for this release

TotalEmail exists to help you determine whether or not an email is malicious. This release is focused on simplifying *and* improving the way emails are processed and stored in TotalEmail.

#### What we did: What we accomplished in this release

Some of the most exiting features of this release include:

- Robust header parsing
    - Email headers are more robustly parsed and stored in the database (a more technical blog on why/how we did this is coming out soon).
    - Unicode/UTF-8 encoded headers are handled more cleanly
- Improved search capability
    - We've added a number of custom search queries you can use to find specific data you are looking for (more documentation on these coming soon).
        - For example, you can:
            - Find emails with a certain domain in the header
            - Find emails with a certain domain in the body
            - Find emails with certain text in the body

#### How we did it: Technical implementation details

To achieve this, we are relying on python's [native email parsing capabilities](https://docs.python.org/3/library/email.html) more than we have in the past. The benefits of this will be discussed in a retrospective blog coming out soon, but the short version is that this lets us rely on an existing and robust solution rather than having to create our own. We are also relying on some functions from the democritus project (more details on this project will probably be released in the second half of 2019).

We sincerely hope you enjoy the "[Andromeda](https://en.wikipedia.org/wiki/Andromeda_(constellation))" release.

[Happy exploring](https://totalemail.io/email/618e6c8fe710ef1fa54f55880ecbe969c3edea969704f62793d96eea3dbae6f5)!

![This release is named "Andromeda" after the constellation representing chained princess from Greek mythology](/imgs/andromeda.png)
