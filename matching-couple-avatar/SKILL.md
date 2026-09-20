---
name: Matching Couple Avatar
description: >-
  Use when the user asks for a separate pairing avatar that matches their given
  portrait (couple set / matching PFPs / 情侣头像): leave their image unchanged;
  generate one independent partner with strong source reference, pixel-level
  local locks; **禁止** starting generation from coarse labels alone; Chinese 对子
  complementarity (complementary mate, not mirror copy), locked spatial/face/brightness/tone/line grammar, and co-framed
  background — see avatar_demo failure atlas in the pack.
---

# Matching Couple Avatar

> **Pack demos (required reading when available):**  
> `high-aesthetic-skills-pack/avatar_demo/`  
> Files: `1L`/`1R`/`1L_gen`, `2L`/`2R`/`2L_gen`, `3L`/`3R`/`3L_gen`, `4L`/`4R`/`4L_gen`  
> (`L`/`R` are **set IDs**, not “left/right of frame”. Facing direction is read from pixels.)

This skill is the specialty path under High Aesthetic Image Expert for **couple / matching PFPs / 情侣头像**. It is intentionally long: short “vibe” skills cause the exact failures documented in the atlas. Read the hard locks, run the study protocol, then generate. Build a measured, reference-anchored brief before any one-line prompt.

---

## 0. One-sentence goal

Produce **one new standalone partner portrait** that:

1. leaves the user’s source portrait file unchanged; deliver only a new partner file,
2. is **visibly a different picture** (fresh identity and props; shared drawing dialect),
3. shares nearly the same **drawing dialect** as the source (line material, spatial habits, face recipe, brightness/cast, motif grammar),
4. forms Chinese **对子** complementarity with the source (opposites that pair), as a complementary mate rather than a mirror clone,
5. keeps **person + background** co-framed — environment stays inside the square whenever the source has environment.

---

## 1. Hard locks — generation drivers

### 1.1 Primary control: pixel-level source features

Drive generation from **observable local features of the source** — line weight, contour breaks, blush hatch, palette RGB, grain, hair clump structure, iris/mouth recipe — with the source image and micro-crops as the primary reference pack.

Genre or mood labels (`anime`, `manga`, `xianxia`, `hanfu vibe`, `watercolor style`, `cute`, `ethereal`, `dreamy`, `soft girl`, and similar) may appear **only after** concrete, source-derived locks are already written into the brief (geometry, stroke behavior, RGB/cast, background structure), and only as a subordinate clause (one clause max). When the prompt is mostly tags, rewrite it around measurements and crops.

| Prefer as primary control | Why it works |
|---|---|
| Line weight / break pattern from hair and profile crops | Locks the source’s stroke dialect |
| Face landmark gaps + eye/nose/mouth recipe from crops | Keeps the same feature grammar |
| Measured face % of canvas + motif placement | Preserves pairability with the source |
| Sampled RGB/luma and wash behavior | Holds cast and paper/field feel |
| Background mass side + foliage drawing method | Keeps co-framed environment |


### 1.1a Emphatic bans (keep these)

Positive locks above are the default voice. These bans stay explicit because they are the recurring failure mode:

1. **禁止仅使用粗 label / 粗粒度 tag 就开始生成。**  
   Forbidden: opening generation with only coarse labels such as `anime`, `二次元`, `manga`, `xianxia` / `同款仙侠`, `hanfu vibe`, `watercolor style`, `cute`, `ethereal`, `dreamy`, `soft girl`, or “same filter as ref.”  
   Required first: pixel-level / measured locks from the source (and micro-crops), then generate.

2. **禁止改写或覆写用户原头像文件。** Deliver only a new partner file; leave the source path untouched.

3. **禁止把镜像翻转 / 同向朝向 / 1:1 配件复制当成对子解。** Facing is opposite so the pair looks toward each other; props follow 对子 logic.

4. **禁止用人像特写裁切吃掉源图构图级背景。** Person + background stay co-framed when the source has environment.

### 1.2 Strong source reference protocol

Before any `GenerateImage` call:

1. Open the source at full resolution.
2. Write internal locks (see §5–§9).
3. Export micro-crops for the locks that matter most this run (especially **stroke** and **eye/mouth**).
4. Build the prompt as **reference-anchored instructions** + measured locks.
5. After generation, **open the output** and compare side-by-side to the source (and to `*_gen` demos when iterating).

### 1.3 Fidelity axes to lock (relative to source dialect and pair logic)

1. **Spatial structure** — subject scale, head/face % of frame, negative space, motif placement side, depth layering.
2. **Facial detail grammar** — eye/nose/mouth/ear recipe (dash mouth vs full lips; pale iris vs dark; nostril present/absent; lash clumping).
3. **Brightness** — whole-frame luma / high-key vs crushed; clothing 对子 may darken/lighten garments while skin and field stay near source.
4. **Color cast / tone** — cool grey-blue vs warm peach; desaturation level; blush hue.
5. **Lines / stroke material** — the #1 recurring real failure when users say the style is completely wrong.

