# GitHub Profile README Redesign Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Transform the GitHub profile README into a high-polish, emoji-free developer portfolio applying `ui-ux-pro-max` and `ui-styling` design systems.

**Architecture:** Replace all emojis with crisp vector Lucide SVG icons and shadcn-inspired badge pills. Structure the profile into 5 clear visual layers: Hero Header (Typing SVG), Profile Overview Card, Categorized Tech Stack Grid (Skillicons), GitHub Metrics & Signature Pacman Graph, and Connect Footer.

**Tech Stack:** GitHub Flavored Markdown (GFM), HTML5, SVG (Lucide icons via Iconify, Readme-Typing-SVG, SkillIcons, Shields.io, GitHub Streak/Stats).

**Spec:** docs/superpowers/specs/2026-11-09-github-readme-redesign.md

## Global Constraints
- Zero emojis across the entire README (no `👋`, `👨‍💻`, `🛠️`, `📊`, `🔗`, `🔭`, `🌱`, `💻`, `⚡`).
- All structural icons must use vector SVGs (Lucide icons with cohesive color `#3b82f6` / `#60a5fa`).
- Maintain dark/light mode compatibility using GitHub `<picture>` tags where applicable.
- Preserve existing automated workflow output (`pacman-contribution-graph.svg` from `output` branch).
- Keep all valid social links (Facebook, Instagram, YouTube) and profile metadata intact.

## Review Focus
1. Markdown table and alignment rendering in both GitHub web and mobile views.
2. SVG asset loading and fallback resilience (e.g. valid URLs, proper sizing attributes `width` and `height`).
3. Total visual density and vertical rhythm: clean 16px/24px spacing, avoiding clustered or cramped icon blocks.
4. Accessibility: proper `alt` tags on all vector images and links.
5. Contrast standards: WCAG AAA compliance on dark and light backgrounds.

---

### Task 1: Draft the Complete Modern README.md

**Files:**
- Modify: `README.md:1-79`

**Interfaces:**
- Consumes: Profile data, existing social links, pacman workflow output link.
- Produces: Polished GitHub profile markdown with zero emojis, vector Lucide icons, categorized skill grids, and responsive metric cards.

- [ ] **Step 1: Write the failing test / verification check**
Check that the current README contains emojis and unorganized devicon blocks.
Run: `grep -P "[\x{1F300}-\x{1F9FF}]" README.md`
Expected: Matches found (multiple emoji occurrences).

- [ ] **Step 2: Update README.md with the emoji-free shadcn UI layout**
Replace `README.md` with the new design:
1. Dynamic typing SVG hero banner.
2. About Me section with Lucide SVG indicators.
3. Categorized Tech Stack cards with SkillIcons dark theme pills.
4. GitHub Activity section with the signature Pacman SVG and dark metrics cards.
5. Sleek contact footer with official brand badges.

- [ ] **Step 3: Verify zero emojis remain**
Run: `grep -P "[\x{1F300}-\x{1F9FF}]" README.md`
Expected: No matches (exit code 1).

- [ ] **Step 4: Verify all URLs and image assets respond with HTTP 200**
Run a curl validation script against all external asset URLs in `README.md`.
Expected: All return HTTP 200.

- [ ] **Step 5: Commit changes**
Run:
```bash
git add README.md docs/
git commit -m "feat: redesign github profile readme with ui-ux-pro-max and zero emojis"
```
