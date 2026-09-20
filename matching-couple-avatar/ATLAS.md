# Matching Couple Avatar — ATLAS

On-demand: open this only when the user says the style/couple/space is wrong, when
self-review fails, or when you are about to regenerate after a failed attempt.

Demo roles are authoritative in `../demo/MANIFEST.md`. Never treat a `working-attempt`
(`*_gen`) as a ship target.

---

## 8. Demo atlas — `avatar_demo/` (how to learn, refine, pass)

Path (user pack): `aesthetic-atelier/demo/avatar_demo/`  
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
