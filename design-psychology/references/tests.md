# Cheap tests

Each test takes minutes to an hour. Use the smallest one that answers the open question. A "fresh person" can be a friend, a family member, or a TestFlight user who has never seen the screen. Anyone who saw the kickoff or the file doesn't count. Three to five people catch most big problems.

## Tests the agent can run alone
These are simulations. Say so, and recommend a human test when the stakes are high.

**Newcomer narration**
- Talk through the screen as someone new with half their attention: Where am I? What's my first move? What will this tap do? Then what?
- Fail: the first fuzzy, hedged, or "probably" sentence. That spot is the issue.

**Load audit** (most-used screen)
- List every term to decode, choice to make, and thing to keep in mind before the user can act.
- For each: does it help the task? Remove it, postpone it, or keep it.

**Options audit**
- Count tabs, menu entries, extra buttons, filters, toggles, mode switches, and settings on the screen.
- Keep on the main path only what most users need most of the time.

**Default audit**
- List every preset: checked boxes, prefilled fields, selected plan, primary button, list order, toggle states, the opening tab.
- For each: if the user accepts everything as is, where do they land, and does that favor them or you?

**Consistency audit**
- Pick the primary action. Screen by screen, note its placement, label, and control type (button, link, icon).
- Then list the nouns used for each concept and keep one.
- Fail: 3 or more placements or labels for the same action, or 2 names for one thing.

**Recall audit**
- Walk a core flow and flag each step that relies on memory: a term, a route, a hidden menu, a gesture.
- Replace with something visible wherever you can.

**First failure test**
- Force every broken state: no network, timeout, invalid input, empty data, permission denied, payment failed, server error, sync conflict.
- For each: is there a concrete action available now? Is the user's input kept?
- Fail: a generic message, no action, lost input, or "contact support" with no link.

**Peak-end map**
- Write the flow as steps and rate the emotional intensity of each (plus or minus).
- Circle the lowest point and the final screen. Were both designed on purpose? Fix the low first, then the ending.

**First-value check**
- Mark the moment a new user first feels real value.
- List everything before it (signup, paywall, permissions, tour, setup). Move or remove each item that doesn't have to come first.

**Progress start check**
- Does the progress indicator start empty? Credit real steps already done.

**Interrupt check**
- For each modal, push, badge, banner, review prompt, and permission prompt: what was the user doing right before, and is this worth breaking into it? Does it come after a success rather than mid-task?

**Assumption flip**
- Name the core assumption of the current idea. Make one rough version where it is false.

**Pre-mortem**
- "It shipped and flopped. What went wrong?" List the top reasons and address the cheapest.

## Tests that need people

**5-second test**
- Show the key screen for 5 seconds, then hide it. Ask: What's this for? What would you do first? Would you trust it with your money or data?
- Variant: show it beside a direct competitor.
- Variant for a new market: ask whether anything feels missing.
- Fail: they can't say what it's for or where to start, or they hesitate on trust.

**Silent walk**
- Give a realistic task. Don't talk, point, or explain.
- Log pauses (cue missing), mis-taps (cue misleading), reaches that stop short, and quits.
- If you itch to help, write down why. That's a finding.

**Cover-the-text test**
- Blur or block all text. Ask which items seem grouped, what looks most important, and where they would start.
- Fail: the grouping they describe is wrong. Fix spacing, alignment, and styling before copy.

**Gut-reaction test**
- First question: "What's your gut reaction, in one word?" Then: "Which moment caused that?"
- Fail: uneasy, irritated, spied on, lost, or indifferent.

**Habit watch**
- Watch or ask about the current routine: which app they reach for, which workaround keeps coming back, what moment sets it off.
- Pick one recurring moment the new product can win.

**Obstacle list** (before building on "I'd use this")
- List what could block the action: no time, existing routine, setup effort, competing priorities, know-how, price. A long list means weak intent.
- Ask: How do you handle this today? When did you last try to fix it, and what happened?

**Small real commitment**
- Ask for something that costs a little: an email, importing their data, coming back 3 days in a row, paying. Behavior beats promises.

**10-minute weak-spot hunt**
- One person spends 10 minutes only looking for where it breaks, no praise. Note your first excuse.

**Reference comparison**
- Lay the design beside 3 strong products tackling a similar job, to reset your eye, not to copy.

**Loss audit** (redesigns)
- Three columns: what users rely on without thinking | what the change does to it | the gain that pays for it.
- Heavy loss column: phase it in, announce it, keep the old path for a while, allow switching back.

## Before research and reviews

**Decide the deal-breaker first**
- Write: "If [specific behavior or number], we [stop or change X]." Example: "If 2 of 5 testers can't log a feeding in under 30 seconds, we redo the entry screen."
- If you can't write it, the study is there to justify, not to learn.

**Private reactions first**
- In reviews, everyone writes their reaction for 2 minutes before anyone talks. Log the objections that lost.

**20-minute rough draft**
- Timer on, make deliberately rough options. If you resist starting, that's stalling.
