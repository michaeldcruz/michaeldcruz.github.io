---
layout: post
title: "Stop Measuring Engineers. Measure the Factory."
subtitle: "The useful unit of output in an AI-native company is not lines per engineer. It's how much of the roadmap ships without a human touching it."
---

There is a rush right now to quantify individual engineering output, and it makes sense on the surface. AI writes a lot of the code now, so leaders want to know what that did to productivity. Commits per head. Throughput per engineer. "Our engineers are twice as productive." The dashboards are getting built as we speak.

They are measuring the wrong noun. In a company where a machine writes the routine change, how productive any individual person is tells you almost nothing about how fast the company can move. The interesting number is not about the people at all.

## Per-engineer metrics assume the human is the unit of production

Every per-engineer metric carries a hidden assumption: that the person is the unit that produces the work, so measuring the person measures the output. That was true when humans typed every line. It is the thing that just stopped being true. When a machine does the routine building, measuring the human harder is like timing the fastest horse the year the car arrived. You can get very precise numbers about a quantity that is no longer the constraint.

And once you have a real factory, the engineer is genuinely not the bottleneck. The bottleneck is the legibility of the system, the automation of the paths, the trustworthiness of the gates. Measuring the engineer tells you nothing about any of those, so it tells you nothing about what actually limits your speed.

## The metric that points at the factory: autonomy rate

The number worth watching is what fraction of your roadmap reaches production with no human in the loop. Call it autonomy rate: the percent of merged changes that no person wrote and no person reviewed. That single number points directly at the thing that matters, because you physically cannot raise it without building everything underneath it. You cannot ship changes autonomously over a system agents cannot read, so autonomy rate rewards legibility. You cannot ship them through paths that need a human to push each button, so it rewards automation. You cannot safely ship them without gates you trust, so it rewards the boring reliability layer. It is a metric you cannot game without actually building the factory, which is exactly what makes it a good one.

## The denominator is not one hundred percent, and that's the point

One trap to name before anyone chases this number off a cliff. The goal is not one hundred percent. Shipping the safe majority of your roadmap with no human is a triumph. Shipping one hundred percent, including auth and billing and irreversible migrations, is not a better triumph. It is a red flag, because it means you removed the gates that make the rest trustworthy. The right target has a ceiling on purpose. A healthy autonomy rate is "as much of the safe work as possible flows on its own, and the consequential work still stops for a person." An autonomy rate of one hundred percent is not a factory operating perfectly. It is a factory with its safety gates removed.

## The line

You don't get a faster company by measuring people harder. You get one by measuring how little of the work still needs them.

## So what

If you are a leader picking a metric this quarter, pick the one that pulls you toward the factory, not the one that pulls engineers toward the keyboard. Measure the fraction of work that ships without a human, keep the deliberate ceiling on it, and watch it force you to build the legibility and automation you were going to need anyway.
