# iOS checklist: concrete rules and values

Paraphrased from the Human Interface Guidelines as of iOS 27 (November 2026), plus Apple's design talks. Use these to make fixes concrete. Don't recite them to the user. Pick the ones that matter for the screen.

## Layout

- Most important content near the top and leading edge. People read top to bottom, leading to trailing.
- Align to shared edges so things scan. Indent to show that something belongs to the item above.
- Group with space first. Add containers or separators only if space isn't enough.
- Respect safe areas and system margins (about 16-20 pt on iPhone). Background content runs edge to edge under the bars.
- The middle and bottom of the screen are easiest to reach. Keep frequent actions there. Swipe back and row swipe actions must work.
- Show fewer controls on screen. Put secondary actions in menus, context menus, or detail views (progressive disclosure).
- Lay out by size class, not device type or orientation. From iOS 27, iPhone apps can be resized on iPad and in iPhone Mirroring, so no fixed widths. Test the smallest and largest layouts.
- Same features in every size class. Only how much is visible changes (a tab bar can become a sidebar on iPad).
- Common practice (not an Apple rule): a consistent spacing scale, such as multiples of 4 or 8 pt.

## Typography

- SF Pro is the system font. New York is the serif option. Use at most 2 typefaces. A custom font works for headlines, but keep system fonts for body and captions, where legibility matters most.
- Use text styles, not fixed sizes. At the default text size: Large Title 34, Title 1 28, Title 2 22, Title 3 20, Headline 17 semibold, Body 17, Callout 16, Subheadline 15, Footnote 13, Caption 1 12, Caption 2 11 pt.
- Body defaults to 17 pt. Never go below 11 pt.
- Avoid Ultralight, Thin, and Light weights for UI text. Use Regular, Medium, Semibold, or Bold.
- Build hierarchy with weight and color (primary vs. secondary label) before adding more sizes.
- Support Dynamic Type up to the largest accessibility sizes. Wrap instead of truncating, stack horizontal rows, cut columns, and keep primary elements at the top. Not everything needs to grow (tab labels can stay put).
- Don't use tight leading on 3 or more lines of text.
- SF Symbols should match the weight of the text next to them and scale with it.

## Color

- Use semantic system colors (label, secondaryLabel, systemBackground, systemGroupedBackground...). Don't hard-code their values.
- Every custom color needs light, dark, and increased-contrast variants. Supply both light and dark even if the app ships in one appearance, so Liquid Glass can adapt.
- One color, one meaning. If the brand color means "tappable", don't use it on static text.
- Use the accent color sparingly: the primary action, the selected tab, status and badges. Brand color works better in the content layer, where it shows through the glass.
- Never rely on color alone. Add a label, symbol, or shape.
- Contrast: at least 4.5:1 for text up to 17 pt, and 3:1 for 18 pt and up or bold text.
- Check in bright sunlight and in a dark room. Check what the colors mean in the target cultures.
- iOS background levels: primary for the view, secondary for groups inside it, tertiary for groups inside those. Use the grouped set for grouped lists.

## Liquid Glass and materials (iOS 26+, refined in iOS 27)

- Glass is the functional layer: tab bars, toolbars, sidebars, floating controls. It doesn't belong in the content layer (cards, rows, backgrounds), which uses standard materials instead. Sliders and toggles turn glassy only while being touched.
- Standard components get glass automatically. Use custom glass sparingly, and only on the most important functional elements.
- The regular variant is the default. Use the clear variant only over rich media (photos, video). If that media is bright, add a dark dimming layer at about 35%.
- Color on glass, sparingly: tint the background of the one primary action (the prominent style), not its label, and not several controls.
- Over colorful content, keep bars monochrome. Avoid label colors that match the content behind them. Make sure the resting state (the top of the scroll) is legible.
- No solid backgrounds behind bars. The scroll edge effect handles legibility, and iOS 27 adds a uniform top toolbar treatment automatically.
- People can set glass anywhere from clear to tinted (iOS 27), and can turn on Reduce Transparency or Increase Contrast. The design has to hold up in all of these.
- Harmony: nested corners are concentric. Capsules work well for touch controls.

