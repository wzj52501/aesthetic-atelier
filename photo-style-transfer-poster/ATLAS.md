# Photo Style Transfer Poster — ATLAS

On-demand: open this only when the user says style/space/crop is wrong, when self-review
fails subjects or space, or when you are about to regenerate after a failed attempt.

Demo roles (`source` / `gold` / `dialect-ref` / `fail-example`) are authoritative in
`../demo/MANIFEST.md`. Never treat a `fail-example` as a spatial pass.

---

## 4. Demo atlas — `poster_demo1` / `poster_demo2`

**Role discipline.** `../demo/MANIFEST.md` is authoritative for what each file is. Regression order: `source` first, then the `dialect-ref` files flagged as high spatial bar (⑤ travel-sketch, ⑨ ink-sketch). **Never** list a `fail-example` (batch B `style-08`) as a spatial pass, and never copy a `working-attempt` as a ship target.

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
- **See:** `demo/poster_demo2/style-08-naive-doodle.jpg` — `fail-example`. The autumn/winter split rewrites the place identity. Never use it as a spatial pass.

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
- **See:** `demo/poster_demo1/style-08-naive-doodle.jpg` — `working-attempt`. Pedestrian groups simplified; not a spatial pass.

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
