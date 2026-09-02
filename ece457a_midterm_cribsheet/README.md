## ECE 457A — Midterm Cheatsheet

Two-sided, 8.5 × 11 landscape crib sheet built on the compact LaTeX cheatsheet
template. Covers the full midterm scope: problem-solving foundations, uninformed
search (BFS/UCS/DFS/DLS/IDS/bidirectional), informed search (heuristics, greedy,
A*, beam), two-player minimax + alpha-beta, trajectory metaheuristics
(hill climbing, simulated annealing, tabu search), and genetic algorithms.

### Build
- Main file: `ece457a-cheatsheet.tex`
- A TeX toolchain (TinyTeX) is installed and its binaries are linked into
  `/opt/homebrew/bin`, so `latexmk`, `pdflatex`, etc. are on your PATH.

```bash
latexmk -pdf ece457a-cheatsheet.tex   # builds ece457a-cheatsheet.pdf
latexmk -c ece457a-cheatsheet.tex     # clean aux files (keep PDF)
```

### Viewing the PDF in VS Code (LaTeX Workshop)
1. Open `ece457a-cheatsheet.tex`.
2. Build: click the green ▶ (TeX badge in the sidebar → "Build LaTeX project"),
   or save the file if build-on-save is enabled, or run the command palette
   "LaTeX Workshop: Build LaTeX project". It now finds `latexmk` on the PATH.
3. View: click the "View LaTeX PDF" icon (top-right of the editor) or run
   "LaTeX Workshop: View LaTeX PDF file" → "in VSCode tab". The PDF opens in a
   side tab with SyncTeX (ctrl/cmd-click jumps between source and PDF).

If the extension still reports `spawn latexmk ENOENT`, reload the window
(command palette → "Developer: Reload Window") so it re-reads the PATH.

### Layout notes
- `content/def.tex` holds the preamble (colors, box styles, tikz node styles).
- Each topic is its own file in `content/` and is `\input` inside the
  `multicols{5}` block in the main file.
- Math uses round-parenthesis mode `\( ... \)` only (never `$...$` or `\[...\]`),
  with `\\` for line breaks, per the template style.
- To fit exactly two pages: keep `\small` (default). If content overflows,
  switch `\small` to `\footnotesize` in `ece457a-cheatsheet.tex`, or drop a
  column with `multicols{4}`. To loosen for readability, raise
  `\baselinestretch` in `content/def.tex`.
