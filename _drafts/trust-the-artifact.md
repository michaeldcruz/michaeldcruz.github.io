---
layout: post
title: "Trust the Artifact"
subtitle: "The single principle that separates an AI demo from an AI company: never believe what the agent says it did. Believe the evidence it left behind."
---

> Draft. This is the core principle. It shows up in the manifesto as a scar; here it gets its own full treatment.

## The thesis

An agent's self-report is a story it might forget to tell. The merged pull request, the green pipeline, the row in the database: those are facts. Build your system to key off the facts, not the narration, and it stops mattering whether the agent remembered to announce itself. This one rule is the difference between something you can leave alone and something you have to babysit.

## Beats to develop

- The stuck ticket. Tell the full version: shipped PR, forgotten marker, hours in limbo, nothing actually wrong.
- Why LLMs make this failure mode routine, not rare. They're built to produce plausible text, and "I finished" is plausible whether or not it's true.
- The fix as a pattern, not a patch. Every important state change should have an objective fallback: read the artifact, move forward, ignore the missing self-report.
- Where else this applies. Tests, deploys, "the customer was notified," "the payment went through." Anywhere you're tempted to trust a claim over a record.

## The line

The agent's self-report was a story it simply forgot to tell. The merged pull request was real. Trust the one that's real.

## So what

Audit your pipeline for every place a decision hangs on an agent saying it did something. Replace each with a check of what actually exists. That's the upgrade from demo to company.
