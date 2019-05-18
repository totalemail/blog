---
title: "TotalEmail v0.4: Apus"
date: 2019-05-18
description: "Version 0.4 is released! Named 'Apus' after the constellation representing a bird of paradise, this release improves the layout of data in the GUI, improves redaction by redacting content matching certain patterns, and improves the email structure. In this blog post, we'll discuss a few of the new things we are most excited about!"
tags: ["Release Notes", "GUI", "Redaction", "Privacy", "Social Security Numbers", "Personally Identifiable Information", "Phone Numbers", "Regexes", "Email Structure", "Django"]
---

![This release is named "Apus" after the constellation representing a bird of paradise](/imgs/apus-annotated.jpg)

#### Why we did it: Our objectives for this release

TotalEmail exists to help you determine if an email is malicious. In this release, we wanted to improve the display of data on the details page for an email (e.g. [https://totalemail.io/email/409e912be8f09795ebb8fe38aa0e71cb3b87fec2a3450a54fbdd6712be713099](https://totalemail.io/email/409e912be8f09795ebb8fe38aa0e71cb3b87fec2a3450a54fbdd6712be713099)). Emails are complicated creatures and we were not displaying the content in a way that handled many of the possible edge-cases. Additionally, we were not displaying data in a way that was very helpful for the visitors. While the layout is still not perfect, we've made some major improvements to the way data is displayed that will help visitors get more meaningful information about an email (and do so more quickly).

Additionally, we want to prioritize your security and privacy when you upload an email. At TotalEmail, we commit to making a system that we ourselves would are comfortable using. To this end, we've added the ability to redact data in an email that looks like a Social Security or phone number. This means that you can be more comfortable importing emails knowing that any sensitive data will be redacted.

#### What we did: What we accomplished in this release

Some of the most exiting features of this release include:

- Simplified display of common domain names (e.g. `google.com` - see https://totalemail.io/email/562195df0efd46d9a644ca53ada6c0a4c17b69be2df3530964e8dcac6ead2397#networkData)
- Adding ability to redact sensitive information (like Social Security numbers and phone numbers) from an email
    - We are now providing an option on import to redact text in the email that even looks like a Social Security or phone number
- Adding ability to copy network data
- Improving display of network data
- Showing the body content type for each body
- Improving search GUI/UX
- Improving derivation and display of email structure

#### How we did it: Technical implementation details

From a technical, software architecture perspective, the major theme of this release has been moving functions to the right place. Writing code that is robust, maintainable, and clear is not just about writing the right code; it is also about putting the right code in the right place. At TotalEmail, we are using [Django](https://www.djangoproject.com/) as our web framework (and we love it!). When we talk about putting the right code in the right place in the context of Django, for us this means moving code from views (or other locations) into the models (see #2 [here](/on-rewriting-code/)). As such, we have been moving a number of functions into the `models.py` file so that the functionality is accessible via multiple other apps/interfaces (e.g. GUI, API, etc.).

![This release is named "Apus" after the constellation representing a bird of paradise](/imgs/apus.png)

We sincerely hope you enjoy the "[Apus](https://en.wikipedia.org/wiki/Apus)" release.

[Have fun](https://totalemail.io/email/562195df0efd46d9a644ca53ada6c0a4c17b69be2df3530964e8dcac6ead2397)!
