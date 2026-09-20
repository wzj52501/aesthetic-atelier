# High Aesthetic Image Skills Pack

**One skill — High Aesthetic Image Expert — with two sub-skills**, for high-aesthetic image work. Shipped as `SKILL.md` operator manuals plus the demo image sets that serve as their regression memory.

The pack's voice is **positive locks**: state what to keep and deliver. Emphatic bans appear only where a failure mode recurs in practice.

```
high-aesthetic-skills-pack/
├── high-aesthetic-image-expert/SKILL.md      ← the skill (92 lines)
├── matching-couple-avatar/SKILL.md           ← sub-skill 1 (996 lines)
├── photo-style-transfer-poster/SKILL.md      ← sub-skill 2 (627 lines)
└── demo/                                     ← regression image sets (32 images)
    ├── avatar_demo/        couple-PFP set (1L–4L)
    ├── poster_demo1/       style-transfer batch A (raw + 9 styles)
    └── poster_demo2/       style-transfer batch B (raw + 9 styles)
```

---

## The skills

**High Aesthetic Image Expert** is the entry point for any image brief. It applies a fixed aesthetic core — restraint, relationship-first composition, color from content, sparse decoration, negative space as design, deconstruct-then-reconstruct, clean delivery — and runs a mandatory self-review before anything ships. Specialty briefs route to the two sub-skills.

**Matching Couple Avatar** takes the user's portrait and delivers one new standalone partner portrait that pairs with it (couple set / matching profile pictures). The source file is never modified. Generation is driven by pixel-level locks measured from the source — stroke material, face recipe, palette, background — so the partner reads as the same illustrator's hand with a new identity, and forms couplet-logic complementarity rather than a mirror clone.

**Photo Style Transfer Poster** turns one photo into one finished styled image of the same moment and space — a styled reconstruction, never the photo itself and never a before/after layout. Two hard locks gate acceptance: every important person, animal, and pose-critical prop stays fully in frame, and the source's spatial structure stays intact. Nine print and illustration recipes are available.

Both sub-skill manuals are deliberately long, and each explains why: short "vibe" skills produce exactly the failures catalogued in the demo atlases below.

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

