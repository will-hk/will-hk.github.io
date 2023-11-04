---
title: Think out of the Box
layout: post
permalink: /think-out-of-the-box
body: |
  One of the projects I worked on has a need to generate a report for each run. The report needs to include functional information throughout the execution flow which would later provide insight while troubleshooting during support.

  With this requirement, it's reasonable to come up with below assumptions:
  - Since we need to write a report, we'll need disk IO. 
  - Since we need to write functional information throughout the run, we'll need to keep the write stream open throughout the run in order not to waste resource.
  - Since the information we write could be of any type, we need to make sure our interfaces accept generic types and our implementation dynamically processes passed in data.
  - Since report writing is not part of the functional logic, we want to ignore any failure that's caused within the report writing logic.

  That sounds all good, but it's quite some work in that we'd have to implement all above, plus come up with and maintain a suite of tests for it. We'd have to deal with intricacies around testing code that does IO. We'd have to test all scenarios (types) with parameterized test. For a simple requirement like this, it just feels too much and doesn't feel right.

  Let's pull back and think twice. Do we really need to implement all this? Could there be any existing solutions?

  The answer is probably "no", but could there be existing tools that make it easier to implement and less costly to maintain a report writer? Is there a thing that
  - streams data to disk
  - you can call at any point of the execution
  - is data type agnostic
  - gracefully fails and doesn't interrupt execution flow

  Yes, you guessed it. Logging! But how do we take advantage of it? If we write report info to log, it's gonna be cluttered with existing logs and hard to make sense of.

  Here's the solution I came up with. With Springboot + Log4j for example, we can have any amount of loggers in addition to the default one. We can config a logger specifically for report writing. We can then inject that writer wherever we need to call it.

  Great! But hang on, we're supposed to generate one report file for one run whilst the logging system continuously streams to a file until a cut-off point defined by rules such as file size or age.

  With Log4j, there's the concept of appender. One of them is called RoutingAppender, which is able to route your logs to different files depending on one or more thread context variables passed at run-time. For example, we can use the date of each run as a thread context variable and direct the appender to write to a file whose name contains the date string.

  With this setup, we get rid of the need to maintain our own logic and tests around report generation. We get all the benefits of the logging system for free, such as compression and purging. Much less mental overhead while troubleshooting knowing our reports sit side by side with logs.

  I hope this inspires you to think out of the box.
---