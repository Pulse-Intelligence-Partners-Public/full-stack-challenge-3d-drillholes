# Product Engineer - Take-Home Challenge

**Time Expectation:** 4-6 hours
**Submission Window:** 72 hours from receipt

---

## The Scenario

You're at Pulse Intelligence, a platform helping mining investors track assets and market data.

The CEO walks over:

> "A client asked if we could turn drill-hole announcements into an interactive 3D view — see the holes in space, intercepts coloured by grade, click through to the source. They want to see if it's feasible before they commit. Can you build something we can demo tomorrow?"

---

## The Task

Using the attached drilling announcement and the data extracted from it, build a proof-of-concept that:

1. **Loads** the drill collars and intercepts from `data/`
2. **Renders** the drill holes in 3D — each hole as a trace starting at its collar, oriented by dip and azimuth, down to its total depth
3. **Highlights** the mineralised intercept intervals along each hole, coloured by grade
4. **Lets the user** interact with the scene (orbit, zoom, click a hole or intercept to inspect it) and reference the source PDF

You pick the stack — anything that gets the outcome. The brief is intentionally open-ended; we want to see the calls you make.

---

## The Data

Three files in `data/`, all for a single ASX announcement (Comet Vale gold project, Western Australia):

- **`source.pdf`** — the original drilling update announcement. Provided for context and so the viewer can cite/link back to the source — the CSVs below are already extracted, so you don't need to re-parse it.
- **`drillhole_collars.csv`** — one row per drillhole. Each hole starts at a collar (`latitude`, `longitude`, `rl` = elevation in metres) and is drilled at a given `dip` (degrees below horizontal, negative = down) and `azimuth` (degrees clockwise from north) for `total_depth` metres. The `east`/`north` columns are the same collar point projected to MGA zone 51 (EPSG:28351) if you'd prefer to work in metres.
- **`drill_intercepts.csv`** — one or more rows per hole. Each row is a mineralised interval along the hole: `depth_from` and `depth_to` (downhole metres from the collar), plus `grade`, `grade_unit`, and `commodity_symbol`.

---

## Evaluation

| Area | Weight |
|------|--------|
| **Working end-to-end** | 30% |
| **3D presentation & UX** | 25% |
| **3D scene correctness** | 20% |
| **Code quality** | 15% |
| **NOTES.md** | 10% |

---

## Stretch Goal

Deploy your solution somewhere we can test it. Include the URL in your NOTES.md.

---

## Submission

Use the "Use this template" button to create your own repo, then push your work there. Share access with @stephendegoede and @tva1992 when you're done.

**Include:**

1. **NOTES.md** with:
   - Actual time spent
   - Your approach and key decisions
   - Trade-offs you made
   - What you'd improve with more time

2. **Clear local setup instructions** in your README

---

## Questions?

Please email us if you have any questions.
