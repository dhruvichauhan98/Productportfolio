# Subsidex Case Study — HTML Page Design

**Date:** 2026-07-19  
**Source:** `assets/ppt/subsidex-architecture-case-study.pptx` (17 slides)  
**Output:** `assets/case-studies/subsidex.html` (standalone, not linked yet)

## Goal

Convert the Subsidex architecture case study PPT into a scrollable long-form HTML page that matches the existing portfolio design system. Not linked anywhere yet.

## Design System

- **Fonts:** Space Grotesk (headings), Public Sans (body), Lora (italic/taglines) via Google Fonts
- **Colors:** `--navy-950: #101018`, `--gold: #7C6FF0`, `--steel: #45C4B0`, `--ink: #EDEBF5`, `--ink-dim: #B4B1C7`
- **Accents:** Gold for primary labels/highlights, teal for secondary accents
- **Layout:** max-width 1180px centered, 48px horizontal padding

## Sections (Thematic Grouping — Approach B)

1. **Hero** (Slide 1) — Eyebrow label, "Subsidex" large heading, one-paragraph description, role/date line, 4-stat row (2 govt portals, 120+ days claims cycle, 5 stakeholder tiers, 3 revisions)
2. **The Problem** (Slide 2) — Intro paragraph, 3 numbered pain points as cards
3. **Objectives** (Slides 3–4) — Two-column layout: 3 business outcome cards + 10 architectural goal list items
4. **Before Subsidex** (Slide 5) — Narrative intro + 4-step horizontal flow (EXTRACT → CURATE → PUSH → REPEAT)
5. **Solution** (Slides 6–11) — Scope checklist (12 items), design inputs (assumptions + constraints in two columns), architecture diagram (image1.jpg), infra architecture (image2.png), 10-step data flow numbered list, RPA engine + integrations two-column card
6. **Security & Compliance** (Slides 12–14) — Data security bullets + image3.png, multi-tenancy bullets + image4.png, archival/RBAC three-column cards
7. **Business Value** (Slide 15) — 7 value points as a card grid
8. **Document History** (Slide 16) — Timeline of 3 revisions (v1.0, v1.1, v1.2) with dates and reviewer names
9. **Closing** (Slide 17) — "Thank you" centered panel with Dhruvi Chauhan's name/role

## Images

Copied from PPTX to `assets/ppt/subsidex-images/`:
- `image1.jpg` → Slide 8 (Application architecture)
- `image2.png` → Slide 9 (Integration & infrastructure architecture)
- `image3.png` → Slide 12 (Data security)
- `image4.png` → Slide 13 (Multi-tenancy)

## Constraints

- Fully self-contained HTML (single file with inline CSS)
- No JavaScript required
- No nav header (standalone page, not linked to portfolio nav yet)
- Responsive down to 375px
