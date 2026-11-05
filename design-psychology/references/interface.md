# The interface

Every visual and structural choice steers what people notice, pick, and do, intended or not.

## 11. Looks earn trust first (thin-slicing)
- What happens: People decide whether a product seems credible within a blink, before touching anything. Attractive products get more patience. The snap judgment is about fit: does this look like a credible example of its category?
- Look for: Low-quality imagery, styling that clashes with the domain (a finance app with cartoon styling, a meditation app with harsh contrast, a pro tool with clip-art), empty states that look unfinished, a first App Store screenshot that doesn't show the app doing its job.
- Do: Run a 5-second test, also next to a direct competitor. Fix credibility of the first screen early, because people who bounce there never show up in your usability sessions.

## 12. Presets steer choices (default effect, framing)
- What happens: Whatever is preselected looks like the expected, endorsed option. Switching costs effort and the current state feels safer, so most people keep it. No arrangement is neutral: order, emphasis, and preselection all steer.
- Look for: Pre-checked boxes, prefilled fields, the highlighted plan on a paywall, which button is primary, list order, initial toggle states, the tab the app opens on.
- Do: Default audit. Good presets match what most users would pick or reuse a choice they already made (region, units, last used). Bad presets favor you at the user's expense (marketing opt-in, maximum data sharing, the priciest plan preselected).

## 13. Make actions visible (signifiers)
- What happens: An action exists whether or not anyone can see it. Visual cues are what make it discoverable. Removing them for a cleaner look causes missed and wrong taps.
- Look for: Plain text that is actually a button, key actions as unlabeled icons, cards that may or may not open, swipe or long-press as the only route, links styled like body copy.
- Do: Give every interactive element at least one cue (tint, fill, border, chevron, underline, label). Keep static elements from looking pressable. During a silent walk, pauses point to absent cues and mis-taps to misleading ones.

## 14. "Intuitive" is learned (schemas)
- What happens: When something feels intuitive, people are recognizing a pattern they already learned in other products. Known patterns cost almost nothing to use; unfamiliar ones eat attention. Navigation tucked behind a menu icon gets discovered much less than navigation on screen.
- Do: When someone says intuitive, ask which users already know this pattern, and from where. Patterns common across many apps (tab bar, standard sheets, swipe back, pull to refresh, search at the top) are safe bets. Patterns only the team knows prove nothing. A new pattern needs a test before it ships.

## 15. Extra effort adds up (cognitive load)
- What happens: Working memory holds roughly four items. Some effort is the task itself. The rest is overhead the interface adds: unclear wording, weak hierarchy, leftover steps. Tiny moments of doubt pile up until people stop. A hard subject (taxes, health, money) is no excuse for a hard interface.
- Do: Load audit. Remove overhead that doesn't serve the task. What has to stay can come later (progressive disclosure: show what the next step needs, reveal the rest on demand). For heavy tasks, ask one thing per screen in everyday words.

## 16. Stay predictable (predictive processing, consistency)
- What happens: People constantly anticipate the next step. Each surprise costs a bit of effort and a bit of trust. Alerts used for trivial things teach people to dismiss all alerts, including the important one. Using several names for one thing (Collection, Folder, Board) makes people wonder whether they are different.
- Do: Consistency audit on the primary action: placement, label, and control type on every screen. Pick one name per concept and remove the others. Reserve confirmations and destructive styling for actions that are truly risky.

## 17. Memory fades (forgetting curve, recognition over recall)
- What happens: Most users drop in now and then. They return having forgotten much of what they learned, and without the onboarding context they learned it in. Tooltips and walkthroughs rarely stick.
- Look for: Important actions only in a "..." menu, gestures as the only path, an empty search box where recent items would help, terms that only make sense if remembered from onboarding.
- Do: Recall audit. Show recent items, suggestions, visible next actions, and labeled icons. Assume the user remembers nothing from last time.

## 18. Highs, lows, and endings stick (peak-end rule)
- What happens: People judge an experience afterwards by its most intense moment and its final moment, not by the average. A bumpy flow that ends well can beat a smooth one that fizzles.
- Look for: A dead-end "Done" screen, success with no next step, the worst moment (an error, a long wait, lost input) left undesigned.
- Do: Map the emotional curve of the flow. Fix the worst low first. Give the ending relief and a next step: a clear confirmation, a touch of delight sized to the stakes, a success haptic. Ask for ratings or upgrades right after a good moment, never after friction.

## 19. Nearness to done motivates (goal gradient, endowed progress)
- What happens: People push harder the closer they feel to finishing, judged as a share of the whole. An empty bar reads like a list of chores ahead. One that credits work already done makes people feel underway and more likely to finish.
- Do: Count real completed steps (account created, email confirmed, first item added) as progress and frame the state as partly done. Never invent steps or fake progress.

## 20. Structure is read before text (Gestalt)
- What happens: The eye groups things by closeness, similarity, alignment, and shared motion before any word is read. Uneven spacing forces people to guess which caption goes with which input. Something nearly aligned looks more wrong than something clearly offset. Elements that animate together read as one unit.
- Do: Cover-the-text test. Tight spacing inside a group, more space between groups. One visual style per role (primary, secondary, destructive). Fix spacing and grouping before rewriting copy.
