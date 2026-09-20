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
  names, not numbers.
---

# Photo Style Transfer Poster

> **Pack demos (required reading when available):**  
> `aesthetic-atelier/demo/poster_demo1/` — coastal / street-memory batch (`raw.jpg` + `style-01`…`style-09`)  
> `aesthetic-atelier/demo/poster_demo2/` — valley back-view batch (`raw.jpg` + `style-01`…`style-09`)  
> Use demos as regression memory for **complete subjects** and **spatial fidelity** — the two axes this skill exists to protect.

This skill is the specialty path under High Aesthetic Image Expert for **photo → styled reconstruction**. It is intentionally long: short “vibe transfer” instructions cause cropped people and rewritten streets. Read the hard locks, inventory subjects + spatial map, then generate.

**Activation:** user says style transfer / `风格迁移` / named recipe / clear vibe synonym.

Parent: **[High Aesthetic Image Expert](sand-workflow:high-aesthetic-image-expert-2)** (or `high-aesthetic-image-expert`).

---

## 0. One-sentence goal

**Emphatic ban:** **禁止**在成片中放入原照片，或做 50/50 / before-after 对照排版。Deliver styled reconstruction only.

From **one** photograph (reference only), deliver **one finished styled image** of the **same moment and space**, with **every important person/animal/key prop still fully visible**, in a locked print/illustration dialect — a complete styled reconstruction the viewer can recognize as that instant.

---

## 1. Hard lock — complete important subjects

### 1.1 Requirement

**Hard lock:** Keep every important person, animal, and pose-critical prop **fully in frame with a clear safe margin**, matching the completeness shown in the source.

| If fully visible in source, keep fully in frame | What “complete” means |
|---|---|
| People: head, hat/hair silhouette, torso, limbs, hands, feet when shown | Full silhouette readable; face/hat/arm/hand/foot remain |
| Animals / pets: full body silhouette as in source | Head, torso, legs, tail as shown |
| Pose-critical props (raft, held object, vehicle mass the pose depends on) | Prop mass stays so the pose stays readable |
| Primary landmark mass the viewer would miss | Landmark stays on-frame at readable scale |

**Whitespace is allowed** when the full primary subjects still sit inside the frame with margin. Build empty space by composition and clutter deletion — keep subjects whole.

**Selective deletion** may remove *clutter* (busy background junk, minor props). Primary people/animals and the limbs that make the pose readable stay.


### 1.1a Emphatic bans (subjects)

Positive locks are the default voice. Keep these bans explicit:

1. **禁止裁切或缺失原图中的重要主体**（尤其人像、动物，以及支撑姿态的关键道具）。Keep them fully in frame with safe margin.
2. **禁止用“大留白 / 简化背景”当借口裁掉人或动物。** Whitespace is composition, not amputation.
3. **禁止对偏位主体做几何中心裁切来“修画幅”。** Prefer regenerate, letterbox/pad, or subject-aware crop.

### 1.2 High-risk patterns (from real runs)

1. **Left- or edge-biased subject** + added negative space + **center-crop to target aspect** → amputated person. Prefer regenerate, pad/letterbox, or subject-aware crop.  
2. Recipe that “simplifies background” misread as deleting a person at the edge — inventory primary groups first.  
3. Generator returns 16:9 / wrong aspect; operator center-crops “to fix ratio” — lock W×H in prompt; pad instead.  
4. Travel-sketch / ink recipes that redraw architecture and omit a pedestrian group — write group count into the spatial map.  
5. Silkscreen/type recipes where bold type or crop marks cross a face — type may clip **frame** edges only; anatomy stays clear of type.

### 1.3 Pre-generation subject inventory (mandatory)

Open the source and list:

- Primary people count + approximate positions (e.g. “one woman center-left, back to camera”).
- Animals count + positions.
- Pose-critical props.
- Completeness note: which limbs/heads are fully visible in source (those stay complete in output).

Write this inventory into Explore locks and into the generation prompt.

### 1.4 Acceptance — subjects

Open the output. For each inventoried subject:

- [ ] Fully inside the frame with a **safe margin**
- [ ] Recognizable as the same actor/pose class
- [ ] Intact after any resize/framing pass

Fail → regenerate with stronger full-subject lock; or pad/letterbox; or **subject-aware** crop around the union of all inventoried subjects + margin.

---

## 2. Hard lock — source spatial structure

### 2.1 Requirement

**Hard lock:** Same moment, same space. Medium and style may change; **layout of the world stays**. Keep relative positions, axes, and depth.


### 2.1a Emphatic bans (space)

