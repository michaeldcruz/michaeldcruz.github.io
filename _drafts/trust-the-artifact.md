---
layout: post
title: "Trust the Artifact"
subtitle: "An agent's report of what it did is a story. The merged pull request is a fact. Build your company on the facts."
---

Ask an AI agent whether it finished the job and it will almost always say yes.

It is not lying. It genuinely believes it. It set out to do the thing, it took the steps, and from the inside the work feels complete. But "the agent believes it is done" and "the work is actually done" are two different claims, and only one of them is safe to build a company on.

We learned the difference the hard way. One of our tickets did everything right: read the issue, wrote the code, opened the pull request, passed CI, merged to develop. The feature shipped. Then the ticket sat in "In Progress" for hours, because the agent had forgotten to print the one line of text our pipeline was waiting for to mark the work done. The change was live in production. The agent's report said nothing. To the system, a shipped feature looked like abandoned work.

That is the whole lesson in one bug. **The agent's self-report is a story it might forget to tell. The artifact is the truth.** The merged pull request was real whether or not the agent announced it. So we stopped asking the agent and started reading the evidence.

## Self-report is the softest signal you have

Think about what you are actually trusting when you trust an agent's summary of its own work.

You are trusting that it understood the task the way you did. That it did not quietly skip a step it decided was unnecessary. That its notion of "done" matches yours. That it did not simply predict the outcome it was hoping for. Every one of those is a place the story and the reality can drift apart, and none of them fail loudly.

A green, merged pull request has none of those failure modes. It either exists or it does not. The tests either ran or they did not. The deploy either happened or it did not. You do not have to trust the narrator, because you are reading the world instead of the narration.

This is not a knock on the models. Humans are the same. "I tested it" is a claim; a passing test in CI is a fact. We built entire practices, code review, continuous integration, staging environments, precisely because we learned not to take a human engineer's word that something worked. Agents do not get an exemption from the thing we already knew about people.

## Design every decision to key off evidence, not narration

Once you take this seriously it stops being a mindset and becomes an architecture rule. Anywhere your system makes a decision based on "did the work get done," ask what objective artifact proves it, and key the decision off that artifact instead of off anyone's report.

At Always Coach this shows up everywhere. A ticket does not advance because an agent says it is finished. It advances because the pipeline sees a merged PR. A change is not verified because a test file exists. It is verified because the check went green against a real running app. When the agent remembers to announce itself, good, that is a nice human-readable bonus. When it forgets, the work still moves, because the marker was never the source of truth. The artifact was.

The failure we hit was survivable precisely because the evidence outlived the agent's memory. Build the other way, on self-report, and the same forgotten line strands a shipped feature forever, with no error and no alert. Silent stranding is the worst class of bug in an autonomous system: nothing is on fire, so nothing tells you to look.

## The line

Never trust what the agent tells you it did. Trust what it left behind.

## So what

Walk your own pipeline and find every place a decision hangs on someone, agent or human, reporting that a thing is done. For each one, name the artifact that would prove it independently: the merged commit, the passing check, the row in the database, the live endpoint answering. Then move the decision onto the artifact. That single reflex, evidence over narration, is most of what separates an AI system you can leave alone from one you have to stand over.
