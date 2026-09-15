# Changelog

All notable changes to Quick Questions are documented here.

---

## v1.2 (founder-alignment) — retroactive catch-up entry, added 2026-09-03

`founder-alignment` (originally tracked locally as `founder-alignment-check`) shipped to live `main` as frontmatter `version: 1.2` with no CHANGELOG entry, Plan doc, or session record anywhere — discovered only when this session verified live GitHub state against BoS OS's local tracking while working RL-229. Per Jo, 2026-09-03: doesn't matter how it happened, fix the record and move on. This entry exists so the gap in this file doesn't repeat itself.

**What changed (inferred from the live file itself, not from any original release note, since none exists):**
- Renamed `founder-alignment-check` → `founder-alignment` (dropped "-check" — now consistent with `your-next-hire`, `why-oh-why`, `ceo-interview-prep`, none of which use the suffix either).
- Rearchitected as a pre-Bootstrap intake: new persona ("Al," not "BoSOS"), produces a "Founder Alignment Brief" that Bootstrap consumes directly and skips its own opening questions for, hands off into Bootstrap in the same session rather than pointing to a GitHub install link.
- `metadata: authors: Mark Littlewood and Business of Software` added to frontmatter.

**Local tracking reconciled 2026-09-03:** `05_ARTIFACTS/Skills/` had two divergent copies — a correctly-content-matching but non-standard-named `founder-alignment/` folder, and a stale, standard-named `founder-alignment-check_v1.1_APPROVED/`. The stale one archived to `_archive/founder-alignment-check_v1.1_APPROVED_SUPERSEDED_2026-09-03/`; the current one renamed to `founder-alignment_v1.2_APPROVED/` to match the naming convention every other skill in this bundle uses. `GitHub_Repos/Quick_Questions/founder-alignment/SKILL.md` (the release-staging mirror) was out of date against live `main` — resynced to match.

**Still open, not fixed by this catch-up entry:**
- `founder-alignment/README.md` still describes the pre-v1.2 flow (a standalone "Founder Brief," no direct Bootstrap handoff) — needs rewriting to match, deferred to whichever session writes RL-229's reply-to-mark CTA into this skill, so it isn't touched twice.
- The packaged `founder-alignment.skill` in the mirror folder was built from the old content and hasn't been rebuilt against this SKILL.md.
- `GitHub_Repos_Registry.md`'s Content line for this repo doesn't mention the v1.2 rearchitecture, and separately omits `ceo-interview-prep` from its skill list entirely — a registry-accuracy gap, not touched here.

---

## Correction, 2026-09-03 (later the same day) — the v1.2 entry above was wrong

The catch-up entry above assumed live GitHub `main` already had the "Al" pre-Bootstrap-intake rearchitecture, based on an earlier session's read of it. A fresh, from-scratch clone of `BoSMark/Quick_Questions` this session (every branch, every PR ref, not just `main`) found that rearchitecture was never live anywhere on GitHub. Real `main`'s `founder-alignment/SKILL.md` still had the original `founder-alignment-check` v1.0.0 content — old persona ("BoSOS"), old "Founder Brief" name, the Go-to/Download/Install handoff block — last touched by PR #10 on 2026-08-12. Where the "Al" content actually came from before it landed in BoS OS's local tracking is still unknown; not investigated further, since it doesn't change what ships next.

Mark's call once this was surfaced: ship the whole thing together — the full rearchitecture and the RL-229 CTA fix, as one real, tracked release, rather than continuing to treat the rearchitecture as a fait accompli. See the v2.0.0 entry below. `founder-alignment_v1.2_APPROVED/` and `founder-alignment_v1.3_APPROVED/` (the latter built on this same wrong assumption, before the correction) are both archived under `05_ARTIFACTS/Skills/_archive/`, kept for the paper trail, not deleted.

---

## PUBLISHED 2026-09-03 — PR #11 merged, commit `ea0838a`

