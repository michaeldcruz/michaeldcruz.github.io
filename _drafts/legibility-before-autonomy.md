---
layout: post
title: "Legibility Before Autonomy"
subtitle: "An agent can't safely change what it can't read and watch. Observability and honest documentation aren't step two of AI adoption. They're the ground everything else stands on."
---

> Draft. The "first, make your system legible" beat from the manifesto, expanded into its own argument.

## The thesis

Everyone wants to jump to agents acting autonomously. But autonomy over a system you can't see is the failure mode, not the goal. Before an agent can safely touch something, it has to be able to read it and watch it: real observability, documentation that reflects reality instead of last year's intentions, a model of how the system actually behaves. Skip legibility and every later step is built on sand.

## Beats to develop

- What legibility actually means. Not "we have some docs." Can a newcomer, human or machine, reason about the system from what's written and instrumented, without asking the one person who remembers.
- The tell: if your engineers can only reason about the system from memory, an agent has no chance.
- Documentation that reflects reality vs documentation that flatters intentions. Why the second is worse than none.
- Observability as the agent's senses. It can't verify its own work against a system it can't observe.

## The line

You cannot delegate to something that cannot see. Legibility is not the paperwork before the real work. It is the real work.

## So what

Before you buy another agent, ask whether an outsider could understand your system from your docs and dashboards alone. If not, that's the project, and it's the one that makes every later project possible.
