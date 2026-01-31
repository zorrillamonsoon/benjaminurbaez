# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal website for Benjamin Urbaez - a Dominican-American spiritual music artist born and raised in Queens, NYC. From a musical family, he channels his Dominican heritage through live afrobeats, spoken word, and indigenous-influenced music, including his collaboration with Dreeemy.

## Tech Stack

- Static HTML/CSS/JS (no build step required)
- Google Fonts: Cinzel (display) + Cormorant Garamond (body)
- CSS custom properties for theming
- Vanilla JS for IntersectionObserver animations and mobile nav

## Local Development

```bash
# Via MAMP (primary)
open http://localhost:8888/benjaminurbaez/

# Alternative without MAMP
npx serve -l 8080 .
```

## Design System

**Colors** (use CSS variables):
- `--black: #0D0B0A` - primary background
- `--burgundy: #722F37` - accent, links, decorative lines
- `--brown: #4A3728` - secondary backgrounds
- `--cream: #E8E0D5` - primary text
- `--cream-muted: #C4B8A8` - secondary text
- Light variants: `--burgundy-light`, `--brown-light`, `--grey-warm`

**Typography**:
- `--font-display` (Cinzel): headings, nav, labels - always uppercase with `letter-spacing: 0.15em+`
- `--font-body` (Cormorant Garamond): body text, weight 300, italic for metadata

**Spacing**: `--space-xs` through `--space-2xl` (0.5rem to 12rem)

**Rules**: No white backgrounds, no box-shadows, no borders (except 1px decorative lines in burgundy)

## CSS Architecture

- BEM naming: `.block__element--modifier`
- Responsive breakpoints: 1024px (tablet), 768px (mobile)
- Animation classes: `.animate-fade-in-up`, `.animate-delay-1` through `.animate-delay-5`
- Container variants: `.container`, `.container--wide` (1600px), `.container--narrow` (900px)

## JavaScript Features

`script.js` handles:
- Mobile nav toggle (hamburger menu at 768px)
- IntersectionObserver for scroll-triggered fade animations
- Hero parallax effect on scroll
- Nav background opacity change after 100px scroll

## Assets

Images in `assets/` folder: `benjaminurbaez_01.jpeg` through `benjaminurbaez_06.jpeg` (plus one `.gif`). Hero uses `_02`, portraits use others contextually.
