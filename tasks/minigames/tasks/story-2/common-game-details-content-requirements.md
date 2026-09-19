# MiniGames Common Game Details Content Requirements (Story 2)

These requirements apply to Story 2 tasks that open or render the Game Details dialog.

## Static dialog content

- At this stage the Game Details dialog always shows the same static mock game content: **Tukoni: Forest Keepers**.
- The same static content is shown regardless of which Library game card or Home slider card opened the dialog.
- Dynamic per-card dialog content is out of scope for Story 2 and will be implemented later.

## Primary action button

- Because the static mock game is free, implement the `Play Now` button state from the mockup.
- The paid `Buy Now: $<price>` variant is out of scope for Story 2 and will be handled later when dynamic game data is introduced.

## Transient UI state (no persistence)

- Interactive UI state inside the Game Details dialog is temporary at this stage and is **not** persisted.
- After the dialog is closed, the following state is reset to the default open state on the next open:
  - `Add to Favorites` button active/inactive state;
  - comment like button active/inactive states;
  - comment input/textarea value (and its auto-grown height, if applicable).
- Persistence of favorites, likes, and drafted comment text is out of scope for Story 2.