1. **禁止把原图当元素库任意重组。** Same moment, same space — restyle the fixed stage.
2. **禁止擅自改道路轴 / 主灯位置 / 主人群相对关系与朝向 / 景深层。** Lock them before generating.
3. **禁止发明另一条街、另一座城、另一个山谷身份。** Place identity stays.

### 2.2 Spatial locks (always preserve)

| Lock | Meaning |
|---|---|
| Road / path axis | Curve/vanishing direction as in source |
| Lamp / primary light | Position relative to frame and subjects |
| Pedestrian / people groups | Relative positions, primary group count, walking/facing directions |
| Depth layers | Foreground → mid → far → sky and relative scale |
| Major anchors | Buildings, shoreline, mountain/valley mass, vehicle that defines the place |
| Relative positions | Who/what sits left/right/above/below of whom |

### 2.3 Deliver spatial fidelity by

- Treating the photo as a **fixed stage** to restyle, not a kit of movable parts  
- Keeping major anchors where they are  
- Keeping place identity (same street / shoreline / valley family)  
- Keeping left–right of the primary structure unless the user asks to flip  
- Keeping depth bands that match the source  
- Allowing off-center composition when the source is off-center (relations stay)

### 2.4 Pre-generation spatial map (mandatory)

Sketch (internally or as notes):

1. Horizon / major axis line  
2. Primary light or lamp marker  
3. Boxes for each primary person/animal group + facing arrows  
4. Depth bands (FG/MG/BG/sky)  
5. What may be deleted as clutter **while** keeping 1–4 intact  

### 2.5 Recipe tension (resolve correctly)

Some recipes say “delete complex background” or “whitespace is the core.” That means:

- Delete **clutter textures**, keep spatial anchors required by §2.2  
- Shrink or symbolize, but keep **who stands where** relative to the axis  
- Naïve Doodle / RISO may empty fields — people stay whole; road/lamp/groups stay locked

Travel Journal Sketch and Photo→Ink require **especially high** spatial fidelity.

---

## 3. Shared hard rules (all recipes)

1. **One photo, one output** — single finished image; invent no foreign scenes.  
2. **Styled reconstruction only** — source photo is analysis/reference. The delivered file is the styled work alone.  
3. **Resolution & aspect** — match source first. Snap to **4:3 only if source is already near 4:3**. Preserve proportions.  
4. **Complete important subjects** — §1.  
5. **Identity from reference** — preserve recognizability (face/hair/pose/wardrobe/key props/scene relations as the recipe allows). Same person, same core action; clutter deletion only for minor props.  
6. **Spatial fidelity** — §2.  
7. **Reconstruction, not photoreal copy** — keep memory points; delete clutter; handmade look per recipe.  
8. **Color** — from the photo, reduced/organized per recipe. Controlled, recipe-limited palettes.  
9. **Text** — sparse editorial text per recipe only.  
10. **Finish** — magazine / art book / exhibition catalog quality.  
11. **Post-process framing** — if aspect is wrong: regenerate, letterbox/pad, or subject-aware crop with margin — keep people/animals whole.

---

## 4. Demo atlas — `poster_demo1` / `poster_demo2`

### 4.1 Layout

| Demo | Path | Source | Outputs |
|---|---|---|---|
| poster_demo1 | `aesthetic-atelier/demo/poster_demo1/` | `raw.jpg` | `style-01-riso.jpg` … `style-09-ink-sketch.jpg` |
| poster_demo2 | `aesthetic-atelier/demo/poster_demo2/` | `raw.jpg` | `style-01-riso.jpg` … `style-09-ink-sketch.jpg` |

Recipe index (filenames):

1 riso · 2 newsprint · 3 paper-theatre · 4 pressed-flower · 5 travel-sketch · 6 silkscreen · 7 jp-line · 8 naive-doodle · 9 ink-sketch  

### 4.2 How to study a demo

1. Open `raw` / `raw.jpg` — build **subject inventory** (§1.3) + **spatial map** (§2.4).  
2. Open each `style-0N-*.jpg` — check subjects complete? axis/lamp/groups/depth intact?  
3. Catalogue failures by recipe — some recipes (⑤ travel-sketch, ⑦ jp-line, ⑨ ink) are stricter on space; whitespace-heavy recipes (①⑧) fail more often on crops.  
4. When regenerating for a user, use the same checklist before shipping.

### 4.3 Cross-cutting failure atlas (F1–F7)

#### F1 — Incomplete people after whitespace

