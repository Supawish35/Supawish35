# Design Specification: GitHub Profile README Redesign (Supawish35)

## Intent & Objective
Transform the GitHub profile README for **Supawit Hanmontree (Supawish35)** from a basic bullet-point and mixed-icon layout into an elite, recruiter-grade developer portfolio. The redesign strictly follows the **UI/UX Pro Max** design system and **UI Styling (shadcn / Tailwind minimal tokens)** principles, completely eliminating font-dependent emojis in favor of crisp vector SVGs and sleek semantic badge tokens.

---

## Design System Tokens
- **Design Philosophy**: Minimalist Flat / Shadcn Zinc Dark Primary
- **Primary Color**: `#09090B` (Zinc-950)
- **Border / Surface**: `#27272A` (Zinc-800) / `#18181B` (Zinc-900)
- **Accent Color**: `#3B82F6` (Electric Blue) / `#60A5FA`
- **Text Primary**: `#F4F4F5` (Zinc-100)
- **Text Secondary**: `#A1A1AA` (Zinc-400)
- **Iconography**: Lucide Vector Icons (`stroke-width: 2`, `#3B82F6` accent) via clean SVGs
- **Badges**: Unified flat-square & pill tokens (`shields.io` + `skillicons.dev`)

---

## Sections & Layout Architecture

### 1. Hero Header
- Dynamic animated typing SVG banner (`readme-typing-svg`) displaying:
  - *Full-Stack Developer*
  - *Backend & System Architecture*
  - *CS Student @ Udon Thani Rajabhat University*
  - *Building Modern Web & Desktop Solutions*
- Headline with clean typography and role descriptor.
- Quick status badge pills: `Location: Thailand` | `Education: UDRU` | `Status: Open to Collab`.

### 2. About Me (Zero Emojis)
- Structured into a clean card layout or minimalist bullet points with Lucide vector SVGs:
  - `<img src=".../lucide/terminal.svg" width="16" />` Current focus: Web and desktop applications using PHP, C#, Node.js, Next.js.
  - `<img src=".../lucide/database.svg" width="16" />` Engineering depth: Backend architecture, system analysis, and relational database modeling.
  - `<img src=".../lucide/shield-check.svg" width="16" />` Security & Performance: Exploring secure authentication, clean API design, and system optimization.
  - `<img src=".../lucide/sparkles.svg" width="16" />` Philosophy: Transforming abstract data flow diagrams into robust, maintainable production code.

### 3. Categorized Tech Stack Grid
Organized cleanly into semantic categories with SkillIcons in consistent dark theme (`theme=dark`):
- **Frontend**: React, Next.js, TypeScript, JavaScript, Tailwind CSS, Bootstrap, HTML5, CSS3
- **Backend & Systems**: Node.js, Express, PHP, C#, Python, C, Kotlin
- **Databases & Storage**: PostgreSQL, MySQL, MariaDB, Microsoft SQL Server
- **Cloud & DevOps**: AWS, Azure, Linux, Git, Docker, Postman

### 4. Metrics & Signature Pacman Contribution Graph
- Embedded full-width container showcasing the custom automated `pacman-contribution-graph-dark.svg` / light SVG from `origin/output`.
- Dual side-by-side performance cards:
  - GitHub Readme Stats (Sigma mirror with Dark Zinc theme: `bg_color=09090b&border_color=27272a&title_color=3b82f6&text_color=e4e4e7&icon_color=60a5fa`)
  - GitHub Streak Stats (`streak-stats.demolab.com` with matching dark theme)

### 5. Connect & Socials Footer
- Polished badge pill buttons with official logos and monochrome hover styling for:
  - GitHub
  - Facebook
  - Instagram
  - YouTube
  - Email contact badge
