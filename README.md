# Aesthetic Atelier

![Aesthetic Atelier](demo/repo-hero-poster.jpg)

> High Aesthetic Image Expert · 1 skill + 2 sub-skills  
> Matching Couple Avatar · Photo Style Transfer Poster · restraint, relation-first, whitespace

**English** | [简体中文](README.zh-CN.md)

**One skill — High Aesthetic Image Expert — with two sub-skills**, for high-aesthetic image work. Shipped as `SKILL.md` operator manuals plus the demo image sets that serve as their regression memory.

The pack's voice is **positive locks**: state what to keep and deliver. Emphatic bans appear only where a failure mode recurs in practice.

```
aesthetic-atelier/
├── high-aesthetic-image-expert/SKILL.md      ← the skill
├── matching-couple-avatar/                   ← sub-skill 1
│   ├── SKILL.md          thin entry + loading protocol
│   ├── CORE.md           always loaded — the law
│   ├── STUDY.md          on demand — measurement protocol
│   ├── ATLAS.md          on demand — failure atlas F1–F8
│   └── APPENDIX.md       on demand — templates, operator notes
├── photo-style-transfer-poster/              ← sub-skill 2
│   ├── SKILL.md          thin entry + loading protocol
│   ├── CORE.md           always loaded — the law
│   ├── ATLAS.md          on demand — failure atlas F1–F7
│   └── recipes/          nine cards, load one at a time
└── demo/                                     ← regression image sets
    ├── MANIFEST.md         per-file role — the authority
    ├── avatar_demo/        couple-PFP set (1L–4L)
    ├── poster_demo1/       style-transfer batch A (raw + 9 styles + 9 aspect-matched)
    ├── poster_demo2/       style-transfer batch B (raw + 9 styles + 9 aspect-matched)
    ├── bear.jpg            general-brief example
    └── repo-hero-poster.jpg  README hero banner (promo, not regression material)
```

