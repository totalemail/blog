---
title: "Introduction to Email Scoring"
date: 2019-05-02
description: "A brief introduction to our email scoring system."
tags: ["Email Scoring", "Traffic Lights"]
---

#### What is email scoring?

Every email that comes into TotalEmail is run through a series of analysis engines which consider different aspects of the email. We consolidate the results from all of these analysis engines into a single score for each email which captures the likelihood that the email is malicious.

An email's score can range from 0 to 1 (inclusive). Lower scores mean an email is less likely to be malicious and higher scores indicate that an email is more likely to be malicious. We also break up the scores into three, qualitative categories:

- "Likely Benign" (scores between 0 and 0.333)
- "Likely Suspicious" (scores between 0.334 and 0.666)
- "Likely Malicious" (scores between 0.667 and 1)

![Our email scoring system seeks to classify emails into one of three categories: "Likely benign", "Likely suspicious", "Likely malicious"](/imgs/scoring_annotated.png)

To communicate an email's score, we are using a [traffic light](https://en.wikipedia.org/wiki/Traffic_light) as a visual metaphor to communicate the score.

A <span style="background-color: #6FEF87;">green</span> traffic light means the email is <span style="background-color: #6FEF87;">likely benign</span>.

A <span style="background-color: #F1D86C;">yellow</span> light means the email is <span style="background-color: #F1D86C;">likely suspicious</span>.

A <span style="background-color: #E64A48;">red</span> traffic light means the email is <span style="background-color: #E64A48;">likely malicious</span>.

#### Why is email scoring helpful?

TotalEmail exists to help you determine whether or not an email is malicious. Our email scoring system does this by providing a single value for you (or an automated program) to consider when making this decision. As we expand the number of analysis engines and methodologies, it will be increasingly valuable to have a single value representing all of these inputs and this is the purpose of the email scoring system.

#### How do we calculate an email's score?

As mentioned, we have a number of analysis engines which are producing results and scores for each email. To calculate an email's score, we follow this algorithm:

- For each score: run the score through a function that converts the score to our 0 to 1 scale. This means that each analysis engine has its own function. For example, if an analysis engine returns a score between 50 and 100 for a malicious email, this score would be converted to fit between 0.667 and 1 (which is our range for en email that is likely malicious).
- Once all of the scores are converted, find the average of the scores and this is the email's score.

From a software design perspective, we have chosen to abstract the score calculation so that we calculate the score for an email every time that email is viewed rather than calculating the score once and storing it in the database. While this requires more processing power, it also allows us to update and fine-tune the email scoring functions and algorithm without having to change anything in the database.

![We use a traffic light to communicate the score of an email](/imgs/traffic-light.png)

#### Updates

- On May 24, we updated the scoring system to go from 0 to 1 instead of -1 to 1. We did this to more intuitively communicate the email's score. In the previous version (the one that used the -1 to 1 scale), zero was used as a neutral or unknown score. We think it is more intuitive to use zero to represent nothingness - namely an almost nonexistent probability that something is malicious.

[Stay safe out there](https://totalemail.io/email/76371e5e493103e4bf2e16d5326316ebf9d846c2b5f0ed0a37f9f37bb3614006)!
