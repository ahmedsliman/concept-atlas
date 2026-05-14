Here's a concrete 12-week plan. I'm designing it to fit around full-time work (roughly 4–5 hours per week of deliberate practice) and to compound across the three skills rather than treating them as separate tracks.

## The core structure

Each week has three slots:

**Slot 1 — Weekend deep work (2 hours):** one focused exercise, rotating through the three skills.
**Slot 2 — Daily micro-practice (15 min × 5 days):** reading, embedded into your existing routine.
**Slot 3 — On-the-job practice (ongoing):** one small habit applied to your actual Payback work.

The rotation matters. Working on all three skills every week is how people burn out and quit. Rotating keeps each skill fresh and lets insights from one week seep into the next.

## Weeks 1–4: Foundation

**Week 1 — System mapping (your own work)**

*Weekend:* Draw Payback's architecture on paper. Services, data stores, external APIs, queues, sync vs async boundaries, auth flow, where money-related state lives. Don't look at existing docs first — draw from memory. Then verify against code/docs and mark every gap in red.

*Daily:* Read one chapter of *Designing Data-Intensive Applications* (DDIA). Start with Chapter 1. Take notes in your own words, not highlights.

*On the job:* For every ticket you pick up this week, write two sentences before coding: "This change affects X. It could break Y." Just that.

**Week 2 — Code reading (your own codebase)**

*Weekend:* Pick the most important Payback module you *didn't* write. Spend 2 hours reading it. Produce a one-page document: what it does, how it's called, what it depends on, where bugs are most likely. Share it with a teammate who knows the module and ask what you missed.

*Daily:* DDIA Chapter 2. Continue the two-sentences habit.

*On the job:* On every PR review this week, open at least one file outside the diff to understand context before commenting.

**Week 3 — Debugging (retrospective)**

*Weekend:* Pick the three hardest bugs you've debugged in the last 6 months. For each, write a short post-mortem: symptom, root cause, why it was hard to find, what would have caught it earlier. Look for patterns across the three.

*Daily:* DDIA Chapter 3. Continue two-sentences habit.

*On the job:* For any bug you hit this week (yours or a teammate's), apply five-whys before fixing.

**Week 4 — System stress-test**

*Weekend:* Take last week's Payback architecture drawing. For each component, ask: what happens if it's slow? If it fails? If traffic 10x's? If two requests race? Write the answers. Where you don't know, mark it and investigate Monday.

*Daily:* DDIA Chapter 4. Continue two-sentences habit.

*On the job:* In your next design discussion or standup, ask one "what happens if this fails?" question.

At the end of Week 4, you should notice: you think about failure modes more automatically, and your sense of Payback's system has sharpened measurably. If not, the plan isn't sticking — we'd adjust.

## Weeks 5–8: External exposure

This phase gets you out of your own codebase, which is where pattern-matching hides gaps.

**Week 5 — Read open-source Laravel internals**

*Weekend:* Read Laravel's service container implementation (`Illuminate\Container\Container`). Not the docs — the source. 2 hours. Write a page explaining how it works in your own words.

*Daily:* 15 min reading Laravel source (pick any file that seems interesting). Goal is fluency, not coverage.

*On the job:* Start a personal "debug journal" file. Every bug you touch gets two lines: symptom and root cause.

**Week 6 — System design (external problem)**

*Weekend:* Pick a product you use daily that isn't yours — Revolut, N26, Klarna. Spend 2 hours designing the core payment authorization flow from scratch. Then search for their engineering blog posts about how they actually did it. Write down three things you missed.

*Daily:* Read one AWS, Cloudflare, or Stripe post-mortem. There's a backlog of years.

*On the job:* Continue the debug journal.

**Week 7 — Lower-layer debugging**

*Weekend:* Pick one tool from this list and spend 2 hours learning it deeply: `strace`, `tcpdump`, MySQL slow query log + `EXPLAIN`, or Xdebug profiler. Use it on something real — a slow endpoint, a weird container issue, anything in your stack.

*Daily:* Continue post-mortems. Switch DDIA to Chapter 5.

*On the job:* Next time something is slow or weird, use the new tool before guessing.

**Week 8 — Code archaeology**

*Weekend:* Pick a gnarly function in Payback. Use `git log -p` and `git blame` to reconstruct its history. Why does it look like this? What bugs shaped it? What requirements? Write the story.

*Daily:* DDIA Chapter 6. Continue debug journal.

*On the job:* When you inherit unfamiliar code, spend 20 minutes reading before changing.

## Weeks 9–12: Integration and ownership

Now you start applying these skills at the level of actual ownership — which is where Payback lead role matters.

**Week 9 — Write a design doc**

*Weekend:* Pick one non-trivial thing you'll build or change in Payback this quarter. Write a real design doc: context, goals, non-goals, proposed design, alternatives considered, failure modes, rollout plan. 2 hours. Share it with a senior engineer you respect, ask for brutal feedback.

*Daily:* DDIA Chapter 7. Continue journal.

*On the job:* Apply the doc's thinking to your week's work.

**Week 10 — Read a hard bug thread**

*Weekend:* Find a famous debugging story — there are great ones in the `danluu/post-mortems` repo, or the Cloudflare blog. Read it actively: before each reveal, predict what you'd do next. 2 hours.

*Daily:* DDIA Chapter 8.

*On the job:* Review a PR in a part of the codebase you don't normally touch.

**Week 11 — Teach something**

*Weekend:* Pick one thing you've learned in the last 10 weeks. Write it up — blog post, internal doc, lunch-and-learn slides. 2 hours. Teaching forces you to find the holes in your understanding.

*Daily:* DDIA Chapter 9.

*On the job:* Offer to pair with a junior engineer on a tricky problem. Narrate your thinking aloud.

**Week 12 — Review and re-measure**

*Weekend:* Go back to Week 1's architecture drawing. Redraw Payback from memory *without* looking at the old one. Compare. The difference is your growth. Also reread the three bug post-mortems from Week 3 — would you now explain them differently? What would you catch earlier?

*Daily:* DDIA Chapter 10.

*On the job:* Plan the next 12 weeks, focusing on whatever area still feels weakest.

## What makes this work (and what kills it)

**What kills it:** treating it as a course to complete. You're not going for completion; you're going for *changed default behaviors*. If you do Weeks 1–4 and the two-sentences habit stops when the week ends, you learned nothing.

**What makes it work:** the on-the-job habits are the actual growth engine. The weekend exercises are scaffolding. After 12 weeks, the two-sentences habit, the debug journal, and the read-before-you-change habit should be permanent. That's the real outcome.

**If you only have 2 hours per week:** drop the weekend slot and keep the daily micro-practice plus on-the-job habits. You'll progress slower but still progress. The worst move is to plan 5 hours, miss a week, feel bad, and quit.

**If you have 8+ hours:** don't add more material. Go deeper on what's there — read more of Laravel's source, do more post-mortems, write a second design doc. Depth beats breadth here.

## One thing before you start

Pick a fixed 2-hour block for your weekend work and put it in your calendar for all 12 weeks right now, today. Not "Saturday morning" in your head — an actual calendar event. The engineers I've seen succeed at this kind of plan treated the time as non-negotiable. The ones who failed treated it as aspirational.

Do you want me to turn this into a checklist or a tracking template you can actually use, or is the prose version enough?