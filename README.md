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
| `presentation.tex` | Beamer presentation template (16:9, light theme) |
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

## Presentation Template

`presentation.tex` is a Beamer template styled to match AU's visual identity — 16:9 aspect ratio, AU blue colour palette, and sharp flat design.

Open `presentation.tex`, update the metadata at the top, and compile:

```bash
pdflatex presentation.tex
```

### Available commands

| Command | Effect |
|---------|--------|
| `\sectionslide{01}{Title}` | Section divider slide with large number and blue bar |
| `\stat{value}{label}` | Stat card with large number (use three in a row) |
| `\callout{Title:}{Text}` | Callout box with blue left border |
| `\done` / `\ongoing` / `\planned` | Colour-coded status labels for timelines |

## Using with Overleaf

You can use this template on [Overleaf](https://www.overleaf.com) without cloning the repository.

### Option 1: Upload as ZIP

1. Download or clone this repository as a ZIP
2. Go to Overleaf and click **New Project** > **Upload Project**
3. Upload the ZIP file — Overleaf will set everything up automatically

### Option 2: Start from a blank project

1. Create a new blank project on Overleaf
2. Copy the contents of `template.tex` (or `presentation.tex`) into `main.tex`
3. Create a folder called `assets` in the Overleaf file tree
4. Download the AU logo and upload it to the `assets` folder:
   - [aulogo_dk_var2_blaa.png](https://raw.githubusercontent.com/ch99q/au-latex-template/main/assets/aulogo_dk_var2_blaa.png) (for presentations)
   - [aulogo_dk_var2_blaa.pdf](https://raw.githubusercontent.com/ch99q/au-latex-template/main/assets/aulogo_dk_var2_blaa.pdf) (for reports — PDF gives sharper output in print)
5. If using the GAI declaration, also copy `declaration.tex` into the project

> **Tip:** Overleaf compiles automatically, so you do not need to run `pdflatex` manually.

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
\item[\unchecked] Programming tasks

% After:
\item[\checked] Programming tasks
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
