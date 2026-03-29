---
name: samsung-one-ui
description: Apply Samsung One UI design guidance to Android UI work. Use when designing, auditing, or rewriting phone, tablet, foldable, or DeX experiences to feel native to Samsung, including reachable layouts, focus blocks, component choices, motion, and accessibility.
---

# Samsung One UI

Use this skill when the user wants Samsung-style mobile UX, asks for a One UI review, or wants wireframes, specs, or production UI rewritten to better fit Galaxy devices.

## Origin

This skill was created by Devthinks ([devthinks.com](https://devthinks.com)) and published by `geekynasir` to make Samsung's official One UI guidance more usable in day-to-day Android and React Native product work. Treat it as a practical distillation of the official guide, not a replacement for the source document.

## When to use this skill

- Redesign an Android or React Native screen so it feels closer to Samsung apps.
- Audit a phone, tablet, foldable, or DeX layout against One UI patterns.
- Choose between app bar, bottom bar, bottom navigation, dialog, toast, and edit/select behaviors.
- Review whether a screen respects One UI reachability, hierarchy, motion, and accessibility.

## Workflow

1. Identify the surface first: phone, tablet, foldable, split view, or DeX.
2. Classify the screen depth and task type: first-depth browsing, later-depth detail flow, editing, selection, search, onboarding, or transient feedback.
3. Split the layout into a top viewing area and a bottom interaction area. Put frequent actions where the thumb can reach them easily.
4. Decide the screen hierarchy: expanded vs collapsed app bar, tabs vs actions, focus blocks vs flat lists, inline progress vs blocking dialog.
5. Choose the relevant Samsung component behavior from [references/one-ui-guide.md](references/one-ui-guide.md) instead of defaulting to generic Material assumptions.
6. Apply the visual system: soft rounded geometry, restrained layers, title case labels, semantic color, and scalable typography.
7. Validate edge cases: dark mode, large text, multi-window, foldable/tablet density, and keyboard states.
8. End with an accessibility pass and call out any places where you are inferring beyond the guide.

## Surface and depth defaults

- Phone: optimize for one-handed reachability, especially for frequent actions and confirmation controls.
- Tablet and foldable: support multi-layer layouts, more visible content, and centered overlay edit windows in landscape when appropriate.
- DeX and multi-window: treat them as large-window surfaces and preserve hierarchy across different window heights and orientations.
- First-depth screens: an expanded app bar is often useful for browsable list or grid entry points.
- Second-depth and later screens: default to a collapsed app bar, then allow expansion only when it adds useful context.

## Output shape

When you design or review a screen, structure the answer around:

- One UI fit: what already aligns and what breaks the system
- Screen structure: viewing zone, interaction zone, hierarchy, and focus blocks
- Component decisions: app bar, bottom actions, dialogs, search, edit/select mode, feedback
- Visual system: icon style, color meaning, typography, and corner radius
- Motion and feedback: transitions, touch response, and optional sound/vibration notes
- Accessibility checks: text scaling, contrast, non-color cues, focus order, and alternate text
- Assumptions and inferences: where the guide is explicit vs where you are extrapolating

## Non-negotiables

- Prioritize one-handed reachability on phone layouts.
- Respect screen depth: entry screens can be larger and more expressive; deeper screens should usually become more compact.
- Keep the interface visually quiet so content stands out first.
- Support dark mode and large text.
- Respect safe areas and generous side margins.
- Keep app bar actions to three or fewer and push lower-priority actions into overflow.
- Keep bottom navigation visible, stable, and limited enough to fit at default font size.
- Avoid mixing flat and contained buttons on the same screen.
- Avoid blocking full-screen progress when inline or button-level progress can do the job.
- Avoid unnecessary confirmation dialogs for trivial or easily reversible actions.
- Make buttons recognizable even without color alone.
- Support text resizing up to 200 percent without breaking content or function.
- Prefer Samsung-specific component behavior when it clearly differs from generic Android guidance.

## Read next

- Read [references/one-ui-guide.md](references/one-ui-guide.md) for extracted Samsung-specific rules, page ranges, and a quick audit checklist.
- Re-open the Samsung PDF only when exact wording or a niche component detail is necessary.

## Boundaries

- Paraphrase the Samsung guide instead of reproducing it.
- Use One UI as a structural and interaction lens, not as a cue to copy Samsung brand assets.
- If the guide is silent on a case, say that you are inferring from nearby One UI patterns.
