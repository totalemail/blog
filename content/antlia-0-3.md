---
title: "TotalEmail v0.3: Antlia"
date: 2019-05-01
description: "Version 0.3 is released! Named 'Antlia' after the constellation representing an air pump, this release improves email redaction and introduces a score for every email. In this blog post, we'll discuss a few of the new things we are most excited about!"
tags: ["Release Notes", "GUI", "Base64", "Redaction", "Privacy", "Email Scoring", "Traffic Lights", "Django", "Heroku", "Whitenoise"]
---

![This release is named "Antlia" after the constellation representing an air pump](/imgs/antlia-annotated.jpg)

#### Why we did it: Our objectives for this release

TotalEmail exists to help you determine whether or not an email is malicious. This release is focused on creating a single representation (both visual and numeric) of the probability that an email is maliciousness.

#### What we did: What we accomplished in this release

Some of the most exiting features of this release include:

- Consolidated email scoring
    - Each email uploaded to TotalEmail is run through a series of analysis engines which provide analysis and insights to help you determine whether or not the email is malicious. We have introduced a system which takes these scores and consolidates them into a single score for each email. You can read more about this system [here](/email-scoring-0/).
- Improved email redaction
    - To continue our commitment to user privacy, we have improved the redaction capabilities to be able to redact content from base64 encoded bodies and header fields.

#### How we did it: Technical implementation details

For a long time, we have wanted to use a traffic light as a visual metaphor. The scoring system and traffic light metaphor is described in more detail [here](/email-scoring-0/). The most difficult, technical aspect of this release was figuring out how to get static images to display when running Django through Heroku. The blog post [here](https://medium.com/agatha-codes/9-straightforward-steps-for-deploying-your-django-app-with-heroku-82b952652fb4) was very helpful as is the [whitenoise](http://whitenoise.evans.io/en/stable/django.html) documentation.

The implementation of the base64 redaction system is also interesting as we have to find base64 bodies/header fields in the email, decode them, redact them, re-encode them in base64, and then replace the unredacted base64 with the redacted base64 in the original email.

![This release is named "Antlia" after the constellation representing an air pump](/imgs/antlia.png)

We sincerely hope you enjoy the "[Antlia](https://en.wikipedia.org/wiki/Antlia)" release.

[Happy exploring](https://totalemail.io/email/409e912be8f09795ebb8fe38aa0e71cb3b87fec2a3450a54fbdd6712be713099)!