Treat the source as a specific spatial + stroke + wash system to re-enter. A single genre label is a summary, not a lock — **禁止** using it alone to start generation (§1.1a).

### 1.4 Non-VAE reconstruction (content ≠ identity)

Users often want:

- **Clearly different content** from any exemplar partner (different face identity, prop, bun/flowers, earring, foliage layout),
- **Nearly identical visual grammar** (stroke, cast, spatial quality, face *recipe*).

Score on dialect match + 对子 readability. A stock soft-girl watercolor in another illustrator’s hand fails even when brightness is close.

---

## 2. 对子 — couple symmetry as complementary opposites

### 2.1 Definition

In this skill, “symmetry” means Chinese couplet logic (**对子**), not geometric mirroring and not identity clone.

**Shared layer (match):**

- stroke material and line weight family,
- face simplification level / feature recipe family,
- palette grammar and paper/wash behavior,
- motif *language* (how flowers, hearts, branches are drawn),
- spatial *habits* (how much empty field, how foliage sits relative to the head).

**Complementary layer (differ on purpose):**

| Axis | Example 对子 |
|---|---|
| Value / robe | dark navy robe ↔ pale mist robe |
| Facing | right profile ↔ left profile |
| Active / passive | hand holding a stem ↔ quiet empty hand + floating motif |
| Motif split | line-art heart on open field ↔ blossom cluster in hair / held sprig |
| Weather / element metaphors (conceptual) | 白对黑、云对雨、雪对风、晚照对晴空、来鸿对去雁 — use as *design thinking*, not as text in the image |
| Gender / role | as briefed; still same drawing hand |

### 2.2 Acceptance — couple logic pass

A pass looks like:

- Partner facing opposite the source so the pair can “look toward” each other.
- Clear complementary plan on at least one primary axis (value, prop, or motion).
- Shared stroke/palette/motif language with the source.
- Accessories related but reallocated (completing the couplet), not pasted 1:1.
- Robe value or another visible opposition when the brief calls for strong 对子 (weak gender-only swap is a soft miss).

### 2.3 Cross-frame continuity

When the source implies a diptych world:

- Gaze height roughly continuous across the pair.
- Shared cool field / shared pink blossom language.
- Split motifs that complete each other (heart on one side, stem/flower on the other) without needing both people in one frame.

---

## 3. Person is primary — background stays co-framed

### 3.1 Rule

Portrait focus keeps the environment. If the source has soft foliage / branch washes, floating line motifs (heart, bow, sparkles), paper texture fields, or petal dabs, the partner keeps **co-framed** background grammar (mirrored or 对子-shifted placement). Blank studio cutouts match blank sources only.

### 3.2 Typical background 对子 placement

- Source faces **right** with foliage mass on the **outer/back** side → partner faces **left** with foliage on their **outer/back** side (usually the opposite canvas side).
- Open-field motif (e.g. thin line heart) sits in the negative space in front of the face — preserve the *idea* of a sparse open-field mark when the source has one; keep clutter low.

### 3.3 Acceptance — background pass

A pass looks like:

- Outer-third foliage/wash present when the source has it.
- Placement follows outer/back logic relative to facing.
- Hair edges interleave with wash (some overlap), reading as one drawing session.
- Background crops were attached as references for the generate call.

When a gen ships a careful face and an empty field, regenerate with background crops and placement locks as first-class refs (environment is part of the PFP, not a post sticker).

---

## 4. Study protocol — what to lock from the source

Work top-down. Skip nothing on picky briefs.

### 4.1 Canvas & identity of files

- Record `W×H`. Output matches source resolution (e.g. 1080×1079).
- `L`/`R` filenames are set IDs only.
- If a true-match exemplar exists in `avatar_demo` (`*R`), study it **when the user allows** or when the brief is to learn the approved pair language. Default for new user photos: **source-only** unless told otherwise.
- Teach from **observable** pair grammar only.

### 4.2 Orientation

- Facing: left / right / three-quarter.
- Partner facing: opposite.
- Verify after any flip by opening files — heuristics lie.

### 4.3 Spatial measurements (write numbers)

- Face height brow→chin as **% of canvas height** (soft full-figure avatars often ~10–12%H; closer bust portraits may be ~15–20%H — **measure**).
- Head mass (hair apex→chin) %.
- Robe/body mass in lower frame %.
- Negative-space %.
- Landmark chain: eye, nose tip, mouth, chin, ear, hair apex — x/y and %W/%H.
- Gaps: eye→nose, nose→mouth, mouth→chin (px and %H).
- Nose projection (profile).

**Acceptance:** gen face % within ~2–3pp of the source’s composition class. Source face ~11%H with gen face ~35–40%H (headshot zoom) fails spatial lock.

### 4.4 Face recipe

