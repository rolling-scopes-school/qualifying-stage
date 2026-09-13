# Task RSS-QS-1-1-2: Set up folder structure (10 points)

## Description

Set up a clear and organized folder structure within the repository, ensuring a maintainable and scalable codebase. By organizing the codebase properly, it will be easier to navigate and contribute code efficiently.

## Acceptance Criteria

- There is a well-defined folder structure for different components, features, and assets.
- The folder structure allows for easy navigation and identification of the project's different parts.

## Reference for Students

The exact folder names may vary, but a "good structure" for an SPA frontend usually means:

- Separation of concerns: routing, pages, UI components, business logic, and styles are split into dedicated folders.
- Predictable locations: team members can quickly guess where to add or find code.
- Scalability: adding a new page/feature requires adding files in one clear place, not rewriting unrelated folders.
- Reuse-first approach: shared UI and utilities are extracted instead of duplicated across pages.
- Co-location where useful: files that work together (component + style + tests) can be stored together.

### Minimal Example (Page-first)

```text
src/
 app/
  index.ts                # app bootstrap
  router.ts               # SPA routes
 pages/
  home/
   home-page.ts
   home-page.scss
  library/
   library-page.ts
   library-page.scss
 components/
  header/
   header.ts
   header.scss
  footer/
   footer.ts
   footer.scss
  dialogs/
   auth-dialog.ts
   game-details-dialog.ts
 features/
  slider/
   slider.ts
   slider.scss
 services/
  api.ts
  storage.ts
 state/
  store.ts
 utils/
  dom.ts
  format.ts
 styles/
  tokens.scss
  mixins.scss
  globals.scss
 assets/
  icons/
  images/
```

### Alternative Example (Feature-first)

```text
src/
 app/
  index.ts
  router.ts
 shared/
  ui/
   button/
   modal/
   input/
  styles/
   tokens.scss
   globals.scss
  utils/
 features/
  auth/
   ui/
   model/
   auth-service.ts
  game-details/
   ui/
   model/
  slider/
   ui/
   model/
 pages/
  home/
  library/
 assets/
```

Both approaches are acceptable if the structure stays consistent and keeps responsibilities clear.

The examples above are illustrative, not mandatory templates. A student's real project structure may differ.
The key requirement is that the structure exists, is logically organized, and is easy for a reviewer to understand.

If the overall structure is valid but a reviewer believes some files should be placed differently, scoring should be in favor of the student.
In such cases, suggested improvements should be provided as review comments rather than used as a reason to reduce the score.
