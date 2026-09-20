# High Aesthetic Image Skills Pack

Three English-language agent skills for high-aesthetic image work, shipped as `SKILL.md` operator manuals — plus the demo image sets that serve as their regression memory.

The pack's voice is **positive locks**: state what to keep and deliver. Emphatic bans are used sparingly, only where a failure mode recurs in practice (e.g. **禁止仅使用粗 label 就开始生成**).

---

## What's in the pack

```
high-aesthetic-skills-pack/
├── high-aesthetic-image-expert/    SKILL.md   parent skill — aesthetic core + self-review
├── matching-couple-avatar/         SKILL.md   specialty — separate matching partner avatar
├── photo-style-transfer-poster/    SKILL.md   specialty — one photo → one styled reconstruction
├── avatar_demo/                    12 files   couple-PFP regression set (1L–4L)
├── poster_demo1/                   10 files   style-transfer batch A (raw + 9 styles)
└── poster_demo2/                   10 files   style-transfer batch B (raw.jpg + 9 styles)
```

| Folder | Skill (`name:`) | Size | Role |
|---|---|---|---|
| `high-aesthetic-image-expert/` | High Aesthetic Image Expert | 92 lines | **Parent.** Any image brief. Fixed aesthetic core, every-turn workflow, mandatory self-review. Routes specialty briefs to the sub-skills. |
| `matching-couple-avatar/` | Matching Couple Avatar | 996 lines | **Specialty.** Leave the user's portrait unchanged; deliver one independent partner portrait (couple set / 情侣头像). |
| `photo-style-transfer-poster/` | Photo Style Transfer Poster | 627 lines | **Specialty.** One photo → one finished styled image of the same moment and space (风格迁移). Nine recipes. |

The two specialty manuals are intentionally long. Both state why: short "vibe" skills produce exactly the failures catalogued in their atlases — tag-led stock dialect, cropped people, rewritten streets, mirror-clone pairs.

---

## 1. High Aesthetic Image Expert (parent)

One job: produce or arrange high-aesthetic, elegant, deliverable images from the user's brief (subject, mood, composition, reference, style).

**Aesthetic core — fixed across all styles:**

1. **Restraint** — quiet confidence over spectacle.
2. **Relationship first** — spatial relations, hierarchy, and silhouette before ornaments.
3. **Color from content** — palette follows subject and light.
4. **Sparse decoration** — few marks; breathing room over sticker piles.
5. **Negative space as design** — empty areas are intentional.
6. **Deconstruct, then reconstruct** — list 3–6 visual facts before generating.
7. **Clean delivery** — ship the finished image; the picture is the answer.

**Style recipes:** photoreal / editorial, anime / illustration, lyrical / mood, oil / material, and user-named styles — all under the same core. A titled poster layout is used only when asked for or when a specialty sub-skill requires it.

**Every-turn workflow:** Brief → Explore (3–6 internal visual facts) → Generate → **Self-review (mandatory)** → Deliver. If one critical constraint is missing, ask **one** question.

**Self-review checklist** covers brief match, style fidelity, pair intent, color coherence, hands/face detail, **complete important subjects**, resolution/crop, frame contents, orientation (when pairing, face the *opposite* direction so the pair looks toward each other), and file attachment. Fail → regenerate, then re-check.

**Resolution rules:** match the user's stated size; if the generator returns a fixed lower size (e.g. 1280×720), crop/resize with subject-aware framing and keep people/animals fully inside; be honest when a result is upscaled.

---

## 2. Matching Couple Avatar (specialty)

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

## 3. Photo Style Transfer Poster (specialty)

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

## Demo atlases (regression memory)

The demos are not decoration — both specialty manuals treat them as the **regression suite** to reopen whenever quality slips.

### `avatar_demo/` — couple PFP set

| ID | Source | Exemplar pair | Partner output |
|---|---|---|---|
| 1 | `1L.jpeg` | `1R.jpeg` | `1L_gen.jpeg` |
| 2 | `2L.jpeg` | `2R.jpeg` | `2L_gen.jpeg` |
| 3 | `3L.jpg` | `3R.jpg` | `3L_gen.jpg` |
| 4 | `4L.jpg` | `4R.jpg` | `4L_gen.jpg` |

