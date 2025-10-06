+++
title = "Coding agents when writing code is the bottleneck"
date = 2025-09-11
description = "Today I realized how useful coding agents can be when writing code _is_ the bottleneck"

[taxonomies]
tags = ["bits", "remote-work", "development", "ai", "llm", "coding-agents"]
+++

With a new AI-powered coding agent being announced seemingly every other day, we must remind ourselves that [writing code was never the bottleneck](https://ordep.dev/posts/writing-code-was-never-the-bottleneck)...

... except when it _is_.

---

Working as a contractor means dealing with company policies that weren't designed with my setup in mind - or my peace of mind.

I am currently working for a company that doesn't allow code, messages or any other form of Intellectual Property to be stored on contractor's computers. Instead, we are required to connect remotely to Windows Virtual Desktop (WVD)^[I'm so happy to be back on Windows /s] instances even if all we want is to send a message on Microsoft Teams^[The best communication app for teams /s]. And, of course, there is no native client for connecting to WVDs on my OS (Ubuntu) - so I need to use a web client. You would think that that is already painful enough, right? Wrong. On top of this, all software development is done on code servers<!-- TODO: is it "Azure" code servers? --> accessed via Microsoft Edge^[Microsoft's recommended browser - probably because it's the best one out here /s].


[---]

My current situation: I develop on Windows Virtual Desktop (WVD) accessed through a web app (no native Linux client), connecting to code servers that can only be reached through those WVDs.

The result? A latency nightmare. There's a noticeable delay between typing and seeing characters appear on screen. It's the kind of lag that makes you question your sanity and turns simple coding tasks into exercises in frustration.

But today I had a realization: **I'm glad coding agents exist.**

I've been relying heavily on AI assistants to write code for me, and suddenly the common criticism of "coding agents aren't the future because writing code was never the bottleneck" feels completely backwards. For me, right now, _writing code_ is literally the bottleneck.

The irony is beautiful: a technology that many dismiss as solving a non-problem has become essential for my productivity. When typing is painful due to infrastructure constraints, having an AI that can generate entire functions, refactor code blocks, or implement features from descriptions becomes invaluable.
