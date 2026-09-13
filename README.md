# Responsible Data Science Analysis - Fairness

This directory contains a ready-to-review reference draft for the DSCI 602
Responsible Data Science Analysis individual assignment.

## Overleaf entrypoint

- `main.tex` is the root Overleaf build file.
- The active draft is `Blueprint2/main.tex`.
- `.bib` files are retained because Overleaf needs them to resolve citations.

## Canonical files

- `fairness_analysis.tex` - IEEE conference-style manuscript source
- `fairness_references.bib` - verified bibliography records
- `fairness_analysis.pdf` - compiled review PDF

The `Blueprint/` and `Blueprint2/` directories each retain their corresponding
compiled `main.pdf` for direct review. Named PDFs are also preserved where they
document a distinct blueprint or reference draft.

## Repository content policy

The repository intentionally retains authoring and review artifacts only:

- LaTeX sources (`.tex`)
- bibliography databases (`.bib`)
- documentation and provenance notes (`.md`)
- intentional review outputs (`.pdf`)
- `.gitignore`, which excludes LaTeX/Overleaf build intermediates

Generated files such as `.aux`, `.bbl`, `.blg`, `.fdb_latexmk`, `.fls`, `.log`,
`.out`, and `.synctex.gz` are not versioned. Overleaf regenerates them during
compilation.

## Evidence boundary

The document is a prospective analysis. It does not claim completed live
fairness mediation, completed DSCI 602 fairness experiments, or new numerical
fairness findings. Prior DSCI 601 and EQUITAS materials were used as conceptual
and structural foundations; unsupported claims from older drafts were excluded.

## Build

Compile with the repository's LaTeX tooling or upload the `.tex` and `.bib`
files to Overleaf. The source uses the same `IEEEtran` `10pt,conference` format
observed in the latest Overleaf quantum manuscript.