## Navigation and structure

- **Tab bar:** top-level sections only, never actions. Always visible. Each tab has an SF Symbol plus a label. Use as few tabs as needed (5 or fewer avoids the More tab). Never hide or disable tabs. Badges only for important information. Search can be its own tab at the trailing end. The bar can minimize on scroll with an accessory, like Music's mini player.
- **Toolbar / nav bar:** the title names the view, never the app. Large titles on top-level screens. Use the standard Back and Close. Keep it to a few items, grouped by function, with extras in a More menu. One primary action, in the prominent style, on the trailing side. Prefer borderless system symbols.
- **Search:** see the search placement section in `principles.md`. The placeholder says what's being searched. Offer suggestions or recents, with privacy in mind.
- **Lists:** inset grouped style for settings-like content. Swipe actions for common row actions. Show a selection state.
- **Context menus:** shortcuts only. Every item is also available elsewhere. Keep them short, most-used first, with one level of submenu at most. Hide unavailable items rather than dimming them.
- **Gestures:** standard ones first. A custom gesture is only ever a shortcut, never the only way to do something. Don't fight system edge gestures.

## Modals, sheets, alerts

- Use a modal only when it clearly helps focus or a decision. Keep it short, and don't build an app inside the app.
- The title names the task. Dismissal is obvious: Cancel on the leading side, Done on the trailing side, swipe down. Before discarding user content, confirm with a Save option.
- One sheet at a time. Never show Cancel, Done, and Back together.
- Sheets on iPhone: consider a medium detent for progressive disclosure. Resizable sheets get a grabber and support swipe to dismiss.
- Full-screen modals are for immersive or complex multi-step tasks (camera, photo editing).
- **Alerts:** rare, critical, actionable. Never at launch, never just for information, never for common undoable actions. The title states the situation. Add body text only if it helps. Buttons are verbs, with "OK" only for purely informational alerts. A destructive button gets the destructive style plus a Cancel. Three buttons max, and no scrolling.
- Choices about something the person just started (delete, share options) go in an action sheet, not an alert.

## Controls

- Hit area at least 44x44 pt. Add about 12 pt of space around bezeled controls and about 24 pt around borderless ones.
- Every custom button needs a pressed state.
- Show emphasis with style (prominent vs. plain), not size. Give the primary role to the most likely action, but never to a destructive one.
- Labels are short verb phrases ("Add to Cart"). Use text when it's clearer than an icon. Use familiar icons for familiar actions.
- If an action doesn't complete instantly, show an activity indicator in the button.
- Offer choices (pickers, toggles, segmented controls) instead of typing. Validate as people type. Show the format in placeholder or hint text. Put errors next to the field.
- Get data from the system where possible: autofill, passkeys, Apple Pay, the location button, contacts.
- Never prefill a password field.

## Motion and fluid interaction

- Respond on touch down. Any lag breaks the feeling of direct manipulation.
- Content tracks the finger 1:1, with continuous feedback through the whole gesture.
- Every animation can be interrupted and redirected mid-flight. Never make people wait for one to finish.
- Things leave the way they came in.
- Carry gesture velocity into the animation. Rubber-band at the edges.
- Springs instead of fixed-duration easing. No bounce when there's no momentum, and a small bounce only when the gesture threw something.
- Motion needs a purpose: show where something came from, what changed, or what's possible. Keep feedback motion brief and precise. Don't add motion to things people do constantly.
- Reduce Motion: replace slides and zooms with fades, tighten springs, and avoid animating blur or depth.
- Use SF Symbol animations for state changes (bounce, replace, appear).

## Haptics

- Use system haptics for what they mean: notification (an outcome: success, warning, error), impact (a physical snap or collision), selection (a value ticking through a picker or slider).
- Haptics add to visible feedback and never replace it. Use them consistently, not on every tap. Standard controls already play their own.
- Haptics should be optional. Remember they also affect anything else happening on the device (camera, audio).

## Accessibility and inclusion

