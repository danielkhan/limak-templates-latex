# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This repository contains LaTeX templates for academic work at LIMAK Austrian Business School (Johannes Kepler Universität Linz). It includes:

- **limak-transferarbeit-latex/**: **Transferarbeit template** - Practice-oriented transfer assignments (shorter format)
- **limak-thesis-latex/**: Master's thesis template (longer format, full thesis structure)
- **jku-templates-report-latex-master/**: Base JKU technical report template (English)
- **instructions/**: LIMAK guidelines and Word templates
  - [Leitfaden_Transferarbeit_2024.pdf](instructions/Leitfaden_Transferarbeit_2024.pdf) - Official LIMAK Transferarbeit guidelines
  - [Vorlage_Transferarbeit_2023.doc](instructions/Vorlage_Transferarbeit_2023.doc) - Word template for Transferarbeiten

## Build Commands

### Compiling LaTeX Documents

The templates use **XeLaTeX** as the primary compilation engine with **Biber** for bibliography management.

#### Transferarbeit compilation:
```bash
cd limak-transferarbeit-latex
xelatex main-transferarbeit.tex
biber main-transferarbeit
xelatex main-transferarbeit.tex
xelatex main-transferarbeit.tex
```

#### Master thesis compilation:
```bash
cd limak-thesis-latex
xelatex main-limak-thesis.tex
biber main-limak-thesis
xelatex main-limak-thesis.tex
xelatex main-limak-thesis.tex
```

#### Quick compilation (during editing):
```bash
xelatex main-transferarbeit.tex  # or main-limak-thesis.tex
```

#### Alternative toolchains:
- **pdfLaTeX**: Supported but will not use professional fonts
- **LuaLaTeX**: Fully supported with professional fonts

### Magic Comments

The main `.tex` files include magic comments at the top that configure editors automatically:
- `% !TeX program = xelatex`
- `% !BIB program = biber`
- `% !TeX encoding = UTF-8`
- `% !TeX spellcheck = de_DE`

Most modern LaTeX editors (TeXstudio, VS Code with LaTeX Workshop) will respect these settings.

## Code Architecture

### Template Selection Guide

**Use limak-transferarbeit-latex/** for:
- Transferarbeiten (transfer assignments for coursework)
- Shorter practice-oriented papers (typically 10-20 pages)
- Assignments that apply course concepts to professional practice
- Works that follow the 5-section structure (see Leitfaden)

**Use limak-thesis-latex/** for:
- Master's thesis (Masterarbeit)
- Longer research-oriented work (60+ pages)
- Full academic thesis with extensive theoretical foundations
- Works requiring detailed chapter structure (9+ chapters)

### LIMAK Transferarbeit Template Structure

The Transferarbeit template ([limak-transferarbeit-latex/](limak-transferarbeit-latex/)) uses a simplified structure:

**Main file**: [main-transferarbeit.tex](limak-transferarbeit-latex/main-transferarbeit.tex)
- Document class: `scrartcl` (article format, shorter than book)
- Simplified title page (no jkureport.sty dependency)
- Direct formatting with Arial 11pt, 1.5 line spacing

**Chapter files** (5-section structure per Leitfaden):
- [01-ausgangssituation.tex](limak-transferarbeit-latex/01-ausgangssituation.tex) - Initial situation and context
- [02-fragestellung.tex](limak-transferarbeit-latex/02-fragestellung.tex) - Research question
- [03-zielsetzung.tex](limak-transferarbeit-latex/03-zielsetzung.tex) - Objectives (theoretical & practical)
- [04-inhaltliche-bearbeitung.tex](limak-transferarbeit-latex/04-inhaltliche-bearbeitung.tex) - Main content (theory-practice transfer)
- [05-schlussfolgerungen.tex](limak-transferarbeit-latex/05-schlussfolgerungen.tex) - Conclusions and recommendations

**Supporting files**:
- [references.bib](limak-transferarbeit-latex/references.bib) - Bibliography with examples
- [fonts/](limak-transferarbeit-latex/fonts/) - Optional professional fonts
- [logos/](limak-transferarbeit-latex/logos/) - LIMAK/JKU logos

### LIMAK Master Thesis Template Structure

The LIMAK thesis template ([limak-thesis-latex/](limak-thesis-latex/)) is organized as follows:

**Main file**: [main-limak-thesis.tex](limak-thesis-latex/main-limak-thesis.tex)
- Document configuration and metadata
- Loads `jkureport.sty` with `[mathesis,fancyfonts,LIMAK]` options
- Imports all chapter files using `\import{./}{filename}`

**Chapter files** (numbered by order):
- [00-abstract.tex](limak-thesis-latex/00-abstract.tex) - German/English abstracts
- [01-einleitung.tex](limak-thesis-latex/01-einleitung.tex) through [09-zusammenfassung.tex](limak-thesis-latex/09-zusammenfassung.tex) - Main content chapters
- [91-anhang.tex](limak-thesis-latex/91-anhang.tex) - Appendix

**Supporting files**:
- [references.bib](limak-thesis-latex/references.bib) - BibLaTeX bibliography database
- [jkureport.sty](limak-thesis-latex/jkureport.sty) - Custom JKU/LIMAK style package
- [fonts/](limak-thesis-latex/fonts/) - Professional font files for XeLaTeX
- [logos/](limak-thesis-latex/logos/) - LIMAK and JKU logo files

### Template Customization System

The `jkureport.sty` package provides a flexible configuration system via options:

**Document type options**:
- `mathesis` - Master's thesis format
- `bathesis` - Bachelor's thesis format
- `phdthesis` - PhD thesis format
- `seminarreport` - Seminar report format

**Branding options**:
- `LIMAK` - LIMAK Austrian Business School (includes logo)
- `BUS` - Generic Business School colors
- `JKU` - Standard JKU gray scheme

**Font options** (requires XeLaTeX/LuaLaTeX):
- `fancyfonts` - Enable professional TrueType fonts
- `nofancyfonts` - Use standard LaTeX fonts (fallback for pdfLaTeX)
- `compactmono` - Condensed monospace everywhere
- `nocompactverb` - Standard monospace for code/verbatim

### LIMAK-Specific Formatting

The LIMAK template applies specific formatting to match institutional requirements:

**Typography** ([main-limak-thesis.tex:120-136](limak-thesis-latex/main-limak-thesis.tex#L120-L136)):
- Main font: Arial (via `\setmainfont{Arial}`)
- Font size: 11pt base
- Line spacing: 1.5 (via `\onehalfspacing`)

**Page layout** ([main-limak-thesis.tex:124-130](limak-thesis-latex/main-limak-thesis.tex#L124-L130)):
- Margins: 3cm top/bottom/left, 2.5cm right
- Paper: A4
- Layout: Single-sided

**Logo positioning** ([main-limak-thesis.tex:157-160](limak-thesis-latex/main-limak-thesis.tex#L157-L160)):
- LIMAK logo has custom dimensions (wider aspect ratio than standard JKU logos)
- Height: 16mm (reduced from standard 25mm)
- Alignment: Right-aligned with text block

### Bibliography System

Uses **BibLaTeX** with **Biber** backend:
- Style: Harvard author-year (authoryear) per LIMAK Leitfaden
- Configuration: [main-limak-thesis.tex:95-103](limak-thesis-latex/main-limak-thesis.tex#L95-L103)
- Two-author separator: `/` (forward slash) per LIMAK guidelines
- Three+ authors: Automatically shortened to "et al."
- URL breaking penalties optimized for better line breaks

## Key Development Notes

### Adding/Removing Chapters

Edit the chapter imports section in [main-limak-thesis.tex](limak-thesis-latex/main-limak-thesis.tex) (around line 284):
```latex
\import{./}{01-einleitung}
\import{./}{02-theoretische-grundlagen}
% Add or remove \import{} commands here
```

### Modifying Thesis Metadata

Key metadata is set in [main-limak-thesis.tex:171-210](limak-thesis-latex/main-limak-thesis.tex#L171-L210):
- `\title{}` - Full thesis title
- `\titleshort{}` - Abbreviated title for headers
- `\subtitle{}` - Optional subtitle
- `\author{}` with `\matno{}` - Author name and matriculation number
- `\supervisor{}` - Thesis supervisor
- `\degree{}{}` - Degree and program name (see curriculum options below)
- `\submissiondepartment{}` - Submitting institution
- `\date{}` - Submission date (defaults to compilation date)
- `\keywords{}` - Document keywords

**Curriculum Version Options** (line 196-200):
- Curriculum ab 2025S: `\degree{Master of Business Administration}{...}`
- Curriculum ab 2023W: `\degree{Executive Master of Business Administration}{...}`

### Bibliography Management

Edit [references.bib](limak-thesis-latex/references.bib) using standard BibTeX/BibLaTeX format:
```bibtex
@book{key2024,
  author = {Lastname, Firstname},
  title = {Book Title},
  year = {2024},
  publisher = {Publisher Name}
}
```

Cite in text using Harvard author-year style:
- `\parencite{key2024}` - Parenthetical citation: (Lastname 2024)
- `\textcite{key2024}` - Narrative citation: Lastname (2024)
- `\parencite[S.~15]{key2024}` - With page number: (Lastname 2024, S. 15)

### Font Issues

If XeLaTeX reports missing fonts:
1. Ensure Arial is installed on the system
2. Alternatively, switch to `nofancyfonts` option in package declaration
3. For pdfLaTeX compatibility, remove `fancyfonts` option entirely

### Eidesstattliche Erklärung (Statutory Declaration)

The statutory declaration is mandatory for LIMAK theses and is pre-configured in [main-limak-thesis.tex:229-244](limak-thesis-latex/main-limak-thesis.tex#L229-L244). The text matches LIMAK institutional requirements and should not be modified without verification.

## LIMAK Transferarbeit Requirements

For Transferarbeiten (transfer assignments), refer to [Leitfaden_Transferarbeit_2024.pdf](instructions/Leitfaden_Transferarbeit_2024.pdf) for official guidelines. Key requirements:

### Formal Requirements

**Formatting** (must match exactly):
- Font: Times New Roman 12pt OR Arial 11pt
- Line spacing: 1.5
- Paper: DIN A4
- Page tolerance: ±10% of specified page count (check course syllabus)

**Title Page Requirements**:
- Program name (e.g., "Master in Management")
- Course title
- Faculty member name
- Author name(s)

**File Naming Convention**:
- Format: `AuthorLastName_FacultyLastName.pdf`
- Example: `Haider_Muehlbacher.pdf`
- Group work: `Group1_FacultyLastName.pdf`
- Must be submitted as PDF (not password-protected)

### Structure Requirements

Standard structure for Transferarbeiten:
1. **Ausgangssituation** - Initial situation/context
2. **Fragestellung** - Research question
3. **Zielsetzung der Arbeit** - Objectives
4. **Inhaltliche Bearbeitung** - Content analysis based on objectives
5. **Schlussfolgerungen mit Handlungsempfehlungen** - Conclusions with recommendations

**Outline Rules**:
- Main chapters: Arabic numerals (1, 2, 3...)
- Table of contents/references: Roman numerals or unnumbered
- Subchapters must have minimum 2 subsections (e.g., 1.1, 1.2)
- Each paragraph must contain more than one sentence

### Language and Style

**Scientific Writing**:
- Avoid personal opinions ("Ich bin der Meinung...")
- Use objective formulations: "daraus lässt sich schließen...", "kann abgeleitet werden, dass..."
- Gender-neutral language required (Generalklausel not permitted)

### Citation Requirements

**General Rules**:
- Must be consistent, traceable, and complete throughout
- Choose either footnotes OR in-text citations (not both)
- No citations in headings

**Harvard Citation Style (as per LIMAK guidelines)**:

The templates use **Harvard authoryear style** with specific LIMAK formatting:

- **In-text citations** - Only surnames, no first names or initials:
  ```
  (Johnson / Scholes 2005, 435)
  Bougon et al. (2006, 117) zeigen, dass...
  ```

- **Narrative citations** - Author names written manually in text:
  ```latex
  Güttel und Kratochvil \parencite{key} betonen...
  ```
  Output: `Güttel und Kratochvil (2019) betonen...`

- **Parenthetical citations** - Full citation in parentheses:
  ```latex
  ... ist dokumentiert \parencite{key}.
  ```
  Output: `... ist dokumentiert (Güttel / Kratochvil 2019).`

**Key LaTeX Configuration** ([main-transferarbeit.tex:73](limak-transferarbeit-latex/main-transferarbeit.tex#L73)):
```latex
\usepackage[backend=biber,style=authoryear,maxcitenames=2,maxbibnames=99,
            sorting=nyt,uniquename=false,uniquelist=false]{biblatex}
```

- `uniquename=false` - Prevents adding first names for disambiguation (Harvard rule: surnames only)
- `uniquelist=false` - Prevents extending author lists for disambiguation
- Two-author separator: `/` (forward slash) as per LIMAK Leitfaden example
- Three+ authors: Automatically shortened to "et al."

**Citation Commands**:
- Use `\parencite{key}` for all citations (generates year in parentheses)
- Write author names manually in German ("und" between authors)
- DO NOT use `\cite{}` or `\textcite{}` - they generate incorrect formats

**Internet sources format**:
```
Author: Title. URL: http://... (dl: DD.MM.YYYY)
Example:
Reichard, Christoph: New Approaches to Public Management.
URL: http://www.example.com/paper.html (dl: 27.02.2006)
```

### Plagiarism Policy

**Results in automatic failure**:
- Copying passages without citation
- Submitting another person's work as your own
- Using AI (KI) to write the work

### Assessment

- Required for course completion
- Grading scale: 1 (sehr gut) to 5 (nicht genügend)
- Late submission may result in grade reduction
- Passed assignments cannot be repeated
