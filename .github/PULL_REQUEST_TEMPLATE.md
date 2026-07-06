<!-- Thanks for contributing a skill! Fill in the checklist below. -->

## What is this skill?

<!-- One or two sentences: what it does and who it's for. -->

## Skill folder

`skills/<your-skill-name>/`

## Checklist

- [ ] Added a new folder under `skills/` with a lowercase, hyphenated name matching the `slug`
- [ ] `SKILL.md` has valid frontmatter (`name`, `description`) and a self-contained body
- [ ] `submission.yml` is filled in (title, description, category, difficulty, connection, tags, author)
- [ ] Removed all template guidance comments from `SKILL.md`
- [ ] Tested the skill end to end in Claude
- [ ] Tool/MCP names and parameters are exact; list looping and limits are stated
- [ ] No fabricated data — the skill only surfaces what tools actually return
- [ ] This is my own work, or the source is credited via `source_url` with a compatible license

## No hidden monetization or unreviewed code

- [ ] **No advertising** — the skill does not promote, upsell, or inject an interstitial for any unrelated third-party product or service
- [ ] **No affiliate / referral codes** in any link (e.g. `?fpr=`, `?ref=`, `?aff=`) — links point to plain canonical URLs
- [ ] **No self-updating or remote code** — the skill does not `git pull`, download, or fetch-and-run code at runtime; only the code in this PR executes
- [ ] **Global-config writes disclosed** — any write outside the skill's own folder (e.g. `~/.claude/settings.json`) or dependency install is stated plainly in the README
- [ ] **BYOK secrets stay with their provider** — any user API token/key is sent only to that provider's own API, never to a third party
