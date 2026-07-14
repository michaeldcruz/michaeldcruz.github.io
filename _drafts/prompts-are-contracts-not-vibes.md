---
layout: post
title: "Prompts Are Contracts, Not Vibes"
subtitle: "If your agents signal outcomes in prose, you're one forgotten sentence away from silent failure. Markers a parser enforces are the difference between a build that fails loudly and work that strands quietly."
---

> Draft. The engineering-discipline post. Concrete, practitioner-facing.

## The thesis

Most people treat prompts as suggestions written in English and hope for the best. In a factory, a prompt is an interface with a contract. The agent emits specific markers, a parser enforces them, and if someone renames one the build fails loudly instead of stranding work in silence. Prose is where reliability goes to die. Contracts are where it lives.

## Beats to develop

- The failure without contracts: an agent's prose drifts, a downstream parser stops matching, and nobody notices until tickets pile up.
- What a marker contract looks like in practice. Named outcome tokens, a single source of truth for those tokens, a validator that fails at build time if a prompt stops emitting one.
- The subtle trap: a renamed token still typechecks, still reads fine, and silently breaks the parser. So the guard has to be an explicit test, not a compiler's good luck.
- The broader principle: treat every place a human hands intent to a machine as an interface that deserves a contract and a test.

## The line

An English sentence is a vibe. A marker a parser enforces is a promise. Autonomy runs on promises.

## So what

Find the prose in your agent pipeline that something downstream depends on. Turn it into an enforced marker. You just converted a silent failure into a loud one, which is the only kind you can fix.
