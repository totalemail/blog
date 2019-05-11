---
title: "Change Log"
date: 2019-05-10
description: "Here's a brief look at what we've accomplished at TotalEmail."
tags: ["Release Notes", "Progress"]
---

#### v0.3: Antlia

![This release is named "Antlia" after the constellation representing an air pump](/imgs/antlia-annotated.jpg)

- Consolidated email scoring
    - Each email uploaded to TotalEmail is run through a series of analysis engines which provide analysis and insights to help you determine whether or not the email is malicious. We have introduced a system which takes these scores and consolidates them into a single score for each email. You can read more about this system [here](/email-scoring-0/).
- Improved email redaction
    - To continue our commitment to user privacy, we have improved the redaction capabilities to be able to redact content from base64 encoded bodies and header fields.
- Improved GUI layout
    - We have improved the GUI; especially on the details page for an email (e.g. [https://totalemail.io/email/409e912be8f09795ebb8fe38aa0e71cb3b87fec2a3450a54fbdd6712be713099](https://totalemail.io/email/409e912be8f09795ebb8fe38aa0e71cb3b87fec2a3450a54fbdd6712be713099))

[Read more about v0.3](/antlia-0-3/) - [Read more about Antlia (the constellation)](https://en.wikipedia.org/wiki/Antlia)

<hr>

#### v0.2: Andromeda

![This release is named "Andromeda" after the constellation representing chained princess from Greek mythology](/imgs/andromeda_annotated.png)

- Robust header parsing
    - Email headers are more robustly parsed and stored in the database (a more technical blog on why/how we did this is coming out soon).
    - Unicode/UTF-8 encoded headers are handled more cleanly
- Improved search capability
    - We've added a number of custom search queries you can use to find specific data you are looking for (more documentation on these coming soon).
        - For example, you can:
            - Find emails with a certain domain in the header
            - Find emails with a certain domain in the body
            - Find emails with certain text in the body

[Read more about v0.2](/andromeda-0-2/) - [Read more about Andromeda (the constellation)](https://en.wikipedia.org/wiki/Andromeda_(constellation))

<hr>

#### v0.1: Pyxis

![This release is named "Pyxis" after the constellation representing a mariner's compass.](/imgs/Pyxis.jpg)

- Improved search capability
- Adding search prefixes
- Adding ability to upload multiple emails (max of 50)
- Adding email structure 'map' (you can see this [here](https://totalemail.io/email/2159d16de88b89a91418ea282c1e26404b625a225aece7921838ab428b74f5a2))

[Read more about v0.1](/pyxis-0-1/) - [Read more about Pyxis (the constellation)](https://en.wikipedia.org/wiki/Pyxis)
