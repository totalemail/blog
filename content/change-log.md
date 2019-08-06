---
title: "Change Log"
date: 2019-05-10
description: "Here's a brief look at what we've accomplished at TotalEmail."
tags: ["Release Notes", "Progress"]
---

You can read more about our future plans [here](/road-map/).

<hr>

#### v0.6: Aquila (*August 3, 2019*)

- Added ability to parse network data from base64 encoded bodies
- Make a network data super-class to generalize the handling of the `modified` and `first_seen` dates
- Using python's [multiprocessing](https://docs.python.org/3/library/multiprocessing.html) module to speed up the email analysis engines
- Minor bug fixes
- Making the side-bar 'sticky' on an email's details page

![This release is named "Aquila" after the constellation representing an eagle](/imgs/aquila-art.png)

[Read more about v0.6](/aquila-0-6/) - [Read more about Aquila (the constellation)](https://en.wikipedia.org/wiki/Aquila_(constellation))

<hr>

#### v0.5: Aquarius (*June 20, 2019*)

- Fixed bugs related to email parsing, analysis, and display
- Adding eight, new email analysis engines
- Improving TotalEmail and analysis engine code
- Adding and improving tests
- Adding a voting feature (you can read more about this [here](https://blog.totalemail.io/email-voting-0/))
- Improved scoring system to go from 0 to 1 (you can find more details [here](https://blog.totalemail.io/email-scoring-0/))

![This release is named "Aquarius" after the constellation representing a water bearer](/imgs/aquarius-annotated.png)

[Read more about v0.5](/aquarius-0-5/) - [Read more about Aquarius (the constellation)](https://en.wikipedia.org/wiki/Aquarius_(constellation))

<hr>

#### v0.4: Apus (*May 18, 2019*)

- Simplified display of common domain names (e.g. `google.com` - see https://totalemail.io/email/562195df0efd46d9a644ca53ada6c0a4c17b69be2df3530964e8dcac6ead2397#networkData)
- Adding ability to redact sensitive information (like Social Security numbers and phone numbers) from an email
    - We are now providing an option on import to redact text in the email that even looks like a Social Security or phone number
- Adding ability to copy network data
- Improving display of network data
- Showing the body content type for each body
- Improving search GUI/UX

![This release is named "Apus" after the constellation representing a bird of paradise](/imgs/apus-annotated.jpg)

[Read more about v0.4](/apus-0-4/) - [Read more about Apus (the constellation)](https://en.wikipedia.org/wiki/Apus)

<hr>

#### v0.3: Antlia (*May 01, 2019*)

- Consolidated email scoring
    - Each email uploaded to TotalEmail is run through a series of analysis engines which provide analysis and insights to help you determine whether or not the email is malicious. We have introduced a system which takes these scores and consolidates them into a single score for each email. You can read more about this system [here](/email-scoring-0/).
- Improved email redaction
    - To continue our commitment to user privacy, we have improved the redaction capabilities to be able to redact content from base64 encoded bodies and header fields.
- Improved GUI layout
    - We have improved the GUI; especially on the details page for an email (e.g. [https://totalemail.io/email/409e912be8f09795ebb8fe38aa0e71cb3b87fec2a3450a54fbdd6712be713099](https://totalemail.io/email/409e912be8f09795ebb8fe38aa0e71cb3b87fec2a3450a54fbdd6712be713099))

![This release is named "Antlia" after the constellation representing an air pump](/imgs/antlia-annotated.jpg)

[Read more about v0.3](/antlia-0-3/) - [Read more about Antlia (the constellation)](https://en.wikipedia.org/wiki/Antlia)

<hr>

#### v0.2: Andromeda (*April 10, 2019*)

- Robust header parsing
    - Email headers are more robustly parsed and stored in the database (a more technical blog on why/how we did this is coming out soon).
    - Unicode/UTF-8 encoded headers are handled more cleanly
- Improved search capability
    - We've added a number of custom search queries you can use to find specific data you are looking for (more documentation on these coming soon).
        - For example, you can:
            - Find emails with a certain domain in the header
            - Find emails with a certain domain in the body
            - Find emails with certain text in the body

![This release is named "Andromeda" after the constellation representing chained princess from Greek mythology](/imgs/andromeda_annotated.png)

[Read more about v0.2](/andromeda-0-2/) - [Read more about Andromeda (the constellation)](https://en.wikipedia.org/wiki/Andromeda_(constellation))

<hr>

#### v0.1: Pyxis (*January 17, 2019*)

- Improved search capability
- Adding search functions
- Adding ability to upload multiple emails (max of 50)
- Adding email structure 'map' (you can see this [here](https://totalemail.io/email/2159d16de88b89a91418ea282c1e26404b625a225aece7921838ab428b74f5a2))

![This release is named "Pyxis" after the constellation representing a mariner's compass.](/imgs/Pyxis.jpg)

[Read more about v0.1](/pyxis-0-1/) - [Read more about Pyxis (the constellation)](https://en.wikipedia.org/wiki/Pyxis)