Verified live via a fresh clone: `founder-alignment` shows `version: 2.0.0` with the CTA in place, `your-next-hire`/`why-oh-why` show `1.1`, all three `.skill` packages verified structurally sound (`SKILL.md` at zip root). RL-229 closed. Handed to Jo to load the Drip sequence — see `01_STATE/handoffs/jo/RL229_FounderAlignment_Live_DripLoad_HANDOFF_2026-09-03.md`.

## STAGED, not yet published — 2026-09-03 (superseded by the entry above, kept for the record)

Built and staged locally (`05_ARTIFACTS/GitHub_Repos/Quick_Questions/`, canonical copies in `05_ARTIFACTS/Skills/`). Per `GitHub_Release_Process.md` Tier 3, this is Stage 2 (Build) only — Mark's Plan and Build sign-off, then a PR into `Quick_Questions`, still need to happen before this is live. Not a release entry until that PR merges; left here so the next session sees what's staged.

**your-next-hire → v1.1**
- Handoff (Step 8) now uses the two-branch Bootstrap pattern already live in `founder-replaceability-check` and `ai-readiness-check` ("if you have the BoS OS plugin installed in Cowork, say 'run the Bootstrap skill'; everyone else, go to BoS_OS_Start") instead of a bare Go-to/Download/Install block.
- Fixed a typo: "The BOSSOS Start pack" → correct install-flow wording, no longer a separate line.
- Added a version line (previously had none live on `main`) and an Integration & Hand-offs section (Design Principle 9).

**why-oh-why → v1.1**
- Handoff (Step 8)'s bracketed "[If no BoS OS exists yet...]" placeholder replaced with the actual concrete instruction, matching the two-branch Bootstrap pattern.
- Added a version line (previously had none live on `main`) and an Integration & Hand-offs section (Design Principle 9).

**founder-alignment: v1.0.0 (real, live) → v2.0.0** — the first actual release of the "Al" pre-Bootstrap-intake rearchitecture (new persona, "Founder Alignment Brief" instead of "Founder Brief," direct in-session Bootstrap handoff instead of a Go-to/Download/Install block) plus the RL-229 fix, shipped together per Mark's call once the correction above surfaced (see that entry). MAJOR bump, not a continuation of the internal-only 1.1/1.2/1.3 numbering used while this was mistakenly tracked as already live — the public release starts from the real baseline (1.0.0), and a full interaction-model rearchitecture is a breaking change to what an existing user of the old flow would experience, per this document's own versioning rules.

RL-229 fix: one line added to the Handoff section, after the M1/M2 explanation and before the transition into Bootstrap: "One more thing. This one's from Mark. I'd love to know what you think, and if I can help, drop me a note at mark+bosos@businessofsoftware.org. Thank you." (Mark's own wording, edited live in review to remove an em dash before approval — his voice doesn't use them.) That reply is the trigger event for RL-229 and the only point in the flow that captures an email address, making the founder taggable in the Founder Alignment Check Drip sequence.

Also in this release: a proper `## Integration & Hand-offs` section (Design Principle 9), replacing `## What Bootstrap Receives` — same content, reframed with a Before/After this skill summary to match `your-next-hire`/`why-oh-why`'s sections. `README.md` rewritten: title dropped "Check," "Founder Brief" corrected to "Founder Alignment Brief," removed the stale separate "run Bootstrap yourself" step (handoff is automatic and in-session now), removed an ungrounded "5–10 minute" duration claim (root `README.md`'s skills table now reads "not timed" for this row — a real number needs grounding in something other than an AI guess before it ships), dropped a bold-label-colon opener. One inherited wording fix caught in this pass: "genuinely different angles" → "different angles" (prohibited intensifier). Canonical copy at `05_ARTIFACTS/Skills/founder-alignment_v2.0.0_APPROVED/`; the mistaken v1.2 and v1.3 copies both archived under `05_ARTIFACTS/Skills/_archive/`, not deleted. Mirror `SKILL.md`, `README.md`, and the bundle-level `README.md` all resynced. Still not done: the packaged `founder-alignment.skill` zip (built from the oldest content, not yet rebuilt against this version) — part of Publish, not this step. See `04_MISSIONS/Onboarding_Sequence_Pattern_Founder_Alignment_Check/blocked.md` gate 4.

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
