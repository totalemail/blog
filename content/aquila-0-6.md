---
title: "TotalEmail v0.6: Aquila"
date: 2019-08-03
description: "Version 0.6 is released! Named 'Aquila' after the constellation representing an eagle, this release improves network data parsing and handling, speeds up the time it takes to analyze an email, and provides some UI improvements. In this blog post, we'll discuss a few of the new things we are most excited about!"
tags: ["Release Notes", "UI", "Network Data", "Multiprocessing"]
---

![This release is named "Aquila" after the constellation representing an eagle](/imgs/aquila-art.png)

#### Why we did it: Our objectives for this release

In this release, we wanted to:

1. Speed up the [email analysis engines](https://blog.totalemail.io/email-analysis-engines-intro/)
2. Parse network data from base64 encoded bodies
3. Improve UI (User Interface) of an email's details page

#### What we did: What we accomplished in this release

Some of the most exiting features of this release include:

- Added ability to parse network data from base64 encoded bodies
- Make a network data super-class to generalize the handling of the `modified` and `first_seen` dates
- Using python's [multiprocessing](https://docs.python.org/3/library/multiprocessing.html) module to speed up the email analysis engines
- Minor bug fixes
- Making the side-bar 'sticky' on an email's details page

#### How we did it: Technical implementation details

As we mentioned earlier, we wanted to decrease the time it takes to analyze an email. To do this, we are using python's [multiprocessing](https://docs.python.org/3/library/multiprocessing.html) module to run multiple analysis engines at one time (and asynchronously). There is a very good introduction to concurrency in python [here](https://realpython.com/python-concurrency/) that describes different types of problems and their possible solutions. For an example using multiprocessing, check out this file from the [ioc-finder](https://github.com/fhightower/ioc-finder/) project: [ioc_finder.py#L388](https://github.com/fhightower/ioc-finder/blob/0c2783223ba1493285484cc78c770cc0f3a29c24/ioc_finder/ioc_finder.py#L388)

We also want to keep improving the UI. As part of this, we wanted to make the the side-bar (on the right side of an email's details page) 'sticky' - meaning it stays on the right side even when you scroll. We are using [Zurb Foundation](https://foundation.zurb.com/) as our front-end framework, so we are using Zurb Foundation's [Sticky](https://foundation.zurb.com/sites/docs/sticky.html) feature.

![This release is named "Aquila" after the constellation representing an eagle](/imgs/aquila.png)

We sincerely hope you enjoy the "[Aquila](https://en.wikipedia.org/wiki/Aquila_(constellation))" release.

[Have fun out there](https://totalemail.io/email/0289c4d13aa493f714bad7b95e3d0aa2c329990e31c42f3ace4ebf532b6f04ae)!
