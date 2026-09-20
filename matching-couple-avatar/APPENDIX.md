# Matching Couple Avatar — APPENDIX

On-demand: templates, workshop material, batch/QA recipes, operator notes and the pack
path reference. Nothing here is needed for a first cold run.

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

## 26. Appendix E — what “almost identical style” allows to change

**May change:** identity, gender (if briefed), hair architecture details, ornaments, held props, exact petal positions, minor expression, earring design — under same dialect.

**Keep locked:** stroke family, face simplification tier, cast band, spatial class (small-face vs close-up), background drawing method, couple facing logic.

---

## 27. Appendix F — pack path reference

Pack root = this skill's parent directory (`..`). Every path below is relative to it; nothing here is machine-specific.

Relevant entries:

- `matching-couple-avatar/SKILL.md` — this skill
- `demo/avatar_demo/` — demos `1L`–`4L` with gens and exemplars
- `high-aesthetic-image-expert/` — parent aesthetic law
- `photo-style-transfer-poster/` — unrelated specialty; keep pipelines separate

Agent workflow mirrors:

- `matching-couple-avatar-2` / `matching-couple-avatar`
- `aesthetic-atelier/matching-couple-avatar`

Keep these synchronized when the skill updates.

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
