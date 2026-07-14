---
layout: post
title: "The Living Spec"
subtitle: "In a dark factory, the spec is the source code. If it's a stale doc nobody trusts, your agents are building from a lie. Keeping it alive is the real engineering discipline."
---

When agents write the routine change, the thing a human actually authors moves up a level. You stop writing the implementation and start writing the intent. The spec goes in; working software comes out. Which means the spec is no longer a document about the work. It is the work. It is the closest thing you have to source code.

That reframes a lot of things people are used to treating as optional, and it makes one old sin suddenly expensive.

## The old sin gets a new price

Every engineering org has stale specs, and for decades that was a tolerable, low-grade problem. The documentation drifted from the system, everyone knew it, and it mostly did not matter, because the humans building from those docs silently corrected for them. A veteran engineer reads a spec that says the system does X, knows the system actually does Y, and quietly builds Y. The lie in the document gets absorbed by human judgment before it can do any harm.

An agent does not have that reflex. Hand it a spec that says X and it builds X, faithfully, even when the running system does Y and everyone who matters knows it. The stale spec, harmless for years because people compensated for it, becomes a corrupted input the moment the builder stops compensating. In a factory, a spec that lies is not a paperwork problem. It is a production bug waiting for its trigger.

## What "living" actually requires

Calling a spec "living" is not a vibe. It is a set of demands. The spec has to update as the system changes, so it tracks reality instead of drifting away from it. And there has to be a mechanism that catches the drift when it happens, some check that surfaces the gap between what the spec claims and what the system actually does, before an agent builds from the gap. Without that, "living spec" is just "stale spec" that has not been caught yet.

This is the same discipline as trusting the artifact and verifying against the running app, pointed at documentation. The spec earns the title "living" only if it is continuously checked against the running truth, exactly the way you would never trust a test that was not run or a report the agent did not have to back up. The word doing the work in "a living spec goes in, working software comes out" is not "spec." It is "living."

## The payoff

Get this right and the spec becomes the highest-leverage artifact you own, because it is the one that literally becomes software. A trustworthy spec is not overhead. It is the lever. Improving it improves everything downstream automatically, because everything downstream is built from it. That is a genuinely new state of affairs: the document is no longer the thing you write instead of the important work. It is the important work, and its accuracy is now a first-class engineering concern rather than a janitorial one.

## The line

A living spec goes in, tested working software comes out. The word doing the work in that sentence is "living."

## So what

Look at your specs and run the honest test: if an agent built exactly what this says, with no judgment and no silent correction, would you get the system you actually have? Every place the answer is no is a place your documentation is lying and your people have been quietly covering for it. That gap is your real backlog, and in a factory it stops being optional to close.