- **Symptom:** Head/hat/arm cut; left-biased subject clipped.  
- **Cause:** Center-crop after letterboxing/whitespace; or “large negative space” misread as crop.  
- **Teach / fix:** Subject inventory; safe margin; regenerate with explicit full-figure lock; pad or subject-aware crop.  
- **Refine:** Compare raw vs out focusing on silhouette completeness.

#### F2 — Element-library spatial rewrite

- **Symptom:** Road axis moved; lamp relocated; pedestrian groups regrouped; place feels like another street. Especially on travel-sketch / ink / some mid recipes.  
- **Cause:** Prompt optimized “pretty poster” over “same space”; model recombined anchors.  
- **Teach / fix:** Explicit spatial map in prompt; “same moment, same space”; attach raw as primary ref.  
- **Refine:** Trace axis/lamp/groups on raw and on output; pass only when they match.

#### F3 — Source photo or comparison layout in frame

- **Symptom:** User sees original photo beside/above art.  
- **Cause:** Old diptych habit.  
- **Teach / fix:** Prompt + self-review: styled reconstruction only.  
- **Refine:** Reject and regenerate as a single styled image.

#### F4 — Forced wrong aspect

- **Symptom:** Squash or unnecessary 4:3 crop that clips subjects.  
- **Cause:** Default poster ratio.  
- **Teach / fix:** Match source; 4:3 only if near.  
- **Refine:** Compare aspect numbers before/after.

#### F5 — Type or crop marks cutting anatomy (silkscreen)

- **Symptom:** Bold title slices a face.  
- **Cause:** “Type may cross frame” misread as “type may cut body”.  
- **Teach / fix:** Type clips **frame edge** only; faces, limbs, and animals stay clear of type.

#### F6 — Clutter deletion removes a person

- **Symptom:** Edge pedestrian gone.  
- **Cause:** “Delete complex background” too aggressive.  
- **Teach / fix:** Inventory primary groups; deletion list = clutter only.

#### F7 — Proxy metric theater

- **Symptom:** Endless color tweaks while people stay cropped or street rewritten.  
- **Cause:** Optimizing easy aesthetics first.  
- **Teach / fix:** Subjects + space are the first acceptance gates — always; palette last.

### 4.4 Demo-specific teaching notes

#### poster_demo1

- Often coastal/street-memory content with architecture + people relations.  
- Use to practice: axis + depth + full pedestrians.  
- Regression: open `raw` vs `style-05-travel-sketch` / `style-09-ink-sketch` first (highest spatial bar), then whitespace recipes for crop risk.

#### poster_demo2

- Valley scene with **female subject centered, back to camera**, looking toward the valley — strong test of **full figure + depth to valley + same place identity**.  
- Regression: confirm full back-view silhouette (head to feet/robe hem as in raw) and unchanged valley depth structure across all nine styles.

### 4.5 Recipe-by-recipe regression checklist (use with demos)

For **each** of style-01…09 against the matching demo `raw`:

1. Silhouette completeness of every primary person/animal.  
2. Count of primary people groups vs raw.  
3. Road/path / shoreline / valley axis direction.  
4. Lamp or primary light relative position (if present in raw).  
5. Depth: does the far plane still feel farther than mid?  
6. Place identity: buildings/mountains match what the source implies.  
7. Delivered frame is styled work only (no source photo pixels).  

Fail any of 1–7 → regenerate with §6d skeleton filled from raw.

### 4.6 Continuous improvement order on this skill

- Round 1: pick recipe, generate, self-review §8.  
- Round 2: if subjects fail → inventory + margin language stronger; change post-process SOP.  
- Round 3: if space fails → rewrite spatial map into prompt; attach raw again; strengthen “same instant” for ⑤⑨.  
- Round 4: only then tweak palette/paper grain.  

Keep that order — subjects and space before color vibes.

---

## 5. Recipe recommendation (do this for the user)

Offer a recipe **name** (or short Chinese activation phrase). Recipe numbers are internal only — recommend by name.

### Input modes

| User gives | What you do |
|------------|-------------|
| Photo only (“做风格迁移” / style transfer) | Read photo; pick best recipe; generate styled-only; name recipe in short English or Chinese activation phrase (not a number). |
| Rough vibe only | Map vibe → choose one; if truly tied, one question with 2 vibe words. |
| Named recipe / clear synonym | Lock and proceed. |
| Hybrid vibe | Shared hard rules; merge only asked languages. |

### Vibe → recipe map

