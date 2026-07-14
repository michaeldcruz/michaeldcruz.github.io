---
layout: post
title: "You Don't Need a Bigger Model"
subtitle: "Most teams stuck at 'the agent keeps doing the wrong thing' don't have a model problem. They have a legibility problem. A smaller model on a readable system beats a frontier model on chaos."
---

> Draft. The contrarian, quotable one. Aimed at teams reaching for the next model release as a fix.

## The thesis

When an agent keeps doing the wrong thing, the reflex is to wait for the next, bigger model. Usually that's the wrong lever. The agent isn't failing because it's dumb. It's failing because it's acting over a system it can't read, with no clear contract for what "right" looks like and no artifact to check itself against. Fix the environment and a modest model succeeds where a frontier model was flailing.

## Beats to develop

- The upgrade treadmill. Bigger model, marginal improvement, same failures, wait for the next one.
- Why it doesn't work. The bottleneck is the system's legibility and the clarity of the contract, not the model's raw capability.
- The counterexample. A smaller model on a legible system with good gates and clear specs, outperforming a bigger one dropped into chaos.
- The reframe. Spend on the environment, not the endpoint. It's cheaper, it compounds, and it survives the next model too.

## The line

You cannot buy your way from level 2 to level 5 with a better model. The levels depend on each other, and the model was never the missing rung.

## So what

Next time an agent underperforms, resist the model upgrade for one week and improve what it can see and what "done" means instead. Measure the difference. It's usually bigger than the model bump would have been.
