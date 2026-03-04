# Aarhus University Report — Writing Guidelines

This is a report for Aarhus University. Follow AU's academic standards and the guidelines below when assisting with writing, editing, or structuring content.

## Report Structure

Reports must follow this section order:

1. **Title page** — title, author names, student IDs (årskortnummer), supervisor, department, Aarhus University, date
2. **Preface** — what the document is, intended audience, prerequisite knowledge
3. **Abstract** — mandatory; summarise purpose, method, results, and conclusion
4. **Acknowledgements** — thank supervisor, technical staff (TAP), and others who helped
5. **Table of contents**
6. **Introduction** — background, motivation, and purpose of the project
7. **Methods / Theory** — experimental methods and necessary theory. Theory should be written last. Focus on what was done, not what was read in a textbook
8. **Results** — present from general to specific, not chronologically. Build around figures, tables, and graphs
9. **Discussion** — connect results into a whole, compare with literature, discuss limitations
10. **Conclusion** — summary of findings and perspectives for future work
11. **References** — complete with all authors, journal title, year, volume, page range. Consistent notation throughout
12. **Appendix** — raw data, detailed calculations, supplementary material

## Formatting

- A4 paper, 12pt, Times New Roman (mathptmx in LaTeX)
- No paragraph indentation, 6pt paragraph spacing
- Standard layout only — do not over-customise margins or fonts
- Figures must have: clear captions, large readable symbols, distinguishable colours (never yellow), axis labels with units
- Figures are typically revised 5–10 times — invest effort in clarity
- Every claim must have a reference. References must be exhaustive and complete

## Writing Principles

- Write in a language you are comfortable with. English requires supervisor approval
- The reader cares about what you did and found — not what you read in a book
- Results should be structured around figures, not experiment chronology
- Provide enough raw data that the reader can verify your conclusions
- When in doubt, include an extra appendix rather than leave out information

## Academic Tone

- Use formal, precise academic language
- Avoid vague claims — quantify where possible
- Do not use first person excessively; prefer passive voice for methods ("The sample was heated to...")
- Define abbreviations on first use
- Be concise — every sentence should add information

## LaTeX Conventions

- Images go in `assets/` — reference without folder prefix: `\includegraphics{filename}`
- Cross-references: `Figure~\ref{fig:label}`, `Table~\ref{tab:label}`, `Equation~\eqref{eq:label}` (use `~` for non-breaking space)
- Citations: `\cite{key}` in text, `\bibitem{key}` in bibliography
- Place figures with `[H]` when they must stay in context
- Use `\nosectionbreak` before `\section` to prevent a page break
- Compile twice for correct references: `pdflatex file.tex && pdflatex file.tex`

## GAI (Generative AI) Policy

- If GAI tools were used (ChatGPT, Copilot, Claude, etc.), a declaration must be submitted as a separate file in WISEflow
- The declaration must state: (1) that GAI was used, (2) which tools and versions, (3) how they were used
- GAI used for proofreading or text feedback must also be declared
- If GAI was not used, no declaration is needed
- Direct GAI-generated text used in the report must be cited as a quote
- Never upload personal or sensitive data (GDPR) to GAI tools
