---
layout: post
title: "The Handoff Was Always the Bottleneck"
subtitle: "Software was never slow because people typed slowly. It was slow at the seams: the waiting, the reviews, the manual gates, the one person who knows how to deploy. AI made typing free and left the seams alone."
---

> Draft. A focused deep-dive on one idea from the manifesto: the bottleneck was never keystrokes.

## The thesis

We keep optimizing the wrong thing because it's the visible thing. Typing is what you watch an engineer do, so making it faster feels like progress. But the time never lived in the typing. It lived in the seams between people: the wait for review, the manual gate, the deploy only one person can run, the context trapped in three heads. AI made the typing free and touched none of the seams. That's why nothing got faster.

## Beats to develop

- A walk through where a change actually spends its time, from idea to production. Almost none of it is composition.
- Each seam, named. Handoffs, reviews, waiting, manual gates, siloed knowledge. Why each is a human-scheduled delay, not a typing delay.
- Why copilots can't touch this. They speed the one step that wasn't slow.
- What does touch it. Automating the paths so the seams close: CI, releases, checks running without a person pushing each button.

## The line

The bottleneck was never how fast a person could type. It was everything that happened between the people.

## So what

Map your change's journey and highlight the waiting, not the working. Then automate the seams. That's where the weeks are hiding.
