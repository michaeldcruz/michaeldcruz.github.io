---
layout: post
title: "Who Wrote This Code?"
subtitle: "When agents author most of your commits, provenance stops being a git-blame trivia question and becomes a governance one. Attribution, accountability, and the audit trail in a dark factory."
---

> Draft. Sparked by the "derive your CapEx split from commit history" idea. If half your commits have a non-human author, that whole premise wobbles. Worth a post.

## The thesis

A lot of financial and legal machinery quietly assumes a person wrote each commit: capitalization estimates from commit history, IP attribution, accountability when something breaks. In a dark factory, an agent authored the change, a parser gated it, and a human approved an exception, or didn't. "Who wrote this code" now has a real, structured answer, and most orgs aren't capturing it. The audit trail is a design decision, not a git default.

## Beats to develop

- The old world: git blame points at a person, and everything downstream (capex, ownership, blame) leans on that. The new world breaks the assumption.
- What good provenance looks like in a factory. The issue, the spec, the agent, the markers it emitted, the artifact that proved it done, the human who approved the exception. All of it captured on purpose.
- Accountability without a human author. When an agent ships a bad change, "who's responsible" is answered by the gate and the trust tier, not by a name in the blame. Design the tiers so the answer is always clear.
- The upside. Done right, an AI-native company has a cleaner, more honest audit trail than a human one ever did, because the evidence is structured instead of remembered.

## The line

In a dark factory, "trust the artifact" isn't just how you ship. It's how you answer for what shipped.

## So what

If you're going to let machines write the code, decide now what record they leave behind. Provenance you didn't design is provenance you don't have.
