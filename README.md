# Lab 1: Experimental Design & Power with DeclareDesign

HPM 883: Advanced Quantitative Methods | Spring 2026

## Overview

In this lab, you will apply the **MIDA framework** (Model-Inquiry-Data-Answer) to design and diagnose randomized experiments using the DeclareDesign package.

**Learning Objectives:**
- Declare a complete experimental design using DeclareDesign
- Diagnose your design's statistical properties (bias, power, coverage)
- Redesign to compare simple vs. blocked randomization
- Analyze trade-offs between sample size, effect size, and power

## Quick Start

### Option 1: GitHub Codespaces (Recommended)
1. Click the green "Code" button above
2. Select "Open with Codespaces" → "New codespace"
3. Wait for the environment to build (~2-3 minutes)
4. Start working in `lab-1-design.qmd`

### Option 2: Local Setup
```bash
git clone <your-assignment-url>
cd <your-repo-name>
```

Open in RStudio/Positron, then:
```r
install.packages("renv")  # Only needed once
renv::restore()
```

## Repository Structure

```
lab-1-template/
├── README.md              # This file
├── lab-1-design.qmd       # YOUR WORK GOES HERE
├── renv.lock              # Package versions (reproducibility)
├── renv/                  # renv infrastructure
├── .devcontainer/         # GitHub Codespaces config
├── hpm883-lab.Rproj       # RStudio project file
└── output/                # Rendered documents
```

## Workflow

1. **Complete the lab** — Work through `lab-1-design.qmd`, filling in code where indicated
2. **Render your document** — Click "Render" or run `quarto render lab-1-design.qmd`
3. **Commit your work** — `git add . && git commit -m "Complete Lab 1"`
4. **Push to GitHub** — `git push`
5. **Submit to Gradescope** — Upload the rendered HTML file

## Codespaces IDE Options

When you open this repository in GitHub Codespaces, you'll see VS Code in your browser. You have two options:

### Option A: VS Code (Browser)
Work directly in the VS Code interface that opens.
- Open `lab-1-design.qmd`
- Run code chunks with `Ctrl+Enter` (`Cmd+Enter` on Mac)
- Use the R terminal in the bottom panel

### Option B: RStudio Server
If you prefer the familiar RStudio interface:
1. Look at the **PORTS** tab in the bottom panel
2. Find port **8787** (labeled "RStudio Server")
3. Click the **globe icon** to open RStudio in a new browser tab

## Key Packages

This lab uses the DeclareDesign ecosystem:
- `DeclareDesign` — Design declaration and diagnosis
- `fabricatr` — Data fabrication/simulation
- `randomizr` — Randomization procedures
- `estimatr` — Robust estimation

All packages are pre-installed via `renv::restore()`.

## Troubleshooting

### "Package not found" error
```r
renv::restore()  # Reinstall all packages
```

### Render fails
- Check for typos in your R code
- Make sure all code chunks run without errors
- Try running each chunk individually first

### Git issues
```bash
git status              # See what's changed
git diff                # See specific changes
```

## Getting Help

- **Slack**: Post questions in #hpm883-help
- **Office Hours**: See syllabus for times

---

*HPM 883: Advanced Quantitative Methods | Spring 2026*
