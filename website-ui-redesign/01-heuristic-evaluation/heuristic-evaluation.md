# Heuristic Evaluation — Rosemary & Rye (Current Site)

Evaluation method: Jakob Nielsen's 10 Usability Heuristics, applied to the current Rosemary & Rye website. Each issue is rated on Nielsen's 0–4 severity scale:

`0` = not a problem · `1` = cosmetic · `2` = minor · `3` = major, high priority · `4` = usability catastrophe

## Current Site Summary

A single-owner bakery/café site last redesigned roughly a decade ago. Fixed-width desktop layout (960px), no mobile stylesheet, mixed fonts inherited from an old page-builder template, and content added over the years without editing older content down.

## Findings

| # | Heuristic | Issue | Severity | Recommendation |
|---|---|---|---|---|
| 1 | Visibility of system status | Clicking "Order Online" opens a third-party ordering site in the same tab with no warning, then the back button returns to a stale cached version of the homepage. | 3 | Open external ordering in a new tab, or clearly signal the handoff. |
| 2 | Match between system and the real world | Menu items are grouped by internal bakery department names ("Bench," "Retail Case," "Wholesale") instead of familiar categories like Breads, Pastries, Cakes. | 3 | Rename categories using customer-facing language. |
| 3 | User control and freedom | No visible way to get back to the homepage from interior pages — the logo isn't a link and there's no persistent nav. | 4 | Make the logo a home link; keep primary nav visible on every page. |
| 4 | Consistency and standards | Three different fonts are used across the homepage (a script font in the header, serif in body text, and a default sans-serif in the footer), and button styles differ page to page. | 3 | Establish one type system and one consistent button style (see style guide). |
| 5 | Error prevention | The contact form has no field validation; empty submissions silently fail with no message. | 3 | Add inline validation and a clear success/error state. |
| 6 | Recognition rather than recall | Store hours are only listed on the "Contact" page, not the homepage, so a user checking "are they open now" has to navigate away from wherever they are. | 2 | Surface hours (and an open/closed state) in the header or footer sitewide. |
| 7 | Flexibility and efficiency of use | No shortcuts for returning customers — e.g. no quick-reorder, no saved favorites — though this may be reasonable for a small bakery site's scope. | 1 | Low priority; consider only if repeat online ordering becomes core to the business. |
| 8 | Aesthetic and minimalist design | The homepage has 6+ competing sections above the fold: a rotating image carousel, a popup email signup, an autoplaying background video, and dense paragraph text — all before any bread is shown. | 4 | Reduce to one clear hero moment; remove autoplay and popups; let the product lead. |
| 9 | Help users recognize, diagnose, and recover from errors | The 404 page is the default web host error page with no bakery branding, navigation, or explanation. | 2 | Replace with a branded 404 that links back to the homepage and menu. |
| 10 | Help and documentation | Ordering/catering FAQs are scattered across old blog posts rather than a dedicated page. | 2 | Consolidate into a single FAQ or catering page linked from the nav. |

## Additional Technical/Accessibility Issues Found

- **No responsive layout:** the fixed 960px width causes horizontal scrolling on any phone-width screen; text does not reflow.
- **Low text contrast:** body copy is light gray (#999) on white, failing WCAG AA contrast for normal text.
- **Small tap targets:** nav links and the "Order" button are under the 44×44px recommended minimum, making them error-prone to tap on mobile.
- **Buried primary action:** the "Order Online" button is small and placed in the footer, despite being the site's most important conversion action.

## Priority Summary (highest severity first)

1. **(Sev 4)** Fix homepage clutter — one hero, no autoplay/popups (Heuristic 8)
2. **(Sev 4)** Add persistent navigation with a working home link (Heuristic 3)
3. **(Sev 3)** Establish a single, consistent type and component system (Heuristic 4)
4. **(Sev 3)** Rename menu categories to customer-facing language (Heuristic 2)
5. **(Sev 3)** Fix the external-ordering handoff and form validation (Heuristics 1, 5)
6. **Cross-cutting:** rebuild responsively, fix contrast, enlarge tap targets

These six priorities directly define the goals for the mood board, style guide, and high-fidelity mockup that follow.