| Vibe (activation synonyms users may type) | Prefer | Also consider |
|------|--------|---------------|
| 怀旧、复古、胶片、旧杂志、老照片 / nostalgia, retro, film, old magazine | Photo→Ink / Old Newsprint / Retro Silkscreen | Travel Journal if travel |
| 电影海报、电影感、filmic / movie poster, filmic | Photo→Ink / Retro Silkscreen | — |
| 文艺、独立杂志、展览海报、年轻松弛 / literary, indie mag, exhibition, young relaxed | RISO Editorial | Naïve Doodle if extreme whitespace |
| 报纸、副刊、知性、编辑感 / newspaper, supplement, intellectual, editorial | Old Newsprint | — |
| 手工、纸艺、童话剧场、立体书、剪纸 / handmade, paper craft, fairy theatre, pop-up, cut paper | Paper Theatre | — |
| 压花、标本、植物、节日温柔、博物 / pressed flower, specimen, botanical, gentle holiday | Pressed Flower | couples / holiday / botanical |
| 旅行、速写、日记、城市写生、手账旅行 / travel, sketch, diary, urban plein-air | Travel Journal Sketch | JP B&W Line if quieter B&W |
| 先锋、丝网、实验印刷、艺术院校海报 / avant-garde, silkscreen, experimental print, art-school poster | Retro Silkscreen | RISO if softer |
| 治愈、日系、黑白线稿、日常、露营街头 / healing, JP lifestyle, B&W line, daily, camping street | JP B&W Line | Naïve Doodle if more playful |
| 涂鸦、稚拙、大留白、马克笔、少即是多 / doodle, naïve, large whitespace, marker, less-is-more | Naïve Doodle | RISO if print color still wanted |

### Photo-content heuristics (no vibe)

- Architecture / street / travel vista with clear spatial layout → **Travel Journal Sketch**  
- Portrait soft light / warm nostalgia → **Photo→Ink Sketch**  
- Couple / holiday / floral / intimate soft → **Pressed Flower**  
- Playful costume / theatrical staging → **Paper Theatre**  
- Bold graphic face / fashion / high contrast → **Retro Silkscreen**  
- Quiet daily / camping / café / candid calm → **JP B&W Line**  
- Intellectual / documentary / city-memory editorial → **Old Newsprint**  
- Young literary / exhibition / small subject + whitespace → **RISO Editorial**  
- Sparse drawing, empty field, smart type–image relation → **Naïve Doodle**  

Default if unclear: **RISO Editorial**.

Delivery phrase examples: “Using Travel Journal Sketch for this one” / name in English, or a short activation phrase such as 旅行速写 — use IDs only if the user asked for them.

---

## 6. Per-recipe subject & spatial risk

All recipes obey §1–§2. Extra emphasis:

| # | Recipe | Subject risk | Spatial risk | Extra lock in prompt |
|---|--------|--------------|--------------|----------------------|
| 1 | RISO | High (whitespace + off-center) | Medium (background slash) | Full figure + safe margin; keep axis/lamp if still drawn |
| 2 | Newsprint | Medium (hero zone 40–60%) | Medium | Whole figure(s) inside hero zone; place clues stay coherent |
| 3 | Paper Theatre | Medium (paper layers) | Medium | Paper edges as material texture; stage depth = source depth bands; limbs complete |
| 4 | Pressed Flower | Medium (silhouette rebuild) | Lower (bg often deleted) | Full specimen silhouette of each primary person/animal |
| 5 | Travel Journal | High if careless | **Highest** | Same instant/scene; positions/scale/facing/gaze match; full people |
| 6 | Silkscreen | High (type/crop marks) | Medium | Type clear of anatomy; keep key pose + place clues |
| 7 | JP B&W Line | Medium | High (simplify perspective) | Full mid-shot figure; necessary props only; same street family |
| 8 | Naïve Doodle | **Highest crop risk** | Medium–High | Small drawing fraction but **fully drawn** people; anchors stay |
| 9 | Photo→Ink | Medium | **Highest** | Same subject/pose/wardrobe/composition/mood; full figures |

When the user says the result “disrespects the photo” or “space went wrong,” diagnose **⑤⑦⑨** first, then **①⑧** for crop risk.

---

## 6c. Post-process SOP (aspect / size)

1. Measure source W×H and aspect.  
2. If generator returns wrong aspect:  
   - Prefer **regenerate** with explicit W×H / aspect in prompt.  
   - Else **pad/letterbox** to locked aspect.  
   - Else **subject-aware crop**: compute bounding box of all inventoried subjects + margin ≥ ~3–5% of min side; crop only outside that union.  
3. When any inventoried subject is left- or edge-biased, prefer regenerate or pad over geometric center-crop.  
4. After any post-process, re-run §8 subject + space checks.

---

## 6d. Generation prompt skeleton (copy / adapt)

State what to generate. Fill brackets from the source.

