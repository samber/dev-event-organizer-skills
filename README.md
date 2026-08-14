# Skills for tech event organizers

**Technical event operations**: conferences, meetups, hackathons, and the community programs around them.

Written for **event organizers, conference producers, hackathon leads, and community builders**, covering strategy through day-of production. Every skill is **tool-agnostic**: it teaches the decision, not one vendor's ticketing console.

## Install

Install every skill in this repo, not just one. Skills here are atomic by design and reference each other freely — picking a single skill leaves its sibling skills uninstalled, so cross-references and routed handoffs go nowhere.

**skills.sh (universal)** — works with any Agent Skills-compatible tool:

```bash
npx skills add samber/dev-event-organizer-skills
```

**Claude Code** — install the plugin:

```bash
/plugin marketplace add samber/cc
/plugin install dev-event-organizer-skills@samber
```

**Codex (OpenAI)** — install via the Codex CLI:

```bash
codex plugin add github:samber/dev-event-organizer-skills
```

**Cursor** — copy into Cursor's skills directory:

```bash
git clone https://github.com/samber/dev-event-organizer-skills.git ~/.cursor/skills/dev-event-organizer-skills
```

Cursor auto-discovers skills from `.agents/skills/` and `.cursor/skills/`.

**Gemini CLI** — install as a Gemini extension:

```bash
gemini extensions install https://github.com/samber/dev-event-organizer-skills
```

Update with `gemini extensions update dev-event-organizer-skills`.

## 📚 Related Collections

- [`developer-relations-skills`](https://github.com/samber/developer-relations-skills) — DevRel strategy & execution — _for developer advocates, DevRel managers, community managers_
- [`developer-platform-skills`](https://github.com/samber/developer-platform-skills) — Platform & SDK developer experience — _for platform engineers, DX engineers, SDK authors, API product managers, DevRel engineers_

_Part of the [samber skills ecosystem](https://github.com/samber?tab=repositories&q=skills)_

## 📦 Skills

This collection covers the full event-organizing surface. Start here:

- [`dev-event-kickoff`](./dev-event-kickoff) — Routes any event-organizing task to exactly one skill in this collection, or names the gap when none fits.
- [`event-team-structure`](./event-team-structure) — Designs the standing organizing team between editions: legal entity, decision rights, roles, succession, burnout guardrails, and the first paid hire.

Browse all skills and their descriptions in [`references/skill-catalog.md`](./references/skill-catalog.md).

## 📄 License

MIT © 2026 Samuel Berthe

---
