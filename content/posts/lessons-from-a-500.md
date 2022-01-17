---
title: "Lessons from a 500"
date: 2022-01-16T05:19:52-08:00
draft: false
---

The other day I got an email from Google welcoming me to using Google on my Windows computer after I logged in from within a Firefox window.

![Bad string replacements](/static/posts/bad-string-replace.png)

Huh? First, an unrelated note to software developers: when you do a ``t(`Welcome to {{company.name}} on your new {{device.type}}`)`` be sure to really think about what types of things are going to end up in `device`. In this case, my device "type" is Windows, which makes the sentence in the picture gramatically...strange.

Okay, grammatical rant aside, this email was pretty useless. And I'm an obsessive unsubscriber, so I smashed that Unsubscribe button. And to my surprise, I was presented with a 500 error! But not just any 500 error...

{{< tweet user="cjcodes" id="1480812042571243520" >}}

A full stack trace!

For whatever it's worth, the domain that threw the 500s, notifications.google.com, appears to be abandonware, likely the victim of a poorly run program within Google. There are only two options available behind the "Unsubscribe from All."

![A tiny product at Google](/static/posts/notifications.google.com.png)

## Servers are not your Edge
Okay. So to start, with some learnings from this. don't assume that if you can run code on the web you're good at 
There's so much going on here. First, and probably most intriguing, is that Google doesn't seem to have their standard exception interception at the 

## Getting support from a company that doesn't do B2C support
So here's the fun part of this post. Google [literally wrote the book on site reliability engineering](https://sre.google/sre-book/table-of-contents/). The trouble with sites like notifications.google.com that get low amounts of traffic compared to the rest of the company is that 

So to the engineer that got paged for this issue, I'm genuinely sorry not sorry.

## Now what?
What would I do in this situation? I'd kill the product. Here's a few data points that go into this:

1. Even from the outside, I can tell that it was not built with the same intention and investment as a full Google product. Viewing the source code of the app, it's a 
1. The server is by far the slowest consumer-facing Google server I've interacted with. Loading the page takes at least 1.5 secondes every pageview.