```
Create ONE finished styled reconstruction of the reference photograph.
Deliver styled reconstruction only — a single finished image.
Match reference aspect ratio [W:H]; use 4:3 only when source is already near 4:3.

SUBJECT INVENTORY (every item fully in frame with safe margin):
- [list people/animals/props + positions]

SPATIAL MAP (same moment, same space — medium change only):
- Road/path axis: [...]
- Lamp/primary light: [...]
- People groups + facing: [...]
- Depth layers FG/MG/BG/sky: [...]
Keep anchors in place; preserve place identity and primary left–right structure.

RECIPE: [full card language — look, color, layout, text, mood, acceptance]
IDENTITY/MEMORY: [...]
COLOR: from photo per recipe
TEXT: [sparse / none]
ACCEPTANCE: subjects complete; space intact; recipe dialect clear; styled only
```

Attach the source as `reference_image_paths`.

---

## Recipe cards (full)

Each card describes the **entire delivered image** (styled reconstruction only). Phrases like “from the photo” mean reference analysis — the output is the styled work.

**Spatial note for all recipes:** Style language may simplify or delete clutter while Shared hard rule 6 (spatial fidelity) stays locked. Off-center and whitespace are fine inside that lock.

**Layout note for all recipes:** Large negative space / off-center composition is welcome when every primary person, animal, and important subject stays fully in frame with a clear safe margin. Background or decorative type may be partial at the frame edge; people and animals stay complete.

### 1 — RISO Editorial
**Also called:** RISO stencil print + freehand line + editorial illustration (RISO孔版)

**Look:** Reconstruct memory points as RISO spot-print + freehand line + editorial illustration. Not photoreal. Lines simple and free: slight jitter, breaks, misregistration, imperfect closure — real hand + plate traces.

**Color / ground:** 2–4 spot colors extracted from the photo and redesigned (coral orange, peach pink, vintage blue, ultramarine, sage, cream yellow, soft violet, black, off-white). Allow slight misregistration, dot overlap, uneven ink, transparent layering. Prefer flat spot fields over complex gradients and smooth vector look. Warm paper grain, fine fiber, print dots, light ink stains — indie publication / art-book / handmade poster.

**Layout:** Small-to-mid subject + large negative space; off-center OK **with safe margin** so the full person/animal stays inside the frame. Simplify complex background; keep only necessary elements. Sparse arrows, star dots, numbers, dates, tiny flowers, coordinates, or hand symbols allowed.

**Text:** Short title / date / number / tiny note; small, light, restrained — art magazine / exhibition poster, restrained editorial stacks.

**Mood:** High-end, literary, warm, young, relaxed, modern, collectible.

**Acceptance:** Spot-print + freehand line dialect reads clearly; full primary subjects with margin; axis/lamp kept when still drawn; sparse editorial text; warm paper grain; single styled image.

---

### 2 — Old Newsprint
**Also called:** Old Newspaper Supplement / Sunday Culture Page / Editorial Newsprint Layout

**Look:** Like a real vintage culture supplement, weekend life page, or old newspaper feature — yellowed / off-white newsprint + multi-column editorial layout: main image zone, section heads, captions, sidebars, small labels, fine rules. Figure translates to newspaper hero art, **halftone** portrait, partial line drawing, or low-sat spot illustration. Keep only key memory points. Visible newsprint fiber, print dots, slight misregistration, fold, uneven ink, archive feel — tidy, archival.

**Color:** Strict: black, gray, aged paper white + **1–2** low-sat spots from photo (dull red, fog blue, olive, faded brown…).

**Layout:** Subject ~**40–60%** of the frame — balanced hero scale, not tiny, not full-bleed. Whole primary figure(s) readable inside the hero zone.

**Text:** Sparse — WEEKEND JOURNAL / CITY MEMORY / SUNDAY NOTES / CULTURE PAGE / Issue No.03 / Archive (or short Chinese culture-page labels if the user wants). No long body copy.

**Mood:** Vintage, literary, intellectual, restrained, culture-supplement, editorial, collectible publishing.

**Acceptance:** Reads as vintage culture supplement; halftone/low-sat hero art; whole figures in hero zone; 1–2 spot colors on aged paper; sparse labels; place clues coherent; styled only.

---

### 3 — Paper Theatre
**Also called:** Paper Puppet Theatre / Cut Paper Diorama / Handmade Paper Collage

**Look:** Real handmade paper-puppet stage — layered cut papers (colored paper, fiber paper, thick card). Head/arms/clothes may join with round paper fasteners / rivets / articulated joints — structure must be obvious. Background as foreground–figure–backdrop paper depth: sky, clouds, buildings, plants, flags, props simplified into height-offset paper layers (mini theatre / paper sculpture). Edges may show slight fray, tear, irregular cut, hand error; keep fiber, crease, press mark, glue trace, natural shadow — “real paper-made” at first glance.

