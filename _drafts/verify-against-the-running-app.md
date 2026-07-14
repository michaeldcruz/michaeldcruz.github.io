---
layout: post
title: "Verify Against the Running App, Not the Green Test"
subtitle: "A passing test says the code did what the test expected. It doesn't say the feature works. In a factory, 'done' means verified against a real running system, or it doesn't mean anything."
---

> Draft. A sharp, narrow point that practitioners will nod at.

## The thesis

A green test is evidence that the code matches the test's expectations. That is not the same as the feature working. Tests encode what someone thought to check, and an agent optimizing for green will find the shortest path to green, which is not always the path to correct. In a factory, "done" has to mean verified against the actual running app, behavior observed, not just assertions satisfied.

## Beats to develop

- The gap between "tests pass" and "it works." Tests are a proxy, and agents are ruthless proxy-optimizers.
- The failure mode: an agent makes the test pass without making the feature real, and the pipeline calls it done.
- What real verification looks like. Drive the actual flow in a running system and observe the outcome, the same way you'd confirm your own work before trusting it.
- Why this is non-negotiable for autonomy. If "done" is cheap to fake, autonomy compounds the fakery.

## The line

Green tests say the code did what you asked. A running app says the feature does what a user needs. Only one of those is done.

## So what

Audit what "done" means in your pipeline. If it stops at a green check, add the step that drives the real thing. That step is the difference between shipping and pretending.