- Skin RGB / cast.
- Blush placement and hue.
- Eye: iris value/hue, catchlight count, lash clumping (few thick clumps vs many realist lashes).
- Nose: single pointed stroke vs modeled volume; nostril yes/no.
- Mouth: short dash length vs full lip render; lipstick fill yes/no.
- Moles / earrings / ornaments.

### 4.5 Stroke & line material (critical)

This axis is where “style completely wrong” most often truly lives — beyond “too bright/too clean” alone.

Observe and match:

- Line color family (charcoal grey vs pure black).
- Line weight variability (tapered digital sketch vs uniform vector).
- Continuity (broken/overlapping vs single clean contour).
- Hair construction: **tonal clumps + moderate tapered flyaways** (stylized digital) when that is what the source shows; stay in that family rather than sliding into hyper-real graphite filament fields or smooth cel slabs.
- Whether washes sit *under* sketch lines or replace them.

Documented misfires: chasing “more sketchy” by sliding into realistic pencil-strand portraits; polished commercial soft-girl lines that ignore the source’s uneven grey pencil-like contours.

Export stroke micro-crops: hair flies, lash zone, profile edge, robe fold lines.

### 4.6 Hair / costume / props

- Bun / ponytail / ahoge architecture.
- Flower-in-hair vs held sprig vs floating motif — 对子 split.
- Robe collar language and value (dark↔pale 对子).

### 4.7 Background

- Foliage: outlined leaves vs soft unoutlined washes.
- Placement side and density.
- Accent pinks / blues RGB.
- Sparse line motifs in open field.

### 4.8 Global tone

- Mean RGB / luma of full frame.
- Std of channels (flat wash vs grainy).
- High-key white field vs mid-grey mud.
- Clothing 对子 limited to garments so skin/bg stay clear.

---

## 5. Explore — 3–6 internal locks (minimum)

Always include:

1. Opposite facing + 对子 robe/value (or other clear complementary axis).
2. Face scale % (within ~2–3pp of source habit for that composition class).
3. Stroke material family (from micro-crops).
4. Eye/nose/mouth recipe.
5. Background co-frame plan (side + density).
6. Global luma/cast target.

Optional seventh: prop 对子 (held stem vs open-field heart, etc.).

---

## 6. Generate — procedure

### 6.1 References

Pass:

- full source,
- stroke crops,
- face feature crops,
- background crop,
- optional flipped source **only as spatial packing hint** (spatial packing, not partner identity).

Prefer source (+ approved exemplar if user allows). Anchor on source crops rather than prior failed gens (keeps dialect stable).

### 6.2 Prompt shape (positive locks)

Order:

1. Task: new independent partner; leave source unchanged; square same size.
2. Facing + 对子 content plan.
3. Spatial % locks.
4. Stroke material locks (state the family to match: clumped variable grey digital sketch, etc.).
5. Face recipe locks.
6. Background co-frame locks.
7. Brightness/cast locks.
8. Delivery clean: one person, finished square, print-ready (no text/UI/guide boxes; single PFP unless a diptych was asked).

### 6.3 Aspect ratio & crop safety

Many generators emit 16:9 even when you ask 1:1.

**Delivery rule:**

1. Prefer native square.
2. If landscape: **height-fit** (preserve full vertical) then slide a horizontal window.
3. Keep the full face and co-framed background inside the square with safe margin — bun apex and chin both inside with air.
4. Verify margins before ship.
5. Ship clean finals (no orange guide boxes, wireframes, or debug overlays).

### 6.4 Redraw under better locks

When a generation misses dialect or face recipe, regenerate under tighter locks and source crops. Global luma nudges after a *good* dialect match are fine. Feature painting on a wrong dialect (mouth dash paint-overs, alpha composites that shatter pale robes) stays out of the delivery path.

### 6.5 Candidate discipline

When dialect is hard, generate 2–3 candidates anchored on the **same source crops**, then pick by **stroke + face recipe** side-by-side — same art system first, “prettier in another hand” second.

---

## 7. Self-review checklist (ship when all pass)

### Identity & format

- [ ] Source file untouched; only a new partner file delivered
- [ ] One partner only; standalone
- [ ] Resolution matches source
- [ ] Clean square: no watermark/text/UI/guide boxes

### Couple logic

- [ ] Facing opposite
- [ ] Reads as 对子 (complementary), shared grammar with clear opposition
- [ ] Shared stroke/palette grammar with source

### Spatial

- [ ] Face/head % within tolerance of source class
- [ ] Full head in frame (bun + chin margins)
- [ ] Same composition class as source (field/bust, not accidental headshot zoom)

### Face

- [ ] Eye/nose/mouth recipe matches micro-crops
- [ ] Mouth/iris family follows source (dash + pale iris stays dash + pale iris)

### Stroke

- [ ] Line material matches source dialect (clumped variable digital sketch when that is the source family)
- [ ] Hair filament density in the same family as source

### Tone

- [ ] Global luma/cast close; clothing 对子 kept on garments

