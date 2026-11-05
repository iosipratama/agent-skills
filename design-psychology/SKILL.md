---
name: "design-psychology"
description: "Use when designing, reviewing, or critiquing an app, website, or digital product (screens, flows, onboarding, empty and error states, settings, paywalls, notifications, redesigns), when planning user tests or reading feedback, or when a design or product decision seems driven by gut feel, the boss, deadlines, metrics, or effort already spent. Applies how users and designers actually think, based on the book Product Design Psychology by Wouter de Bres."
---

# Design Psychology

Every design choice is a prediction about what people will notice, understand, feel, and do. This skill makes those predictions explicit and checks them against how people really behave, and against the biases of whoever is designing (including you, the agent).

Problems show up in four places, in this order: the designer's mind, the interface, the user, the team. Reference files follow the same split. Load only the one you need.

- `references/designer-mind.md`: biases that distort the designer's own judgment
- `references/interface.md`: how screens steer seeing, choosing, and acting
- `references/users.md`: goals, habits, feelings, attention, failure, plus ethics
- `references/team.md`: authority, meetings, rebuilds, metrics, roadmaps, framing
- `references/tests.md`: cheap tests, with steps and fail signals

## Pick the mode

| Request | Workflow | Load if needed |
|-|-|-|
| Review a screen, flow, screenshot, prototype | Review | interface.md, users.md |
| Design a new feature, flow, onboarding | Design | users.md, interface.md |
| Plan a test, research, or read feedback | Research | tests.md, designer-mind.md |
| Stuck, debating, rebuild, roadmap, metric calls | Decision | team.md, designer-mind.md |

## Review workflow

1. Read it as a newcomer with half their attention who forgot last week's session. Talk it through in first person: "Where am I? What's my first move? What will this tap do?" The first spot where the narration gets fuzzy is the first issue.
2. Check in this order (highest user impact first). Stop at the top 3 real problems. Do not list everything.
   1. First read: within about 5 seconds, is it clear what this is for, where to start, and whether it is trustworthy? Does the look suit the category?
   2. Findable actions: does every tappable thing look tappable, and nothing static look tappable? Is the main action visible, not hidden in an icon, menu, gesture, or plain text?
   3. Structure: with the text blurred, do spacing and alignment show what is grouped and what comes first?
   4. Failure states: does every error, empty, offline, timeout, and permission-denied state offer a specific next action? Is input kept?
   5. Mental work: what must the user decode, decide, or keep in mind before acting? Cut what does not serve the task, push the rest later.
   6. Memory: does any step depend on remembering a path, term, gesture, or hidden menu?
   7. Consistency: same action, same place, same word everywhere? Platform patterns over custom ones?
   8. Defaults: if the user accepts every preset as is, where do they land, and does that favor them or you?
   9. Timing and shape: how soon does a new user feel real value? What is the most intense moment (often an error or wait), and how does it end?
   10. Feeling: what one word would a newcomer use? Salesy, patronizing, stiff, clingy, intrusive? Does any modal, prompt, badge, or push interrupt without earning it?
   11. Ethics, always: would a user who saw exactly how this works feel looked after, or played?

## Design workflow

1. Outcome: one concrete sentence on what improves in the user's life if this works (not "finish onboarding"). Each step must move toward it or justify itself.
2. Current habit: name what they do today instead (another app, Notes, screenshots, a spreadsheet, nothing). That is the real competitor. Plan the bridge: import, carry over what works, win one repeated moment first.
3. First value: pick the exact moment they first feel the product help them. Move it as early as honestly possible. Put signup, permissions, paywall, tour, and setup after it where you can.
4. Break fixation: name the main assumption in the first idea (it's a list, it's started manually, it needs its own screen, it needs an account) and sketch one option where it is false. Offer at most 3 real alternatives, not tweaks of one.
5. Design the edges before polishing the middle: errors with next actions, empty states, the ending, the most intense moment.
6. One obvious default. Advanced options off the main path until needed.
7. Pre-mortem: "It shipped and flopped. What went wrong?" Fix the cheapest of the top 3 reasons.
8. Name the cheap test that could prove the design wrong (see tests.md).

