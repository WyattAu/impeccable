  champagne: "oklch(91% 0 0)"                 # headlines, <strong>; neutral white (name kept for compat)
  text-warm: "oklch(88% 0 0)"                 # body; neutral near-white
  gold-hairline: "oklch(78% 0 0 / 0.16)"      # default rule; neutral (name kept for compat)
  gold-hairline-strong: "oklch(74% 0.09 82 / 0.6)" # active rule; gold
- **Buttons**: use `.ks-button` + a variant (`.ks-button-primary`, `-secondary`, `-ghost`, `-disabled`). Do not write a new `.hero-cta-primary` / `.footer-cta` / `.section-action-button` class; those are the bespoke vocabularies the kit is meant to replace.
- **Section scaffolding**: use `.ks-section` for the container, `.ks-section-head` for the header, `<h2>` inside that (the kit styles it), and `.ks-section-sub` for the subhead. Eyebrow above the h2 is optional via `.ks-section-eyebrow`; skip it on editorial walkthroughs where every-section eyebrows read as AI scaffolding.
Invent only when the kit truly doesn't cover the shape. When you do invent, flag it; a new pattern that solves a real recurring need belongs in the kit, not in page-specific CSS. Page CSS is for genuinely page-specific scenery (hero illustrations, unique editorial visuals), not for reinventing primitives the kit already has.
- `.ks-brand`; wrapper for the brand mark + wordmark lockup (anchor or div).
- `.ks-mark`; the carved-tile glyph (a solid kinpaku square split by a diagonal slash), 38×38, no container border.
- `.ks-wordmark`; the IMPECCABLE wordmark text, solid Alumni Sans (`--ks-font-wordmark`), uppercase, weight 400, letter-spacing 0.15em.
- `.ks-section`; page-level section container, 1320px max-width, kit gutters.
- `.ks-section-head`; the section header block.
- `.ks-section-eyebrow`; small mono eyebrow above the h2 (optional).
- `.ks-section-head h2`; auto-styles any h2 inside `.ks-section-head` to the section title scale (weight 300, kit display family).
- `.ks-section-sub`; subhead paragraph below the h2.
- `.ks-subsection`; nested grouping inside a section.
- `.ks-subsection-label`; small mono label above a subsection's content.
- `.ks-button.ks-button-primary`; filled kinpaku CTA, dark text. Both classes required.
- `.ks-button.ks-button-secondary`; outlined kinpaku CTA.
- `.ks-button.ks-button-ghost`; text-only kinpaku button.
- `.ks-button[disabled]` or `.ks-button.ks-button-disabled`; disabled state.
- `.ks-button-arrow`; wrapper for an arrow SVG inside a button (sized correctly).
- `.ks-button-row`; flex row helper for horizontal button groups.
- `.ks-form-sample`; vertical form layout.
- `.ks-toggle`; switch (checkbox underneath, label visible).
- `.ks-checkbox`; checkbox with label.
- `.ks-select`; dropdown.
- `.ks-tabs`; tab container.
- `.ks-tab-list`; tab buttons row.
- `.ks-tab-panel`; tab content panel.
- `.ks-badge` + `.is-detected` / `.is-improved` / `.is-ready`; pill badge with dot.
- `.ks-badge-row`; flex row helper.
- `.ks-tag` + `.is-detected` / `.is-improved` / `.is-neutral` / `.is-ready`; slim tag, no dot.
- `.ks-tag-row`; flex row helper.
- `.ks-toast` + `.is-success` / `.is-warning`; alert toast with icon + dismiss.
- `.ks-toast-icon` / `.ks-toast-close`; inner parts.
- `.ks-modal` + `.ks-modal-actions` / `.ks-modal-close`; dialog box.
- `.ks-empty` + `.ks-empty-icon`; empty-state block.
- `.ks-skeleton`; loading shimmer.
- `.ks-pagination`; paged-list nav.
- `.ks-icon-button` + `.ks-tooltip`; circular icon button with hover tooltip.
- `.ks-bento`; 12-column grid with dark plinth + 8px gutters.
- `.ks-bento-tile`; single tile within a bento.
- `.ks-bento-tile--span-4` / `--span-6` / `--span-8`; sizing (e.g. 8/4, 6/6, 4/8).
- `.ks-bento-num`; tiny mono caps marker for tile numbering. Add `data-color="patina"` to flip to verdigris.
- `.ks-changelog`; vertical list wrapper.
- `.ks-changelog-entry`; single dated entry.
- `.ks-changelog-date`; left-column date.
- `.ks-changelog-body`; right-column content. Use `<em>` inside `<strong>` for a small "NEW" badge.
Do not hand-type oklch values or font sizes in page CSS. If a value isn't in the token file, it's either a token that needs adding or a sign that the visual moment is bespoke enough to live page-locally; either way, the decision needs to be deliberate.
- **Strong Gold Hairline** (`oklch(74% 0.09 82 / 0.6)`): Active borders, focus outlines, and structural anchors. Stays gold; this is where the hairline is meant to read as brand.
**The Gold-By-Size-On-Paper Rule (light mode).** On paper, gold usage is gated by size, not banned. **Large display accents stay gold**; the hero's gold accent word reads beautifully at display scale (see the Designing hero: "with Impeccable" in kinpaku gold on paper). But **at body and label sizes gold fails contrast on the bright ground, so it is never used for small accent text on paper.** There, the roles swap to verdigris: links, active nav, and inline command code use `--ks-link-on-paper` (patina-deep, `oklch(49% 0.08 188)`) for contrast, and small labels fall back to muted ink. Verdigris also carries state on paper (active nav, "you are here"), consistent with the Patina Has Meaning rule. Gold otherwise stays on fills and marks (logo, CTA fills, nodes, active rules). Reach for the light-mode tokens (`--ks-link-on-paper`, `--ks-nav-active`, the `light-*` surfaces) when building on paper; the token list below is dark-first, so a naive read pulls you toward gold *body* text that the light theme forbids.
**The Two-Face Rule.** Display sizes use Alumni Sans; thin (100) for the h1, heavier (300) for h2s. Anything sized below `1.2rem` uses Albert Sans. The thin display cut reads too light at small sizes, so it never carries body or UI text.
- Do not use beige, paper, or cream as the page ground **in the default (dark) theme**. (Light mode intentionally uses a warm paper ground; see the Gold-Is-A-Mark-On-Paper rule.)