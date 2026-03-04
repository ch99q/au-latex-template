<p align="center">
  <img src="assets/aulogo_dk_var2_blaa.png" alt="Aarhus University" width="300">
</p>

# Aarhus University - LaTeX Report Template

Unofficial LaTeX template for reports at Aarhus University. Follows the formatting guidelines from AU's "Tips til Rapportskrivning" by Henrik Birkedal.

> **Note:** This is a community template and is not officially maintained by Aarhus University.

## What's Included

| File | Description |
|------|-------------|
| `template.tex` | Main report template with example content |
| `declaration.tex` | GAI declaration form (required if you used AI tools) |
| `assets/` | AU logo and other assets |

## Quick Start

### 1. Clone or copy the template

```bash
git clone https://github.com/ch99q/au-latex-template.git my-report
cd my-report
```

Or use GitHub's "Use this template" button to create your own copy.

### 2. Fill in your metadata

Open `template.tex` and update the metadata section near the top:

```latex
\newcommand{\reporttitle}{Report Title}
\newcommand{\projectname}{Project Name}
\newcommand{\authorA}{Author 1}
\newcommand{\authorB}{Author 2}
\newcommand{\studentidA}{AU ID 1}
\newcommand{\studentidB}{AU ID 2}
\newcommand{\supervisor}{Supervisor Name}
\newcommand{\department}{Department Name}
```

### 3. Compile

```bash
pdflatex template.tex
pdflatex template.tex   # run twice for references
```

## Template Structure

The report follows AU's recommended structure:

1. **Title page** -- title, authors, student IDs, supervisor, department, date, AU logo
2. **Preface** -- what the document is and expected reader prerequisites
3. **Abstract** -- summary with purpose, method, results, conclusion (required)
4. **Acknowledgements** -- thanks to supervisor, TAP staff, etc.
5. **Table of contents**
6. **Introduction**
7. **Methods** (experiments + theory)
8. **Results**
9. **Discussion**
10. **Conclusion**
11. **References**

## Formatting

The template is configured to match AU guidelines:

- **Paper:** A4
- **Font:** Times New Roman (mathptmx), 12pt
- **Header:** AU logo (left), report title + project name (right)
- **Footer:** Page number
- **Sections:** Each major section starts on a new page (use `\nosectionbreak` to override)
- **Paragraphs:** No indentation, 6pt spacing

## GAI Declaration

If you used generative AI tools (ChatGPT, Copilot, Claude, etc.) while working on your report, AU requires you to submit a GAI declaration.

### How to use `declaration.tex`

1. Update the metadata at the top (same fields as `template.tex`)
2. Mark which tools you used in section 2
3. Change `\unchecked` to `\checked` for each applicable use case in section 3
4. Describe your usage in section 4
5. Compile and upload as a **separate file** in WISEflow under "bilag"

```latex
% Before:
\item[\unchecked] Til programmeringsopgaver

% After:
\item[\checked] Til programmeringsopgaver
```

> If you have **not** used GAI tools, you do not need to submit a declaration.

## Useful Commands

| Command | Effect |
|---------|--------|
| `\nosectionbreak` | Place before `\section` to prevent page break |
| `\checked` / `\unchecked` | Checkbox symbols for `declaration.tex` |

## Requirements

A LaTeX distribution with the following packages (all included in TeX Live / MiKTeX):

`inputenc`, `fontenc`, `babel`, `mathptmx`, `geometry`, `graphicx`, `float`, `amsmath`, `amssymb`, `tikz`, `pgfplots`, `fancyhdr`, `lastpage`, `titlesec`, `needspace`, `hyperref`, `caption`, `cite`, `enumitem`

## License

This template is provided as-is for academic use at Aarhus University. The AU logo is property of Aarhus University.
