---
title: "TotalEmail 0.1: Pyxis Nautica"
date: 2019-01-17
description: "Version 0.1 is released! Named 'Pyxis Nautica' after a constellation representing a mariner's compass, this release provides basic upload and search functionality that will guide future releases. In this blog post, we'll discuss a few of the new things we are most excited about."
tags: ["Release Notes", "Search", "Import", "Email Structure", "Django", "PostgreSQL", "Flask"]
---

#### Why we did it: Our objectives for this release

TotalEmail exists to help you determine whether or not an email is malicious, spam, or benign. This release provides the foundation on which we will build to accomplish our mission. The primary objective of this release is to get something released that we can iterate on and improve. You have to start somewhere!

#### What we did: What we accomplished in this release

Some of the most exiting features of this release include:

- Search capability
    - The search capability includes search prefixes which let you narrow down your searches <!-- TODO: it would be nice to have a link to the search prefixes documentation --> . For example, a search for [sub:spam](https://alpha.totalemail.io/search?q=sub%3Aspam) finds all emails with "spam" in the subject line while searching for [spam](https://alpha.totalemail.io/search?q=spam) finds all emails with the word "spam" in them (anywhere in the email).
    - Queries are preserved in the URL as [query strings](https://en.wikipedia.org/wiki/Query_string) so you can bookmark and share helpful search queries (e.g. If you want to see emails with the phrase "don't wait" in them, see: [https://alpha.totalemail.io/search?q=don%27t+wait](https://alpha.totalemail.io/search?q=don%27t+wait)).
- Multi-upload
    - We've added functionality which lets you upload multiple emails at once! We plan to expand this in the future to make it easier to find emails that you have uploaded.
- Email 'map'
    - When viewing the details page for an email, there is a 'map' of the email's structure on the right side of the page (here is an [example](https://alpha.totalemail.io/email/5a0ba393b6a917b9a381920a24dabccb5db449920a2cb773279a0ca52b12e4a2)). We're excited to expand and improve this feature to make it easy to view an email's structure and jump to the important places.

#### How we did it: Technical implementation details

We are primarily using [Django](https://www.djangoproject.com/) for this project. It has been our first experience working with Django and, so far, we have found it delightful. We are comfortable working in python and the documentation is first-rate. The underlying database is [PostgreSQL](https://www.postgresql.org/) which is powerful and integrates nicely with Django. We also have internal APIs and testing systems built using [Flask](http://flask.pocoo.org/) which is fantastic for rapid prototyping and testing.

We sincerely hope you enjoy the "Pyxis Nautica" release.

[Happy exploring](https://alpha.totalemail.io/email/5a0ba393b6a917b9a381920a24dabccb5db449920a2cb773279a0ca52b12e4a2)!

![This release is named "Pyxis" after the constellation representing a mariner's compass.](/imgs/pyxis.png)