**Color:** 3–5 main colors from photo + warm white/cream paper; desaturate; unify.

**Layout:** Keep key narrative elements rather than a full scene copy. Subject ~**50–70%** of the frame; off-center OK with full figure visible; use layer offset for stage depth. Paper cut edges are material texture — limbs stay complete behind the paper language.

**Text:** Sparse handwritten title/date/number/theatre note — PAPER THEATRE / A MOMENT IN THE WIND / SCENE 01 / TRAVEL MEMORY.

**Mood:** Handmade, fairy-theatre, artistic, vintage, gentle, narrative, collectible paper-craft publishing.

**Acceptance:** Obvious layered paper + fasteners; stage depth matches source depth bands; full figures; 3–5 unified colors on cream paper; sparse theatre notes; styled only.

---

### 4 — Pressed Flower
**Also called:** Pressed Flower Herbarium Collage / Botanical Specimen Poster

**Look:** Pressed flowers, botanical specimen, paper archive, natural-history collecting page. Dual (or key) subjects rebuilt from dried petals, leaves, twigs, translucent plant fragments, thin-paper collage into recognizable silhouettes and interaction. Optional plant labels, numbers, collection date, tiny Latin, fine annotation lines, specimen tape, stitches, press marks — like a holiday page in a high-end herbarium.

**Note:** Original source prompts often emphasize couples / smiles / gestures / holiday accessories / red–green festive mood when present; for non-holiday photos, keep herbarium language and drop forced Christmas props.

**Color:** 2–4 colors; cream / off-white / aged paper / light warm gray ground; large whitespace. Prefer soft red, pine green, cream, light khaki/gold when festive cues exist; always low-sat, gentle, quiet, light-vintage.

**Layout:** Subjects ~**45–60%** of the frame — readable specimen scale. Full primary people/animals as specimen silhouettes. Simplify away full background copy.

**Text:** Sparse — WINTER SPECIMEN / HOLIDAY MEMORY / collected joy / Dec.25.

**Mood:** Natural, feminine, collectible, festive (when relevant), gentle, literary, light-vintage, high-end publishing.

**Acceptance:** Herbarium collage dialect; full specimen silhouettes of primary subjects; 2–4 soft colors on cream ground; sparse labels; gentle archival mood; styled only.

---

### 5 — Travel Journal Sketch
**Also called:** Travel Journal Mirror Sketch / Pen & Colored Pencil / Light Watercolor

**Look:** Same instant, same scene as a travel-journal sketch. Relative positions, scale, facing, gaze, and spatial relations **highly match the reference photo** so a viewer recognizes the moment at a glance. Allow slight hand deviation, deletion, and generalization — handmade sketch language, not mechanical tracing or a sketch filter. **All primary people/animals fully in frame**, matching the source’s completeness.

**Medium:** Fine pen/pencil structure + colored-pencil hatching as main; only thin transparent watercolor washes. Lines natural and loose: breaks, restatements, imperfect closure, cross-hatching. Architecture keeps needed structure; figures/plants/distance moderate. Warm cream/ivory paper with visible fiber, pencil grain, colored-pencil friction, light hand traces. Watercolor only for sky, water, plants, local light — light coverage.

**Color:** From the reference photo, moderately desaturated; keep warm/cool relations; palette stays controlled.

**Text:** Optional handwritten short title and/or short line in whitespace (e.g. A Day Worth Remembering / Little Moments, Lasting Memories) — real pen feel, light pressure variation; tiny date/underline/heart only if restrained.

**Mood:** Warm, nostalgic, relaxed, literary, travel, real handmade, collectible travel-log.

**Acceptance:** Viewer recognizes the same instant; positions/scale/facing/gaze match; full people/animals; pen + colored-pencil + light wash on cream paper; sparse handwriting optional; styled only.

---

### 6 — Retro Silkscreen
**Also called:** Retro silkscreen + coarse-grain print + experimental editorial (复古丝网)

**Look:** High-contrast silhouette language, coarse halftone, granulated color blocks, partial spot-print — graphic print language, not fine photoreal tracing. Keep key face shape, hair, pose, memory points for recognizability. Print may feel like coarse-grain photographic silkscreen (grain is a **print material**, not a pasted photo).

