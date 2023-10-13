---
title: Inclusive Peer Review
layout: post
permalink: /inclusive-peer-review
body: |
  Being a developer grants you some "privileges" you don't often get working in other occupations. One such privilege is the right to point out the defects in any of your peers' code in front of everyone else. I'm not kidding. This process has a fancy name - peer review or PR.

  Due to the nature of this process, there's actually a lot more to take into consideration than it seems. So I'm writing this blog post to share my thought process and use it as a reminder to myself as well.

  Let's be honest, if you're doing PR for someone, most of your comments would essentially be saying "You're not doing this right", "You're doing that wrong", etc.. It's a form of complaining / blaming. To make it worse, those comments go without any tones or facial expressions, and you're not supposed to use emojis in every comment, are you?;) While the purpose of those comments is often positive, such as in the hope that things could improve going forward, it often varies on an individual basis how well they are received. Some would thrive through those constructive comments. Some just wouldn't survive them. Thus PR is really a process of careful language picking and concise idea conveying. It's an art for reviewers to provide comments in a way that makes it easy to understand and accept.

  Here's a list of tips from my experience:
  - Avoid personally addressing the peer. If absolutely necessary, use "We". So instead of saying "You shouldn't do something this way", we can say "Something could be done that way". "Would it be better if something is done that way instead?" or "We could have done it that way", etc.
  - Avoid interrogation. So instead of asking "Why do you do...?", we can directly point out the solution.
  - Make it clear if a comment is really a question instead of a suggestion, such as "For my own knowledge...", "I wonder...", "Question: ...".
  - Use existing references whenever you can so that the comment stays concise and to the point. Such as "Please refer to ...", "... is a good source of inspiration". Existing solutions often stand the test of time and take into account scenarios we don't necessarily foresee.
  - Use charts, diagrams for concepts that are hard to explain using plain words. A diagram is often worth a thousand words.

  Some of the principles I'd follow when I'm not sure:
  - Standing in the peer's shoes. How would I feel if I were to receive a comment of some kind?
  - Focusing on the subject. Am I only talking about the code itself or am I unintentionally implying on the peer's knowledge / experience?
  - Staying unambiguous. Am I assuming anything in terms of the audience's knowledge? 

  What can we do as an organization to promote and encourage inclusive peer review?

  First we need to recognize the importance of peer review. It serves as an extra line of defense that protects us from production issues and technical debts. It's a premium paid upfront to save us cost + interest down the line, i.e., net cost reduction. It's a chance for us to wield the power of diversity and gain extra perspectives. And it's not optional at all.

  Second we need to acknowledge the effort involved in the PR process and allocate dedicated resources accordingly. One thing I noticed over my career is, PR is often considered an optional process that could be skipped giving way to other priorities. To me, it's an indispensable process that requires significant amount of resources / time to make right. A thorough review and rectification of a poorly authored pull request can often take more time and effort than the original pull request itself. It could involve back and forth conversations, further researches, refactoring of existing codebase, adding missing tests, etc.. And these are absolutely necessary to do in order to avoid technical debt we cannot afford to pay back later when it snowballs. Therefore it's crucial for teams to actually allocate resources for PR during planning sessions, giving reviewers sufficient time so that they don't have to worry about their own priorities while doing the reviews. Treat reviewers as humans (not machines) who have finite cognitive energy and require warm-up during context switching.

  Last but not least, educate. We need to raise awareness on the set of right things to do when it comes to PR. We need to shed light on the pitfalls so developers can avoid them. We could have "reviews of reviews" or "comments on comments" so that everyone can learn from others' lessons.

  I hope this inspires you to think differently. Happy PRs.
---