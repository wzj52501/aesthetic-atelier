# Matching Couple Avatar — STUDY

On-demand: open this when CORE locks are not enough to write measurements, or when you
need the full measurement protocol, stroke cookbook, or spatial/background engineering.

Load it to **produce numbers**, not to browse.

---

## 4. Study protocol — what to lock from the source

**Role discipline.** Serve a new user's portrait **source-only** — measure `nL` (and the user's own image), never a pack `*_gen`. Reach for a `role: gold` `*R` file only when you are teaching or checking **couplet grammar**. `*_gen` files are `working-attempt` unless `../demo/MANIFEST.md` promotes them; opening source + gen to catalogue a gap is correct, treating a gen as the style oracle is not.

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
