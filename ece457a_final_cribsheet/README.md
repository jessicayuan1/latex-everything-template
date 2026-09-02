## ECE 457A — Final Cheatsheet

Two-sided, 8.5 × 11 landscape crib sheet (exactly 2 pages) built on the same
compact template as the midterm sheet. Covers the full final scope:

- Midterm review (conceptual) + heuristic search, A*, alpha–beta.
- Trajectory metaheuristics: Simulated Annealing, Tabu Search (with worked examples).
- Swarm intelligence: Ant Colony Optimization, Particle Swarm Optimization.
- Evolutionary: Genetic Algorithms, Differential Evolution, Evolution Strategies,
  Memetic Algorithms, No Free Lunch.
- Genetic Programming: tree-based, Cartesian/graph GP, GSGP (syntax vs semantics),
  bloat, closure.
- Metaheuristic comparison + "which algorithm when" selection guide + GP pseudocode.
- Full **Winter 2026** final (all 6 questions) with answers and the Q1 graph diagram.
- Full **Fall 2024** final (all 7 questions) with answers. Cycle crossover is
  intentionally excluded (not on the final); PMX is kept.

### Build
```bash
latexmk -pdf ece457a-final-cheatsheet.tex   # builds ece457a-final-cheatsheet.pdf
latexmk -c ece457a-final-cheatsheet.tex     # clean aux files (keep PDF)
```

### Layout notes
- `content/def.tex` holds the preamble (colors, box styles, tikz node styles).
  Header text and node styles match the midterm sheet; a `gpnode` style was added
  for GP trees/graphs.
- Each topic is its own file in `content/`, `\input` inside the `multicols{5}`
  block in the main file, in reading order.
- Base font is `\scriptsize` to fit the two full finals plus all theory on 2 pages.
  If you need it larger and can drop the exam sections, switch to `\footnotesize`.
- Math uses round-parenthesis mode `\( ... \)` only, with `\\` line breaks, and no
  blank line after section headings — same as the midterm sheet.
