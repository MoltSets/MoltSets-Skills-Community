# Contributing

Thanks for taking the time to contribute! 🎉 This repo is the community home for **Claude Skills** that work with [MoltSets](https://app.moltsets.com) and the wider B2B / SEO / GTM stack. Accepted skills are published to the [MoltSets Skills Library](https://library.moltsets.com) with credit to you.

You don't need to be an expert to contribute. If you've built a skill that saves you time, someone else probably wants it too.

## Table of contents

1. [Getting started](#getting-started)
2. [Ways to contribute](#ways-to-contribute)
3. [Submitting a skill](#submitting-a-skill)
4. [Quality bar](#quality-bar)
5. [Pull requests](#pull-requests)
6. [Issues](#issues)
7. [Code of conduct](#code-of-conduct)
8. [License](#license)

## Getting started

- Read the [Code of Conduct](./CODE_OF_CONDUCT.md) first.
- New to Claude Skills? A skill is a `SKILL.md` file with a short YAML frontmatter (`name`, `description`) and a markdown body of instructions Claude follows. See [Anthropic's skills docs](https://docs.claude.com/en/docs/claude-code/skills) for the format.
- Browse the [live library](https://library.moltsets.com) and the existing skills in this repo to get a feel for the house style before you write your own.

## Ways to contribute

- **Submit a new skill** — the main event. See [Submitting a skill](#submitting-a-skill).
- **Improve an existing skill** — fix a bug, tighten the instructions, correct an API parameter, add an edge case. Open a PR against that skill's folder.
- **Report a problem** — a skill that doesn't work, an outdated tool reference, a broken link. Open an [issue](#issues).

For anything bigger than a small fix, open an issue or a [GitHub Discussion](../../discussions) first so we can agree on the approach before you spend time on it.

## Submitting a skill

Each skill lives in its own folder under `skills/`:

```
skills/
└── your-skill-name/
    ├── SKILL.md         # the skill Claude loads (frontmatter + instructions)
    └── submission.yml   # metadata used to publish it in the library
```

1. **Fork** this repo and create a branch: `git checkout -b skill/your-skill-name`.
2. **Copy the template:** `cp -r skills/_template skills/your-skill-name`.
3. **Write `SKILL.md`.** Fill in the frontmatter and body. Keep it self-contained — a fresh Claude session with no other context should be able to follow it. Delete the guidance comments.
4. **Fill in `submission.yml`.** Title, description, category, difficulty, connection(s), tags, example prompts, and author details. Allowed values are documented inline in the file.
5. **Use a lowercase, hyphenated folder name** that matches the `slug` in `submission.yml`.
6. **Open a pull request.** Fill in the PR template checklist.

> Don't edit the site itself — this repo feeds the library; a maintainer handles publishing. Just add your `skills/<slug>/` folder.

## Quality bar

Skills are reviewed before publishing. To get merged quickly:

- **It actually works.** Test the skill in Claude end to end before submitting.
- **Triggers are clear.** The `description` and a `## Triggers` section should make it obvious when Claude should (and shouldn't) use the skill.
- **Tool calls are correct.** Use exact tool/MCP names and exact parameter names. If a skill loops over a list, say so and note any per-call limits.
- **No fabricated data.** Skills must only surface what a tool actually returns — never invent emails, numbers, metrics, or page content.
- **Self-contained.** No reliance on hidden context, private files, or another skill being loaded (link to prerequisite skills instead).
- **Honest scope.** Don't claim capabilities the underlying tools don't have.
- **Safe.** No destructive actions, scraping that violates a provider's terms, or handling of personal data beyond the stated purpose.
- **Original or attributed.** Submit your own work, or credit the source via `source_url` and confirm the license allows redistribution.

## Pull requests

- Keep one skill per pull request where possible — it's faster to review.
- Reference any related issue (`Closes #123`).
- Fill in the [pull request template](./.github/PULL_REQUEST_TEMPLATE.md) checklist.
- A maintainer will review for the quality bar above, may suggest edits, and will handle publishing to the library once merged.
- Be patient and responsive to review comments — most skills need a small round of tweaks before they ship.

## Issues

- Search [existing issues](../../issues) first to avoid duplicates.
- For a broken skill, include: which skill, what you asked Claude, what happened vs. what you expected, and any tool errors (quoted exactly).
- For a new-skill idea you don't want to build yourself, open an issue describing the outcome and who it helps.

## Code of conduct

This project follows a [Code of Conduct](./CODE_OF_CONDUCT.md). By participating, you agree to uphold it. Be kind.

## License

Unless a skill states otherwise in its `submission.yml`, contributions are released under the repo's [MIT license](./LICENSE). By submitting, you confirm you have the right to contribute the work under that license.
