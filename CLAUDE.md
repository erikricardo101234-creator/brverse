# CLAUDE.md — AI Assistant Guide for brverse

## Repository Overview

**brverse** is a community-curated reference repository listing R packages for accessing Brazilian data sources. The name combines "Brazil" and "verse" (as in a universe of packages, inspired by the tidyverse concept).

This is a **documentation-only repository** — there is no application code, build system, test suite, or deployment infrastructure. The primary artifact is `README.md`.

**Language:** Content is written in Brazilian Portuguese.

---

## Repository Structure

```
brverse/
├── README.md          # The main content — categorized list of R packages
├── CLAUDE.md          # This file
└── brverse_logo.png   # Project logo displayed in README header
```

---

## Core Policy

> **Only packages published on CRAN are included.**

This is the single most important rule when evaluating contributions. Packages hosted only on GitHub, r-universe, or other repositories are not eligible for inclusion, regardless of their quality or usefulness.

---

## README Structure

The README organizes packages into 10 thematic categories, each as an H2 section:

| Category (PT) | Category (EN) |
|---|---|
| Economia e Finanças | Economics & Finance |
| Eleitorais e Política | Electoral & Politics |
| Espaciais e de endereços | Spatial & Addresses |
| Meio ambiente | Environment |
| Nomes | Names |
| População e dados socioeconômicos | Population & Socioeconomic |
| Saúde | Health |
| Segurança pública | Public Security |
| Transportes | Transportation |
| Miscelânea | Miscellaneous |

### Entry Format

Each package entry follows this exact format:

```markdown
- [PackageName](URL): Short English description of what the package does
```

- **Package name:** Use the exact CRAN package name (case-sensitive)
- **URL:** Prefer the CRAN page (`https://CRAN.R-project.org/package=PackageName`) when available; project/documentation sites are acceptable as alternatives
- **Description:** One-line English description, typically taken from the package's CRAN title

---

## Common Tasks for AI Assistants

### Adding a New Package

1. Verify the package is on CRAN before adding it
2. Identify the correct category based on the package's domain
3. Add the entry in alphabetical order within its category (preferred, though not strictly enforced)
4. Use the standard `- [Name](URL): Description` format
5. Keep the description concise — one line only

### Updating an Existing Entry

- Update URLs if a package has moved (e.g., from GitHub to CRAN)
- Update descriptions if the package scope has changed
- Never remove a package unless it has been archived/removed from CRAN

### Removing a Package

Only remove a package if it has been removed from CRAN and is no longer maintained. Always verify before removing.

---

## Git Workflow

This repository uses a standard PR-based contribution model:

```bash
# Check current branch
git status

# Make changes to README.md
# ...

# Stage and commit
git add README.md
git commit -m "Add <PackageName> to <Category>"

# Push to feature branch
git push -u origin <branch-name>
```

### Commit Message Conventions

Commit messages observed in the project history:
- `Add <package> package` — for new packages
- `Update <package> link to CRAN` — for URL updates
- `Update README to clarify <topic>` — for policy/documentation changes
- `Remove <package> package link` — for removals

Keep messages short and descriptive. No conventional commits prefix (feat:, fix:) is required.

---

## What This Repository Is NOT

- Not an R package itself
- Not a website with a build step
- Not an API or service
- Has no tests to run
- Has no dependencies to install
- Has no environment variables or configuration files

---

## Contribution Guidelines (for AI Assistants)

When helping with this repository:

1. **Always verify CRAN status** before adding any package
2. **Preserve existing formatting** — match the markdown style exactly
3. **Write descriptions in English** — even though the README headers are in Portuguese
4. **Do not reorganize categories** unless explicitly asked
5. **Do not add packages not on CRAN** — this is a hard policy boundary
6. **Check for duplicates** before adding a new entry
7. **Maintain alphabetical order** within categories where possible
