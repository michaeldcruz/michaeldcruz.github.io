---
layout: post
title: "The Handoff Was Always the Bottleneck"
subtitle: "Software was never slow because people typed slowly. It was slow at the seams: the waiting, the reviews, the manual gates, the one person who knows how to deploy. AI made typing free and left the seams alone."
---

We keep optimizing the wrong thing, and we do it because the wrong thing is the visible thing.

When you picture an engineer working, you picture them typing. So making the typing faster feels like making the work faster. That is the intuition the entire first wave of AI coding tools was sold into, and it is why so many teams bought a faster keyboard and wondered why the company did not speed up. The time was never in the typing. It was in the seams.

## Follow a change and watch where the time goes

Take a single change from idea to production and account for where it actually spends its life. A little of it is someone composing the code. Almost all the rest is waiting. Waiting for a review. Waiting for the reviewer to have time. Waiting in a queue behind other changes. Waiting for someone to run the deploy, or to be available to run the deploy, or to remember the sequence of manual steps the deploy requires. Waiting for the one person who understands the fragile part to weigh in.

Add it up honestly and the composition, the part AI made faster, is a rounding error against the waiting. You optimized the fifteen minutes and left the three days alone.

## Every seam is a human-scheduled delay

Look closely at each seam and they share a shape. A handoff is a change sitting still until a specific person picks it up. A review is a change sitting still until someone with the right context has attention to spare. A manual gate is a change sitting still until a human performs a step by hand. Tribal knowledge is a change sitting still because the one person who knows is in a meeting. None of these are typing delays. They are all human-scheduling delays, the friction of coordinating people, and they are where software actually goes slowly.

This is why a copilot cannot touch your throughput. It speeds the one step that was never the constraint. It makes the fast part faster and leaves every slow part exactly as slow. The demo looks great and the quarter looks the same.

## What actually closes the seams

The thing that moves throughput is automating the paths, so the seams stop being human-scheduled. Continuous integration, so a change is checked the moment it exists instead of when a person gets around to it. Releases that run without someone pushing each button. Checks that gate automatically instead of waiting on an available human. When the default path to production runs on its own, the change stops sitting still between the steps, and the waiting, which was the actual bottleneck, drains out of the process.

That is the unglamorous work everyone wants to skip on the way to the exciting agents. But it is the work that makes the exciting agents matter, because an agent that writes code fast, dropped into a process full of human-scheduled seams, just gets to wait faster.

## The line

The bottleneck was never how fast a person could type. It was everything that happened between the people.

## So what

Map one change's real journey to production, and highlight the waiting instead of the working. Be honest about how much of the calendar is coordination, not composition. Then automate the seams, in that order of pain. That is where the weeks are hiding, and no faster keyboard will ever find them.
