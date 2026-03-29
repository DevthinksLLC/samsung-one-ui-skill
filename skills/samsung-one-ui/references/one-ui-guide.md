# Samsung One UI Reference

Source: Samsung One UI Design Guidelines PDF  
URL: https://design.samsung.com/global/contents/one-ui/download/oneui_design_guide_eng.pdf

Curated by Devthinks ([devthinks.com](https://devthinks.com)) for reusable agent workflows and published by `geekynasir`. This file distills the official Samsung guide into implementation-ready heuristics for design reviews and UI rewrites.

Use this file when a request needs Samsung-specific layout, component, motion, or accessibility decisions. Keep outputs paraphrased.

## Core intent

- Create a UX that feels consistent with other Samsung mobile apps and devices.
- Reduce learning cost across phones, tablets, foldables, and DeX.
- Make important content easy to see and frequent actions easy to reach.

## Architecture

### Viewing and interaction areas

- Divide phone screens into a top viewing area and a bottom interaction area.
- Put titles and passive content higher on the screen.
- Put frequent actions, tabs, and action-required dialogs lower on the screen.

### Focus blocks

- Use large rounded containers to pull attention to important content.
- Increase contrast between a focus block and the surrounding blank space so the block reads quickly.
- Use focus blocks for cards, lists with media, or any content that benefits from a strong focal point.

### Themes and dark mode

- Support both a default theme and dark mode.
- In dark mode, keep the whole screen darker, including focus blocks, dialogs, and controls.
- Dark themes should reduce glare and work comfortably at night.

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

## Components

### App bar

- Use the app bar to communicate screen context and expose actions.
- Prefer icon actions.
- Keep app bar actions to three or fewer.
- If no actions are available, show no actions.
- Put lower-priority commands into more options.

### Expandable app bar

- Use on list or grid screens where a larger first-depth header improves context.
- Allow it to expand and collapse between discrete states.
- It works well with tabs, search, and scrollable content.
- On later-depth screens, default to collapsed but allow expansion when the view supports it.
- Do not use it on keyboard-heavy screens except for simple input.
- Avoid it when media or user content may be cropped.
- Full-screen landscape phone layouts do not support the expandable app bar.

### Bottom bar

- Use for high-priority actions.
- Allow up to five actions.
- Use icons, text, or a mix of both.
- Do not add overflow menus here.
- Do not make bottom-bar actions horizontally scrollable.

### Bottom navigation

- Use bottom navigation to switch between primary sections.
- Keep tabs visible even while content scrolls.
- Each main tab should own its own view.
- Keep all bottom tabs visible on one screen at default font size whenever possible.
- Use top subtabs for categories on the current screen.
- Make subtabs scrollable when there are five or more.

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

### First-time use

- Use a welcome page for brief app explanations or legal notices.
- Use a loading page if first-run loading takes time.
- Use a no-items page when empty states need explanation and a shortcut to create the first item.

### Label toast

- Use for icon-only or otherwise ambiguous controls that need clarification on tap-and-hold.
- Dismiss after a short time or when the user touches elsewhere.
- Do not use if tap-and-hold already performs a more important app action.

### Action toast

- Use action toast for quick follow-up actions related to the toast content.
- Let it disappear automatically like a toast.
- Provide at most two actions.
- Do not use actions like Dismiss, Close, Done, or OK as the main value.

### Navigation bar

- Choose opaque, translucent, or transparent based on the app design.
- Transparent and translucent navigation bars are not driven by theme or background in the same way as opaque bars.

### Edit mode

- Use edit mode when changes are not saved live and the user can confirm or cancel.
- On phone portrait, place confirmation actions at the bottom.
- On phone landscape, move confirmation actions to the top so they do not steal body space.
- When a keyboard is open, place confirmation actions above the keyboard.
- On tablet portrait, let create and compose fill the screen.
- On tablet landscape, present create and compose as centered overlay windows.
- Tapping outside a tablet overlay should behave like Back.
- Keep edit and display layouts visually similar where practical.

### Selection control

- Enter select mode through Edit or long-press.
- Do not show different contextual menus before select mode starts.
- Once in select mode, switch the app bar and toolbar to selection behavior.
- Show the number of selected items in the app bar.
- Use the app-bar checkbox or radio control for select all.
- If select mode starts from long-press, wait until the finger lifts before showing the toolbar.
- Keep list layout stable when search is used in select mode.

## Visual design

### Icons

- Use clear metaphors that users can recognize instantly.
- Keep shapes minimal, modular, and reusable across the icon set.
- Use common building blocks so the set feels related.
- Use rounded stroke terminals to match One UI softness.
- Keep stroke corners sharp enough to preserve contrast and detail.
- Choose icon colors that express the app character, but keep the app palette and icon tones distinct.

### Color

- Use a categorized palette so color changes propagate consistently across related UI elements.
- The guide shows One UI blue as the primary accent family for many defaults.
- Apply color based on semantic meaning, not decoration alone.
- Consider cross-cultural meaning when choosing colors for warning, safety, or status.

### Typography

- Use title case for titles, subheaders, text-only buttons, and tabs.
- The guide uses Roboto as the default typeface.
- Design for scalable type rather than a fixed text size.

### Thumbnail radius

- Use large rounded rectangles for focus blocks and thumbnails.
- The guide shows radius values including 26dp, 20dp, and 12dp depending on grid and target.
- Pick the radius that preserves a soft, consistent One UI feel for the screen density and component size.

## Motion and interaction

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

### Tangible

- Make controls respond like they are attached to the user’s fingertip.
- Sliders can enlarge while touched for finer control.
- Dragged content should feel stuck to the finger and reveal related context naturally.

## Auditory design

- Use sounds consistently so users learn their meaning.
- Use positive sound feedback when a goal is completed.
- Avoid repetitive sounds that become annoying.
- If sound is important, consider visual or vibration reinforcement as well.

## Accessibility

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

- Provide alternate text for non-text content.
- Keep voice guidance concise and specific.
- Add distinct labels when similar controls would otherwise sound identical.
- Expose state changes and dynamic updates to assistive tech.
- Ensure focus order is sequential and intuitive.
- Do not focus decorative elements.
- Provide multiple notification channels, with at least two of screen, sound, and vibration.
- Prevent typing errors where possible.
- Avoid auto-playing background music.
- Keep component placement consistent.
- Provide subtitles, transcripts, or equivalent support for multimedia.
- Give users control over time-limited or automatically changing content.

## Practical review heuristics

- If a phone screen forces repeated reaches to the upper corners, it is drifting away from One UI.
- If a design uses many competing surfaces, reduce layers and use focus blocks instead.
- If a loading flow blocks the whole screen without need, move progress inline.
- If an action needs explanation, prefer contextual structure first and toast-based help second.
- If accessibility depends on color, sound, or gesture alone, the design is incomplete.
