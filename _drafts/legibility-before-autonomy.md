---
layout: post
title: "Legibility Before Autonomy"
subtitle: "An agent can't safely change what it can't read and watch. Observability and honest documentation aren't step two of AI adoption. They're the ground everything else stands on."
---

Here is a question that will tell you more about your readiness for AI than any demo: could a competent stranger understand how your system works from your documentation and dashboards alone, without asking the one person who remembers?

If the answer is no, you are not ready to hand any of it to an agent. Not because the agent isn't smart enough, but because you are about to delegate to something that cannot see.

Everyone wants to jump straight to the exciting part, agents acting on their own. But autonomy over a system you cannot observe is not the goal. It is the failure mode. An agent confidently changing something it cannot read is exactly the disaster people are afraid of, and it is what you get when you skip the unglamorous step that comes first.

That step is legibility. Before an agent can safely touch anything, the system has to be readable and watchable: real observability, documentation that reflects reality instead of last year's intentions, and a model of how the thing actually behaves. **Legibility is not the paperwork before the real work. It is the real work.**

## Legibility is not "we have some docs"

Most teams think they have this covered because a wiki exists. That is not what I mean.

Legibility means a newcomer, human or machine, can reason about the system from what is written and instrumented, and be right. It means the documentation describes how the system behaves today, not how someone hoped it would behave when they wrote the page eighteen months ago. It means the important paths are instrumented, so you can watch what is actually happening instead of guessing.

There is a simple tell. If your own engineers can only reason about the system from memory, if the real architecture lives in a few people's heads and the docs are a polite fiction, then an agent has no chance. It is working from the same fiction, without the memory to correct it.

## Documentation that flatters intentions is worse than none

Stale documentation is not neutral. It is actively dangerous, because it is confidently wrong.

No documentation at least tells you the truth: go read the code, go watch the system, trust nothing else. Documentation that describes an intended design the system drifted away from tells a lie with a straight face, and an agent will believe it. It will make decisions on a map that no longer matches the territory. The honest half-page beats the impressive, obsolete twenty pages every time.

## Observability is the agent's senses

An agent cannot verify its own work against a system it cannot observe. This is the same principle as trusting the artifact, pointed one step earlier: the agent needs to see the world in order to check itself against it. Without instrumentation, "did that change do what I intended" is unanswerable, so the agent falls back on the only thing it has left, its own belief. And you already know how much that is worth.

Observability is what lets an agent close the loop: act, observe the result, correct. Take away the senses and you have not built an autonomous worker. You have built a confident one, working blind.

## The line

You cannot delegate to something that cannot see. Legibility is not the step before autonomy. It is what autonomy is made of.

## So what

Before you buy another agent or write another prompt, run the stranger test on your own system. Could an outsider understand it from your docs and dashboards, with no tribal knowledge? Wherever the answer is no, that is your next project, and it is the one that makes every later project possible.
