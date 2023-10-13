---
title: Write Less, Do More
layout: post
permalink: /write-less-do-more
body: |
  As a developer, I often find myself deleting code.

  But isn't that code what the company has spent money hiring people to write, you wonder? Wouldn't it be a crime to destroy that company-owned asset?

  It totally would be unless we can achieve the same thing after code deletion. That is, as jQuery's slogan says: "write less, do more". Given the same code quality, style, cognitive complexity, etc., less code makes better maintainability. Therefore, a net deletion of code without impacting logic would make developers' life much easier down the road. And needless to say better dev experience means more predictable delivery schedules, more efficient development process, and less prod issues, etc..

  In that sense, it'd be a sin if we don't leverage the power and wisdom of the community.

  How can we "write less, do more"? I feel this needs to be a collective effort which can be broken down into 3 perspectives.

  Developers' Perspective

  Being a developer with daily obligations to meet, I'd look at if I have reused libraries as much as possible. It wouldn't feel right if I have to spend time / effort beyond a certain threshold worrying about technical side of things. Reusing the libraries that are mature and well-tested would save us a ton of reinventing the wheel and make our codebase much smaller. I'd deem it worthwhile to take the time to research for possible existing solutions before head down coding. Instead of rushing into a solution, I'd spend time on that "hang on..." and "but wait..." conversation with myself, getting through that struggle to strive for the best of all worlds. Of course there's a slim chance that that effort doesn't lead to anything meaningful and you'd eventually have to go with a painful solution. But I'd say that rarely happens. Keep in mind, we're not the first generation of developers and chances are someone's been through the pains already so we don't have to.

  Library Authors' Perspective

  Being a lib author is anything but trivial. A library is not some code that's used by one project that so happens can be used by another. It needs to be well thought out from the get go, stand the test of time, and evolve through user comments. It needs to be focused and generic enough at the same time. It should be  focused on a single responsibility so that it's easily composable depending on use cases. It should be generic enough within the area it cares to cover and not assume any usage scenarios so that it can benefit as many users as possible. We also need to make sure it's relatively leading in terms of technology iterations so that even the more cutting-edge projects could benefit from reusing the lib. In software, library authors are sometimes called "vendors". I think that's a great analogy. As a vendor, you want to make your products as small and granular as possible so as to widen your customer base. And in order to gain more market share, you want to make your products the best in their verticals.

  Organization's Perspective

  Being an organization, we need to make sure we are encouraging code reuse the right way. I've seen projects which are "blessed" to be reusable / lib projects. And then teams are forced to reuse those libs because they're meant to be reused. But that doesn't necessarily mean they're designed to be reused. In fact, those projects often go with poor documentation, monolithic highly-coupled codebase, and poor support. It's a pain to use such libs but usage is enforced, so less productive devs, higher dev / maintenance costs, etc.. Sitting on a fixed budget, those projects don't really have incentives to create something great. How do we as an organization facilitate code reuse? Take Github for example, it's like a marketplace where everybody's empowered to contribute. The market gets to choose which libs work best. The ones that are poorly designed, outdated, or simply not robust enough naturally see less or zero reuse. It can hardly be a bad idea if we empower everybody to contribute and make it a marketplace where only love is funded. Thus in order to facilitate code reuse as an organization, it's important to provide

  - a platform where existing solutions are easy to find and usage stats are transparent
  - the incentives for libraries to be well thought out / considerately implemented / battle tested / well documented / shamelessly promoted
  - an easy way for developers to collaborate on de facto best libs in their verticals so that they evolve over time and remain state-of-the-art

  I hope this inspires you to think about coding less but achieving more.
---