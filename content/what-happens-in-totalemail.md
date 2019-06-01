---
title: "What Happens When an Email is Analyzed by TotalEmail?"
date: 2019-06-07
description: "A peek behind-the-scenes of TotalEmail."
tags: ["Email Scoring", "Analysis Engines", "Email Scoring"]
---

#### What happens when you upload an email to TotalEmail?

When you upload an email in [TotalEmail](https://totalemail.io/)...

1. The email is parsed (using python's [standard, email library](https://docs.python.org/3/library/email.html#module-email))
2. The email and some of its component parts (e.g. header, bodies, attachments) are saved in TotalEmail's database 
3. The email is submitted to a series of analysis engines (including various regex and pattern matching, spam detection, and natural language processing systems) and the results from these analysis engines are stored in the database
4. When you view the details page for an email (you can find an example <a href="https://totalemail.io/email/6aba7f776ceb852fd0c7d58cc7b75edeaba0a95c5fd6d41dfe42e3e266532736" target="_blank">here</a>), TotalEmail takes all of the data from the most recent analysis engine results, boils this into a single score for that email, and presents it in the GUI (you can read more about how the score is calculated [here](https://blog.totalemail.io/email-scoring-0/))

![Emails uploaded to TotalEmail are stored in the database and submitted to multiple analysis engines](/imgs/te-import-flow-with-gui.png)

[When it rains, it pours... don't forget an umbrella](https://totalemail.io/email/0cdc6e339008c06b19eeab7437218ede327df3be54f2e0ae8c5d4a4c7188fd8b)!