- Dynamic Type up to the largest accessibility size (Settings > Accessibility > Display & Text Size > Larger Text).
- Every icon-only control and meaningful image has a VoiceOver label. Reading order is logical. Related elements are grouped.
- Contrast ratios as above. Increase Contrast variants. Bold Text works with custom fonts.
- Every gesture has an alternative. Visible labels so Voice Control can name things. No time limits without control. No autoplay without controls. Respect Dim Flashing Lights.
- Localization: text gets longer in other languages, so leave room. System components handle right-to-left mirroring. Format dates and numbers for the locale.
- Use inclusive language and imagery. Don't assume gender, family structure, or ability.

## Writing

- Set the voice once, and adjust the tone to the moment (a celebration and an error don't sound the same).
- Buttons and links start with a verb. "Send" beats "Let's do it!". Avoid "Click here".
- Plain words, no jargon. Use "tap", not "click", on touch devices.
- Use "my" and "your" sparingly ("Favorites", not "Your Favorites"). Never say "we" in errors: "Unable to load content", not "We're having trouble".
- Errors go next to the problem, without blame, and say how to fix it: "Choose a password with at least 8 characters", not "Password too short". No "Oops". If many people hit the same error, rethink the interaction instead of rewording the message.
- Empty states say what goes here and offer the action to start. Don't put anything crucial there, since it disappears.
- Keep settings labels plain. Link straight to a setting instead of describing where it is.
- Pick a capitalization style and stick to it everywhere.

## States and moments

- **Launch:** instant. The launch screen matches the first screen, with no logo or text. Restore where people left off, including scroll position.
- **Onboarding:** fast, fun, optional. Teach by doing. Prefer contextual tips (TipKit) over an upfront tour. No license text. Use good defaults instead of setup questions. Ask for a rating or purchase only after people have used the app.
- **Loading:** show layout or placeholders right away. Use a determinate progress bar when the duration is known. Let people do other things while they wait.
- **Empty:** a next step and a button.
- **Error:** inline, specific, keeps the input, offers retry.
- **Offline:** show cached content and say how fresh it is.
- **Success:** confirm only significant actions (payments, sends). Otherwise the result is the confirmation.
- **Ratings:** use the system prompt, only after real engagement, never mid-task, and don't nag.

## Privacy, permissions, notifications

- Ask for a permission when the feature first needs it. Ask at launch only if the app can't work without it, and then explain why during onboarding.
- A custom pre-permission screen has one button, and it clearly opens the system prompt. Nothing that could mislead, especially before the tracking prompt.
- Permission text says plainly what the data is used for. Collect only what's needed. Process on device where possible. Offer the location button for one-time location.
- Notifications: get permission first. Set the right interruption level, and use Time Sensitive only for things that matter right now. No marketing pushes without explicit opt-in. Let people manage notification settings inside the app.

## AI features

- Show where AI is used, and set clear expectations about what it can and can't do.
- People stay in control: preview before applying, easy to refine, revert, or regenerate. Ask before anything irreversible.
- Expect wrong output. Add guardrails wherever harm is possible, and cut the feature if the risk outweighs the value.
- Design for wait time: specific, reassuring progress feedback. Consider offering a few alternative results.
- The app must still be great when AI is unavailable or turned off.
- Ask before using personal data. Let people rate or report outputs, and confirm when a correction has taken effect.

## Adaptivity and platform

- iPad: a sidebar, or a tab bar that adapts into one. Let people customize tabs when there are many sections.
- Keep context through rotation and resizing.
- App icon: simple, one focal point, filled overlapping shapes, layered in Icon Composer. Must work in default, dark, clear, and tinted. No text unless essential, no photos, no copied UI, no Apple hardware.
- SF Symbols: outline variant next to text and in toolbars, fill for selected tab bar items and swipe actions. Use variable color only to show change (volume, signal), not depth.

## Check on device

Static mockups hide most craft problems. Before calling a design done:

1. Largest accessibility text size
2. Dark Mode, Increase Contrast, Reduce Transparency, Reduce Motion
3. A quick VoiceOver pass through the screen
4. One hand, thumb only
5. Outdoors in sunlight
6. The smallest and largest supported iPhone, plus a resized window on iPad
7. A long language (German) or long user content
8. Slow network and airplane mode