## Research workflow

- Before any test, decide which result would change the plan: "If 2 of 5 testers can't log a feeding in under 30 seconds, we redo the entry screen." Without that line, the study is decoration.
- Trust behavior over promises. Ask how they handle it today and what happened the last time they tried to fix it. Ask for a small real commitment (come back tomorrow, import data, pay). "I'd use this every day" is a weak signal.
- Test with people who have zero context, not the team, fans, or anyone from the kickoff.
- Stay silent during sessions. If you feel the urge to help, note why: that is a finding.
- Ask for the gut reaction first, then which moment caused it.
- In synthesis, start with the surprises and failures. Never file a struggling participant under "edge case" or "not our user" without evidence.

## Decision workflow

Ask the question that matches the trap:

- A boss, client, or founder opinion moved the work: "What's behind that?" Separate the reason from the rank.
- Group review: everyone writes their reaction privately before discussion. Log objections that lost.
- "Let's rebuild it": list 5 concrete, evidenced problems with one shared root cause only a rebuild fixes. Fewer than 5: fix the worst one, measure, repeat.
- A new target metric: "How could we hit this number while making the product worse?"
- A roadmap promise: "If this weren't planned yet, would we add it now, given what we've learned?"
- Months already spent: "If a stranger handed us this feature today, would we release it as is?"
- A late concern before a deadline: "What's the smallest check that would settle this, and how long would it take?" Size the check instead of arguing ship versus delay.
- An old debate returns: "Did we try this before? What happened?" Check the decision log.
- Self-doubt cutting the bold option: "Do I have evidence against it, or am I just nervous about defending it?"

## Red-flag phrases

When the user, a teammate, or you say one of these, name the trap and offer the check.

| Phrase | Trap | Check |
|-|-|-|
| "It's intuitive" | familiar mistaken for clear | Which users already know this pattern? Silent walk |
| "They'll figure it out" / "needs a tooltip" | curse of knowledge | Newcomer narration, silent walk |
| "Not our target user" / "that tester was an outlier" | false consensus | The struggling user is the data |
| "Users said they'd love it" | intention-behavior gap | Ask for a small real commitment |
| "Make it bigger so they notice" | attention is limited | Does it deserve the interruption? |
| "Just add a setting" | choice overload | Do most users need it? Keep it off the main path |
| "It looks dated" | rebuild fantasy | Name 5 real problems |
| "We already promised it" / "too late to change scope" | escalation, sunk cost | Not-planned-yet and stranger questions |
| "The research backs it" | research as cover | Which result would have stopped it? |
| "They'll get used to it" (after a change) | loss aversion | Loss audit |
| "It's a copy problem" / "users need educating" | confirmation bias | Maybe the thing itself isn't landing |
| "Everyone liked it in the review" | conformity | Private reactions first |
| "I love this direction" (after days in the file) | familiarity, mere exposure | 5-second test, compare to 3 strong references |

## Your own bias, agent

Your read of a screen is a simulation, not user evidence. Say "likely" and "may", not "users will". When stakes are high or you are unsure, name the cheapest human test that would settle it. Never call anything intuitive.

## Output for reviews

Start with a one-line verdict. Then up to 3 issues, ranked by user impact:

- **Issue:** what the user experiences, in plain words
- **Why:** the principle, in a few words
- **Fix:** the smallest concrete change that solves it

End with one cheap test to confirm. Add an ethics flag only if something triggered it.

## Rules

- Smallest fix that works. Polish over rebuild.
- Platform conventions (iOS HIG, standard web patterns) over novel ones unless a test says otherwise.
- Use persuasion (defaults, progress, framing, reminders) only when it reflects something true and serves the user's own goal.
- Never suggest: pre-ticked consent or marketing, fake urgency or countdowns, fake progress, cancel harder than signup, guilt-trip copy, decline buried while accept is one tap.
- Every interruption (modal, push, badge, review prompt, permission prompt) must earn its moment.
