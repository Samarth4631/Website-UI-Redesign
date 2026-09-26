# Style Guide — Rosemary & Rye Redesign

Translates the heuristic evaluation's priorities into concrete visual decisions. See the mood board ([`moodboard.svg`](moodboard.svg)) for these tokens shown together.

## Design Principles

- **One hero, not six.** The homepage gets a single clear opening moment — a headline, one supporting line, one CTA — instead of competing carousels and popups.
- **Bread leads, chrome follows.** Visual weight goes to the product (illustrated in this exercise, photography in production), not to navigation decoration.
- **Grounded, not generic.** Warm and tactile like a neighborhood bakery, without defaulting to the cream-and-terracotta look every AI-generated bakery site reaches for — this palette leans into deeper plum and ink instead.
- **One accent, used sparingly.** Mustard gold marks exactly one thing per screen: the primary action.

## Color Palette

| Token | Hex | Use |
|---|---|---|
| Ink | `#2B241C` | Primary text, nav background |
| Flour | `#EDE6D6` | Page background |
| Plum | `#4A2439` | Secondary backgrounds, section dividers |
| Sage | `#71805B` | Supporting accents, icons |
| Mustard | `#C7972B` | Primary CTA only — used sparingly |
| Card White | `#FBF8F2` | Card surfaces on the flour background |

This directly fixes Heuristic 8 (contrast) from the evaluation: Ink-on-Flour body text measures well above WCAG AA contrast, replacing the old #999-on-white body copy.

## Typography

| Role | Typeface | Notes |
|---|---|---|
| Display / Headings | **Fraunces** (serif) | High-contrast, slightly quirky serif — carries the bakery's handmade character. Used at large sizes only. |
| Body / UI | **Work Sans** (sans-serif) | Clean and highly legible at small sizes; used for all body copy, nav, and buttons. |

**Type scale** (desktop → mobile):

| Level | Desktop | Mobile | Weight |
|---|---|---|---|
| Display (H1) | 56px | 34px | 600 |
| H2 | 36px | 26px | 600 |
| H3 | 24px | 20px | 600 |
| Body | 17px | 16px | 400 |
| Small / labels | 14px | 13px | 500 |

Line length is kept under ~75 characters for body paragraphs, per typographic best practice for readability.

## Spacing & Layout

- Base unit: **8px**. Section padding uses multiples of it (32px, 64px, 96px).
- Max content width: **1120px**, centered, with 24px side gutters on mobile.
- Grid: 12-column on desktop, collapsing to a single column below 720px.

## Components

- **Buttons:** one primary style (mustard fill, ink text, 8px radius) and one secondary style (ink outline, transparent fill). No third button style — this directly fixes Heuristic 4 (inconsistent buttons) from the evaluation.
- **Nav:** persistent header on every page, logo always links home (fixes Heuristic 3), inline links on desktop, full-height overlay menu on mobile.
- **Cards:** flat Card White surfaces with a 1px hairline border rather than a drop shadow — keeps the tactile, paper-like feel instead of a generic "SaaS card" look.
- **Tap targets:** all interactive elements minimum 44×44px, addressing the accessibility issue found in evaluation.

## Responsive Breakpoints

| Breakpoint | Width | Behavior |
|---|---|---|
| Desktop | ≥ 900px | Multi-column hero and menu grid, inline nav |
| Mobile | < 720px | Single-column stack, hamburger nav opens full-screen overlay |

(720–900px transitional styles are handled by the same rules scaling down; the mockup's CSS uses a single breakpoint at 720px to keep the demo focused, per the low-fidelity → high-fidelity progression of this exercise.)
