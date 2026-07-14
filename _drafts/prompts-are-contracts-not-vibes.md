---
layout: post
title: "Prompts Are Contracts, Not Vibes"
subtitle: "If your agents signal outcomes in prose, you're one forgotten sentence away from silent failure. Markers a parser enforces are the difference between a build that fails loudly and work that strands quietly."
---

Most people treat a prompt as a suggestion written in English. You describe what you want in nice paragraphs, the model reads them, and you hope the output lands close enough. For a chat window, fine. For a factory that runs unattended, that hope is a liability.

In a system where agents hand work to other agents, a prompt is not prose. It is an interface. And interfaces have contracts.

## The failure that hides

Picture a pipeline where one agent finishes a phase and signals the outcome so the next step knows what to do. If it signals in prose, "I've completed the analysis and everything looks good," then something downstream has to interpret that sentence. Maybe it matches on a keyword. Maybe another model reads it. Either way, you have built a dependency on the exact shape of a sentence a language model generates fresh every time.

Then the sentence drifts. A prompt gets edited, the phrasing changes, the agent says "analysis complete" instead of "completed the analysis," and the thing downstream stops matching. Nothing errors. Nothing alerts. Work just quietly stops flowing, and you find out when tickets pile up and someone asks why the pipeline went quiet. This is the worst kind of failure: invisible, gradual, and rooted in something nobody thought was load-bearing.

## What a contract looks like

The fix is to stop signaling in prose and start signaling in markers. The agent emits a specific token for each outcome. A parser reads that exact token. There is a single source of truth defining the tokens, and a validator that fails at build time if a prompt stops emitting one it is supposed to.

Now the interface is enforced. If someone changes the marker, the build breaks immediately, in front of the person making the change, instead of silently three weeks later in production. You converted an invisible runtime failure into a loud compile-time one, which is the only kind of failure you can actually fix before it costs you.

There is a subtle trap worth naming. A renamed marker still reads fine to a human and still typechecks, because to the compiler it is just a different string. Your good intentions and your type system will both wave it through. So the guard cannot be "we'll be careful" or "the compiler will catch it." It has to be an explicit test that asserts the prompt still emits every marker its parser expects. The contract is only real if something automatically checks that both sides still agree.

## The general principle

This is bigger than prompts. Every place a human hands intent to a machine, or a machine hands intent to another machine, is an interface. And every interface your system depends on deserves a contract and a test, whether or not it happens to be written in English. The fact that a prompt looks like a friendly paragraph is exactly what fools people into skipping the discipline they would never skip on an API.

## The line

An English sentence is a vibe. A marker a parser enforces is a promise. Autonomy runs on promises.

## So what

Find the prose in your agent pipeline that something downstream quietly depends on. Turn it into an enforced marker with a test that fails when the two sides drift apart. You will have taken one silent failure and made it loud, which is the whole game.
