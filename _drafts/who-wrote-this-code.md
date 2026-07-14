---
layout: post
title: "Who Wrote This Code?"
subtitle: "When agents author most of your commits, provenance stops being a git-blame trivia question and becomes a governance one. Attribution, accountability, and the audit trail in a dark factory."
---

A surprising amount of a company's financial and legal machinery quietly assumes that a person wrote each commit. Capitalization estimates get derived from commit history. Intellectual property attribution leans on who authored what. When something breaks, accountability starts with a name in the blame. All of it rests on an assumption so old nobody states it: behind every change is a human you can point to.

In a dark factory, that assumption breaks. An agent authored the change. A parser gated it. A human approved an exception, or the tier was safe enough that no human needed to. "Who wrote this code" still has an answer, a real and structured one, but it is no longer a name in git blame, and most organizations are not capturing it. The audit trail in an AI-native company is a design decision, not a git default.

## The old world leaned on a name

In the old world, git blame pointed at a person, and a lot of downstream machinery leaned on that pointer. How much engineering effort to capitalize? Estimate it from who committed what. Who owns this IP? Whoever wrote it. Who is accountable for this outage? Start with the author. None of that machinery was necessarily rigorous, but it worked well enough because the underlying assumption held: a human was behind each line, and the name was a real handle on a real responsible party.

Let agents author a large share of the commits and every one of those downstream systems is standing on an assumption that no longer holds. The name in the blame is now a tool, not a person, and the questions that name was answering, cost, ownership, accountability, need somewhere else to point.

## What good provenance looks like in a factory

The answer is not to find a human to blame anyway. It is to capture the real chain of custody on purpose. In a well-built factory, a change has a structured lineage: the issue that motivated it, the spec that defined the intent, the agent that authored it, the markers it emitted to signal its outcome, the artifact that proved it done, and the human who approved the exception if the tier required one. That is a richer, more honest record than a single name in git blame ever was, and it exists only if you decide to record it.

Accountability works differently, and better, when you design for it. When an agent ships a bad change, "who is responsible" is not answered by hunting for an author. It is answered by the gate and the trust tier: what was this agent permitted to do, what should have stopped it, which boundary was supposed to catch this. Design the tiers well and the answer to "how did this happen, and who owns it" is always legible, because responsibility lives in the structure of what each part of the system was trusted to do, not in the accident of whose name is on the commit.

## The upside

Done right, this is not a loss of accountability. It is an upgrade. A human engineering org's audit trail is ultimately a set of names and memories, reconstructed after the fact from commit logs and people's recollections of what happened and why. An AI-native org's audit trail can be structured evidence, captured at the moment it was created: the spec, the markers, the artifact, the approval. This is "trust the artifact" applied to governance. The same discipline that says ship on evidence rather than self-report says answer for what shipped with structured provenance rather than reconstructed blame. The factory can know exactly what happened, because it was built to leave a record instead of a memory.

## The line

In a dark factory, "trust the artifact" isn't just how you ship. It's how you answer for what shipped.

## So what

If you are going to let machines write the code, decide now what record they leave behind: the issue, the spec, the agent, the markers, the artifact, the approval. Provenance you did not design is provenance you do not have, and the first time finance, legal, or an incident review comes asking who wrote this code, "an agent did" is only an acceptable answer if you can show the whole chain behind it.
