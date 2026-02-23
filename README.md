# Lab 2: ML Regularization, Trees & Forests

HPM 883: Advanced Quantitative Methods | Spring 2026

## Overview

This two-part lab builds hands-on intuition for the ML tools underlying Double Machine Learning.

**Part 1 (Mon Feb 23, Remote):** Regularized regression — OLS, Ridge, LASSO, Elastic Net, and the instability problem.

**Part 2 (Wed Feb 25, In-Person):** Tree-based methods — decision trees with `rpart`, random forests with `ranger`, and model comparison.

**Learning Objectives:**
- Fit and compare OLS, Ridge, LASSO, Elastic Net, decision trees, and random forests
- Visualize how regularization shrinks and zeros out coefficients
- Select optimal tuning parameters using cross-validation and OOB error
- Demonstrate LASSO's instability — the key motivation for DML
- Compare linear and tree-based methods on the same dataset

## Quick Start

### Option 1: GitHub Codespaces (Recommended)
1. Click the green "Code" button above
2. Select "Open with Codespaces" → "New codespace"
3. Wait for the environment to build (~2-3 minutes)
4. Start working in `lab-2-ml-regularization.qmd`

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
lab-2-template/
├── README.md                       # This file
├── lab-2-ml-regularization.qmd     # YOUR WORK GOES HERE
├── renv.lock                       # Package versions (reproducibility)
├── renv/                           # renv infrastructure
├── .devcontainer/                  # GitHub Codespaces config
├── hpm883-lab.Rproj                # RStudio project file
└── output/                         # Rendered documents
```

## Workflow

1. **Work through the lab** — Run each code chunk in `lab-2-ml-regularization.qmd` interactively
2. **This is a code-along** — All chunks have `eval: false`, so you run them yourself
3. **Try the exercises** — Part 8 has optional exercises to deepen understanding
4. **No formal submission required** — This is an ungraded in-class activity

## Codespaces IDE Options

When you open this repository in GitHub Codespaces, you'll see VS Code in your browser. You have two options:

### Option A: VS Code (Browser)
Work directly in the VS Code interface that opens.
- Open `lab-2-ml-regularization.qmd`
- Run code chunks with `Ctrl+Enter` (`Cmd+Enter` on Mac)
- Use the R terminal in the bottom panel

### Option B: RStudio Server
If you prefer the familiar RStudio interface:
1. Look at the **PORTS** tab in the bottom panel
2. Find port **8787** (labeled "RStudio Server")
3. Click the **globe icon** to open RStudio in a new browser tab

## Key Packages

This lab uses:
- `glmnet` — Ridge, LASSO, and Elastic Net regression
- `ISLR2` — Hitters dataset (baseball salary prediction)
- `tidyverse` — Data manipulation and visualization
- `rpart` — Decision trees (CART)
- `rpart.plot` — Tree visualization
- `ranger` — Fast random forests

All packages are pre-installed via `renv::restore()`.

## Troubleshooting

### "Package not found" error
```r
renv::restore()  # Reinstall all packages
```

### Render fails
- This lab is designed to be run interactively, not rendered
- Run each chunk individually using Ctrl+Enter / Cmd+Enter

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
