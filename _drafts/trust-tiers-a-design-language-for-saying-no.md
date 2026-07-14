---
layout: post
title: "Trust Tiers: A Design Language for Saying No"
subtitle: "The intelligence in an autonomous system isn't what it does. It's how it decides what it's not allowed to touch. Layered trust is how a process that reads a stranger's message never reaches your production database."
---

> Draft. The architecture post, more technical. Pairs with "The Gate Is the Product" but focuses on the how.

## The thesis

Autonomy is not one switch. It's a set of boundaries, and the design work is drawing them well. A process that reads untrusted input, a user's message, an incoming issue, physically cannot be allowed to write to production, because trust is layered by design, not by hope. Trust tiers are how you turn "the agent should be careful" into "the agent structurally can't."

## Beats to develop

- The core move: separate by trust, not by convenience. What reads a stranger's input is a different tier than what touches money.
- Concrete tiers. Untrusted-input readers, routine-change actors, money-and-auth actors that must escalate to a human. Each with different permissions, enforced structurally.
- Why "be careful" is not a control and layering is. Careful is a wish. A permission boundary is a fact.
- Designing the escalation. The genuinely ambiguous cases route to a person, and that routing is the valuable judgment, not a fallback.

## The line

Careful is a wish. A tier is a wall. Build walls.

## So what

For every agent, ask what it reads and what it can write, and whether those two facts are safe to combine. Where they aren't, that's a tier boundary you should be enforcing, not trusting.
