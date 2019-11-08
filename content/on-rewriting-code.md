---
title: "Three Things We Observed When Rewriting our Code-Base"
date: 2019-04-16
description: "We recently rewrote our code-base and we'd like to share three observations from the process."
tags: ["Developer Notes", "Lessons Learned", "Software Architecture", "Django", "Complexity"]
---

We've recently rewritten much of our code-base (for various reasons I won't go into here). It was frustrating to have to do this at first, but looking back, it was an insightful and profitable experience! In this post, I'm going to highlight a few of lessons that stood out to us as we rewrote/restructured our code-base.

#### #1: Use Standard Libraries As Much As Possible (or: Don't Reinvent the Wheel)

I'm embarrassed to even mention this principle as it is so obvious, but I have to admit that we strayed away from this principle as this project progressed. Python has an [email](https://docs.python.org/3/library/email.html) library and we should have been relying on this library much more than we originally were. We've moved over to use the standard library as much as possible and it has produced a system that is more accurate, more robust, and more simple than the previous versions. Lesson learned:  Don't reinvent the wheel.

It's not as though we didn't already know that, but now we have *experienced* it. It was amazing how just using the standard library simplified so many other systems and fixed many other problems... which brings me to my next point: **Complexity Compounds**.

![When possible, don't reinvent the wheel](/imgs/reinvent-wheel.jpg)

*Photo by [Jon Cartagena](https://unsplash.com/photos/mmf7olkmhfw?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on Unsplash*

#### #2: Complexity Compounds (or: Ask "Why?")

Unnecessary complexity in a system is a problem for at least two reasons:

1. Unnecessary complexity is unnecessary - make it simple!
2. Complexity in one part of a system often spills over into other parts of a system

The first reason is pretty obvious to us, but the second reason is often ignored. Complexity compounds! If I am designing a cookie making process and the recipe is unnecessarily complex, the mixing step will be overly complex as well; it has complexity forced upon it by another part of the system. One might say:

```
Some [systems] are born complex, some achieve complexity, and some have complexity thrust upon them.
```

Some systems are inherently (read ontologically) complex, some systems are made complex unnecessarily, and some systems appear to be inherently complex only because the constraints and context of the surrounding system.

If we are trying to avoid unnecessary complexity, the challenge is to determine whether a system is necessarily complex or if it has complexity "thrust upon it" by the surrounding system. A helpful tool to think through this line of questions is the [5 "Whys"](https://en.wikipedia.org/wiki/5_Whys) system. You can read more about it on your own, but the basic goal is to determine the root cause of a problem by repeatedly asking the question "Why?".

When we started asking "Why?" as we were going through out code base, we were able to identify multiple areas where our code had complexity thrust upon it (and we were able to restructure the entire system to alleviate the complexity). For example, using the standard email library more produced a number of unexpected simplifications throughout the code-base. Also, we noticed that we had a lot of complex code in the [Django views](https://docs.djangoproject.com/en/2.2/topics/http/views/). As we started to ask "Why?", we found that it made a lot more sense to move things to the [Django models](https://docs.djangoproject.com/en/2.2/topics/db/models/). I'm open to correction on this as I'm still learning Django best practices, but for now, I think this is a helpful, general principle for Django:

```
Do not put in a view what makes more sense in a model.
```

Additionally, we starting storing email headers in the database as [json fields](https://docs.djangoproject.com/en/2.1/ref/contrib/postgres/fields/#jsonfield) rather parsing individual headers out and storing those.

Long story short:

```
Before trying to solve a problem or untangle a bundle of complexity, it is important to ask "Why does the complexity exist in the first place?"
```

#### #3: Cultivate Clarity

One of the principles that I rarely hear mentioned when talking about software architecture and design is clarity. Systems should be designed and executed with clarity in mind. When I say clarity, I mean the ability to know what is going on in a system (rather than clarity, I could have said perspicuity, comprehensibility, or debugability (which is a word I just made up)). When I design a system, I want to be able to easy understand what is going on in the system. I would rather adopt a faulty system with a lot of problems that is clear than a system that generally works pretty well but whose inner workings are unclear or inaccessible.

When it comes to designing and writing software, the obvious way to improve clarity is by writing clean code (and, perhaps, adding comments). This is true, but there is a lot more to clarity than just clean code. Strategically planning the names, layouts, and interfaces between systems improves clarity. Writing tests greatly improves clarity (and debugability). The general principle I am learning is:

```
Given two options, choose the one that is the most clear (and which promotes the most clarity in related systems).
```

![Create systems with clarity in mind](/imgs/clarity.jpg)


*Photo by [Anika Huizinga](https://unsplash.com/photos/RmzR87vTiYw?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on Unsplash*


Thanks for reading and [happy hunting](https://totalemail.io/email/e7e16789f3d5cc59a72a23a084edf656e2ccca4dff321c6c126fe694355eb857)!
