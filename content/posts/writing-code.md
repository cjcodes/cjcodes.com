---
title: "Writing Code"
date: 2021-12-29T10:33:32-08:00
draft: true
---

Every so often, I get feedback from my team that my ability to help them write code or do devops work can be helpful. But it's something that's generally frowned upon as you make your way up the management chain, because it's very easy to fall into the micromanagement trap. It's an area that I've continued to try to figure out how to refine my usage of. Personally, I don't think I can be an effective manager at a developer-focused company without maintaining my connection to code.

However, I do now consider myself allergic to writing and operating code in production, because I don't maintain the same context and state as the engineers on the team. Last time I went to deploy something using our internal tooling, the whole interface had changed and a teammate told me the change had happened months ago. So there's a concrete risk to pretending like I know what I'm doing.

The scenarios where I will step in generally fall into these categories:
1. No other engineers are available (for example, during a PTO spike around the holidays)
2. A problem has made the rounds with the team and needs a fresh perspective
3. A roll-forward solution is needed for high-severity incident remediation
4. Confirming implementation matches my understanding of how something works

All of these share a common outcome: time optimization. Time utilization is definitely a topic for a future blog post, <!-- TKTK --> but I generally think about time utilization on a spectrum of tradeoffs. As a general rule, when there is reduced time pressure, learning trumps efficiency based on the assumption that more learning will yield more long-term efficiency at the cost of the short-term efficiency. If that weren't true, I would run a team of exclusively senior engineers (who would still need to learn, anyway). And that is both selfish and doing the industry a disservice.

For some context, the leadership of an independent team at my company is made up of an Engineering Manager, a Technical Lead, a Product Manager, and usually a UX Designer. The roles are split up about as you'd expect given the titles: the manager manages the people and delivery, TL is accountable for the team's technical architecture, PM the product and backlog, and UX Designer the product design.

When the manager in this leadership group steps into a technical role, it muddies responsibility. What if I have a strong opinion about an architectural decision? Since the TL usually reports to the EM, there's a conflict of interest, and the nature of the power relationship will usually result in the manager's opinion trumping that of the TL because of a perception (whether real or not) that disagreement will result in retaliation.

Not to mention, it's also just awkward to give your manager feedback on a PR. As much as I enjoy a culture of spirited debate, having a spirited debate with your manager is perceived as risky and can amplify insecurities. Personally, I don't hold anyone accountable to debating with me as long as the

There [have been studies](https://hbr.org/2016/12/if-your-boss-could-do-your-job-youre-more-likely-to-be-happy-at-work) that show employees have a higher level of trust for managers that they know can do their job, because it gives them confidence in their empathy.

## Over Time
The challenge starts coming once you take a step up above a line manager. Would you expect a CEO of a ten-thousand employee company to be capable of both writing code and performing IT asset inventory? I know a few CEOs who would like to think they could, but those are not the kinds of CEOs that I would enjoy working with. At a smaller scale, would you expect a manager-of-managers to be able to do the work of the ICs under their directs?

A lot of folks reading this will likely come from a software engineer perspective, where your career growth and advancement is cumulative -- you learn new things, add them to your tool belt, and over time your tool belt becomes one of a seasoned professional (with the IC level to match). In other words, once you learn `git pull`, you're going to use `git pull` for the rest of your career. Maybe you sprinkle in some `--rebase` over time, but you're effectively building on knowledge that you've accumulated over time.

As a manager, there are parts of your skill set that you will intentionally choose to set behind you once you step beyond line manager. Presented in an overly-simplistic way, I think of it kinda like this:

<!-- tktk this looks ugly as sin -->
<svg width="500" height="210" style="stroke: #000;">
  <ellipse cx="105" cy="145" rx="100" ry="100" stroke-width="3" fill="none"></ellipse>
  <ellipse cx="245" cy="145" rx="100" ry="100" stroke-width="3" fill="none"></ellipse>
  <ellipse cx="325" cy="145" rx="100" ry="100" stroke-width="3" fill="none"></ellipse>
  <text x="95" y="20">IC</text>
  <text x="210" y="20">Manager</text>
  <text x="25" y="40">MoM</text>
</svg>

Realistically, there's more overlap between Manager of Managers and Manager skill sets, but

The challenge I'd put out to those stepping up above a line manager is to make sure you build channels of empathy down to the ICs. You are more empowered to make radical change on their behalf than the line managers are, so if you identify that tech debt is taking up too much of your org's time, figure out how to empower the teams to make a change.

<!-- tktk fix post date to be honest about the date I finally publish this -->
