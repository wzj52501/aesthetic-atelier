# Matching Couple Avatar — CORE

Default-loaded law for this skill. Section numbers are kept from the original single-file
manual so cross-references (`§1.1a`, `§6.3`, …) stay valid.

Demo file roles (`source` / `gold` / `working-attempt`) are authoritative in
`../demo/MANIFEST.md`. A `*_gen` file is a **working-attempt**, not a style oracle.

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
