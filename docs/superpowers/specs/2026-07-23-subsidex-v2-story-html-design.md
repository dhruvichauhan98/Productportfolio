# Subsidex Case Study v2 — Story-Flow HTML Design

**Date:** 2026-07-23  
**Source:** `assets/ppt/subsidex-architecture-case-study.pptx` (17 slides) + existing `assets/case-studies/subsidex.html`  
**Output:** `assets/case-studies/subsidex-v2.html` (standalone, not linked yet)  
**Constraint:** Do NOT modify `subsidex.html`

## Goal

A second version of the Subsidex case study HTML that tells the story as a journey — five phases with shifting visual temperature — rather than a section-by-section conversion. The reader should feel momentum and narrative logic as they scroll.

## Narrative Arc — Five Phases

| # | Name | Sections | Background treatment |
|---|---|---|---|
| 1 | Cold | Hero + Problem | `#0d0d17` with faint cool blue radial glows |
| 2 | Shift | Objectives + Baseline | Neutral `#101018` |
| 3 | Build | Solution | `#101018`, open and spacious |
| 4 | Guard | Security | `#0f1019` with faint teal radial bloom |
| 5 | Warm | Value + History + Closing | `#101018` with gold/purple radial bloom |

## Visual Technique — Background Temperature (Static CSS Only)

- Each phase is a `<div class="phase phase-[name]">` wrapper
- Background is a CSS `radial-gradient` stack directly on the div — no pseudo-elements, no JS
- Bridges between phases use `linear-gradient` to dissolve from one phase background to the next over ~120px

## Between-Phase Bridges

Four bridge elements, each containing:
1. A 40px gold rule (`<div class="pq-rule">`)
2. A pull quote (`<blockquote class="pull-quote">`) — Space Grotesk 30–58px clamp, italic, bold
3. A narrative bridge paragraph (`<p class="narrative-bridge">`) — Lora 17px italic, max 50ch

### Pull quotes and narrative bridges

**Bridge 1 (Cold → Shift):**
- Quote: *"120+ days. Still run by hand."*
- Narrative: "The problem wasn't new technology or missing data. It was that every piece of it was moving through human hands — slowly, inconsistently, with no visibility into what was falling through the cracks. The architecture needed to fix all of that at once."

**Bridge 2 (Shift → Build):**
- Quote: *"There was no system to displace. Just a habit."*
- Narrative: "Before proposing anything, I needed to understand what we were replacing. Not a system — a process. No migration path, no legacy data to preserve. We were building from zero, onto live ground."

**Bridge 3 (Build → Guard):**
- Quote: *"Ten steps. Zero manual intervention."*
- Narrative: "The architecture wasn't just sound on paper. It had to hold against government portal downtime, third-party failures, and a data pipeline that couldn't afford to lose a single file. Security came next — not as an afterthought, but baked into every decision that came before."

**Bridge 4 (Guard → Warm):**
- Quote: *"Every tenant's data: isolated by design."*
- Narrative: "A platform carrying government credentials and financial reconciliation data had one non-negotiable: no tenant's data could ever touch another's. The security architecture answered that. Then it went further."

## Within-Phase Connectors

Between sections *within* the same phase, a subtle `chapter-connector` element:
- Thin hairline + small uppercase label (e.g. "The problem", "The vision")
- Color: `rgba(255,255,255,.06)` — barely visible, just enough to mark a beat

## Layout Rhythm Per Phase

- **Cold:** Compact card padding (22px), tighter section padding (72px), cards feel dense/pressured
- **Shift:** Standard spacing, analytical columns
- **Build:** Open — subsections separated by 80px, images full-width with more border-radius (20px), data flow steps have 22px padding
- **Guard:** Precise, tight grid (archival cards 20px padding), deliberate
- **Warm:** Generous — value items 24px padding, timeline has more vertical room, closing has 120px top padding

## Design System

Same as v1: navy/gold/teal palette, Space Grotesk + Lora + Public Sans, Google Fonts.

## File

`assets/case-studies/subsidex-v2.html` — images reference `../ppt/subsidex-images/`