### Background

- [ ] Environment grammar present when source has it
- [ ] Placement follows 对子 / outer-side logic

Open the files. Confirm each box from pixels.

---

## 8. Demo atlas — `avatar_demo/` (how to learn, refine, pass)

Path (user pack): `high-aesthetic-skills-pack/avatar_demo/`  
Also sync copies under agent workflows / box packs when present.

| ID | Source | Exemplar pair | Partner output |
|---|---|---|---|
| 1 | `1L.jpeg` | `1R.jpeg` | `1L_gen.jpeg` |
| 2 | `2L.jpeg` | `2R.jpeg` | `2L_gen.jpeg` |
| 3 | `3L.jpg` | `3R.jpg` | `3L_gen.jpg` |
| 4 | `4L.jpg` | `4R.jpg` | `4L_gen.jpg` |

Study method:

1. Open `nL` and lock facing, scale, stroke, face recipe, bg, cast.
2. Open `nR` as **pair grammar exemplar** (how 对子 was resolved in an approved set) when learning from the pack.
3. Open `nL_gen` as a working partner attempt — compare to `nL` for dialect match and to the pair for couple readability.
4. Catalogue gaps → regenerate with tighter locks.

### 8.1 Failure atlas (English titles) — regression memory

Use these as mental regression tests before shipping.

#### F1 — Tag-led stock dialect

- **Symptom:** Output looks like stock soft-girl / fantasy-costume illustration unrelated to `nL` stroke.
- **Cause:** Prompt led with genre labels instead of measurements.
- **Pass path:** Attach `nL` + crops; describe observed stroke/face/bg; keep any mood word subordinate.
- **Refine:** Side-by-side `nL` vs gen focusing on **line edges** and **eye recipe**, not overall prettiness.

#### F2 — Spatial collapse (headshot zoom / unsafe square crop)

- **Symptom:** Face jumps from ~11%H to ~30%+H; or bun/forehead sliced after 16:9→square.
- **Cause:** Face % unwritten; landscape center-crop without height-fit slide.
- **Pass path:** Write face % into locks; height-fit then slide; verify bun/chin margins.
- **Refine:** Measure face % on the candidate before overwrite.

#### F3 — Background abandonment

- **Symptom:** Decent face, empty field; user asks where the branches/petals went.
- **Cause:** Portrait-only focus; no foliage crop in refs.
- **Pass path:** Always include bg crop; describe outer-side wash placement.
- **Refine:** Compare right/left outer thirds to source.

#### F4 — Mirror clone instead of 对子

- **Symptom:** Same robe value, same motifs, same energy; reads as twin cosplay.
- **Cause:** “Matching” read as copy.
- **Pass path:** Explicit complementary plan (pale↔dark, held sprig↔open-field mark, etc.).
- **Refine:** Ask: what is the couplet opposition?

#### F5 — Wrong stroke dialect (the silent killer)

- **Symptom:** User reports style/line material wrong even when colors are muted and composition is vaguely similar.
- **Cause A:** Commercial smooth lines / plastic skin.
- **Cause B:** Over-correction into hyper-real graphite filament hair.
- **Pass path:** Match **clumped, variable-thickness digital sketch strokes** when that is what `nL` shows; use hair/lash micro-crops; state the stroke family to match in the prompt.
- **Refine:** Crop hair regions of `nL` vs gen at matching scale; judge stroke family only.

#### F6 — Proxy metric chasing

- **Symptom:** Endless fixes to brightness/crop while dialect stays wrong; user reads it as perfunctory apology.
- **Cause:** Optimizing easy numbers instead of stroke/face grammar.
- **Pass path:** If user names an axis (e.g. stroke), make that axis the primary acceptance test.
- **Refine:** One primary axis per iteration; show compare crops for that axis.

#### F7 — Patching a failed base instead of redrawing

- **Symptom:** Broken composites, painted mouths, floating tiles, muddy alpha on pale robes.
- **Cause:** Local patches on wrong base.
- **Pass path:** Regenerate from source refs; gentle global tone match only after dialect is accepted.

#### F8 — Clothing value 对子 bleeding into the whole frame

- **Symptom:** Dark-hoodie/pale-robe opposition crushes entire frame into grey mud or bleaches skin.
- **Cause:** Value shift applied globally.
- **Pass path:** Limit strong value 对子 to garments; keep skin/bg/global luma near source.

### 8.2 Per-demo teaching notes (pack)

#### Demo 1 — `1L` / `1L_gen` (/ `1R`)

- Practice: opposite facing; shared motif language; verify after flips.
- Watch: hand/finger recipe if present; keep hands as flat as the source when the source is flat.

#### Demo 2 — `2L` / `2L_gen` (/ `2R`)

- Practice: stronger local feature matching (cloth folds, hair masses).
- Watch: background shapes staying in the same simplification family.

#### Demo 3 — `3L` / `3L_gen` (/ `3R`)

