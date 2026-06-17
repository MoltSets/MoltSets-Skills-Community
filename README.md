# MoltSets Skills Community

Community-submitted [Claude Skills](https://docs.claude.com/en/docs/claude-code/skills) for [MoltSets](https://app.moltsets.com) and the wider B2B / SEO / GTM stack — identity resolution, enrichment, prospecting, SEO/AEO, and more. Accepted skills are published to the [MoltSets Skills Library](https://library.moltsets.com) with credit to you.

## What's a skill?

A skill is a `SKILL.md` file — a short YAML frontmatter (`name`, `description`) plus a markdown body of instructions Claude follows. It teaches Claude to do one job well: when to act, which tools to call, and what to return. Download a skill, drop it into Claude via **Settings → Skills**, and prompt away.

## Use a skill

1. Browse the [library](https://library.moltsets.com) or the [`skills/`](./skills) folder here.
2. Download the skill's `SKILL.md`.
3. In Claude, go to **Settings → Skills → Add skill** and select the file.
4. Open a new chat and use one of the skill's example prompts.

## Contribute a skill

Built something useful? Share it.

1. Fork this repo.
2. Copy the template: `cp -r skills/_template skills/your-skill-name`.
3. Fill in `SKILL.md` (the skill) and `submission.yml` (library metadata).
4. Open a pull request.

Full guidelines, the quality bar, and field reference are in **[CONTRIBUTING.md](./CONTRIBUTING.md)**.

## Repo structure

```
.
├── CONTRIBUTING.md            # how to contribute + quality bar
├── CODE_OF_CONDUCT.md
├── LICENSE                    # MIT
├── .github/
│   └── PULL_REQUEST_TEMPLATE.md
└── skills/
    ├── _template/             # copy this to start a new skill
    │   ├── SKILL.md           # the skill Claude loads
    │   └── submission.yml     # title, category, difficulty, connection, author…
    └── your-skill-name/       # one folder per submitted skill
```

## Links

- 🗂️ [MoltSets Skills Library](https://library.moltsets.com) — browse published skills
- 🚀 [MoltSets](https://app.moltsets.com) — people data API & MCP (get started free)
- 📚 [Developer docs](https://developer.moltsets.com) — API reference + MCP setup
- 💬 [Discussions](../../discussions) · [Issues](../../issues)

## License

[MIT](./LICENSE). By submitting a skill you confirm you have the right to contribute it under that license (or the license noted in its `submission.yml`).