**Color:** 2–4 high-recognition spot colors redesigned from photo (deep blue, brick red, ink green, cream white, black, orange-red, gray-violet…). Bold but controlled. Allow local misregistration, ink coverage, dots, wear, uneven print, rough edges — real silkscreen / old magazine reprint. Prefer flat/granulated fields over smooth gradients.

**Layout:** Large whitespace, strong contrast, bold type. Subject mid-scale; off-center OK **with safe margin**. Type may clip the **frame edge** or overlap background — faces, limbs, and animals stay clear of type. Reduce complex background to few environment clues. Sparse thick lines, numbers, arrows, color blocks, stamps, page marks, crop marks — restrained.

**Text:** Important visual element — short title/date/number/English. Bold sans, condensed, typewriter, or oversized type; may cross the frame or run vertical. Restrained editorial copy only.

**Mood:** Avant-garde, vintage, restrained, fashionable, experimental, indie publishing, art-school poster, collectible print.

**Acceptance:** Coarse silkscreen/halftone dialect; type clear of anatomy; key pose + place clues intact; 2–4 bold spot colors; full subjects with margin; styled only.

---

### 7 — JP B&W Line
**Also called:** JP healing B&W lifestyle illustration / fineliner hand-drawn feel (日系治愈线稿)

**Look:** Hand-drawn line look simulating fineliner/sign pen. Mostly B&W; flat fill + whitespace; light hatching rather than thick paint or complex coloring. Lines natural with slight jitter; outer contour slightly thicker; inner detail thinner; hair/folds/furniture/props may use light hatching; small black masses for rhythm/contrast.

**Layout:** Clean and airy; figure centered or mid-shot with full primary subject visible; background simplified to necessary props (bench, tent, sign, chair, window, ground…); gentle perspective; one clear focal center; clear whitespace. Quiet, relaxed, gentle, cute, daily — travel essay, lifestyle comic, daily picture book, indie illustrator.

**Text:** Tiny title/date/number/short line in corners or whitespace.

**Mood:** Fresh, healing, quiet, daily, cute, minimal, lived-in, lifestyle-comic.

**Best for:** People, travel, camping, street, casual daily photos.

**Acceptance:** Fineliner B&W lifestyle dialect; full mid-shot figure; necessary props only; same street/place family; quiet whitespace; tiny text optional; styled only.

---

### 8 — Naïve Doodle
**Also called:** Hand-drawn Doodle Lifestyle / Naïve Illustration / Marker Drawing

**Look:** Actively delete most irrelevant info; re-direct via deletion and scale change (**spatial anchors stay locked**). Simplify, symbolize, loose and personal. Jittery/broken/irregular hand lines; marker / crayon / oil-pastel-like natural fills; slight overshoot, show-through, hand error OK. Favor personal proportion and gesture over realist proportion, full perspective, or fine depiction.

**Whitespace is the core:** entity graphics are a **small** fraction; leave the rest empty on purpose. Subject may be off-center or floating — **still fully drawn**. Prefer less drawing over filling; delete clutter; keep primary subjects.

**Color:** Strict 2–3 main colors + black/dark gray lines + warm white paper. If the photo is chromatically complex, keep one key color-memory group — few, light, clean, unified.

**Text + layout:** Design as one system — invisible grid, visual axis, reading path. Words may hug silhouette, follow contour, sit in negative space; offset, interlock, asymmetric echo. Prefer organic placement over mechanical centering or stacked templates. Few meaningful words/short lines in natural handwriting with slight width/pressure variation; one clearer short line + tiny support text OK. Short phrases only.

**Mood:** Naïve drawing + mature composition + smart text–image relation + massive whitespace + sparse color = high-end indie magazine / lifestyle editorial illustration / art publishing — adult editorial, not children’s scrapbook.

**Acceptance:** Small fully-drawn people/animals; anchors locked; massive whitespace; 2–3 colors + dark line on warm white; smart sparse handwriting; adult editorial finish; styled only.

---

### 9 — Photo→Ink Sketch
**Also called:** Nostalgic photo→ink sketch page (怀旧素描)

**Look:** Loose B&W ink sketch of the **same** subject, pose, expression, wardrobe, composition, and mood as the reference photo, on warm textured paper. Soft nostalgic / filmic atmosphere in the drawing language (not by pasting a film photo). Minimal editorial layout, small heads, poetic handwritten title, tiny notes. Cream negative space, subtle paper texture, Japanese visual-diary aesthetics, warm nostalgia, natural anatomy. Full primary figure(s) as in the source. Clean frame (no watermark or logo).

**Mood:** Nostalgic, filmic, diary, art-book page.

**Acceptance:** Same subject/pose/wardrobe/composition/mood; full figures; warm paper B&W ink dialect; sparse poetic notes; single styled page (no photo+sketch comparison).

