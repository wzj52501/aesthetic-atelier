# Photo Style Transfer Poster — CORE

Default-loaded law for this skill. Section numbers are kept from the original single-file
manual so cross-references (`§1.1a`, `§6c`, …) stay valid.

**Demo role discipline.** `demo/MANIFEST.md` is authoritative: only `source` and `gold` are
positive exemplars. `dialect-ref` teaches the look but proves nothing about aspect or space;
`working-attempt` and `fail-example` are for gap analysis only. The poster side's spatial
**gold** anchors are the aspect-matched `style-05-travel-sketch_matched.jpg` and
`style-09-ink-sketch_matched.jpg` of each batch.

**Recipe card rules — apply to every card in `recipes/`:**

Each card describes the **entire delivered image** (styled reconstruction only). Phrases like “from the photo” mean reference analysis — the output is the styled work.

**Spatial note for all recipes:** Style language may simplify or delete clutter while Shared hard rule 6 (spatial fidelity) stays locked. Off-center and whitespace are fine inside that lock.

**Layout note for all recipes:** Large negative space / off-center composition is welcome when every primary person, animal, and important subject stays fully in frame with a clear safe margin. Background or decorative type may be partial at the frame edge; people and animals stay complete.

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

## 6c. Post-process SOP (aspect / size) — including generator caps

### 6c.1 Measure first

1. Record source `W_s × H_s` and aspect `r_s = W_s / H_s`.
2. Record generator native output `W_g × H_g` (many pipelines cap at **1280×720**, `r_g = 16/9`).
3. “Near 4:3” means `|r_s − 4/3| ≤ 0.05` (about ±5%). Only then may you snap the deliverable aspect to 4:3.
4. Otherwise **the deliverable aspect must equal `r_s`** (tolerance `|r − r_s| ≤ 0.02`).

### 6c.2 When generator aspect ≠ source aspect (typical: 1280×720 vs a 4:3 raw)

**禁止**为了「铺满 16:9」或「去掉黑边」而对人物做几何中心裁切。

Order of preference:

1. **Regenerate** with explicit `W×H` / aspect = source (if the tool allows custom size).
2. **Pad / letterbox** the native canvas into a canvas with aspect `r_s`:
   - Compute the target canvas that contains the full generator image without cropping subjects (fit inside: scale uniformly until one side matches; pad the other side).
   - Pad color: recipe paper / flat field / subtle grain — not a random unrelated scene.
   - Keep every inventoried subject fully visible with safe margin (≥ ~3–5% of min side).
3. **Subject-aware crop** only if padding is impossible **and** the union bbox of all inventoried subjects + margin still fits the target aspect.
4. Re-run subject + space acceptance after any post-process.

### 6c.3 Demo regression note

Files under `demo/poster_demo*/style-*.jpg` are **generator-native 1280×720**. Treat them as **style / dialect references**, never as proof that 16:9 is correct. When studying spatial fidelity, compare structure on a **common aspect** (pad the style to the `raw` aspect, or compare after letterbox). `*_matched.jpg` companions exist for exactly this — see `demo/MANIFEST.md`. For gold acceptance of new runs, require the §6c.1 aspect match to the user's source.

---

## 6d. Generation prompt skeleton (copy / adapt)

State what to generate. Fill brackets from the source.

```
Create ONE finished styled reconstruction of the reference photograph.
Deliver styled reconstruction only — a single finished image.
Match reference aspect ratio [W_s:H_s] (r=[r_s]).
If the generator returns 1280×720 or any other aspect, do NOT center-crop to "fill".
Pad/letterbox to r_s with recipe ground; keep all inventoried subjects inside with margin.
Use 4:3 only when |r_s - 4/3| <= 0.05.

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