- Practice: hoodie/value 对子 with stable global luma.
- Watch: face scale and stroke consistency under larger clothing masses.

#### Demo 4 — `4L` / `4L_gen` (/ `4R`)

- Practice: high-key cool field; profile pair; pale↔dark robe 对子; sparse open-field mark vs floral/hair props; soft unoutlined foliage washes.
- Watch especially: **stroke material**, **background co-frame**, **non-VAE difference** (partner is a new drawing in the same hand), **pixel-level locks over genre labels**.
- When learning from the pack, compare `4L`↔`4L_gen` for dialect and `4L`↔`4R` for how an approved pair resolves 对子 — both as observable pair grammar.

---

## 9. Refinement loop

1. **Name the axis** the user cares about (stroke / space / bg / 对子 / face recipe).
2. **Show evidence** — side-by-side or micro-crop compares for that axis.
3. **Change the method** for that axis (refs, locks, crop policy) — method change, not apology-only.
4. **Regenerate** under the new method.
5. **Re-measure** face %, luma, and stroke family.
6. Stop when the user accepts; if they pick a prior candidate, **freeze that file** as `*_gen` and halt churn.

---

## 10. Intake (ask only what’s missing)

Need:

- Source image
- Partner cues if any (gender/hair) — else infer complementary partner
- Motif keep/swap
- Count (one preview default)
- Whether pack exemplars / true-match R may be studied

If already provided, start.

---

## 11. Relationship to High Aesthetic Image Expert

Fixed aesthetic core still applies: restraint; relationship-first; color from content; sparse decoration; whitespace as design; deconstruct 3–6 facts then reconstruct; deliver finished work only.

This sub-skill **adds** couple-specific law: pixel-level locks over coarse tags, 对子 complementarity, background co-frame, stroke fidelity, spatial % discipline.

---

## 12. Appendix A — prompt skeleton (fill with source facts)

```
TASK: Independent partner portrait for couple PFP / 情侣头像.
Leave the user's source portrait file unchanged; deliver a new partner file only.
FORMAT: Same W×H as source; one person; clean finished square.

COUPLE / 对子:
- Source faces {DIR} → partner faces {OPP}.
- Complementary plan: {robe value / prop / motif split}.
- Shared drawing hand with source references (same dialect, new identity).

SPATIAL LOCKS:
- Face height ≈ {x}%H; head ≈ {y}%H; negative space habits as source.
- Landmark gaps: ...
- Full head margins (bun apex + chin) with safe air.

STROKE LOCKS (primary):
- Match hair/profile/lash crops: {clumped variable grey digital sketch / ...}.
- Line color family: {charcoal grey / ...}; weight: {tapered uneven / ...}.

FACE LOCKS:
- Eye/nose/mouth recipe from crops: ...

BACKGROUND LOCKS:
- Outer-side foliage/washes: ...
- Open-field sparse motif if source has one: ...

TONE LOCKS:
- Global luma/cast ≈ source; clothing 对子 limited to garments.

CONTENT: Clearly new identity/props vs any exemplar; same dialect.
```

---

## 13. Appendix B — quick acceptance test (30 seconds)

1. Squint: do source and gen look like the **same artist session**?  
2. Zoom hair edge: same **stroke family**?  
3. Check face % and bun margins.  
4. Check outer background third.  
5. Check 对子 (facing + value/prop opposition).  
6. If user named an axis, test **only that axis** before anything else.

If any miss → regenerate with tighter locks for that axis.

---

## 14. Appendix C — glossary

| Term | Meaning here |
|---|---|
| Source / `L` | User portrait to keep unchanged |
| Partner / `*_gen` | New standalone matching avatar |
| Exemplar / `R` | Approved pair mate in demos (grammar reference when allowed) |
| 对子 | Complementary opposition + shared grammar |
| Dialect / drawing hand | Stroke + face recipe + wash + spatial habits as a system |
| Coarse tag | Genre/mood keyword used as primary generation driver |
| Non-VAE | Different content, same dialect — fresh drawing, same hand |
| 情侣头像 | Couple / matching PFP set (activation concept) |

---

## 15. Deep dive — reading a source like a production board

When you open `nL`, narrate locks in this order (internal; user-facing delivery stays image-first):

### 15.1 Pass A — silhouette & field

- Where is the largest empty region?
- Is the subject left-weighted, right-weighted, or centered?
- Does hair break the top margin or sit with air?
- Is the garment a dark mass or a pale wash mass?

### 15.2 Pass B — profile mechanics

For a true profile:

- Brow ridge continuity into nose.
- Eye as a stack: crease / lid / lashes / iris / catchlight.
- Philtrum length implied by nose→mouth gap.
- Chin round vs pointed.
- Ear vertical span vs eye–nose band.

Write the gaps in px **and** %H so generators that ignore px still see ratios.

### 15.3 Pass C — stroke archaeology

Zoom to 200–300%:

