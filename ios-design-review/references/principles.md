# Apple's design principles, as review questions

Sources, paraphrased: HIG "Design principles" (reintroduced June 2026), WWDC26 "Principles of great design", WWDC25 "Get to know the new design system", WWDC18 "Designing Fluid Interfaces", WWDC17 "Essential Design Principles", WWDC26 "Craft clear names for features and labels", WWDC26 "Design intuitive search experiences", Apple Design Awards categories.

Apple says there's no formula for combining these principles. They often pull against each other (flexibility vs. simplicity, delight vs. getting out of the way). Use them to name the trade-off, then make a call.

## The 8 principles (2026)

### 1. Purpose
Build something genuinely useful, focus on the few features that matter most, and solve the problem in a way that's yours rather than copying what exists.
- What is this app and this screen for, in one sentence?
- Which features are the core? Are they the best-made parts?
- What could be removed without anyone missing it?
- What makes this different from the obvious existing solution, and does the design show it?

Failure signs: features added because competitors have them, equal weight on everything, a screen that serves the business more than the person.

### 2. Agency
Stay out of the way, let people explore freely, and make mistakes cheap to recover from.
- Can people get straight to the task or content, or is something in the way (tour, signup, setup, upsell)?
- Can every guided flow be skipped or escaped?
- Is there undo? Is a confirmation only shown for destructive actions people didn't mean?
- Can people go at their own pace instead of down a fixed path?

Failure signs: locked modes, forced linear flows, "Are you sure?" everywhere, losing typed input on dismiss.

### 3. Responsibility
Be open about what the product does and why. Collect only what's needed, protect it, and think through misuse and harm.
- Is every permission asked at the moment of need, with a clear reason?
- Is any data collected that the feature doesn't need?
- How could this be misused, and who could it hurt? What's the safeguard?
- For AI: what happens when the model is wrong? Apple's example is a recipe app suggesting an ingredient someone logged an allergy to. Preview, confirm, disclaim, or cut the feature if the risk outweighs the value.

### 4. Familiarity
Build on what people already know from the real world and other apps. Keep things consistent, and give clear feedback.
- Do metaphors land, neither too literal nor too abstract?
- Do common actions use the standard symbol and do the standard thing (trash means delete, nothing else)?
- Things that look the same behave the same. Is that true here?
- Does every action find its place in the same spot across screens?
- Does every action show a clear result: control states, content changes, system alerts for real problems?

### 5. Flexibility
Design for the full range of people, contexts, inputs, and devices.
- Who's actually using it: age, language, novice or pro, accessibility needs?
- Does it hold at the largest text size, in Dark Mode, with VoiceOver, Voice Control, a keyboard?
- Does context survive rotation, resizing, and moving between devices, with content and controls in predictable places?
- Is each platform treated with the same care (iPhone quick and touch-first, iPad and Mac deeper)?
- Where no single layout fits everyone, can people personalize (reorder, hide controls)?

### 6. Simplicity
Include only what's necessary, say it in the fewest clear words, and build strong hierarchy. Simple isn't minimal. Burying everything in one menu looks minimal but isn't simple.
- Is the most important item always the most obvious one?
- Does the screen answer: what should I look at, what can I tap, and how?
- Could complex data be a chart or a summary?
- Does anything need more context to be simple (labels, time remaining, units)?
- Are steps to finish the main task as few as possible?

### 7. Craft
Every detail shows how much you care: visuals, animation, wording, sound. Prototype, iterate, test in real settings, and keep the product current after launch.
- Do taps respond instantly? Is scrolling smooth? Is anything misaligned? Does rotation break the layout?
- Are fonts, colors, symbols, and motion the high-quality "materials" they should be?
- Was it tested on a device, in real conditions, at the edges?
- Has it adopted the current platform design (Liquid Glass, current controls), or does it look like an older iOS?

### 8. Delight
Pick the emotion you want to create, make defining moments, and don't confuse delight with decoration. Delight is what you get when everything else is right.
- What's the one emotion? A fitness app might energize, a meditation app might calm.
- Where is the one defining moment (completing the core action, an empty state, an error) that could carry the app's character?
- Is any flourish slowing down the task? Remove it.
- Is the overall aesthetic matched to the product: practical, or a bit whimsical?

## The Liquid Glass era headline principles (HIG, iOS 26+)

- **Hierarchy:** controls and navigation sit on a separate floating layer that lifts and separates them from the content beneath.
- **Harmony:** shapes echo the rounded hardware. Nested corners are concentric (inner radius = outer radius minus the padding between them). Capsules suit touch controls.
- **Consistency:** follow platform conventions so the design adapts across window sizes and displays.

