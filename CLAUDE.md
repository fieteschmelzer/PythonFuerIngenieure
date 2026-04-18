# CLAUDE.md

This file provides guidance to Claude Code when working in this repository.

## What This Is

Course repository for **Python für Ingenieure** at TU Berlin (instructor: Gert Herold). All work is done in Jupyter notebooks (`.ipynb`). No build system, no package manager beyond a local `.venv`.

## Folder Structure

| Folder | Purpose |
|---|---|
| `Arbeitsmaterial/` | Lecture notebooks provided by the course — do not modify |
| `Hausaufgaben/` | Homework submissions, one subfolder per assignment |
| `Skripte/` | Standalone Python scripts |

Homework folders follow the pattern `Hausaufgaben/HA<Nr>/` and the submission file is named `HA<Nr>_Gruppe<Gruppennr>.ipynb`.

## Branching Rules

- `main` is stable — only finished, reviewed material lands here.
- Each homework gets its own branch: `HA<Nr>_<kurzer-titel>`, e.g. `HA1_Schleifen`.
- Changes to `main` only via Pull Requests — never push directly.

## Commit Conventions

- Messages in German or English, clear and concise: what changed and why.
  - Good: `HA1: Aufgabe 2 gelöst, Schleife optimiert`
  - Bad: `update`, `fix`, `asdf`
- One logical change per commit.
- Before committing: all notebook cells must run clean (`Kernel → Restart & Run All`).

## Notebook Rules

- Write own code directly under `# Hier eigenen Code schreiben ...` comments.
- All `assert`-cells (plausibility tests) must pass without errors before submission.
- Cell outputs may be committed — they help during review.
- No empty trailing cells, no unnecessary kernel restarts left in history.
- Do not check in solution files (`Musterlösung`) or others' solutions into homework folders.

## What Is Never Committed

Already covered by `.gitignore`:
- `.venv/` — virtual environment
- `__pycache__/`, `*.pyc` — Python cache
- `.ipynb_checkpoints/` — Jupyter checkpoints
- `.DS_Store` — macOS metadata

## Environment

```bash
# Activate venv
source .venv/bin/activate

# Start Jupyter
jupyter notebook
```

## Obsidian Notes

Course notes live in the Second Brain vault at:
`/Users/fiete/Documents/App-Data/Obsidian/Fiete's Second Brain copy/04 Studium/Master/Python for Engineers/`
