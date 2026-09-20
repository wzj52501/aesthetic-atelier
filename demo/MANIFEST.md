# demo/MANIFEST.md — regression roles

**Authoritative for agents.** A file's role comes from this manifest, never from its name or
from how pretty it looks. If a `*_gen` file later passes the hard locks, promote its role to
`gold` here and drop its `fail_tags` — the manifest is the source of truth.

## Roles

| role | Meaning | How an agent may use it |
|---|---|---|
| `source` | The input the user holds (`nL` / `raw`) | The only truth for measurements and the spatial map |
| `gold` | An approved sample that passes the hard locks | Positive exemplar for couplet grammar and subject/space acceptance |
| `dialect-ref` | Recipe / stroke dialect reference. **Does not guarantee** aspect or full spatial marks | Learn the look. Acceptance still runs against `source` + hard locks |
| `working-attempt` | A real generation attempt (mostly `*_gen`) | Gap analysis only — find the delta, then tighten locks. **Never** a ship target |
| `fail-example` | A deliberately kept failure | Only when `ATLAS.md` is open, to match an F-code. **Never** a positive exemplar |
| `mood-ref` | Mood / aesthetic reference; the brief may be only loosely met | General-brief demos. Not scored against couplet or poster hard locks |

One primary role per file. `fail_tags` reference the F-codes in the relevant `ATLAS.md`.

**Aspect note:** `style-*.jpg` are **generator-native 1280×720 (16:9)**. Their `*_matched.jpg`
companions are the same image letterboxed to the aspect of that set's `raw`. Neither is a
statement that 16:9 is correct — see `photo-style-transfer-poster/CORE.md §6c`.

```yaml
avatar_demo:
  1L.jpeg:      { role: source }
  1R.jpeg:      { role: gold, notes: "approved couplet grammar vs 1L" }
  1L_gen.jpeg:  { role: working-attempt, fail_tags: [F3, F5], notes: "lost hearts/co-frame; cleaner stroke than source" }
  2L.jpeg:      { role: source }
  2R.jpeg:      { role: gold, notes: "pinch interaction continuous with 2L" }
  2L_gen.jpeg:  { role: working-attempt, notes: "interaction seam not closed; expression drift" }
  3L.jpg:       { role: source }
  3R.jpg:       { role: gold }
  3L_gen.jpg:   { role: working-attempt, fail_tags: [F5], notes: "stroke drifts watery/soft vs 3L" }
  4L.jpg:       { role: source }
  4R.jpg:       { role: gold }
  4L_gen.jpg:   { role: working-attempt, fail_tags: [F3, F5], notes: "weaker floral co-frame; painterly dialect drift" }

poster_demo1:
  raw.jpg:                          { role: source, aspect: "1706x1279 ~4:3 (r=1.334)" }
  style-01-riso.jpg:                { role: dialect-ref }
  style-02-newsprint.jpg:           { role: dialect-ref }
  style-03-paper-theatre.jpg:       { role: dialect-ref }
  style-04-pressed-flower.jpg:      { role: dialect-ref }
  style-05-travel-sketch.jpg:       { role: dialect-ref, notes: "high spatial bar — preferred for space regression after aspect match" }
  style-06-silkscreen.jpg:          { role: dialect-ref }
  style-07-jp-line.jpg:             { role: dialect-ref }
  style-08-naive-doodle.jpg:        { role: working-attempt, fail_tags: [F6], notes: "pedestrian groups simplified" }
  style-09-ink-sketch.jpg:          { role: dialect-ref, notes: "high spatial bar" }
  style-01-riso_matched.jpg:        { role: dialect-ref, notes: "letterboxed to raw aspect r=1.333" }
  style-02-newsprint_matched.jpg:   { role: dialect-ref, notes: "letterboxed to raw aspect r=1.333" }
  style-03-paper-theatre_matched.jpg: { role: dialect-ref, notes: "letterboxed to raw aspect r=1.333" }
  style-04-pressed-flower_matched.jpg: { role: dialect-ref, notes: "letterboxed to raw aspect r=1.333" }
  style-05-travel-sketch_matched.jpg: { role: dialect-ref, notes: "letterboxed to raw aspect r=1.333" }
  style-06-silkscreen_matched.jpg:  { role: dialect-ref, notes: "letterboxed to raw aspect r=1.333" }
  style-07-jp-line_matched.jpg:     { role: dialect-ref, notes: "letterboxed to raw aspect r=1.333" }
  style-08-naive-doodle_matched.jpg: { role: working-attempt, fail_tags: [F6], notes: "letterboxed to raw aspect r=1.333" }
  style-09-ink-sketch_matched.jpg:  { role: dialect-ref, notes: "letterboxed to raw aspect r=1.333" }

poster_demo2:
  raw.jpg:                          { role: source, aspect: "1024x677 ~1.51 (r=1.513)" }
  style-01-riso.jpg:                { role: dialect-ref }
  style-02-newsprint.jpg:           { role: dialect-ref }
  style-03-paper-theatre.jpg:       { role: dialect-ref }
  style-04-pressed-flower.jpg:      { role: dialect-ref }
  style-05-travel-sketch.jpg:       { role: dialect-ref }
  style-06-silkscreen.jpg:          { role: dialect-ref }
  style-07-jp-line.jpg:             { role: dialect-ref }
  style-08-naive-doodle.jpg:        { role: fail-example, fail_tags: [F2], notes: "autumn/winter split — place identity rewritten. NOT gold, never a spatial pass" }
  style-09-ink-sketch.jpg:          { role: dialect-ref }
  style-01-riso_matched.jpg:        { role: dialect-ref, notes: "letterboxed to raw aspect r=1.513" }
  style-02-newsprint_matched.jpg:   { role: dialect-ref, notes: "letterboxed to raw aspect r=1.513" }
  style-03-paper-theatre_matched.jpg: { role: dialect-ref, notes: "letterboxed to raw aspect r=1.513" }
  style-04-pressed-flower_matched.jpg: { role: dialect-ref, notes: "letterboxed to raw aspect r=1.513" }
  style-05-travel-sketch_matched.jpg: { role: dialect-ref, notes: "letterboxed to raw aspect r=1.513" }
  style-06-silkscreen_matched.jpg:  { role: dialect-ref, notes: "letterboxed to raw aspect r=1.513" }
  style-07-jp-line_matched.jpg:     { role: dialect-ref, notes: "letterboxed to raw aspect r=1.513" }
  style-08-naive-doodle_matched.jpg: { role: fail-example, fail_tags: [F2], notes: "letterboxed to raw aspect r=1.513" }
  style-09-ink-sketch_matched.jpg:  { role: dialect-ref, notes: "letterboxed to raw aspect r=1.513" }

bear.jpg: { role: mood-ref, notes: "romantic meadow reads well; the small tumbling bear from the brief is not really met — not a hard-lock gold" }
```
