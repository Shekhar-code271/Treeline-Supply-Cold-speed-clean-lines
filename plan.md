# Treeline Supply implementation plan

## Product direction

Treeline Supply is a premium alpine equipment landing experience for skiers who move quickly through changing terrain. The experience treats scroll like a terrain test: cinematic frame sequences, crisp technical metadata, and restrained product storytelling.

## Design system

- **Design movement:** alpine technical editorial — the visual language of ski film title cards, field notes, and performance outerwear tags.
- **Core principles:** cinematic but quiet; utility over decoration; high-contrast type over photographic depth; precise motion tied to scroll.
- **Color philosophy:** graphite/navy surfaces create cold depth, powder white keeps information legible, pale cyan signals speed and altitude, and lime gear green marks the next action or active equipment state.
- **Layout paradigm:** full-bleed sticky film sections break into an asymmetric lookbook and a low, glassy CTA panel; copy sits in the negative space created by the imagery rather than in centered marketing blocks.
- **Signature elements:** dotted technical surfaces, vertical/horizontal progress rails, and thin translucent equipment cards with lime index labels.
- **Interaction philosophy:** scrolling advances the same way a skier advances through terrain: every frame and product card is a deliberate state, with no gratuitous motion.
- **Animation:** frame sequences update from section-relative scroll progress with requestAnimationFrame throttling; cards use short cubic-bezier opacity/translate transitions; non-image UI stays nearly static.
- **Typography:** Anton carries the wordmark, navigation, headings, and product names; IBM Plex Mono handles technical copy and metadata; Instrument Serif is reserved for optional editorial accents.
- **Brand essence:** technical ski equipment for fast, thoughtful laps — precise, cold, direct. Personality: **focused, rugged, considered**.
- **Brand voice:** short, concrete, confident. Example lines: “Cold speed, clean lines.” and “The line is waiting.”
- **Wordmark:** a tracked uppercase wordmark with a small angled “ridge notch” separator in the header, evoking a contour line without becoming a logo illustration.
- **Signature brand color:** `#d7ff63`, used sparingly as the signal color for active gear and the primary CTA.

## Implementation

- Use a Vite + React + TypeScript client with CSS variables and utility-like semantic classes in `src/styles.css`.
- Keep all requested imagery under `public/assets` copied from the source repository. The runtime generates local `/assets/...` frame URLs and never uses remote image URLs.
- `src/App.tsx` owns the landing-page composition, data arrays, and a reusable `useScrollFrame` hook for preloading and section-relative frame selection.
- `src/styles.css` owns the responsive alpine layout, dotted technical surfaces, hero/gear overlays, typography, cards, and mobile breakpoints.
- `public/manus-routes.json` declares the single `/` page for the managed preview and published static route.
- `plan.md` and `TODO.md` preserve the approved scope and outcome criteria.

## Serving

The Vite dev server listens on `0.0.0.0:3000`. The page is static and does not require managed server or database features. The initial runtime is preview-only until the project is checkpointed/published through Webdev.
