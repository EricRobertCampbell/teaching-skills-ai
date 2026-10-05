---
name: thinking-classrooms-transformations
description: >-
  Create Math 30-1 Thinking Classrooms worksheets for the transformations unit
  (translations, stretches, reflections, combined transformations). Use when
  writing worksheet-tc-*.tex under the transformations unit, or when converting
  among verbal descriptions, variable replacements, and mappings.
---

# Thinking Classrooms — Transformations (Math 30-1)

## Prerequisite

Follow **thinking-classrooms-worksheets** for general TC layout, boilerplate, build, sketch-on-same-axes, B&W graph styling, and page-break conventions. Read that skill first, then apply the unit rules below.

## Three forms

Students convert among:

1. **Verbal description**
2. **Variable replacement** (equation)
3. **Mapping**

Name these three forms in the question when asking for conversions. Do **not** tell students in the prompt to use SRT / canonical form—that belongs in the solutions.

## SRT / canonical form (solutions only)

When order is ambiguous or non-canonical, rewrite into **stretch → reflect → translate** (SRT), then present the forms consistently in the key.

## Variable replacements (equations)

- Attach everything possible to \(y\) (left side), not only to \(f(\ldots)\)
- Fully factor horizontal inputs: \(f(2x+6)\) → \(f\bigl(2(x+3)\bigr)\)
- Example: \(y=-2f(2x+6)+1\) → \(-\dfrac{y-1}{2}=f\bigl(2(x+3)\bigr)\)

## Mappings

- Fully simplify / expand; do **not** leave factored translation forms
- Example: \((x,y)\to\bigl(2(x+3),\,y\bigr)\) → \((x,y)\to(2x+6,\,y)\)
- Include **stretch** mappings routinely (provincial diploma commentary: translations/reflections in mapping form are stronger than stretches)

## Diploma alignment (transformations)

Prefer at least one item per sheet that targets a provincial weak spot from the Math 30–1 Information Bulletin 2025–2026 commentary:

- Mapping notation that includes a horizontal and/or vertical **stretch**
- Counting or identifying **invariant points** for a non-reflection transformation (or a combined transformation)
- Verbal explanations in `\answer{...}` that use full transformation vocabulary (no abbreviations), matching review-math-30 expectations

## Typical conversion sets

1. Give one form; ask for the other two
2. Give a non-canonical / unfactored form; ask for all three forms (solutions rewrite to SRT)
3. Rotate which form is given (verbal / equation / mapping) across parts
4. Include a stretch-focused mapping conversion and/or an invariant-point follow-up

## Graph and point items

- For sketch items, show the graph only when a formula is unnecessary; prefer lattice points
- Piecewise graphs (e.g. parabola joined to a line) work well
- Identification items: show original and image with B&W-safe styling; ask for equation and mapping (SRT only in the key)
- Size axes so common errors (e.g. inverted stretch factor) still fit
- Large graph questions often work best as full pages (`\clearpage`) rather than split across pages
- Parameter items: a point such as \(\bigl(k,(k+2)^2\bigr)\) under a named transformation, with an image coordinate that forces a factorable quadratic in \(k\)

## Checklist (unit-specific)

- [ ] General TC skill conventions followed
- [ ] Questions name the three forms when relevant; SRT appears in solutions only
- [ ] Equations factored/canonical in solutions; mappings expanded in solutions
- [ ] Stretch mappings and/or non-reflection invariant points appear where the sheet allows
- [ ] Graph items use shared axes, lattice-friendly points, and roomy B&W-safe styling