`L`/`R` are **set IDs, not "left/right of frame"** — facing direction is read from pixels. Study method: open `nL` and lock facing/scale/stroke/face recipe/background/cast; open `nR` as pair-grammar exemplar; open `nL_gen` as a working attempt; catalogue gaps and regenerate with tighter locks.

**Failure atlas F1–F8:** tag-led stock dialect · spatial collapse (headshot zoom / unsafe square crop) · background abandonment · mirror clone instead of 对子 · wrong stroke dialect (the silent killer) · proxy-metric chasing · patching a failed base instead of redrawing · clothing-value 对子 bleeding into the whole frame.

### `poster_demo1/` and `poster_demo2/` — style-transfer batches

| Demo | Source | Outputs | Content |
|---|---|---|---|
| poster_demo1 | `raw` | `style-01-riso.png` … `style-09-ink-sketch.png` | Coastal / street-memory batch — practice axis, depth, and full pedestrians |
| poster_demo2 | `raw.jpg` | `style-01-riso.png` … `style-09-ink-sketch.png` | Valley back-view batch — centered female subject, strong test of full figure + depth to valley + same-place identity |

**Failure atlas F1–F7:** incomplete people after whitespace · element-library spatial rewrite · source photo or comparison layout in frame · forced wrong aspect · type or crop marks cutting anatomy · clutter deletion removing a person · proxy-metric theater.

Recipes ⑤ travel-sketch, ⑦ jp-line, and ⑨ ink are the strictest on **space**; whitespace-heavy ① and ⑧ fail most often on **crops**. Diagnose ⑤⑦⑨ first when a user says the result "disrespects the photo," then ①⑧ for crop risk.

---

## Shared doctrine

Both specialty skills sit under the same fixed aesthetic core and add their own law. Compressed:

- **Pixel-level locks lead; tags stay subordinate.** A genre label is a summary, not a lock.
- **Subjects and space are the first acceptance gates** — palette and grain come last.
- **Measure, don't vibe** — write face %, luma, aspect, and axis positions into the brief.
- **Redraw under better locks** rather than patching a failed base.
- **Name the failing axis** (stroke / face / space / background / 对子) before changing anything.
- **When the user freezes a candidate, stop** — save it as `*_gen` and halt churn.
- **Recommend by name, not by number.**
- **Use the demo atlases as regression memory.**

---

## Using these as agent skills

Each folder is a self-contained skill: the directory name is the skill slug and `SKILL.md` carries YAML frontmatter (`name`, `description`) that an agent runtime uses for discovery and routing.

```yaml
---
name: Matching Couple Avatar
description: >-
  Use when the user asks for a separate pairing avatar that matches their given
  portrait (couple set / matching PFPs / 情侣头像) ...
---
```

To install, drop a skill folder into your agent's skills directory (or reference this pack directly). `high-aesthetic-image-expert/` is the entry point and routes specialty briefs to the other two; the sub-skills link back to it with the runtime's `sand-workflow:` link scheme.

**Trigger vocabulary is bilingual by design** — English ("style transfer", "matching PFPs", "movie poster") and Chinese (风格迁移, 情侣头像, 对子, 怀旧, 日系治愈线稿) both activate the matching recipe or skill.

---

## Repo notes

- **`poster_demo1/raw` has no file extension** (it is a JPEG, 1706×1279). `poster_demo2/raw.jpg` is 1024×677.
- The `poster_demo*/style-*.png` files are **JPEG-encoded data under a `.png` extension** — all 1280×720, the generator's fixed landscape size. Keep this in mind if you re-encode or script over them.
- Avatar demos are square except set 3 (706×941): 474×474, 736×736, 706×941, 1080×1079.
- `matching-couple-avatar/SKILL.md` §27 references an absolute pack path (`/home/zijianwang/Pictures/high-aesthetic-skills-pack/`) and lists agent-workflow mirror names. Adjust these when vendoring the pack elsewhere.
- Aesthetic core, workflow, and self-review live in the parent skill; the specialty manuals restate only what they add.

## License

No license file is included in this repository. Contact the author before redistributing.
