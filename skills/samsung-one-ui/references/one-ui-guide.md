# Samsung One UI Reference

Source: Samsung One UI Design Guidelines PDF  
URL: https://design.samsung.com/global/contents/one-ui/download/oneui_design_guide_eng.pdf

Curated by Devthinks ([devthinks.com](https://devthinks.com)) for reusable agent workflows and published by `geekynasir`. This file distills the official Samsung guide into implementation-ready heuristics for design reviews and UI rewrites.

Use this file when a request needs Samsung-specific layout, component, motion, or accessibility decisions. Keep outputs paraphrased.

## Table of contents

- How to use this reference
- Architecture
- Components
- Visual design
- Motion and interaction
- Accessibility
- Quick audit checklist
- Section map

## How to use this reference

- Start with Architecture for any redesign or audit.
- Read only the component sections that match the screen you are working on.
- Use the Quick audit checklist for fast reviews.
- Use the Section map when you need to jump back into the source PDF for a specific area.

## Architecture (guide pages 6-14)

### Core intent

- Create a UX that feels consistent with other Samsung mobile apps and devices.
- Reduce learning cost across phones, tablets, foldables, and DeX.
- Make important content easy to see and frequent actions easy to reach.

### Viewing and interaction areas

- Divide phone screens into a top viewing area and a bottom interaction area.
- Put titles and passive content higher on the screen.
- Put frequent actions, tabs, and action-required dialogs lower on the screen.

### Screen depth and hierarchy

- First-depth browsable screens are allowed to feel larger and more spacious, especially when they benefit from an expanded app bar.
- Second-depth and later screens should usually be more compact and more task-focused.
- When in doubt, make deeper screens denser and clearer rather than more decorative.

### Focus blocks

- Use large rounded containers to pull attention to important content.
- Increase contrast between a focus block and the surrounding blank space so the block reads quickly.
- Use focus blocks for cards, lists with media, or any content that benefits from a strong focal point.

### Themes and dark mode

- Support both a default theme and dark mode.
- Lighter default backgrounds can improve general legibility by reducing overall contrast fatigue.
- In dark mode, keep the whole screen darker, including focus blocks, dialogs, and controls.
- In Samsung's examples, very dark or black backgrounds can visually merge with a black bezel and make content feel more immersive.
- Dark themes should reduce glare and work comfortably at night.
- Let the user switch to dark mode at their preferred or scheduled time.

### Responsive behavior

- Design for phones, tablets, foldables, multiple aspect ratios, orientations, multi-window, and DeX.
- On larger screens, show more content and account for multi-layer layouts and varied window sizes.

### Margins and safe area

- Keep at least 24dp side margins.
- Keep touch targets and sparse interactive controls inside the safe area.
- Avoid placing tappable elements into curved or rounded-corner regions where they may be obscured or hard to hit.

### Screen optimization

- Expect user-controlled font size changes, zoom, resolution changes, and home screen density changes.
- Do not rely on a layout that only works at one scale.
- Test whether labels, tabs, and action buttons remain intelligible when font size or zoom changes.
- When text gets longer because of localization or font settings, demote lower-priority actions into overflow rather than breaking the hierarchy.

### Architecture heuristics

- If important content feels lost, add focus blocks before adding more color or chrome.
- If the screen demands repeated reaches to the upper corners on a phone, the interaction area is probably too high.
- If a tablet or foldable layout still looks like a stretched phone, add density and consider multi-layer structure.

## Components (guide pages 16-56)

### App bar

- Use the app bar to communicate screen context and expose actions.
- The title can act as an app title, page title, or page filter.
- Prefer icon actions.
- Keep app bar actions to three or fewer.
- If no actions are available, show no actions.
- Put lower-priority commands into more options.
- If the title is too long, far-right actions can move into overflow to preserve the title.
- Show or hide actions as needed for language and font settings, but keep the same priority rules.
- Use text buttons only when iconography would be unclear.
- A spinner shows the current selected value and opens an anchored dropdown of options.

### Expandable app bar

- Use on list or grid screens where a larger first-depth header improves context.
- It has only two states: expanded and collapsed, with no intermediate resting state.
- It works well with tabs, search, and scrollable content.
- On later-depth screens, default to collapsed but allow expansion when the view supports it.
- On first main screens, showing the expanded app bar by default is often appropriate.
- Do not use it on keyboard-heavy screens except for simple input.
- Avoid it when media or user content may be cropped.
- Avoid it on screens that need to be filled entirely by controllers or additional vertically scrolling elements.
- Full-screen landscape phone layouts do not support the expandable app bar.
- In multi-window, foldable, and DeX layouts, landscape support is allowed when the window height exceeds 580dp.
- If the user scrolls upward while expanded, collapse the app bar; if they scroll downward while collapsed, expand it.
- When the finger lifts mid-gesture, snap to expanded or collapsed based on whether the threshold was crossed.
- If search is essential, the search bar can live in the expandable area, hide while scrolling, and reappear afterward.

### Bottom bar

- Use for high-priority actions.
- Allow up to five actions.
- Use icons, text, or a mix of both.
- The bar can appear or hide while scrolling depending on how much space the content needs.
- Do not add overflow menus here.
- Do not make bottom-bar actions horizontally scrollable.
- Do not place the bar above the keyboard unless the actions are directly related to keyboard input, such as Cancel, Done, Save, or Next.
- Treat the bottom bar as an action surface, not as navigation.

### Bottom navigation

- Use bottom navigation to switch between primary sections.
- Keep tabs visible even while content scrolls.
- Each main tab should own its own view.
- Prefer four or fewer main tabs; five is the upper limit.
- Name the screen title the same as the corresponding bottom tab when possible.
- Do not use overflow menus inside bottom navigation.
- Do not let the user switch main tabs by swiping horizontally across the content body.
- Do not place bottom navigation above the keyboard.
- If the main tab already represents the app, you can use that name as the title and omit a separate app title.
- Keep all bottom tabs visible on one screen at default font size whenever possible.
- Use top subtabs for categories on the current screen.
- Make subtabs scrollable when there are five or more.
- Users can move between top subtabs by swiping horizontally in the content area.
- If translated labels become long, abbreviate them for the bottom tab if necessary but keep the full title in the app bar and on larger surfaces.

### Buttons

- Use flat buttons when you want to avoid creating unnecessary visual layers.
- Use contained buttons when the action would otherwise be easy to miss in a busy layout.
- Do not mix flat and contained buttons on the same screen.

### Slider

- Use sliders for ranged values such as volume or brightness.
- Provide immediate feedback while the value changes.

### Dialogs

- Put action-required dialogs at the bottom so they are easy to reach.
- Center a dialog only when interaction must be blocked and no alternative action is allowed.
- Show dropdown menus at the touched location.
- Skip confirmation dialogs for low-risk deletions when the content can be recreated or restored easily.
- Do not use pop-ups for lightweight descriptions or trivial feedback.
- Show important pop-ups whenever needed, not only once, except for legal notices.
- Long-press contextual menus in list or grid views should be dropdown-style and titleless.
- For tablet layouts, the guide shows narrower centered dialog widths than on phones.

### Lists

- Use lists for vertically stacked continuous content.
- Keep the primary title to one line.
- Secondary text can be longer.
- Use subheaders when grouped items need separation.
- For content like email or messages, show the total count at the bottom.

### Search

- Provide search for large content collections.
- Show suggestions from recent terms or frequently used conditions before the user types.
- Support autocomplete to improve perceived speed and result quality.

### Progress indicator

- Use a progress bar when duration and progress are known.
- Use a progress circle when completion time is unknown.
- Prefer isolated progress in the app bar, content area, or tapped button.
- Avoid covering the whole screen with progress pop-ups.
- If an action leads to a destination page, load the page frame first and show progress inside the updating content.
- If the action affects the current screen, show progress on the tapped button when possible.
- Use the tapped action button itself as the progress container when that is the least disruptive option.

### First-time use

- Use a welcome page for brief app explanations or legal notices.
- Use a loading page if first-run loading takes time.
- Use a no-items page when empty states need explanation and a shortcut to create the first item.

### Label toast

- Use for icon-only or otherwise ambiguous controls that need clarification on tap-and-hold.
- It can also be used for controls whose text must stay fixed because of space limits.
- Dismiss after a short time or when the user touches elsewhere.
- If the user taps outside the toast, execute the action for that touched area immediately.
- Do not use if tap-and-hold already performs a more important app action.
- Do not use it for indicators without actions or for ordinary text-only buttons.

### Action toast

- Use action toast for quick follow-up actions related to the toast content.
- Let it disappear automatically like a toast.
- Provide at most two actions.
- Do not use actions like Dismiss, Close, Done, or OK as the main value.
- Think of it as lighter and more transient than a snackbar.

### Navigation bar

- Choose opaque, translucent, or transparent based on the app design.
- Transparent and translucent navigation bars are not driven by theme or background in the same way as opaque bars.
- In the guide's examples, the navigation bar stays black for 16:9 aspect-ratio cases.

### Edit mode

- Use edit mode when changes are not saved live and the user can confirm or cancel.
- On phone portrait, place confirmation actions at the bottom.
- On phone landscape, move confirmation actions to the top so they do not steal body space.
- When a keyboard is open, place confirmation actions above the keyboard.
- On tablet portrait, let create and compose fill the screen.
- On tablet landscape, present create and compose as centered overlay windows.
- Tapping outside a tablet overlay should behave like Back.
- Dim irrelevant areas behind the tablet overlay.
- Keep edit and display layouts visually similar where practical.
- In split view, keep the edit experience in edit view rather than inventing a different interaction model.

### Selection control

- Enter select mode through Edit or long-press.
- Do not show different contextual menus before select mode starts.
- Once in select mode, switch the app bar and toolbar to selection behavior.
- Show the number of selected items in the app bar.
- Use the app-bar checkbox or radio control for select all.
- If select mode starts from long-press, wait until the finger lifts before showing the toolbar.
- Hide the toolbar while the user is continuously selecting through scrolling, then show it again after the finger lifts.
- Do not show the toolbar when no items are selected.
- Keep list layout stable when search is used in select mode.

## Visual design (guide pages 58-66)

### Icons

- Use clear metaphors that users can recognize instantly.
- Keep shapes minimal, modular, and reusable across the icon set.
- Use common building blocks so the set feels related.
- Use rounded stroke terminals to match One UI softness.
- Keep stroke corners sharp enough to preserve contrast and detail.
- Choose icon colors that express the app character, but keep the app palette and icon tones distinct.

### Color

- Use a categorized palette so color changes propagate consistently across related UI elements.
- The guide's example palette uses One UI blue as the primary accent family, including values such as `#0381fe` and darker or active variants for light and dark themes.
- Apply color based on semantic meaning, not decoration alone.
- Consider cross-cultural meaning when choosing colors for warning, safety, or status.

### Typography

- Use title case for titles, subheaders, text-only buttons, and tabs.
- The guide uses Roboto as the default typeface.
- Design for scalable type rather than a fixed text size.
- Avoid all-caps UI labels unless there is a very strong reason outside the guide.

### Thumbnail radius

- Use large rounded rectangles for focus blocks and thumbnails.
- The guide shows radius values including 26dp, 20dp, and 12dp depending on grid and target.
- Pick the radius that preserves a soft, consistent One UI feel for the screen density and component size.

## Motion and interaction (guide pages 68-82)

### Intuitive

- Use motion to explain structure and next action.
- Drill-in list screens should rise from the bottom and retreat upward when going back.
- Horizontal app-to-app switching should feel lateral.
- Dialogs should appear from the bottom and dismiss downward.

### Seamless

- Preserve continuity between states.
- Let app icons expand smoothly into app screens while preserving corner logic.
- Make expandable app bars react directly to scroll movement.
- Keep shared elements visible across transitions when possible.
- When switching between apps or app states, continuity should feel preserved rather than reset.

### Tangible

- Make controls respond like they are attached to the user’s fingertip.
- Sliders can enlarge while touched for finer control.
- Dragged content should feel stuck to the finger and reveal related context naturally.

## Auditory design (guide pages 80-82)

- Use sounds consistently so users learn their meaning.
- Use positive sound feedback when a goal is completed.
- Avoid repetitive sounds that become annoying.
- If sound is important, consider visual or vibration reinforcement as well.

## Accessibility (guide pages 84-92)

### Principles

- The guide frames accessibility around consideration, comprehensiveness, coherence, and co-creation.
- Aim for equal access rather than a separate experience.
- Samsung explicitly aligns the guidance with WCAG principles.

### Vision

- Allow text to resize up to 200 percent without loss of content or function.
- Do not rely on color alone to communicate state or action.
- Target at least 4.5:1 contrast for normal text.
- Target at least 3:1 for large text.
- Show button shapes clearly so buttons are recognizable even without color cues.

### Hearing

- Pair important sounds with visual or vibration feedback.
- Support options like left-right balance and mono audio when relevant to the experience.

### Interaction and dexterity

- Provide alternative ways to complete complex actions such as drag.
- Avoid requiring difficult gestures when a simpler control will do.
- Support assistive interaction patterns and submenu-based alternatives where appropriate.

### Accessibility checklist distilled from the guide

- Provide alternate text for non-text content, including abbreviations, badges, emoji-like media, and charts or tables when selected.
- Keep voice guidance concise, specific, and differentiated when similar controls appear on the same screen.
- Expose ongoing work, changed state, and dynamically updated content to assistive technology.
- Ensure focus order is sequential, intuitive, and grouped where it helps the user understand similar elements.
- Do not focus decorative elements or irrelevant supporting imagery.
- Help the user understand where focus currently is.
- Prevent controls from hiding automatically when the user still needs them.
- Provide an alternative to complex gestures such as drag.
- Do not rely on shape, location, direction, color, or sound alone for instructions.
- Provide notifications in at least two channels among screen, sound, and vibration.
- Help prevent typing errors.
- Avoid auto-playing background music.
- Ensure unintended transitions or events still make sense to the user.
- Make components recognizable through assistive technologies.
- Provide subtitles, transcripts, sign language, or equivalent support for multimedia when relevant.
- Keep interface components placed consistently.
- Give users control over time-limited content and automatically changing content.

## Quick audit checklist

- Does the screen clearly separate viewing content from the touch-heavy interaction area?
- Is the screen depth correct, with a larger entry experience and a more compact deeper-state experience?
- Are the highest-priority actions close to the thumb on phones?
- Are app bar actions limited, prioritized, and resilient to long text or localization?
- Does the layout still work with dark mode, larger fonts, and different window sizes?
- Are bottom tabs stable, visible, and able to fit at default font size?
- Are progress states inline and minimally disruptive?
- Are dialogs, toasts, and edit/select states using the Samsung-specific behavior rather than generic Android defaults?
- Does the visual system feel soft and restrained instead of layered and noisy?
- Can the screen be understood and operated without depending on color, sound, or precise gestures alone?

## Section map

- Overview: guide page 4
- Architecture: guide pages 6-14
- Components: guide pages 16-56
- Visual design: guide pages 58-66
- Motion and interaction: guide pages 68-79
- Auditory design: guide pages 80-82
- Accessibility: guide pages 84-92