- Are hair edges **clumps with a few flyaways** or **filament carpets**?
- Do robe folds use 1–2 light strokes or dense hatching?
- Is the profile edge a single grey polyline with breaks?
- Do lashes form 3–7 clumps or a continuous fringe?

Photograph these with micro-crops. Clarity here means readiness to generate.

### 15.4 Pass D — pigment islands

Sample:

- Open bg
- Skin mid
- Blush peak
- Hair dark / mid
- Robe hi / shadow
- Foliage blue / pink accents
- Line dark

Store RGB + luma. Use them as fences, not as poetry.

### 15.5 Pass E — motif inventory

List every non-person mark:

- held object
- hair ornaments
- floating line icons
- branch washes
- sparkles / petals

Partner **reallocates** this inventory under 对子, keeping the motif language alive.

---

## 16. 对子 design workshop (expanded)

### 16.1 Classical pairs as design metaphors

Use these as **thinking tools** when inventing complementary content (keep Chinese couplet text out of the image pixels unless asked):

| Pair | Design translation for avatars |
|---|---|
| 白对黑 | Pale robe ↔ charcoal/navy robe; light field accents ↔ dark hair mass emphasis |
| 云对雨 | Soft unoutlined washes ↔ slightly denser dabbed petals |
| 雪对风 | Still pose ↔ flyaway-heavy hair motion |
| 晚照对晴空 | Warmer micro-blush ↔ cooler high-key field (keep shared cast family) |
| 来鸿对去雁 | Motif arriving (held sprig toward chest) ↔ motif departing (open-field mark ahead of face) |
| Mountain ↔ water | Solid hair bun architecture ↔ flowing shoulder strands |
| Long ↔ short | Long earring ↔ tight stud / none |
| Open ↔ closed | Slightly parted mouth dash ↔ closed shorter dash |

### 16.2 Choosing one primary opposition

Pick **one** dominant 对子 axis per run so the pair reads instantly:

- Value (most common for demo 4 class): dark↔pale garment.
- Prop: held botanical ↔ floating line heart.
- Motion: calm hair ↔ wind-cut flyaways.

Secondary oppositions can exist; keep them subordinate to the primary.

### 16.3 Shared grammar checklist while opposing

Even when opposing value/prop:

- Same line color family
- Same desaturation band
- Same eye simplification tier
- Same foliage *drawing method* (wash vs outline)
- Same paper/empty-field behavior

---

## 17. Stroke cookbook — matching line material with pixel locks

### 17.1 Source dialects you will actually see

1. **Clumped digital sketch** (common in soft couple PFPs): hair = soft grey masses + tapered sketch strokes + limited flyaways; profile = thin broken grey; lashes = few clumps.
2. **Flat cel-adjacent**: hard closed contours, smooth fills — match only when source truly is this.
3. **Painterly wash-first**: color blobs dominate; lines sparse.
4. **Graphite study**: hundreds of strand lines, paper tooth, mono — stay out of this family when fixing “sketchiness” if source is (1).

### 17.2 Prompt language that targets stroke (tag-free)

Prefer:

- “tapered uneven dark-grey sketch strokes”
- “hair built from soft tonal clumps then moderate flyaways”
- “broken profile polyline, charcoal grey not pure black”
- “lash clumps like the crop (approx N groups)”

State the observed family. Genre lineart/mood tags as standalone drivers stay out of the prompt lead.

### 17.3 Compare protocol for stroke acceptance

1. Crop source hair edge 400×400.
2. Crop gen hair edge 400×400 at similar relative location.
3. Judge: clump vs filament carpet vs cel slab.
4. On mismatch, regenerate with stronger crop refs and clearer stroke-family language — keep post blur/sharpen off the stroke-fake path.

### 17.4 Known over-corrections → better moves

| Intent | Drift risk | Better move |
|---|---|---|
| More like hand-drawn | “Detailed individual hairs” → graphite dialect | Lock clumped digital strokes from crops |
| More premium | Smooth everything → commercial soft-girl | Keep uneven grey contour family |
| More artistic | “Watercolor paper texture” keyword → poster-wash | Sample wash RGB from source crops |
| Match soft look | Raise exposure only → proxy theater | Primary axis = stroke/face recipe |

---

## 18. Spatial engineering & delivery math

### 18.1 Face percent classes

| Class | Face brow→chin | Typical framing |
|---|---|---|
| Small-face field portrait | ~9–13%H | Lots of air; motifs matter |
| Medium bust | ~14–20%H | Head + upper chest |
| Close character crop | ~22%H+ | Rare for these demos; measure |

Always measure the actual source. Demo 4-class sources often sit in small/medium — blowing to close-up destroys pairability with `nL`.

### 18.2 Landscape generator survival pipeline

```
raw_gen (e.g. 1280×720)
  → height-fit to H=source_H (or 1080)
  → find content bbox
  → choose x0 so: full head, preferred motifs (open-field mark + outer foliage) retained
  → if bun touches y=0, pad top with bg sample RGB then resize back
  → final resize to exact source W×H
  → open & verify
```