## Older Apple lenses still worth using

### Wayfinding (WWDC17)
An app is one big wayfinding system, like signs in an airport for tired, rushed people. Every screen should answer:
- Where am I? (title, selected tab)
- Where can I go? (tabs, rows, buttons)
- What will I find there? (labels that predict content)
- What's nearby? (related items, siblings)
- How do I get out? (Back, Cancel, swipe down)

### Mental models, affordance, mapping, proximity (WWDC17)
- **Mental model:** people predict behavior from experience. Match the model they already have, not the system's internals.
- **Affordance:** what something looks like tells people what they can do with it. Tappable things look tappable, static things don't.
- **Mapping:** controls resemble or mirror what they affect (a vertical slider for something that goes up and down, controls laid out in the same order as the things they change).
- **Proximity:** put a control next to the thing it affects. The closer it is, the more people assume a link.
- **Progressive disclosure:** start simple, reveal complexity as people need it.
- **Grouping and symmetry:** related things grouped, layouts balanced. People read symmetry as order and care.

### Fluid interaction (WWDC18)
The goal is an interface that feels like an extension of your hand and mind.
- **Respond instantly.** People are extremely sensitive to latency. Any lag makes it feel disconnected.
- **Redirect and interrupt.** Any animation can be grabbed and reversed mid-flight. Thinking and gesturing happen together.
- **Spatial consistency.** Things leave the way they came in. A view that slides up dismisses down.
- **Hint in the direction of the gesture.** Elements start to move or grow toward their final state as you press.
- **Light input, amplified output.** Short flicks carry momentum (scrolling, throwing a card).
- **Rubber-band at the edges.** Soft resistance instead of a hard stop.
- **1:1 tracking and continuous feedback.** Content sticks to the finger during the whole gesture.
- **Springs, not fixed durations.** Tune damping and response. Use no overshoot when there's no momentum, and a little bounce when the gesture threw it (Apple used 100% damping to open Now Playing and about 80% to swipe it closed).
- **Detect gestures in parallel** from the first touch, so people don't have to choose before they move.

### Naming (WWDC26)
Good names do three things:
- **Belong:** fit the app's voice and sit well with everything else it names.
- **Set the right expectation:** people predict what they'll find from the name, and the screen delivers it. That builds trust.
- **Work everywhere:** across languages, markets, and platforms.

Method: list what people should think, feel, and do when they meet the feature, group the themes, then drop each candidate into a sentence you'd say to a friend ("Check out Visited Places"). Name for what it does for people, not the technology behind it. Where trust matters (money, health, privacy), clarity beats brand: "Balance", not "Spending Power". A clever name is allowed, but it costs extra work to make it understood.

### Search placement (WWDC26)
Decide from two questions: how do people navigate the app, and what does the search cover?
- App-wide search in a tabbed app: a search tab at the trailing end. Use a standard tab with a browse/suggestions page for exploring, or the prominent button style that opens the keyboard right away for quick lookups (like the Phone app).
- Search field in the bottom toolbar: rises above the keyboard, good for reach.
- Inline field under the title: for searching just this list. The placeholder text names the scope.

## The Apple Design Awards bar

Use this when asked "is this great?" or "is this award-level?" Grade 1-5 on whichever categories apply:

| Category | What Apple rewards |
|-|-|
| Delight and Fun | Memorable, engaging, satisfying experiences, made better by Apple technologies |
| Inclusivity | A great experience for people of many backgrounds, abilities, and languages |
| Innovation | A novel use of Apple technologies that sets the app apart in its category |
| Interaction | Intuitive interfaces and effortless controls tailored to the platform |
| Social Impact | Improves lives in a meaningful way |
| Visuals and Graphics | Stunning imagery, skillfully drawn interfaces, and quality animation with a distinctive, cohesive theme |

Most strong indie apps win on one clear idea done exceptionally well, not on feature count.

## The senior designer's question bank

Ask these out loud during a review:
- What is this screen for, in one sentence?
- What's the one thing you want me to do here? Is it the most obvious thing?
- What can we remove?
- Why is this custom? What does the system component not do?
- What happens when it's empty, broken, offline, or holding 1,000 items, a 40-character name, the largest text size, or German?
- Can I undo that?
- Where did that come from, and where does it go back to?
- Does this need to interrupt me right now?
- What should people feel, and does this moment support it?
- Would this make sense to someone who has never seen the app?
