---
layout: post
title: "You Don't Need a Bigger Model"
subtitle: "Most teams stuck at 'the agent keeps doing the wrong thing' don't have a model problem. They have a legibility problem. A smaller model on a readable system beats a frontier model on chaos."
---

When an agent keeps doing the wrong thing, there is a reflex, and the reflex is almost always the same: wait for the next model. The bigger one, the smarter one, the release that is surely a few weeks out. Once it lands, the thinking goes, the failures will stop.

They usually will not, and it is worth understanding why, because the belief is expensive. It puts your progress on someone else's release schedule and it aims your spend at the one lever that is rarely the problem.

## The agent isn't failing because it's dumb

Watch closely when an agent goes wrong and you will usually find it is not a reasoning failure. It is an environment failure. The agent is acting over a system it cannot fully read. There is no clear contract for what "right" looks like, so it guesses. There is no artifact for it to check itself against, so it trusts its own belief. Given all that, a wrong answer is not a sign of a weak model. It is the predictable result of a strong model working blind.

A bigger model does not fix any of those conditions. It still cannot read what is not legible. It still has no contract where you did not write one. It still cannot verify against an artifact that does not exist. You have made the guesser smarter without giving it anything better to work from, and so you get a marginally better version of the same failure.

## The counterexample that should change your spending

Put a modest model on a legible system, one with real observability, clear specs, enforced contracts, and a way to verify against the running app, and it will outperform a frontier model dropped into chaos. Not because it is more capable in the abstract, but because capability was never the binding constraint. The system was. Once the agent can see what it is doing, check itself, and know what done means, an ordinary model does extraordinary work, because the environment is doing half the job.

This is the same truth as the ladder from autocomplete to autonomy. You cannot buy your way from the middle rungs to the top with a better endpoint. The rungs depend on each other, and the model was never the missing one.

## Spend on the environment, not the endpoint

The practical case is almost boring. Investing in the environment, the legibility, the contracts, the verification, is cheaper than most people assume, it compounds instead of resetting, and it survives the next model. Every dollar you put into making your system readable pays off with the model you have today and again with every model that comes after. Every dollar you spend waiting for a bigger model buys you one bump and leaves the underlying problem exactly where it was.

## The line

You cannot buy your way from level two to level five with a better model. The levels depend on each other, and the model was never the missing rung.

## So what

Next time an agent underperforms, resist the upgrade for one week. Instead, improve what it can see and sharpen what "done" means, then measure the difference. It is usually larger than the model bump would have been, and unlike the model bump, it is yours to keep.
