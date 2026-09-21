---
name: Photo Style Transfer Poster
description: >-
  Use when the user wants a style-transfer image from one photo: deliver the
  styled reconstruction only (same moment and space). Match source
  resolution/aspect (4:3 only if source near 4:3). Keep every important
  subject fully in frame with safe margin (people, animals, key props). Lock
  spatial structure (road axis, lamp/light, pedestrian groups, depth, relative
  positions) — medium change only. See poster_demo1/poster_demo2 failure
  atlas in the pack. Nine recipes; recommend from photo/vibe — offer recipe
  names, not numbers. Load CORE.md by default; open ATLAS.md or one
  recipes/*.md card on demand — do not ingest the full manual unless
  reviewing a failure.
---

# Photo Style Transfer Poster

> **Pack demos (required reading when available):**  
> `aesthetic-atelier/demo/poster_demo1/` — coastal / street-memory batch (`raw.jpg` + `style-01`…`style-09`)  
> `aesthetic-atelier/demo/poster_demo2/` — valley back-view batch (`raw.jpg` + `style-01`…`style-09`)  
> Use demos as regression memory for **complete subjects** and **spatial fidelity** — the two axes this skill exists to protect.  
> Per-file roles (`source` / `gold` / `dialect-ref` / `working-attempt` / `fail-example`) are authoritative in `aesthetic-atelier/demo/MANIFEST.md`.

This skill is the specialty path under High Aesthetic Image Expert for **photo → styled reconstruction**. The manual is **layered**: `CORE.md` carries the law, `recipes/` carries one card at a time, `ATLAS.md` carries the failure atlas. Read the hard locks, inventory subjects + spatial map, then generate.

**Activation:** user says style transfer / `风格迁移` / named recipe / clear vibe synonym.

Parent: **[High Aesthetic Image Expert](sand-workflow:high-aesthetic-image-expert)** — folder name `high-aesthetic-image-expert`, which is the slug.

## Loading protocol (mandatory)

Default context budget for this skill is **CORE only**. Do not ingest the whole manual.

1. **Always load:** this `SKILL.md` + `CORE.md`.
2. **After a recipe is chosen:** load **exactly one** file under `recipes/`. Never preload all nine cards.
3. **Load `ATLAS.md` only when:**
   - the user says the style, space, or crop is wrong, or
   - self-review fails subjects / space, or
   - you are about to regenerate after a failed attempt.
4. Never preload the sibling specialty skill in full.

## Where everything lives

| File | Contents |
|---|---|
| `CORE.md` | Goal · both hard locks · shared hard rules · recipe choice · **§6c aspect SOP** · **§6d prompt skeleton** · workflow · self-review · doctrine |
| `recipes/01-riso.md` … `recipes/09-ink-sketch.md` | One full recipe card each — **load one at a time** |
| `ATLAS.md` | Demo atlas · F1–F7 failure atlas · per-recipe risk table |

Section numbers (`§1.1a`, `§6c`, …) are kept from the original single-file manual so cross-references stay valid.
