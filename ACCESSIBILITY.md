# Accessibility

nixkeeper's pages are for every nixpkgs maintainer, so they should work
with a keyboard, a screen reader, a phone, zoom, and any colour vision.
This covers [nixkeeper.com](https://nixkeeper.com/) (and every copy of it,
like [the demo](https://demo.nixkeeper.com/)) and
[status.nixkeeper.com](https://status.nixkeeper.com/), and is the statement
of every repository in the [nixkeeper organisation](https://github.com/nixkeeper)
without one of its own.

## The goal

[WCAG 2.2](https://www.w3.org/TR/WCAG22/) level AA. It hasn't been audited
against it: this says what's been built for it, and what's known to fall
short.

## What's there

- **Contrast:** text, muted text included, is at least 4.5:1 on its
  background, in the light and dark themes (and Catppuccin's), which follow
  the system's.
- **Not by colour alone:** a package's status dot has a text label
  ("Outdated: a newer release is out", ...) for screen readers and on
  hover, and badges and counts say in words what their colour means.
- **Keyboard:** the controls are links and buttons, with a visible focus
  ring; `/` jumps to the filter.
- **Screen readers:** the page is in English (`lang="en"`), icon buttons
  have labels, toggles say whether they're on (`aria-pressed`,
  `aria-expanded`), decorative icons and the trend lines are hidden from
  them, and the list's new size is announced after filtering or searching.
- **Motion:** with "reduce motion" set in the system, nothing animates.
- **Phones and zoom:** the layout reflows to a phone's width with no
  sideways scrolling, and what a finger taps is at least 24 pixels each
  way.
- **Without the pages:** the same data is in the open (`data` branches, in
  JSON), and [nixkeeper-mcp](https://github.com/nixkeeper/nixkeeper-mcp)
  answers questions about it in text, through an assistant.

## What's known to fall short

- The trend lines (sparklines) are pictures only: their latest numbers are
  in the cards beside them, but not the trend itself.
- The package list is long and dense; with a screen reader, the filter and
  the search are the way through it rather than reading every row.
- It hasn't been tried end to end with every screen reader: VoiceOver and
  NVDA reports are especially welcome.

## Reporting a barrier

[Open an issue](https://github.com/nixkeeper/nixkeeper/issues/new/choose)
in nixkeeper (or the repository it's about) saying what you tried to do,
with what (browser, screen reader, zoom level), and where it stopped you.
Barriers are fixed before features. If you'd rather not report it in
public, write to the maintainer, [@iedame](https://github.com/iedame).
