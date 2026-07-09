# AGENTS.md

## Project
LaTeX textbook "Precálculo" (Precalculus, Algebra & Trigonometry) by Juliho David Castillo Colmenares. CC BY 4.0 license.

## Structure
- `ebook/` — Main textbook source. Entry point: `ebook/[Precálculo].tex`
- `soluciones/` — Solutions manual. Entry point: `soluciones/[Precálculo - Soluciones].tex`
- `ebook/calculo/`, `ebook/trig/`, `ebook/edo/`, `ebook/md/`, `ebook/mba/`, `ebook/cvv/`, `ebook/em/`, `ebook/precalculo/` — Image assets per topic

## Build
No Makefile or scripts. Compile manually:
```
cd ebook && pdflatex "[Precálculo].tex"
```
Run 2–3 times for TOC/refs to resolve. Output: `ebook/[Precálculo].pdf`

## Conventions
- Document class: `tufte-book` (margin notes, wide margins)
- Language: Spanish (`babel` with `spanish,mexico`)
- Encoding: UTF-8 (`inputenc`)
- Chapter files use `(p)` suffix for practice/exercise sections (e.g., `logica.tex` + `logica(p).tex`)
- Shared config: `_paquetes.tex` (packages), `_comandos*.tex` (macros), `_tufte.tex` (class tweaks)
- Custom macros in `comandos.tex`: `\R`, `\N`, `\Q`, `\C`, `\Z`, `\lap{}`, `\lapin{}`, etc.

## Key gotchas
- Filename `[Precálculo].tex` contains brackets — quote paths in shell commands
- No CI, tests, or linting — this is a pure LaTeX document project
- Images are all PNG/JPG/SVG in topic subdirectories under `ebook/`
