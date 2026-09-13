# MiniGames Common Layout Requirements

These requirements apply to all tasks focused on layout implementation and Pixel Perfect checks.

- Use semantically appropriate HTML tags for each section. Using only `<div>` elements is grounds for a score reduction.
- Match the Figma mockup at breakpoints 375, 768, and 1920 (Pixel Perfect verification, deviation up to 10px allowed).
- The layout should not break at any viewport width from 375px and above. Viewport narrower than 375px are not checked.
- Resize fluidly between breakpoints without layout breakage.
- At viewport widths of 1921px and above, the desktop layout remains centered and does not continue to expand; only the side spacing increases.
- Avoid horizontal page scrollbars and unnecessary internal section scrollbars.
- Style interactive elements according to the design style guide, including required states (`default`, `hover`, `active`, `disabled`) where applicable.
- All interactive elements should use an appropriate cursor variant that clearly indicates interactivity.

> **Note:** If a task describes functionality or an element state that is not represented in the Figma design, its implementation is left to the student's discretion. While adhering to the application's general visual style is recommended, styling variations for these elements are not evaluated during code review and will not lead to point deductions.