Both sub-skills treat these demos as their **regression suite** — reopen them whenever quality slips. The generation prompts for every image below are in [Generation prompts](#generation-prompts).

### Couple avatars — `demo/avatar_demo/`

`L`/`R` are **set IDs, not "left/right of frame"** — facing direction is read from pixels.

| Set | Source (`nL`) | Approved pair (`nR`) | Generated partner (`nL_gen`) |
|:---:|:---:|:---:|:---:|
| 1 | <img src="demo/avatar_demo/1L.jpeg" width="200"> | <img src="demo/avatar_demo/1R.jpeg" width="200"> | <img src="demo/avatar_demo/1L_gen.jpeg" width="200"> |
| 2 | <img src="demo/avatar_demo/2L.jpeg" width="200"> | <img src="demo/avatar_demo/2R.jpeg" width="200"> | <img src="demo/avatar_demo/2L_gen.jpeg" width="200"> |
| 3 | <img src="demo/avatar_demo/3L.jpg" width="200"> | <img src="demo/avatar_demo/3R.jpg" width="200"> | <img src="demo/avatar_demo/3L_gen.jpg" width="200"> |
| 4 | <img src="demo/avatar_demo/4L.jpg" width="200"> | <img src="demo/avatar_demo/4R.jpg" width="200"> | <img src="demo/avatar_demo/4L_gen.jpg" width="200"> |

Study method: open `nL` and lock facing, scale, stroke, face recipe, background, and cast; open `nR` as pair-grammar exemplar; open `nL_gen` as a working attempt; catalogue gaps and regenerate with tighter locks.

**Failure atlas F1–F8:** tag-led stock dialect · spatial collapse (headshot zoom / unsafe square crop) · background abandonment · mirror clone instead of couplet logic · wrong stroke dialect (the silent killer) · proxy-metric chasing · patching a failed base instead of redrawing · clothing-value opposition bleeding into the whole frame.

### Style-transfer batch A — `demo/poster_demo1/`

Coastal / street-memory batch. Practice axis, depth, and full pedestrians.

**Source** — `demo/poster_demo1/raw.jpg`

<img src="demo/poster_demo1/raw.jpg" width="420">

| ① RISO Editorial | ② Old Newsprint | ③ Paper Theatre |
|:---:|:---:|:---:|
| <img src="demo/poster_demo1/style-01-riso.jpg" width="240"> | <img src="demo/poster_demo1/style-02-newsprint.jpg" width="240"> | <img src="demo/poster_demo1/style-03-paper-theatre.jpg" width="240"> |

| ④ Pressed Flower | ⑤ Travel Journal Sketch | ⑥ Retro Silkscreen |
|:---:|:---:|:---:|
| <img src="demo/poster_demo1/style-04-pressed-flower.jpg" width="240"> | <img src="demo/poster_demo1/style-05-travel-sketch.jpg" width="240"> | <img src="demo/poster_demo1/style-06-silkscreen.jpg" width="240"> |

| ⑦ JP B&W Line | ⑧ Naïve Doodle | ⑨ Photo→Ink Sketch |
|:---:|:---:|:---:|
| <img src="demo/poster_demo1/style-07-jp-line.jpg" width="240"> | <img src="demo/poster_demo1/style-08-naive-doodle.jpg" width="240"> | <img src="demo/poster_demo1/style-09-ink-sketch.jpg" width="240"> |

Regression: open `raw.jpg` vs `style-05` / `style-09` first (highest spatial bar), then the whitespace-heavy recipes for crop risk.

### Style-transfer batch B — `demo/poster_demo2/`

Valley scene with a **female subject centered, back to camera**, looking toward the valley — a strong test of full figure, depth to valley, and same-place identity.

**Source** — `demo/poster_demo2/raw.jpg`

<img src="demo/poster_demo2/raw.jpg" width="420">

| ① RISO Editorial | ② Old Newsprint | ③ Paper Theatre |
|:---:|:---:|:---:|
| <img src="demo/poster_demo2/style-01-riso.jpg" width="240"> | <img src="demo/poster_demo2/style-02-newsprint.jpg" width="240"> | <img src="demo/poster_demo2/style-03-paper-theatre.jpg" width="240"> |

| ④ Pressed Flower | ⑤ Travel Journal Sketch | ⑥ Retro Silkscreen |
|:---:|:---:|:---:|
| <img src="demo/poster_demo2/style-04-pressed-flower.jpg" width="240"> | <img src="demo/poster_demo2/style-05-travel-sketch.jpg" width="240"> | <img src="demo/poster_demo2/style-06-silkscreen.jpg" width="240"> |

| ⑦ JP B&W Line | ⑧ Naïve Doodle | ⑨ Photo→Ink Sketch |
|:---:|:---:|:---:|
| <img src="demo/poster_demo2/style-07-jp-line.jpg" width="240"> | <img src="demo/poster_demo2/style-08-naive-doodle.jpg" width="240"> | <img src="demo/poster_demo2/style-09-ink-sketch.jpg" width="240"> |

Regression: confirm the full back-view silhouette (head to hem as in the source) and unchanged valley depth across all nine styles.

**Failure atlas F1–F7:** incomplete people after whitespace · element-library spatial rewrite · source photo or comparison layout in frame · forced wrong aspect · type or crop marks cutting anatomy · clutter deletion removing a person · proxy-metric theater.

Recipes ⑤ travel-sketch, ⑦ jp-line, and ⑨ ink are the strictest on **space**; whitespace-heavy ① and ⑧ fail most often on **crops**. Diagnose ⑤⑦⑨ first when a user says the result "disrespects the photo," then ①⑧ for crop risk.

---

## Generation prompts

> **Provenance.** The original generation prompts were not archived alongside these images. The prompts below are **reconstructed from this pack's own prompt skeletons** — Matching Couple Avatar Appendix A and Photo Style Transfer Poster §6d — filled with each demo's documented teaching notes. Values in `{braces}` must be measured from the actual source image before use; that measurement step is the point of both manuals.

### Couple avatar prompts

Shape per §6.2: task → facing and couplet plan → spatial % → stroke → face → background → tone → clean delivery. All four demos use this skeleton; the per-set lines are what differ.

```
TASK: Independent partner portrait for couple PFP.
Leave the source portrait file unchanged; deliver a new partner file only.
FORMAT: same W×H as source; one person; clean finished square.

COUPLE PAIRING:
- Source faces {DIR} → partner faces {OPP}.
- Complementary plan: {robe value / prop / motif split}.
- Shared drawing hand with the source (same dialect, new identity).

SPATIAL LOCKS:
- Face height ≈ {x}%H; head ≈ {y}%H; negative-space habits as source.
- Landmark gaps: {eye/nose/mouth spacing from crops}.
- Bun apex and chin both inside frame with safe air.

STROKE LOCKS (primary):
- Match hair / profile / lash crops: {clumped variable grey digital sketch}.
- Line color family {charcoal grey}; weight {tapered, uneven}.

FACE LOCKS:
- Eye / nose / mouth recipe from crops: {dash mouth / pale iris / lash clumping}.

BACKGROUND LOCKS:
- Outer-side foliage or wash placement: {describe}.
- Open-field sparse motif if the source has one.

TONE LOCKS:
- Global luma and cast ≈ source; clothing value opposition limited to garments.

CONTENT: clearly new identity and props vs any exemplar; same dialect.
DELIVERY: one finished square, print-ready, no text/UI/guide boxes.
```

| Set | Per-set lines to substitute |
|---|---|
| 1 | `COUPLE PAIRING: opposite facing; shared motif language.` `FACE LOCKS: keep hands as flat as the source when the source is flat.` |
| 2 | `STROKE/FEATURE LOCKS: stronger local feature matching — cloth folds, hair masses.` `BACKGROUND LOCKS: background shapes stay in the source's simplification family.` |
| 3 | `COUPLE PAIRING: hoodie/value opposition.` `TONE LOCKS: hold global luma stable — value shift limited to the garment.` `SPATIAL LOCKS: keep face scale and stroke consistent under larger clothing masses.` |
| 4 | `TONE LOCKS: high-key cool field.` `COUPLE PAIRING: profile pair; pale-to-dark robe opposition; sparse open-field mark vs floral/hair props.` `BACKGROUND LOCKS: soft unoutlined foliage washes.` |

### Style-transfer prompts

The §6d skeleton is shared by every recipe; only the `RECIPE` line changes. Prompts are written for **batch B** (valley back-view) since its subject is documented; for **batch A** (coastal / street) swap in the inventory and spatial map below.

```
Create ONE finished styled reconstruction of the reference photograph.
Deliver styled reconstruction only — a single finished image.
Match reference aspect ratio {W:H}; use 4:3 only when the source is already near 4:3.

SUBJECT INVENTORY (every item fully in frame with safe margin):
- Centered female subject, back to camera; full figure head-to-hem as in source.
- {any companions, animals, or pose-critical props — keep whole}

SPATIAL MAP (same moment, same space — medium change only):
- Depth: near ridge → mid slope → far valley floor → sky.
- Subject centered at mid-scale; gaze direction toward the valley.
- Keep horizon height and primary left–right structure.

RECIPE: {recipe language copied from the poster sub-skill's recipe card}
IDENTITY/MEMORY: {back-view silhouette, hair, wardrobe, valley profile}
COLOR: from the photo, reduced per recipe.
TEXT: {recipe text rule}
ACCEPTANCE: subjects complete; space intact; recipe dialect clear; styled only.
```

**Batch A substitution** — replace the inventory and map blocks with:

```
SUBJECT INVENTORY: {every pedestrian and animal fully in frame with safe margin}
SPATIAL MAP: road/path axis {direction}; lamp or primary light {position};
pedestrian groups {count, positions, facing}; depth layers FG/MG/BG/sky;
place identity and primary left–right structure.
```

Prompt language to avoid (from both atlases): leading with genre or mood tags, `same filter as ref`, `pretty poster`, and any instruction that trades spatial anchors for decoration.

---

## Installation

Each skill folder is self-contained: the folder name is the skill slug and `SKILL.md` carries YAML frontmatter (`name`, `description`) used for discovery and routing. The format follows the [Agent Skills](https://agentskills.io) standard, so the same folders work across tools.

### 1. Clone the pack

```bash
git clone <this-repo-url> ~/high-aesthetic-skills-pack
cd ~/high-aesthetic-skills-pack
```

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
ln -sfn ~/high-aesthetic-skills-pack ~/.cursor/skills/high-aesthetic-skills-pack
# or project-scoped:
# ln -sfn ~/high-aesthetic-skills-pack .cursor/skills/high-aesthetic-skills-pack
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

The sub-skills mark the demos as *required reading when available*. They are referenced by pack-relative paths such as `high-aesthetic-skills-pack/demo/avatar_demo/`. Because the demo folders sit next to the skills rather than inside them, tell your agent where the pack lives — for example by adding one line to `AGENTS.md` / `CLAUDE.md`:

```markdown
High aesthetic image skills pack is cloned at ~/high-aesthetic-skills-pack.
Demo regression sets: ~/high-aesthetic-skills-pack/demo/{avatar_demo,poster_demo1,poster_demo2}
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

No license file is included in this repository. Contact the author before redistributing.
