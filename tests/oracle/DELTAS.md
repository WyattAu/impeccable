text colour itself is dropped, because a `1.0:1; text #ffffff on #ffffff` is
  `1.1:1 (need 4.5:1); text #f2f2f2 on #ffffff`, the `.faint-text` paragraph
  `2.0:1 (need 4.5:1); text #dfaaa1 on #ffffff`, the `.pass-alpha-color` case
  `2.2:1 (need 4.5:1); text #b0b0b0 on #ffffff`, case 6, the collapsed
  - `1.2:1 (need 4.5:1); text #cbd5e0 on #e2e8f0 (gradient on nav.pale-header)`:
  - `1.6:1 (need 3:1); text #fdfdfd on #fbbf24 (gradient on div.feature-tile)`
    and `1.5:1 (need 3:1); text #fdfdfd on #a3e635 (gradient on div.feature-tile)`:
  - `1.3:1 (need 4.5:1); text #e0e0e1 on #ffffff (gradient on div.edge-banner)`:
  - `1.3:1 (need 4.5:1); text #dfdfe0 on #ffffff (gradient on div.edge-banner)`:
pass at the same ratio, `2.6:1 (need 4.5:1); text #51545b on #0a0b10`, and the
  per should-flag case. They are `4.49:1 (need 4.5:1); text #777777 on #070707`,
  `2.99:1 (need 3:1); text #595959 on #000000`,
  `4.49:1 (need 4.5:1); text #7b7b7b on #101010` (a link) and
  `:hover state 4.49:1 (need 4.5:1); text #747474 on #000000`. Base prints
  - `1.3:1 (need 4.5:1); text #4aab5d on #1d9634`, words at a fifth of white on
  - `2.1:1 (need 4.5:1); text #b3b3b3 on #ffffff`, the code line in words.
  - `2.4:1 (need 4.5:1); text #6d83cb on #1e40af`, the visible launcher.
    (yna.co.kr), `/` in swiper fraction pagination, `◯` (bt.cn 80918, 81097), `-`
  (`1.6:1 (need 4.5:1); text #cecfd1 on #ffffff`, the dark word, and
  `1.1:1 (need 4.5:1); text #f3f3f3 on #ffffff`, the sliding row) and scores
  the faint word at its blended colour (`1.1:1 (need 4.5:1); text #efeff0 on
  `1.0:1 (need 4.5:1); text #ffffff on #ffffff` initials, should-pass copy the
  2 to 1, `1.0:1 (need 3:1); text #ffffff on #ffffff`, the pass hero caption.
  `1.0:1 (need 4.5:1); text #0f172a on #0f172a (gradient on a.underline-link)`,
- `detect-fixture-json-modern-color-borders-html`, `detect-fixture-text-modern-color-borders-html`: `4.49:1; text #64748b on #fef7f2` is advisory (14 to 13 counted).
- `detect-fixture-json-named-color-borders-html`, `detect-fixture-text-named-color-borders-html`: `4.4:1; text #64748b on #f6f6f6` is advisory (8 to 7 counted).
- `detect-fixture-json-overlay-positioning-html`, `detect-fixture-text-overlay-positioning-html`: `4.2:1; text #ffffff on #8b5cf6 (gradient on button.ai-btn)` is advisory (32 to 31 counted).
    printed against the surface it reads best on: `3.2:1 (need 4.5:1); text
  corner (visiby.net 3806 and 3809 printed `1.2:1; text #8b8d87 on #c96442
  (layer on article.pc)` and now print `3.0:1; text #8b8d87 on #faefe6`).
  `low-contrast` findings at full severity (`2.9:1 (need 4.5:1); text
Row-stripe follow-ups (`detect-row-stripes-followup`): `side-tab-status-rows.html` gains six should-pass rows (an `!important` style reset that outlasts a later side border, a plain cell edged on both sides, a plain branch beside a status branch whose row is not on the page, a cell wrapper in a selected row, a row selected through `data-state="selected"`) and three should-flag rows (a row card rounded by another rule, a rounded error cell, a stale row inside an `.active` tab pane). The per-fixture goldens (`detect-fixture-json-side-tab-status-rows-html`, `detect-fixture-text-side-tab-status-rows-html`) were re-recorded from the binary and reviewed by hand: 5 to 8 `side-tab` findings, the three new should-flag rows, with the row card reported once by the card scan (`.row-card.is-overdue; inset box-shadow 4px stripe (left)`) and not again as a row stripe; none of the should-pass rows reports. The directory sweeps were left as `detect-status-row-stripes` recorded them: re-recording them now would also take in the `low-contrast-resting-states.html` findings main brought in, which are not this change's to accept. They gain these three findings at their next re-record.