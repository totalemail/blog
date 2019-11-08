---
title: "TotalEmail v0.7: Ara"
date: 2019-11-08
description: "Version 0.7 is released! Named 'Ara' after the constellation representing an altar, this release improves the code-base, specifically the code-base of the analysis engine. In this blog post, we'll discuss a few of the new things we are most excited about!"
tags: ["Release Notes", "Analysis Engines", "Scrapy", "Software Design"]
---

![This release is named "Ara" after the constellation representing an altar](/imgs/ara-art.png)

#### Why we did it: Our objectives for this release

In this release, we wanted to:

1. Clean the code in the [email analysis engines](https://blog.totalemail.io/email-analysis-engines-intro/)
2. Improve UI (User Interface) in minor ways
3. Prepare for public release and usage of the Python SDK
4. Prepare collection systems to collect emails from various locations on the internet so that we can better train and identify suspicious and malicious emails

#### What we did: What we accomplished in this release

Some of the most exiting features of this release include:

- Cleaned the code-base on the analysis engines to make it easier to add more engines moving forward
- Added a [search function](https://blog.totalemail.io/search-functions-0/) to view emails with attachments
- Showed the hash for attachments
- Set up an automated collection system to collect malicious and suspicious emails from various locations on the internet
- Ran load on our API
- Updated our [Python SDK](https://gitlab.com/totalemail/te-python) to be more user-friendly and intuitive

#### How we did it: Technical implementation details

As we are setting up a system to collect emails from various locations on the internet, we have been looking for a good system to help us collect this content. We have been using and have been very happy with [Scrapy](https://scrapy.org/). Scrapy makes it easy to write what they call a 'spider' which is used to collect data from a website (there is an introduction to Scrapy [here](https://docs.scrapy.org/en/latest/intro/overview.html)). It makes the process of data collection much easier by abstracting some complexities and generalizing common use-cases. If you have not used scrapy before, we highly recommend giving it a try!

![This release is named "Ara" after the constellation representing an altar](/imgs/ara.png)

We sincerely hope you enjoy the "[Ara](https://en.wikipedia.org/wiki/Ara_(constellation))" release.

[Happy hunting](https://totalemail.io/email/afc39f139241d28ab6e3ef3ce78aa9b4185fbdb5e7013b01900e01fa8c59e0f8)!