---

## 7. Workflow (operator)

1. **Intake** — photo required; vibe optional; recipe name optional; recommend by name (numbers internal).  
2. **Recommend & lock** — vibe map + photo heuristics; one recipe.  
3. **Explore (internal) — required**  
   - Identity / memory points  
   - **Complete-subject inventory (§1.3)**  
   - **Spatial map (§2.4)**  
   - Delete list = clutter only (inventory + spatial map stay intact)  
   - Palette; text yes/no  
   - Output size = source size/aspect (4:3 only if near)  
   - Flag left/edge-biased subjects (high clip risk)  
4. **Generate** — `reference_image_paths` = source. Prompt must include: styled only; size/aspect; **full people/animals with safe margin**; **same space — lock axis/lamp/groups/depth**; full recipe language; identity locks; acceptance criteria.  
5. **Self-review** — §8; fail → revise. Aspect fix: regenerate / pad / subject-aware crop — keep subjects whole.  
6. **Deliver** — finished styled image only; optional one short English or Chinese recipe name.

Batch: one output per photo; same recipe across a batch unless content clearly needs a switch (say so).

---

## 8. Self-review (positive checklist)

- [ ] **Styled reconstruction only** — single finished image  
- [ ] Size/aspect matches source (or 4:3 only because source was near 4:3); proportions preserved  
- [ ] **Every important person/animal (and pose-critical prop) fully in frame** with safe margin  
- [ ] **Spatial fidelity** — road/path axis, lamp/primary light, pedestrian-group relations & directions, depth layers; same place identity  
- [ ] Post-process kept off-center subjects whole (pad / subject-aware / regenerate)  
- [ ] Matches **locked recipe card** look, color, layout, text, mood  
- [ ] Memory points kept; clutter deleted; recognizability clear (esp. Travel Journal / Photo→Ink)  
- [ ] Palette per recipe; text sparse or absent  
- [ ] Recipe **Acceptance** criteria met  
- [ ] File attached  
- [ ] User received a recipe **name**, not a forced number  

---

## 9. Prompt must include (positive)

- One finished styled image — styled reconstruction only  
- Aspect/size: match reference (4:3 only if near)  
- **Full important subjects in frame with safe margin**  
- **Same space: lock road axis, lamp/primary light, pedestrian groups, depth layers**  
- Identity/memory locks from the reference  
- Full recipe-card essence (medium, color, layout, text, acceptance)  
- Shared hard rules + per-recipe Acceptance  

---

## 10. Refinement loop

1. Name the failing axis: **subjects complete?** or **space intact?** (or recipe dialect).  
2. Show evidence: raw vs out silhouette crop; or axis/lamp/group overlay notes.  
3. Change method (stronger inventory/map in prompt; different post-process; regenerate) — concrete fix, not apology-only.  
4. Re-check §8 before overwrite.  
5. When user accepts a batch, freeze files in `poster_demo*` naming and stop churn.

---

## 11. Out of scope (compact)

Keep this list short. Prefer the hard locks and Acceptance sections above for day-to-day guidance.

1. Delivering the source photo, photo strip, 50/50, or before/after diptych — emphatic ban in §0  
2. Face-swap / identity break / swapping the primary person  
3. Stretch, warp, or squash to force a ratio  
4. Cropping or truncating people, animals, or pose-critical props — see §1.1a  
5. Geometric center-crop through left/edge-biased subjects after whitespace  
6. Element-library recombination / relocating road axis, lamp, or pedestrian groups — see §2.1a  
7. Inventing foreign place architecture or a different street/city/valley  
8. Forcing 4:3 when source is not near 4:3  
9. Forcing recipe ID numbers on the user  
10. Default Q-chibi, glossy 3D plastic, neon/cyber candy, HDR skin polish  
11. Children’s scrapbook cheapness or dense commercial ad templates  
12. Optimizing palette/grain before subjects + space pass (F7)

---

## 12. Final doctrine

1. **Deliver styled reconstruction only.**  
2. **Keep every important person/animal fully in frame with safe margin.**  
3. **Same moment, same space — relative positions stay.**  
4. **Clutter may go; anchors and primary subjects stay.**  
5. **Match source aspect; use 4:3 only when source is near 4:3.**  
6. **Recommend recipes by name.**  
7. **Use poster_demo1/2 as regression memory.**  
8. **Subjects + space before color vibes.**  
9. **This skill stays long so “transfer” means the same place, restyled — not a pretty wrong place.**

---

*End of Photo Style Transfer Poster skill. Operator manual length (tens of KB), not a 5–10k blurb.*
