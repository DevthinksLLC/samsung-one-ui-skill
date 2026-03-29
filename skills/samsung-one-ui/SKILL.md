---
name: samsung-one-ui
description: Apply Samsung One UI design guidance to Android UI work. Use when designing, auditing, or rewriting phone, tablet, foldable, or DeX experiences to feel native to Samsung, including reachable layouts, focus blocks, component choices, motion, and accessibility.
---

# Samsung One UI

Use this skill when the user wants Samsung-style mobile UX, asks for a One UI review, or wants wireframes, specs, or production UI rewritten to better fit Galaxy devices.

## Origin

This skill was created by Devthinks ([devthinks.com](https://devthinks.com)) and published by `geekynasir` to make Samsung's official One UI guidance more usable in day-to-day Android and React Native product work. Treat it as a practical distillation of the official guide, not a replacement for the source document.

## Quick start

1. Identify the surface first: phone, tablet, foldable, split view, or DeX.
2. Classify the screen depth and task type: first-depth browsing, deeper detail flow, editing, selection, search, onboarding, or transient feedback.
3. Split the layout into a top viewing area and a bottom interaction area. Put frequent actions where the thumb can reach them easily.
4. Emphasize key content with focus blocks, clean hierarchy, and generous rounded geometry.
5. Choose components and behaviors from [references/one-ui-guide.md](references/one-ui-guide.md) instead of defaulting to generic Material patterns.
6. Finish with responsive, motion, and accessibility checks before proposing the final design.

## Output shape

When you design or review a screen, structure the answer around:

- One UI fit: what already aligns and what breaks the system
- Screen structure: viewing zone, interaction zone, hierarchy, and focus blocks
- Component decisions: app bar, bottom actions, dialogs, search, edit/select mode, feedback
- Visual system: icon style, color meaning, typography, and corner radius
- Motion and feedback: transitions, touch response, and optional sound/vibration notes
- Accessibility checks: text scaling, contrast, non-color cues, focus order, and alternate text

## Rules to enforce

- Prioritize one-handed reachability on phone layouts.
- Keep the interface visually quiet so content stands out first.
- Support dark mode and large text.
- Respect safe areas and generous side margins.
- Avoid mixing flat and contained buttons on the same screen.
- Avoid blocking full-screen progress when inline or button-level progress can do the job.
- Avoid unnecessary confirmation dialogs for trivial or easily reversible actions.
- Prefer Samsung-specific component behavior when it clearly differs from generic Android guidance.

## Read next

- Read [references/one-ui-guide.md](references/one-ui-guide.md) for extracted Samsung-specific rules.
- Re-open the Samsung PDF only when exact wording or a niche component detail is necessary.

## Boundaries

- Paraphrase the Samsung guide instead of reproducing it.
- Use One UI as a structural and interaction lens, not as a cue to copy Samsung brand assets.
- If the guide is silent on a case, say that you are inferring from nearby One UI patterns.