### 18.3 Delivery acceptance

A pass looks like:

- Uniform scale into exact source W×H (square preserved).
- Open-field motif and outer foliage retained in the crop window.
- Pale robes continuous with clean alpha / no speckled composite.
- Finals free of debug overlays.

---

## 19. Background engineering

### 19.1 Wash foliage

When source foliage is unoutlined:

- Describe “soft translucent cool-grey/blue/pink blobs, no hard leaf contours”.
- Attach foliage crop.
- Place on outer/back side relative to facing.

### 19.2 Sparse open-field marks

When source has a thin heart / bow / sparkle:

- Keep stroke ultra-thin and sparse.
- Place in negative space ahead of face.
- Preserve sparseness (one clear mark family, not a sticker cluster).

### 19.3 Integration test

Hair edges should interleave with wash (some overlap), reading as one co-framed drawing.

---

## 20. Worked failure→fix stories (anonymized patterns)

### Story A — “Only the person”

Generator returned a clean profile on white. User asked for background.  
**Strong response:** add foliage crop + placement locks; regenerate; show outer-third compare.

### Story B — “Style completely wrong”

Team debated exposure. User clarified: not brightness — **stroke**.  
**Strong response:** hair micro-crop compare; lock clumped digital strokes; stay in source stroke family.

### Story C — “Redraw rather than patch”

Local mouth painting and matte composites worsened artifacts.  
**Strong response:** freeze rule — redraw from source refs only.

### Story D — “Not VAE reconstruction”

Near-copy of an exemplar bored / angered the brief.  
**Strong response:** change identity/props while freezing dialect locks; score = dialect + 对子, not euclidean nearness to exemplar.

### Story E — Tag-led stock

Prompt led with fantasy-genre labels; output became stock costume art.  
**Strong response:** rebuild prompt from measurements and crops.

---

## 21. Batch mode (1L–4L)

When processing a folder like `avatar_demo`:

1. For each `nL`, run full study independently (fresh locks per ID).
2. Keep a table: facing, face%, stroke class, bg class, 对子 plan, luma.
3. Generate partners one-by-one; verify each before next.
4. Name outputs `nL_gen` with same suffix family as source.
5. Optional: contact sheet `nL | nL_gen | nR` for pack QA — finals stay clean (debug annotations in a separate file).

---

## 22. QA contact sheet recipe

Create `compare_n.jpg`:

- Column 1: source `nL`
- Column 2: `nL_gen`
- Column 3 (pack learning): `nR` exemplar

Annotate lightly in a *separate* debug file if needed; finals stay clean.

Minimum crops beside the sheet:

- hair stroke pair
- eye pair
- outer background pair

---

## 23. Integration with agent behavior

- Default user language for this agent may be Chinese; **skill text stays operational English** with Chinese 对子 / 情侣头像 activation terms preserved.
- Deliver finished images first; explain only when asked — and **internally** still run full study.
- If the user names a single pain axis, that axis becomes the acceptance gate.
- If the user selects a prior candidate as final, overwrite `*_gen` with that file and stop regenerating.

---

## 24. Pre-flight script (mental)

```
[ ] Source opened
[ ] Facing locked → opposite planned
[ ] Face% measured
[ ] Stroke class named + crops exported
[ ] Face recipe locked
[ ] Background plan locked
[ ] 对子 primary axis chosen
[ ] Luma/cast sampled
[ ] Prompt led by pixel locks (tags subordinate or absent)
[ ] Refs attached
[ ] After gen: open files
[ ] Stroke crop compare pass
[ ] Face% pass
[ ] BG pass
[ ] 对子 pass
[ ] Exact size save
```

---

## 25. Appendix D — mapping user complaints to actions

| User says (often Chinese) | Likely real axis | Action |
|---|---|---|
| Style wrong / looks off | Dialect / stroke | Hair crop compare; regenerate with stroke locks |
| Line material / stroke wrong | Stroke | §17 cookbook; lock source stroke family |
| Where is the background? | Background | §3 + §19 |
| Face got cropped | Delivery crop / scale | §18 |
| Too much like a copy / VAE | Content identity | Change props/face; keep dialect |
| Skip coarse tags | Prompt hygiene | §1 |
| Redraw, leave old gen alone | Process | Redraw only |
| Symmetry / pair feels wrong | 对子 | §2 / §16 |

---

## 26. Appendix E — what “almost identical style” allows to change

**May change:** identity, gender (if briefed), hair architecture details, ornaments, held props, exact petal positions, minor expression, earring design — under same dialect.

**Keep locked:** stroke family, face simplification tier, cast band, spatial class (small-face vs close-up), background drawing method, couple facing logic.

---

## 27. Appendix F — pack path reference

Primary user pack:

`/home/zijianwang/Pictures/high-aesthetic-skills-pack/`

Relevant entries:

