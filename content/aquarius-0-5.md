---
title: "TotalEmail v0.5: Aquarius"
date: 2019-06-20
description: "Version 0.5 is released! Named 'Aquarius' after the constellation representing a water bearer, this release improves the robustness and maintainability of the code under the hood of TotalEmail. In this blog post, we'll discuss a few of the new things we are most excited about!"
tags: ["Release Notes", "Voting", "Pytest", "Testing", "Django"]
---

![This release is named "Aquarius" after the constellation representing a water bearer](/imgs/aquarius-annotated.png)

#### Why we did it: Our objectives for this release

TotalEmail exists to help you determine if an email is malicious. In this release, we wanted to spend some time cleaning up the code and tests under the hood of TotalEmail to make the system more robust and maintainable.

#### What we did: What we accomplished in this release

Some of the most exiting features of this release include:

- Fixed bugs related to email parsing, analysis, and display
- Adding eight, new email analysis engines
- Improving TotalEmail and analysis engine code
- Adding and improving tests
- Adding a voting feature (you can read more about this [here](https://blog.totalemail.io/email-voting-0/))
- Improved scoring system to go from 0 to 1 (you can find more details [here](https://blog.totalemail.io/email-scoring-0/))

#### How we did it: Technical implementation details

As we've spent some time writing and improving tests for this release, it is only fitting that we draw your attention to [pytest](https://docs.pytest.org/en/latest/). Pytest is a *fantastic* testing framework for python. It is easy to write tests for pytest and it has powerful, advanced features if you want to do something out of the ordinary. If you have not used pytest, we highly recommend it! If you are using django, you can use [pytest-django
](https://pytest-django.readthedocs.io/en/latest/) to test django views and apps. Test away!

![This release is named "Aquarius" after the constellation representing a water pitcher](/imgs/aquarius.svg.png)

We sincerely hope you enjoy the "[Aquarius](https://en.wikipedia.org/wiki/Aquarius_(constellation))" release.

[Have fun out there](https://totalemail.io/email/5c38b3d55ca07cf7b4363ae666f7ed2b9a469a727d4f877dc286f420b42137fd)!
