---
title: "Improving Network Data Parsing Using Grammars"
date: 2019-03-16
description: "This blog post describes how we are using grammars to find network data (like URLs, email addresses, ip addresses, etc)."
tags: ["Developer Notes", "Grammars", "Pyparsing", "Network Data", "Indicators of Compromise"]
---

When an email is uploaded to TotalEmail, we want to find all of the network data in the email (data points like URLs, IP addresses, email addresses, and domain names). This helps us identify malicious links, accurately predict whether or not the email is malicious, and help you make connections between emails with the same or similar content. The question is: How can we parse network data from an email (or any text blob for that matter)?

To parse network data from text, [Floyd Hightower](https://hightower.space/) (a member of the TotalEmail team) created the [ioc-finder](https://github.com/fhightower/ioc-finder) project. The package is specifically designed to parse what are known as "indicators of compromise"<sup><b>[1]</b></sup> (or "iocs" - hence the "ioc" in the name of the package) from text, but because data like URLs, IP addresses, email addresses, and domain names can be indicators of compromise, the ioc-finder package will work for TotalEmail's use-case as well.

What makes ioc-finder interesting is that it doesn't follow the normal approach to parsing network data from text. The normal approach involves using regexes (a.k.a [regular expressions](https://en.wikipedia.org/wiki/Regular_expression)), but ioc-finder uses [grammars](https://web.mit.edu/6.005/www/fa15/classes/17-regex-grammars/#grammars) (specifically it uses [pyparsing](http://infohost.nmt.edu/tcc/help/pubs/pyparsing/pyparsing.pdf)). There are a number of advantages to using grammars. They are:

- More readable (and therefore more maintainable)
- Easier to build on one another
- Easier to create because you don't have to worry as much about whitespace and word boundaries

<img src='https://drscdn.500px.org/photo/229249691/m%3D900/v2?user_id=23113227&webp=true&sig=7be84b0a19f25c7c8b86c210afad67da6ec70feaa3807a40dfd398bb3ad84b60' alt='What does the text say? by Floyd Hightower on 500px.com'>

*Photo by [Floyd Hightower](https://hightower.space/) on [500px](https://500px.com/photo/229249691/what-does-the-text-say-by-floyd-hightower)*

#### Improving IOC-Finder

When we started the TotalEmail project, ioc-finder was very young and was still having some problems parsing network data correctly. For example, given:

```html
<A hRef='https://bit.ly/123456'>
```

ioc-finder would parse `https://bit.ly/123456'` as a URL (note the trailing single quotation mark). Recently, however, ioc-finder has been updated and is working properly! We will be adding a feedback page soon, so if you notice anything strange with our network data parsing, feel free to contact us or [raise an issue](https://github.com/fhightower/ioc-finder/issues).

Enjoy and [happy hunting](https://totalemail.io/email/6a42a5371724605726b80bbce2fa3a09e0930624e04658bc24f6c1c62cb3817e)!

#### Notes

[1] - [https://en.wikipedia.org/wiki/Indicator_of_compromise](https://en.wikipedia.org/wiki/Indicator_of_compromise)
