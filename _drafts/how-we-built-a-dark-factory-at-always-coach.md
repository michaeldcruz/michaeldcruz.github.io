---
layout: post
title: "How We Built a Dark Factory at Always Coach"
subtitle: "Not a manifesto this time. The actual story: what we tried, what broke, what we killed, and the order we did it in. The origin post."
---

> Draft note to self: this is the narrative anchor, the one that earns the consulting. It needs the specifics only I can supply, so I've left bracketed prompts where a real detail, date, or number should go. Fill those in and cut the scaffolding.

Everyone wants the end state. An autonomous factory that ships while you sleep, agents doing the work, humans deciding what is worth doing. I write about that end state a lot. This post is not about the end state. It is about how we actually got partway there at Always Coach, in sequence, with the wrong turns left in, because the wrong turns are the part you cannot get from a framework.

The framework came later. First there was a company hitting the same wall over and over, and the factory is the shape of that wall.

## Where we started

[Set the scene honestly. What Always Coach was at the point this started, and where the pain actually lived. The handoffs, the manual gates, the deploy that only one person really knew how to run. Name the specific thing that made you think "this cannot be how we keep working."]

The pain was not that anyone was slow. It was that the work kept sitting still between the people. A change would get written quickly and then wait: for a review, for a gate, for the one person who understood the fragile part. We were fast at the typing and slow at everything around it, which is to say we were slow.

## The first thing we made legible

Nothing worked until we made the system legible, and I did not understand that ordering at the time. [Tell what you actually did first: the observability you added, the documentation you dragged into line with reality. What was illegible before, and what changed once you could see it.]

The lesson that stuck: an agent cannot safely touch what it cannot read, and neither, it turns out, could we. The work of making the system legible for a machine made it legible for the humans too. That was the first sign we were building the right thing, even though it felt like the least glamorous possible place to start.

## Automating the paths

Then the boring middle that everyone wants to skip. [The specifics of automating the paths to production. CI, releases, the checks. What was manual before, who used to push which button, and what it took to make the default path run without a person babysitting it.]

This is the part no one wants to fund because it does not look like AI. It is just reliability engineering. But without it there is no factory to put an agent into, only a person with extra chores. We did this before we let a single agent act, and I would do it in that order again.

## The ticket that got stuck

Then we let an agent act, and I got the lesson that became the thing I say most often.

A ticket did everything right. The agent read the issue, wrote the code, opened the pull request, passed CI, and merged. The feature was live. And then the ticket sat in "In Progress" for hours, because the agent had finished the work and forgotten to print the one line of text our pipeline was waiting for to mark it done. Everything downstream keyed off that line. No line, no state change. A shipped feature looked, to our own system, like abandoned work.

That bug taught me the most important thing I know about building with agents: never trust what the agent tells you it did, trust the artifact. The merged pull request was real. The agent's report was a story it forgot to tell. So we changed the rule, and the system now reads the evidence and moves the work forward whether or not the agent remembered to announce itself. [Add what else this scar changed in how you build, if anything, beyond this one fix.]

## The gates we drew on purpose

The next thing surprised the people I described it to. As the agents took on more, we deliberately drew gates: auth, billing, database migrations. The agents ship the safe majority of the roadmap on their own and stop, on purpose, before those. [Describe the moment you decided where the gates went, and any case that taught you a gate belonged somewhere you had not put one.]

People read the gates as immaturity, as if we were racing to remove them. It was the opposite. The refusal to touch billing unsupervised is what makes the rest trustworthy. The gate was the design, not a gap in it.

## What it did to the team

This is the part nobody prepares for. When the machine does the routine middle, the people move up the stack, from executors to taste-makers and metric-owners. Their job stops being to do the work and starts being to define what good means and own whether it turned out well. [Tell the honest version. How the team actually felt about that shift, who took to it and who did not, what you got wrong in how you communicated it, what you would do differently to bring people along.]

I will not pretend this part was clean. It is a real change in what people's days are made of, and treating it as a pure upgrade that everyone should obviously want is how you lose the people you most need for the new work.

## What still isn't done

We are early, and I would rather say so than sell a finished thing that does not exist. [Be specific about where it is still fragile, what breaks, what you are not comfortable letting the agents near yet, and what you would rebuild if you started over knowing what you know now.]

## The line

We didn't design a factory and build it. We built a company, kept hitting the same wall, and the factory is the shape of the wall.

## So what

If you want the end state, you cannot copy ours. Your wall is in a different place. But you can walk the same sequence, in the same order, make it legible, automate the paths, let agents act, reframe the people, and skip a few of the scars we kept. That sequence, walked with other companies, is the work I do now.
