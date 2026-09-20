# High Aesthetic Image Skills Pack

**One skill — High Aesthetic Image Expert — with two sub-skills**, for high-aesthetic image work. Shipped as `SKILL.md` operator manuals plus the demo image sets that serve as their regression memory.

The pack's voice is **positive locks**: state what to keep and deliver. Emphatic bans appear only where a failure mode recurs in practice (e.g. **禁止仅使用粗 label 就开始生成**).

```
high-aesthetic-skills-pack/
├── high-aesthetic-image-expert/SKILL.md      ← the skill
├── matching-couple-avatar/SKILL.md           ← sub-skill 1
├── photo-style-transfer-poster/SKILL.md      ← sub-skill 2
└── demo/
    ├── avatar_demo/        couple-PFP regression set (1L–4L)
    ├── poster_demo1/       style-transfer batch A (raw + 9 styles)
    └── poster_demo2/       style-transfer batch B (raw + 9 styles)
```

| Path | Role | Size |
|---|---|---|
| `high-aesthetic-image-expert/` | **The skill.** Any image brief. Fixed aesthetic core, every-turn workflow, mandatory self-review. Routes specialty briefs to the sub-skills. | 92 lines |
| `matching-couple-avatar/` | **Sub-skill.** Leave the user's portrait unchanged; deliver one independent partner portrait (couple set / 情侣头像). | 996 lines |
| `photo-style-transfer-poster/` | **Sub-skill.** One photo → one finished styled image of the same moment and space (风格迁移). Nine recipes. | 627 lines |
| `demo/` | Regression memory for both sub-skills — see [Demo gallery](#demo-gallery). | 32 images |

The two sub-skill manuals are intentionally long. Both say why: short "vibe" skills produce exactly the failures catalogued in their atlases — tag-led stock dialect, cropped people, rewritten streets, mirror-clone pairs.

---

## The skill: High Aesthetic Image Expert

One job: produce or arrange high-aesthetic, elegant, deliverable images from the user's brief (subject, mood, composition, reference, style).

**Aesthetic core — fixed across all styles:**

1. **Restraint** — quiet confidence over spectacle.
2. **Relationship first** — spatial relations, hierarchy, and silhouette before ornaments.
3. **Color from content** — palette follows subject and light.
4. **Sparse decoration** — few marks; breathing room over sticker piles.
5. **Negative space as design** — empty areas are intentional.
6. **Deconstruct, then reconstruct** — list 3–6 visual facts before generating.
7. **Clean delivery** — ship the finished image; the picture is the answer.

**Style recipes:** photoreal / editorial, anime / illustration, lyrical / mood, oil / material, and user-named styles — all under the same core. A titled poster layout is used only when asked for or when a sub-skill requires it.

**Every-turn workflow:** Brief → Explore (3–6 internal visual facts) → Generate → **Self-review (mandatory)** → Deliver. If one critical constraint is missing, ask **one** question.

**Self-review checklist** covers brief match, style fidelity, pair intent, color coherence, hands/face detail, **complete important subjects**, resolution/crop, frame contents, orientation (when pairing, face the *opposite* direction so the pair looks toward each other), and file attachment. Fail → regenerate, then re-check.

**Resolution rules:** match the user's stated size; if the generator returns a fixed lower size (e.g. 1280×720), crop/resize with subject-aware framing and keep people/animals fully inside; be honest when a result is upscaled.

---

## Sub-skill 1: Matching Couple Avatar

**Goal:** produce **one new standalone partner portrait** that

1. leaves the user's source portrait file unchanged — deliver only a new partner file,
2. is visibly a *different* picture (fresh identity and props, shared drawing dialect),
3. shares nearly the same **drawing dialect** as the source (line material, spatial habits, face recipe, brightness/cast, motif grammar),
4. forms Chinese **对子** complementarity with the source — a complementary mate, not a mirror clone,
5. keeps **person + background co-framed**.

**Primary control is pixel-level source features** — line weight, contour breaks, blush hatch, palette RGB, grain, hair clump structure, iris/mouth recipe — driven from the source image and micro-crops. Genre or mood labels (`anime`, `xianxia`, `hanfu vibe`, `watercolor style`, `ethereal`, …) may appear **only after** concrete source-derived locks are written, and only as one subordinate clause.

**对子 — couple symmetry as complementary opposites.** A shared layer (stroke material, face recipe family, palette grammar, motif language, spatial habits) pairs with a deliberately opposed layer:

| Axis | Example 对子 |
|---|---|
| Value / robe | dark navy robe ↔ pale mist robe |
| Facing | right profile ↔ left profile |
| Active / passive | hand holding a stem ↔ quiet empty hand + floating motif |
| Motif split | line-art heart on open field ↔ blossom cluster in hair / held sprig |
| Weather / element metaphors | 白对黑、云对雨、雪对风、晚照对晴空 — design thinking, never text in the image |

**Emphatic bans** (recurring failure modes):

1. **禁止仅使用粗 label / 粗粒度 tag 就开始生成** — measure and crop from the source first.
2. **禁止改写或覆写用户原头像文件** — deliver only a new partner file.
3. **禁止把镜像翻转 / 同向朝向 / 1:1 配件复制当成对子解.**
4. **禁止用人像特写裁切吃掉源图构图级背景.**

**Fidelity axes to lock:** spatial structure, facial detail grammar, brightness, color cast / tone, and **lines / stroke material** — the #1 recurring real failure when users say the style is completely wrong.

The manual also carries a study protocol, prompt skeleton (Appendix A), a 30-second acceptance test (Appendix B), a glossary (Appendix C), a 对子 design workshop, a stroke cookbook, spatial engineering & delivery math, background engineering, worked failure→fix stories, batch mode, and a QA contact-sheet recipe.

---

## Sub-skill 2: Photo Style Transfer Poster

**Goal:** from **one** photograph (reference only), deliver **one finished styled image** of the **same moment and space**, with every important person/animal/key prop still fully visible, in a locked print/illustration dialect.

**Two hard locks** are the acceptance gates — subjects and space come before color vibes:

- **Complete important subjects.** Every important person, animal, and pose-critical prop stays **fully in frame with a clear safe margin**, matching the completeness shown in the source. Whitespace is composition, not amputation.
- **Source spatial structure.** Road/path axis, lamp or primary light, pedestrian-group relations and directions, depth layers, and place identity stay locked — **medium change only**. No element-library recombination.

**Emphatic bans:** **禁止**裁切或缺失原图中的重要主体；**禁止**用"大留白 / 简化背景"当借口裁掉人或动物；**禁止**把原图当元素库改空间；**禁止**成片放入原照片或 50/50 / before-after 对照排版.

**Resolution & aspect:** match the source. Snap to **4:3 only when the source is already near 4:3**. If the generator returns the wrong aspect: regenerate → pad/letterbox → subject-aware crop with margin (never a geometric center-crop through an edge-biased subject).

**Recommendation:** offer a recipe **name** (or a short Chinese activation phrase) — recipe numbers stay internal. Default when unclear: **RISO Editorial**.

---

## The nine recipes

Each recipe card describes the entire delivered image — medium, color, layout, text, mood, and acceptance criteria.

| # | Recipe | Also called | Focus |
|---|---|---|---|
| 1 | **RISO Editorial** | RISO孔版 | 2–4 spot colors, freehand line with jitter/breaks/misregistration, small subject + large negative space, warm paper grain |
| 2 | **Old Newsprint** | Vintage culture supplement | Yellowed newsprint, multi-column editorial layout, halftone hero art, subject ~40–60%, strict palette + 1–2 low-sat spots |
| 3 | **Paper Theatre** | Cut-paper diorama | Layered cut paper, rivets/fasteners, paper depth bands as stage depth, subject ~50–70%, 3–5 unified colors on cream |
| 4 | **Pressed Flower** | Botanical specimen poster | Dried petals/leaves rebuilt into silhouettes, herbarium labels and specimen tape, 2–4 soft colors, subject ~45–60% |
| 5 | **Travel Journal Sketch** | Pen & colored pencil | Same instant, same scene; positions/scale/facing/gaze **highly match** the photo; pen structure + colored-pencil hatching + light wash on cream |
| 6 | **Retro Silkscreen** | 复古丝网 | High-contrast silhouette, coarse halftone, granulated blocks, bold type that may cross the **frame edge** but never faces/limbs/animals |
| 7 | **JP B&W Line** | 日系治愈线稿 | Fineliner B&W lifestyle look, flat fill + whitespace, light hatching, simplified props, quiet and airy |
| 8 | **Naïve Doodle** | Marker / crayon lifestyle | Massive intentional whitespace, small but **fully drawn** people, 2–3 colors + dark line, smart text–image relation, adult editorial finish |
| 9 | **Photo→Ink Sketch** | 怀旧素描 | Loose B&W ink of the same subject/pose/wardrobe/composition/mood on warm textured paper, poetic handwritten title |

**Vibe → recipe** (activation synonyms users may type):

| Vibe | Prefer | Also consider |
|---|---|---|
| 怀旧、复古、胶片、旧杂志 / nostalgia, retro, film | Photo→Ink / Old Newsprint / Retro Silkscreen | Travel Journal if travel |
| 电影海报、电影感 / movie poster, filmic | Photo→Ink / Retro Silkscreen | — |
| 文艺、独立杂志、展览海报 / literary, indie mag, exhibition | RISO Editorial | Naïve Doodle if extreme whitespace |
| 报纸、副刊、知性 / newspaper, editorial | Old Newsprint | — |
| 手工、纸艺、童话剧场、剪纸 / paper craft, pop-up | Paper Theatre | — |
| 压花、标本、植物、节日温柔 / pressed flower, botanical | Pressed Flower | couples / holiday / botanical |
| 旅行、速写、日记、手账 / travel, sketch, urban plein-air | Travel Journal Sketch | JP B&W Line if quieter B&W |
| 先锋、丝网、实验印刷 / avant-garde, silkscreen | Retro Silkscreen | RISO if softer |
| 治愈、日系、黑白线稿、露营街头 / healing, JP B&W line | JP B&W Line | Naïve Doodle if more playful |
| 涂鸦、稚拙、大留白 / doodle, naïve, less-is-more | Naïve Doodle | RISO if print color still wanted |

When no vibe is given, photo content decides: architecture/street vista → Travel Journal; soft-light portrait → Photo→Ink; couple/holiday/floral → Pressed Flower; theatrical staging → Paper Theatre; bold graphic face → Retro Silkscreen; quiet daily → JP B&W Line; documentary city memory → Old Newsprint; sparse drawing with smart type → Naïve Doodle.

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

Study method: open `nL` and lock facing/scale/stroke/face recipe/background/cast; open `nR` as pair-grammar exemplar; open `nL_gen` as a working attempt; catalogue gaps and regenerate with tighter locks.

**Failure atlas F1–F8:** tag-led stock dialect · spatial collapse (headshot zoom / unsafe square crop) · background abandonment · mirror clone instead of 对子 · wrong stroke dialect (the silent killer) · proxy-metric chasing · patching a failed base instead of redrawing · clothing-value 对子 bleeding into the whole frame.

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

Valley scene with a **female subject centered, back to camera**, looking toward the valley — a strong test of full figure + depth to valley + same-place identity.

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

Shape per §6.2: task → facing + 对子 → spatial % → stroke → face → background → tone → clean delivery. All four demos use this skeleton; the per-set lines are what differ.

```
TASK: Independent partner portrait for couple PFP / 情侣头像.
Leave the source portrait file unchanged; deliver a new partner file only.
FORMAT: same W×H as source; one person; clean finished square.

COUPLE / 对子:
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
- Global luma and cast ≈ source; clothing 对子 limited to garments.

CONTENT: clearly new identity and props vs any exemplar; same dialect.
DELIVERY: one finished square, print-ready, no text/UI/guide boxes.
```

| Set | Per-set lines to substitute |
|---|---|
| 1 | `COUPLE / 对子: opposite facing; shared motif language.` `FACE LOCKS: keep hands as flat as the source when the source is flat.` |
| 2 | `STROKE/FEATURE LOCKS: stronger local feature matching — cloth folds, hair masses.` `BACKGROUND LOCKS: background shapes stay in the source's simplification family.` |
| 3 | `COUPLE / 对子: hoodie/value opposition.` `TONE LOCKS: hold global luma stable — value shift limited to the garment.` `SPATIAL LOCKS: keep face scale and stroke consistent under larger clothing masses.` |
| 4 | `TONE LOCKS: high-key cool field.` `COUPLE / 对子: profile pair; pale↔dark robe opposition; sparse open-field mark vs floral/hair props.` `BACKGROUND LOCKS: soft unoutlined foliage washes.` |

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

RECIPE: {recipe line from the table below}
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

**Recipe lines** — substitute into `RECIPE:`:

| # | `RECIPE:` line |
|---|---|
| ① | RISO Editorial — 2–4 spot colors extracted from the photo and redesigned; freehand line with slight jitter, breaks, and misregistration; flat spot fields over gradients; warm paper grain and print dots; small-to-mid subject with large negative space. |
| ② | Old Newsprint — yellowed newsprint with a multi-column editorial layout (hero zone, section heads, captions, sidebars, fine rules); halftone or low-sat spot hero art at ~40–60% of the frame; black, gray, aged paper white plus 1–2 low-sat spots. |
| ③ | Paper Theatre — layered cut paper with visible round fasteners and articulated joints; sky, ground, and props simplified into height-offset paper layers matching the source's depth bands; 3–5 desaturated colors on cream; fiber, crease, and glue traces. |
| ④ | Pressed Flower — primary subjects rebuilt from dried petals, leaves, twigs, and translucent plant fragments into recognizable specimen silhouettes; herbarium labels, specimen tape, press marks; 2–4 soft colors on cream with large whitespace. |
| ⑤ | Travel Journal Sketch — fine pen and pencil structure with colored-pencil hatching and only thin transparent watercolor washes; relative positions, scale, facing, and gaze highly match the photo; loose hand lines with breaks and cross-hatching on warm cream paper. |
| ⑥ | Retro Silkscreen — high-contrast silhouette, coarse halftone, granulated color blocks; 2–4 bold spot colors with local misregistration and ink wear; large whitespace; type may clip the frame edge but stays clear of faces, limbs, and animals. |
| ⑦ | JP B&W Line — fineliner/sign-pen look, mostly B&W with flat fill and whitespace; outer contour slightly thicker, inner detail thinner, light hatching; background reduced to a few necessary props; one clear focal center. |
| ⑧ | Naïve Doodle — most irrelevant information actively deleted; small but fully drawn subjects; jittery broken hand lines with marker/crayon-like fills; massive intentional whitespace; 2–3 main colors plus dark line on warm white; sparse handwriting placed in negative space. |
| ⑨ | Photo→Ink Sketch — loose B&W ink sketch of the same subject, pose, wardrobe, and composition on warm textured paper; soft filmic nostalgia carried by the drawing language, not by pasting a photo; cream negative space and a small poetic handwritten title. |

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

**Trigger vocabulary is bilingual by design** — English ("style transfer", "matching PFPs", "movie poster") and Chinese (风格迁移, 情侣头像, 对子, 怀旧, 日系治愈线稿) both activate the matching recipe or skill.

---

## Shared doctrine

Both sub-skills sit under the same fixed aesthetic core and add their own law. Compressed:

- **Pixel-level locks lead; tags stay subordinate.** A genre label is a summary, not a lock.
- **Subjects and space are the first acceptance gates** — palette and grain come last.
- **Measure, don't vibe** — write face %, luma, aspect, and axis positions into the brief.
- **Redraw under better locks** rather than patching a failed base.
- **Name the failing axis** (stroke / face / space / background / 对子) before changing anything.
- **When the user freezes a candidate, stop** — save it as `*_gen` and halt churn.
- **Recommend by name, not by number.**
- **Use the demo atlases as regression memory.**

---

## Repo notes

- Demo images are **JPEG**. The style-transfer outputs are all 1280×720 — the generator's fixed landscape size — while batch B's source is 1024×677 and batch A's source is 1706×1279. Avatar demos are square except set 3 (706×941): 474×474, 736×736, 706×941, 1080×1079.
- The style files were originally named `*.png` while containing JPEG data; they were renamed to `.jpg` so GitHub serves them with a matching content type and they render in this README.
- Batch A's source was an extensionless file named `raw`; it is now `raw.jpg` so it renders inline.
- `matching-couple-avatar/SKILL.md` §27 references an absolute pack path (`/home/zijianwang/Pictures/high-aesthetic-skills-pack/`) and lists agent-workflow mirror names. Adjust these when vendoring the pack elsewhere.
- Aesthetic core, workflow, and self-review live in the parent skill; the sub-skill manuals restate only what they add.

## License

No license file is included in this repository. Contact the author before redistributing.
