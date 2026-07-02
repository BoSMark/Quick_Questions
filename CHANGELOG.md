# Changelog

All notable changes to Quick Questions are documented here.

---

## v1.2 — 2026-07-02

**Added**
- `why-oh-why` — new Quick Question skill. Conversational laddering diagnostic: takes any stated want and asks "why" repeatedly to surface the root driver underneath it, producing a WhyOhWhy Brief (stated want, the ladder, the bedrock, the gap). Added to README's Available Questions table.

**Fixed**
- `why-oh-why/SKILL.md` frontmatter had a duplicated/malformed `description` field (the full YAML block was nested inside the description string). Corrected to a plain `name` / `description` pair matching the other four skills.

---

## v1.1 — 2026-07-01

**Added**
- The two standing principle blocks — "Fix the System, Not Just the Symptom" (Kaizen/systemic-thinking framing) and "BoS Talk Library" (pointer to businessofsoftware.org/talks/ as a reference source) — added to the three skills that didn't have them yet:
  - `founder-alignment/SKILL.md`
  - `founder-replaceability-check/SKILL.md`
  - `ai-readiness-check/SKILL.md`
- `your-next-hire` already shipped with both blocks in v1.0 (PR #1); this release brings the other three up to the same standard.

**Note**
- Content is based on what's actually live on `main` for each skill, not on any locally-cached/installed copy — a check before this release found the local Cowork skill cache had diverged from GitHub in places (an older placeholder link in `founder-alignment`, an unreviewed longer draft of `founder-replaceability-check`, and a duplicate-frontmatter artifact in `ai-readiness-check` that only existed locally, not on GitHub). None of that divergence is carried into this release — each file here is GitHub's current content plus the two blocks, nothing else changed.

## v1.0 — 2026-07-01

- Initial four-skill set: Founder Alignment Check, Founder Replaceability Check, AI Readiness Check, Your Next Hire (PR #1).
