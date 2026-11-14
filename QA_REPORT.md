# v58 acceptance review — evidence and limitations

## Verified static checks
- Resource inventory: 44 entries.
- Audience/topic matrix: 45 combinations, 44 with at least one tagged resource.
- One intentional zero-result combination: Scholar × Adult SEL.
- JavaScript syntax: 13/13 scripts passed node --check.
- ZIP integrity: checked on final package.
- Empty-result guidance now offers relevant scholar-focused topics or a way to broaden audience filters.

## Blocked checks
Chromium/Playwright navigation to local HTTP returned ERR_BLOCKED_BY_ADMINISTRATOR in this environment. Therefore no new live interaction, visual layout, mobile, keyboard, persistence, or external permission test is counted as passed.

## Acceptance gates still open
- Browser interaction matrix and screenshots at desktop/mobile.
- Save/reopen/remove/reload; MTSS plan save/reload.
- External document links and GRPS Drive permissions.
- Live GitHub Pages deployment and smoke test.

## November 2026 browser acceptance (headless Chrome, 1366px and 390px)
Closed from the open gates above:
- Browser interaction matrix: every visible control on the home page clicked at both widths; all nine menu items open their section; no JavaScript errors.
- Resource Finder: all nine needs return results (Build Relationships 13, Build Belonging 13, Support Attendance 10, Teach SEL 8, Adult SEL 7, Support a Family 6, Manage Emotions 5, Support Behavior 5, Resolve Conflict 4); every audience filter narrows correctly; Scholar × Adult SEL shows the intended guidance.
- Save → reload → saved list → remove: passes at both widths.
- MTSS plan notes save → reload → notes restored; plan summary renders.

Fixed in this pass:
- The sticky header (z-index 1000) covered the dialog (z-index 90), so clicking × on desktop opened "Adult SEL" instead of closing the dialog.
- No navigation at phone width (menu hidden under 900px with no toggle). Added a Menu button.
- Browser Back left the hub after opening a section; Back now closes the section.
- Section links (#mtss, #finder, #families, #educators, #scholars, #schoolwide, #adult) now open that section when shared or pasted.
- Floating HOME button hidden until the visitor scrolls; favicon added.

Still open:
- External document links and GRPS Drive permissions (outside sites are blocked from the test environment).
- Live GitHub Pages smoke test after merge.