**Jump to:** [The skills](#the-skills) · [The nine recipes](#the-nine-recipes) · [Demo gallery](#demo-gallery) · [Generation prompts](#generation-prompts) · [Installation](#installation) · [Shared doctrine](#shared-doctrine) · [License](#license)

---

## The skills

**High Aesthetic Image Expert** is an aesthetic image expert, and the entry point for **any** image brief — a realistic photo, an illustration, a mood piece, a poster, a wallpaper, a concept, or a scene that exists only in words. It applies a fixed aesthetic core — restraint, relationship-first composition, color from content, sparse decoration, negative space as design, deconstruct-then-reconstruct, clean delivery — and runs a mandatory self-review before anything ships.

The two sub-skills are **specialised training for two recurring task types** — not the limit of what the skill does:

- **Matching Couple Avatar** takes the user's portrait and draws **one** new partner portrait to pair with it (couple set / matching profile pictures). It is not a two-image batch — the portrait you supply is never redrawn or altered, only the missing half is drawn. Generation is driven by pixel-level locks measured from the source — stroke material, face recipe, palette, background — so the partner reads as the same illustrator's hand with a new identity, and forms couplet-logic complementarity rather than a mirror clone.
- **Photo Style Transfer Poster** turns one photo into one finished styled image of the same moment and space — a styled reconstruction, never the photo itself and never a before/after layout. Two hard locks gate acceptance: every important person, animal, and pose-critical prop stays fully in frame, and the source's spatial structure stays intact. Nine print and illustration recipes are available.

Everything else — every other subject, style, or brief — runs through the expert directly.

### Runtime loading

The manuals are **layered**, so a cold run does not pull ~80 KB into context. Each sub-skill's `SKILL.md` states its own protocol:

- **Always loaded:** that sub-skill's `SKILL.md` + `CORE.md` — goal, hard locks, workflow, self-check.
- **On demand — `ATLAS.md`:** only after a failure or a user complaint, to match an F-code.
- **On demand — `STUDY.md` / `APPENDIX.md`:** only when CORE locks are not enough to write actual measurements.
- **One at a time — `recipes/*.md`:** never preload all nine cards.

The parent skill routes to a sub-skill by loading its `SKILL.md` + `CORE.md` only, never the whole manual.

---

## The nine recipes

| # | Recipe | What it is |
|---|---|---|
| 1 | **RISO Editorial** | Spot-color stencil print with freehand line, misregistration, and warm paper grain. |
| 2 | **Old Newsprint** | Vintage culture-supplement page with halftone hero art and a multi-column layout. |
| 3 | **Paper Theatre** | Layered cut-paper diorama with visible fasteners and paper depth bands. |
| 4 | **Pressed Flower** | Botanical specimen collage that rebuilds the subject from dried petals and leaves. |
| 5 | **Travel Journal Sketch** | Pen and colored-pencil sketch that keeps the exact instant and spatial relations. |
| 6 | **Retro Silkscreen** | High-contrast coarse-halftone print with bold type and granulated color blocks. |
| 7 | **JP B&W Line** | Quiet fineliner black-and-white lifestyle illustration with generous whitespace. |
| 8 | **Naïve Doodle** | Small but fully drawn subjects in massive intentional whitespace. |
| 9 | **Photo→Ink Sketch** | Loose black-and-white ink page of the same subject on warm textured paper. |

**Vibe → recipe**, for briefs that name a mood instead of a style:

| Vibe | Prefer | Also consider |
|---|---|---|
| nostalgia, retro, film, old magazine | Photo→Ink / Old Newsprint / Retro Silkscreen | Travel Journal if travel |
| movie poster, filmic | Photo→Ink / Retro Silkscreen | — |
| literary, indie mag, exhibition poster | RISO Editorial | Naïve Doodle if extreme whitespace |
| newspaper, supplement, intellectual, editorial | Old Newsprint | — |
| handmade, paper craft, fairy theatre, pop-up | Paper Theatre | — |
| pressed flower, specimen, botanical, gentle holiday | Pressed Flower | couples / holiday / botanical |
| travel, sketch, diary, urban plein-air | Travel Journal Sketch | JP B&W Line if quieter B&W |
| avant-garde, silkscreen, experimental print | Retro Silkscreen | RISO if softer |
| healing, JP lifestyle, B&W line, camping street | JP B&W Line | Naïve Doodle if more playful |
| doodle, naïve, large whitespace, less-is-more | Naïve Doodle | RISO if print color still wanted |

When no vibe is given, photo content decides: architecture or street vista → Travel Journal; soft-light portrait → Photo→Ink; couple, holiday, or floral → Pressed Flower; theatrical staging → Paper Theatre; bold graphic face → Retro Silkscreen; quiet daily → JP B&W Line; documentary city memory → Old Newsprint; sparse drawing with smart type → Naïve Doodle.

---

## Demo gallery

Both sub-skills treat these demos as their **regression suite** — reopen them whenever quality slips. See [Generation prompts](#generation-prompts) for input-to-output examples.

**Regression roles:** only `gold` (and `source` as the lock origin) are positive acceptance exemplars. `working-attempt` and `fail-example` exist for **gap analysis** — never copy them as ship targets. The per-file authority is [`demo/MANIFEST.md`](demo/MANIFEST.md).

### Couple avatars — `demo/avatar_demo/`

> **One image in, one image out.** This is not a two-image batch. The portrait you hand over is never redrawn or altered — the skill draws a single new partner avatar to sit opposite it. The usual case is that you only hold one half of the pair: your own portrait, or a photo of a crush, where the other half has to be drawn to match.

`L`/`R` are **set IDs, not "left/right of frame"** — facing direction is read from pixels.

| Set | Source (`nL`) — **`source`** | Approved pair (`nR`) — **`gold`** | Generated partner (`nL_gen`) — **`working-attempt`** |
|:---:|:---:|:---:|:---:|
| 1 | <img src="demo/avatar_demo/1L.jpeg" width="200"> | <img src="demo/avatar_demo/1R.jpeg" width="200"> | <img src="demo/avatar_demo/1L_gen.jpeg" width="200"> |
| 2 | <img src="demo/avatar_demo/2L.jpeg" width="200"> | <img src="demo/avatar_demo/2R.jpeg" width="200"> | <img src="demo/avatar_demo/2L_gen.jpeg" width="200"> |
| 3 | <img src="demo/avatar_demo/3L.jpg" width="200"> | <img src="demo/avatar_demo/3R.jpg" width="200"> | <img src="demo/avatar_demo/3L_gen.jpg" width="200"> |
| 4 | <img src="demo/avatar_demo/4L.jpg" width="200"> | <img src="demo/avatar_demo/4R.jpg" width="200"> | <img src="demo/avatar_demo/4L_gen.jpg" width="200"> |

Study method: open `nL` and lock facing, scale, stroke, face recipe, background, and cast; open `nR` as pair-grammar exemplar; open `nL_gen` as a working attempt; catalogue gaps and regenerate with tighter locks.

**Failure atlas F1–F8:** tag-led stock dialect · spatial collapse (headshot zoom / unsafe square crop) · background abandonment · mirror clone instead of couplet logic · wrong stroke dialect (the silent killer) · proxy-metric chasing · patching a failed base instead of redrawing · clothing-value opposition bleeding into the whole frame.

### Style-transfer batch A — `demo/poster_demo1/`

Coastal / street-memory batch. Practice axis, depth, and full pedestrians.

> **Aspect note:** the gallery shows the **aspect-matched** `*_matched.jpg` versions — letterboxed to this batch's `raw.jpg` aspect (batch A ≈4:3 at 1706×1279, batch B ≈1.51 at 1024×677), so comparing them against the source is apples-to-apples. The `style-01`…`style-09` originals sit alongside them and are **generator-native 1280×720 (16:9)**: `dialect-ref` only, and never a correct deliverable aspect. See `CORE.md §6c`.

**Source** — `demo/poster_demo1/raw.jpg`

<img src="demo/poster_demo1/raw.jpg" width="420">

| ① RISO Editorial | ② Old Newsprint | ③ Paper Theatre |
|:---:|:---:|:---:|
| <img src="demo/poster_demo1/style-01-riso_matched.jpg" width="240"> | <img src="demo/poster_demo1/style-02-newsprint_matched.jpg" width="240"> | <img src="demo/poster_demo1/style-03-paper-theatre_matched.jpg" width="240"> |

| ④ Pressed Flower | ⑤ Travel Journal Sketch | ⑥ Retro Silkscreen |
|:---:|:---:|:---:|
| <img src="demo/poster_demo1/style-04-pressed-flower_matched.jpg" width="240"> | <img src="demo/poster_demo1/style-05-travel-sketch_matched.jpg" width="240"> | <img src="demo/poster_demo1/style-06-silkscreen_matched.jpg" width="240"> |

| ⑦ JP B&W Line | ⑧ Naïve Doodle | ⑨ Photo→Ink Sketch |
|:---:|:---:|:---:|
| <img src="demo/poster_demo1/style-07-jp-line_matched.jpg" width="240"> | <img src="demo/poster_demo1/style-08-naive-doodle_matched.jpg" width="240"> | <img src="demo/poster_demo1/style-09-ink-sketch_matched.jpg" width="240"> |

Regression: open `raw.jpg` vs `style-05` / `style-09` first (highest spatial bar), then the whitespace-heavy recipes for crop risk. The aspect-matched `style-05-travel-sketch_matched.jpg` and `style-09-ink-sketch_matched.jpg` are this batch's **`gold`** spatial anchors. **⑧ Naïve Doodle** here is kept as a `working-attempt` (F6 — pedestrian groups simplified), not a spatial pass.

### Style-transfer batch B — `demo/poster_demo2/`

Valley scene with a **female subject centered, back to camera**, looking toward the valley — a strong test of full figure, depth to valley, and same-place identity.

> **Aspect note:** the gallery shows the **aspect-matched** `*_matched.jpg` versions — letterboxed to this batch's `raw.jpg` aspect (batch A ≈4:3 at 1706×1279, batch B ≈1.51 at 1024×677), so comparing them against the source is apples-to-apples. The `style-01`…`style-09` originals sit alongside them and are **generator-native 1280×720 (16:9)**: `dialect-ref` only, and never a correct deliverable aspect. See `CORE.md §6c`.

**Source** — `demo/poster_demo2/raw.jpg`

<img src="demo/poster_demo2/raw.jpg" width="420">

| ① RISO Editorial | ② Old Newsprint | ③ Paper Theatre |
|:---:|:---:|:---:|
| <img src="demo/poster_demo2/style-01-riso_matched.jpg" width="240"> | <img src="demo/poster_demo2/style-02-newsprint_matched.jpg" width="240"> | <img src="demo/poster_demo2/style-03-paper-theatre_matched.jpg" width="240"> |

| ④ Pressed Flower | ⑤ Travel Journal Sketch | ⑥ Retro Silkscreen |
|:---:|:---:|:---:|
| <img src="demo/poster_demo2/style-04-pressed-flower_matched.jpg" width="240"> | <img src="demo/poster_demo2/style-05-travel-sketch_matched.jpg" width="240"> | <img src="demo/poster_demo2/style-06-silkscreen_matched.jpg" width="240"> |

| ⑦ JP B&W Line | ⑧ Naïve Doodle | ⑨ Photo→Ink Sketch |
|:---:|:---:|:---:|
| <img src="demo/poster_demo2/style-07-jp-line_matched.jpg" width="240"> | <img src="demo/poster_demo2/style-08-naive-doodle_matched.jpg" width="240"> | <img src="demo/poster_demo2/style-09-ink-sketch_matched.jpg" width="240"> |

Regression: confirm the full back-view silhouette (head to hem as in the source) and unchanged valley depth across all nine styles. The aspect-matched `style-05-travel-sketch_matched.jpg` and `style-09-ink-sketch_matched.jpg` are this batch's **`gold`** spatial anchors. **⑧ Naïve Doodle** here is kept as a `fail-example` (F2 — the autumn/winter split rewrites the place identity). It must never be used as a spatial pass.

**Failure atlas F1–F7:** incomplete people after whitespace · element-library spatial rewrite · source photo or comparison layout in frame · forced wrong aspect · type or crop marks cutting anatomy · clutter deletion removing a person · proxy-metric theater.

Recipes ⑤ travel-sketch, ⑦ jp-line, and ⑨ ink are the strictest on **space**; whitespace-heavy ① and ⑧ fail most often on **crops**. Diagnose ⑤⑦⑨ first when a user says the result "disrespects the photo," then ①⑧ for crop risk.

---

## Generation prompts

What the interaction actually looks like. Every example below uses the same three blocks: **Prompt**, then **Input**, then **Output**.

### General brief — a scene from a novel

**Prompt**

> Here's a passage from a novel. I want a beautiful, romantic, literary, high-resolution image of the scene it describes:
>
> "I like you more than anything, Midori."
> "How much?"
> "As much as a bear in spring."
> "A bear in spring?" Midori looks up again. "What kind of bear is that?"
> "You're walking alone through a spring meadow, and a small lovely bear comes toward you — fur like velvet, round button eyes. It says, 'Hello, miss, would you like to roll around with me?' So you hug the bear, and the two of you go tumbling down a hillside of clover and play there the whole day long. Isn't that wonderful?"
> "That's wonderful."
> "That's how much I like you."

**Input** — the passage above (paraphrased); no reference image

**Output** — `demo/bear.jpg`

<img src="demo/bear.jpg" width="520">

### Matching couple avatar

**Prompt**

> Here's an avatar. I want a matching couple avatar for it.

| **Input** — `demo/avatar_demo/3L.jpg` | **Output** — `demo/avatar_demo/3L_gen.jpg` |
|:---:|:---:|
| <img src="demo/avatar_demo/3L.jpg" width="240"> | <img src="demo/avatar_demo/3L_gen.jpg" width="240"> |

The source file is left untouched. The output is a single new portrait, drawn in the same hand and facing the opposite way so the two read as a pair.

### Style transfer — Pressed Flower

**Prompt**

> Here's a photo. I want a pressed-flower style literary poster from it.

| **Input** — `demo/poster_demo2/raw.jpg` | **Output** — `demo/poster_demo2/style-04-pressed-flower_matched.jpg` |
|:---:|:---:|
| <img src="demo/poster_demo2/raw.jpg" width="240"> | <img src="demo/poster_demo2/style-04-pressed-flower_matched.jpg" width="240"> |

Same photo, same moment and space: the subjects stay complete and the layout stays put — only the medium changes. Swap the style name for any of the nine recipes in the table above.

---

## Installation

> **TL;DR — just tell your agent *"install https://github.com/wzj52501/aesthetic-atelier"*.** It clones the pack and links the skills into its own skills directory; Claude Code, Cursor, and Codex each know where theirs is. Everything below is the manual version, for when you want to control exactly where the files land.

Each skill folder is self-contained: the folder name is the skill slug and `SKILL.md` carries YAML frontmatter (`name`, `description`) used for discovery and routing. The format follows the [Agent Skills](https://agentskills.io) standard, so the same folders work across tools.

### 1. Clone the pack

```bash
git clone https://github.com/wzj52501/aesthetic-atelier.git ~/aesthetic-atelier
cd ~/aesthetic-atelier
```

The repository is public, so that is all it takes. SSH works too:

```bash
git clone git@github.com:wzj52501/aesthetic-atelier.git ~/aesthetic-atelier
```

Any directory works — the rest of this guide assumes `~/aesthetic-atelier`.

### 2. Link the skills into your tool

**Claude Code** — personal (all projects) or project-scoped:

```bash
SKILLS=~/.claude/skills          # personal
# SKILLS=.claude/skills          # project-scoped, committed for your team
mkdir -p "$SKILLS"
for s in high-aesthetic-image-expert matching-couple-avatar photo-style-transfer-poster; do
  ln -sfn "$PWD/$s" "$SKILLS/$s"
done
```

Claude Code expects `<skill-name>/SKILL.md` directly under the skills root, then invokes them as `/matching-couple-avatar` and so on. Manual install without symlinks: copy each folder into `~/.claude/skills/`.

**Cursor** — Cursor walks the skills root recursively and takes the skill name from the folder containing `SKILL.md`, so one symlink of the whole pack is enough:

```bash
ln -sfn ~/aesthetic-atelier ~/.cursor/skills/aesthetic-atelier
# or project-scoped:
# ln -sfn ~/aesthetic-atelier .cursor/skills/aesthetic-atelier
```

Cursor reads `.cursor/skills/`, `.agents/skills/`, and their `~/` global equivalents, and also loads skills from `.claude/skills/` and `.codex/skills/` for compatibility. You can also use the built-in `/create-skill` to scaffold your own.

**Codex** — user scope, or `.agents/skills/` inside a repo:

```bash
SKILLS=~/.agents/skills          # user scope
mkdir -p "$SKILLS"
for s in high-aesthetic-image-expert matching-couple-avatar photo-style-transfer-poster; do
  ln -sfn "$PWD/$s" "$SKILLS/$s"
done
```

Codex reads `$CWD/.agents/skills`, `$REPO_ROOT/.agents/skills`, `$HOME/.agents/skills`, and `/etc/codex/skills`, and follows symlinked skill folders. Disable a skill without deleting it via `[[skills.config]]` in `~/.codex/config.toml`.

**Any other Agent Skills tool** — `.agents/skills/` in the project or `~/.agents/skills/` globally is the shared convention read by both Codex and Cursor.

| Tool | Skills root | Discovery |
|---|---|---|
| Claude Code | `~/.claude/skills/` · `.claude/skills/` | `<skill-name>/SKILL.md`; `/skill-name` to invoke |
| Cursor | `~/.cursor/skills/` · `.cursor/skills/` · `.agents/skills/` | recursive — nested category folders work |
| Codex | `~/.agents/skills/` · `.agents/skills/` · `/etc/codex/skills` | symlinked folders followed |
| Generic | `.agents/skills/` | Agent Skills standard |

### 3. Make the demos available (optional)

The sub-skills mark the demos as *required reading when available*. They are referenced by pack-relative paths such as `aesthetic-atelier/demo/avatar_demo/`. Because the demo folders sit next to the skills rather than inside them, tell your agent where the pack lives — for example by adding this to `AGENTS.md` / `CLAUDE.md`:

```markdown
aesthetic-atelier is cloned at ~/aesthetic-atelier.
Demo regression sets: ~/aesthetic-atelier/demo/{avatar_demo,poster_demo1,poster_demo2}
Per-file demo roles: ~/aesthetic-atelier/demo/MANIFEST.md
```

Tools that scan recursively (Cursor) can instead take the single whole-pack symlink shown above, which keeps the documented paths valid as-is.

### 4. Verify

```bash
ls -l ~/.claude/skills/ | grep -E 'aesthetic|couple|poster'
head -12 ~/.claude/skills/matching-couple-avatar/SKILL.md
```

Then ask your agent for an image brief and confirm it loads the skill — the `description` field is what drives automatic selection.

The **Matching Couple Avatar** description also carries Chinese activation terms, so a Chinese-language brief for a matching avatar selects that sub-skill directly. Every other skill in the pack is described in English only.

---

## Shared doctrine

Both sub-skills sit under the same fixed aesthetic core and add their own law. Compressed:

- **Pixel-level locks lead; tags stay subordinate.** A genre label is a summary, not a lock.
- **Subjects and space are the first acceptance gates** — palette and grain come last.
- **Measure, don't vibe** — write face %, luma, aspect, and axis positions into the brief.
- **Redraw under better locks** rather than patching a failed base.
- **Name the failing axis** (stroke / face / space / background / couplet logic) before changing anything.
- **When the user freezes a candidate, stop** — save it as `*_gen` and halt churn.
- **Recommend by name, not by number.**
- **Use the demo atlases as regression memory.**

---

## License

Released under the [MIT License](LICENSE). Copyright (c) 2026 wzj52501.
