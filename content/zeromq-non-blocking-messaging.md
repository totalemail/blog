---
title: "Non-Blocking Messaging Using ZeroMQ"
date: 2019-02-27
description: "How we are using ZeroMQ to improve speed and code maintainability."
tags: ["Developer Notes", "Flask", "ZeroMQ"]
---

Under the hood of TotalEmail, we have multiple systems which are communicating with one another. In early versions of theses systems, we used [Flask](http://flask.pocoo.org/), a Python microframework. This presented two difficulties:

1. It requires code to handle API routes, parse query parameters and request bodies, and return HTTP responses. This means there is more code and requires more maintenance than it is worth.
2. Using the HTTP request-response model means that the system making a request has to wait for a response. If System A makes a request to System B, System A waits for a response from System B before proceeding.

To make the code more simple and maintainable and to make each system work more quickly (by not requiring systems to wait for responses), we decided to use [ZeroMQ](http://zeromq.org/). ZeroMQ is a messaging queue (hence "MQ") that makes it very easy to connect systems in a variety of ways (you can read more about the details here: [http://zguide.zeromq.org/page:all](http://zguide.zeromq.org/page:all)). We are using a Push-Pull model like the one described here: [https://hightower.space/thoughts/zeromq-push-pull/](https://hightower.space/thoughts/zeromq-push-pull/). The advantage of the Push-Pull model is that the client which pushes does not wait for a response from the server (which pulls).

If you have never used ZeroMQ, we highly recommend you give it a try. It is a fantastic system which makes a complex task very easy. ZeroMQ has support for most, common programming languages and is well documented (as long as you are willing to do some reading).

Enjoy and [happy hunting](https://totalemail.io/email/2dc687010f612dc4d2393895f748acd8a523d69d65090c7c1345a1eafca22c81)!
