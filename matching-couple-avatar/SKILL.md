---
name: Matching Couple Avatar
description: >-
  Use when the user asks for a separate pairing avatar that matches their given
  portrait (couple set / matching PFPs / 情侣头像): leave their image unchanged;
  generate one independent partner with strong source reference, pixel-level
  local locks; **禁止** starting generation from coarse labels alone; Chinese 对子
  complementarity (complementary mate, not mirror copy), locked spatial/face/brightness/tone/line grammar, and co-framed
  background — see avatar_demo failure atlas in the pack. Load CORE.md by
  default; open ATLAS.md or STUDY.md on demand — do not ingest the full manual
  unless reviewing a failure.
---

# Matching Couple Avatar

> **Pack demos (required reading when available):**  
> `aesthetic-atelier/demo/avatar_demo/`  
> Files: `1L`/`1R`/`1L_gen`, `2L`/`2R`/`2L_gen`, `3L`/`3R`/`3L_gen`, `4L`/`4R`/`4L_gen`  
> (`L`/`R` are **set IDs**, not “left/right of frame”. Facing direction is read from pixels.)  
> Per-file roles (`source` / `gold` / `working-attempt`) are authoritative in `aesthetic-atelier/demo/MANIFEST.md`. A `*_gen` file is a **working-attempt**, never a style oracle.

This skill is the specialty path under High Aesthetic Image Expert for **couple / matching PFPs / 情侣头像**. The manual is **layered**: `CORE.md` carries the law, `STUDY.md` carries the measurement protocol, `ATLAS.md` carries the failure atlas, `APPENDIX.md` carries templates and operator notes. Read the hard locks, run the study protocol, then generate. Build a measured, reference-anchored brief before any one-line prompt.

## Loading protocol (mandatory)

Default context budget for this skill is **CORE only**. Do not ingest the whole manual.

1. **Always load:** this `SKILL.md` + `CORE.md`.
2. **No recipe cards** — this skill has one procedure, not a menu of styles.
3. **Load `ATLAS.md` only when:**
   - the user says the style, couple logic, or space is wrong, or
   - self-review fails identity / couplet / spatial / stroke, or
   - you are about to regenerate after a failed attempt.
4. **Load `STUDY.md` only when** CORE locks are insufficient to write actual measurements.
5. Never preload the sibling specialty skill in full.

## Where everything lives

| File | Contents |
|---|---|
| `CORE.md` | Goal · hard locks §1 · 对子 §2 · co-framed background §3 · explore §5 · generate §6 · self-review §7 · refinement loop §9 · intake §10 · doctrine §28 · minimal viable run §30 · out of scope §32 |
| `STUDY.md` | Study protocol §4 · deep-dive reading §15 · stroke cookbook §17 · spatial engineering §18 · background engineering §19 · pre-flight script §24 |
| `ATLAS.md` | Demo atlas §8 + failure atlas F1–F8 · worked failure→fix stories §20 · complaint→action map §25 |
| `APPENDIX.md` | Prompt skeleton §12 · quick acceptance §13 · glossary §14 · 对子 workshop §16 · batch mode §21 · QA sheet §22 · agent integration §23 · appendices E/F §26–§27 · operator addendum §29 · extended notes §31 |

Section numbers (`§1.1a`, `§6.3`, …) are kept from the original single-file manual so cross-references stay valid.
