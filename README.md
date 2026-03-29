# Devthinks Skills

Installable agent skills packaged for the `skills` CLI.

This repository is maintained by Devthinks at [devthinks.com](https://devthinks.com) and published by `geekynasir`. The goal is to turn deep product and design guidance into practical agent skills that other teams can install and reuse.

## Included skills

- `samsung-one-ui`: A Devthinks skill that distills Samsung's official One UI design guidance into practical rules for Android, React Native, and UX audits.

## Why this exists

The Samsung One UI guide is strong, but it is easier to use in day-to-day product work when its patterns are distilled into repeatable prompts and review rules. This repository packages that work so other teams can install the skill directly from GitHub instead of rebuilding the same guidance from scratch.

## Repository layout

This repository uses the standard `skills/` layout that `skills.sh` can discover from a GitHub repo:

```text
skills/
  samsung-one-ui/
    SKILL.md
    agents/openai.yaml
    references/one-ui-guide.md
```

## Install with skills CLI

After pushing this repo to GitHub, replace `OWNER/REPO` below with your actual repository path:

```bash
npx skills add OWNER/REPO --list
npx skills add OWNER/REPO --skill samsung-one-ui
```

You can also test the repository locally before pushing:

```bash
npx skills add . --list
npx skills add . --skill samsung-one-ui
```

## Notes

- The installable skill lives in [skills/samsung-one-ui](skills/samsung-one-ui).
- `SKILL.md` contains the activation instructions.
- `references/one-ui-guide.md` contains the distilled guidance derived from Samsung's official One UI design document.
- `agents/openai.yaml` provides optional UI metadata for compatible tools.