- `matching-couple-avatar/SKILL.md` — this skill
- `avatar_demo/` — demos `1L`–`4L` with gens and exemplars
- `high-aesthetic-image-expert/` — parent aesthetic law
- `photo-style-transfer-poster/` — unrelated specialty; keep pipelines separate

Agent workflow mirrors:

- `matching-couple-avatar-2` / `matching-couple-avatar`
- `high-aesthetic-skills-pack/matching-couple-avatar`

Keep these synchronized when the skill updates.

---

## 28. Final doctrine (memorize)

1. **Pixel-level locks lead; tags stay subordinate.**  
2. **Strong reference beats genre summary.**  
3. **对子, complementary mate.**  
4. **Background co-frames the person.**  
5. **Stroke truth over proxy metrics.**  
6. **Measure space; keep composition class.**  
7. **Redraw under better locks.**  
8. **Use `avatar_demo` as regression memory.**  
9. **When the user freezes a candidate, stop.**  
10. **This skill stays long so couple PFPs get measured work, not vibes.**

---

## 29. Operator addendum — session lessons compressed into rules

1. If the user says the style is wrong, **ask which axis** (stroke / face / space / bg / 对子) before thrashing proxies.
2. Stroke compare crops beat whole-image vibes.
3. `L`/`R` names are IDs; facing is pixels.
4. Non-VAE means new content; dialect lock means old hand.
5. Background is part of the PFP, built into the generate call.
6. Tag-led prompts fail even when the rest of the prompt is long — rewrite around crops.
7. When a candidate is chosen, overwrite `*_gen` and halt.
8. Pack demos are the regression suite — reopen them when quality slips.
9. Confirm success by opening the output file.
10. Keep this skill long; resist collapsing it into slogans.

---

## 30. Minimal viable run (only when user wants speed)

Even in “fast” mode, still:

1. Open source  
2. Lock facing + face% + stroke class + bg plan + 对子 axis  
3. Attach source + at least hair + eye + bg crops  
4. Generate from pixel locks  
5. Open output + stroke crop compare  
6. Save exact size  

These six steps are the minimum that keeps couple PFPs inside the pass criteria this skill exists to protect.

---

## 31. Extended operator notes — keeping length and substance

### 31.1 Why this skill stays long

Couple PFPs fail in predictable, narrow ways: tag-led stock dialect, spatial zoom, missing background, mirror clones, stroke family drift, proxy-metric theater, and patching a bad base. Each section above exists because a short slogan did not stop that failure in practice. Keep the measured locks; keep the atlas; keep the acceptance checklists.

### 31.2 Reference packing checklist (per generate call)

Attach, when available:

1. Full source at native resolution  
2. Hair edge / flyaway crop  
3. Lash / eye crop  
4. Mouth / nose profile crop  
5. Robe fold or collar crop (value + line)  
6. Outer foliage / wash crop  
7. Optional open-field motif crop  

Caption each crop in the brief with what it locks (“clumped grey digital stroke”, “dash mouth length”, “unoutlined cool wash”).

### 31.3 Side-by-side review habit

After every generate:

1. Open source and partner at the same zoom.  
2. Run the 30-second acceptance test (§13).  
3. If stroke is the named axis, crop hair edges first.  
4. If space is the named axis, measure face % before anything else.  
5. If background is the named axis, compare outer thirds.  
6. Ship only when the named axis and the hard locks all pass.

### 31.4 Candidate freeze protocol

When the user points at a prior candidate:

1. Copy/rename that file to the canonical `*_gen` path.  
2. Confirm exact W×H.  
3. Halt further regenerate churn for that ID unless the user reopens the brief.  
4. Optionally archive runners-up under `*_cand2`, `*_cand3` for the pack — separate from the frozen final.

### 31.5 Teaching from pack exemplars without overfitting

When `nR` is allowed:

- Study how 对子 was resolved (facing, value, prop split).  
- Study shared dialect (stroke, cast, face recipe).  
- Generate a **new** partner identity — dialect lock from `nL`, couple grammar informed by `nR`, content distinct from both.  

Score on dialect + 对子 readability, not pixel nearness to `nR`.

---

## 32. Out of scope (compact)

Single list — residual boundaries, not repeated every section:

1. Coarse genre/mood tags as the primary generation driver — see §1.1a emphatic ban  
2. Editing or overwriting the user’s source portrait file  
3. Mirror-flip / same-facing / 1:1 accessory clones as the couple solution  
4. Headshot zoom or bun-chopping center crops that break source composition class  
5. Empty cutout backgrounds against leafy/motif sources  
6. Patching failed gens (mouth paint, broken alpha) instead of redraw from source refs  
7. Feeding prior failed gens as style anchors; shipping 16:9 or debug overlays as finals  
8. Diptych/collage when the user asked for one partner PFP  

---

*End of Matching Couple Avatar skill. Target length is a full operator manual (tens of KB), not a 5–10k blurb.*
