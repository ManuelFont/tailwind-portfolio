# Manuel Font Personal Portfolio — Design System

## Direction

The site is a compact, playful developer portfolio. It combines an earthy editorial palette with expressive, tactile cards: warm colors, rounded geometry, strong offset shadows, oversized icons, and small moments of movement. The result should feel personal, friendly, and handmade while remaining readable and technically polished.

## Color palette

Use the existing Tailwind theme tokens from `input.css`; do not introduce raw color values in markup.

| Token | Role |
| --- | --- |
| `portrait-olive` | Page background; the dominant muted green field |
| `portrait-cream` | Primary light text, borders, and light card surfaces |
| `portrait-espresso` | Deep contrast for text, dark surfaces, icons, and shadows |
| `portrait-teal` / `primary` | Cool green accent and dark/light card gradient endpoint |
| `portrait-wood` | Warm orange-brown accent and contact card surface |
| `portrait-cedar` | Deeper warm brown used with plum |
| `portrait-leaf` | Bright green status and verification accent |
| `portrait-sky` | Blue accent for infrastructure-oriented cards |
| `portrait-plum` | Purple accent for backend-oriented cards |

Use transparency variants of these tokens for subtle borders and muted text. New colors must be added to the `@theme` block in `input.css` before use.

## Typography

- Use the locally defined `Inter` font through the `font-sans` theme token.
- Use bold or extra-bold display text for the name and project labels.
- Use `font-mono` for the handle/status pill to create a developer-tool detail.
- Keep body copy centered, concise, and relaxed with readable contrast against the olive background.

## Layout

- Keep the content centered in a narrow portfolio column (`max-w-xl` currently).
- Use generous horizontal padding and compact vertical rhythm on mobile.
- The project area is a one-column grid that expands to three columns on small screens and above; feature cards may span two columns.
- The portrait leads the page, followed by the identity pill/name, social links, introduction, project cards, and a quiet footer.

## Components and shapes

- Use fully rounded portrait treatment and pill-shaped identity/status elements.
- Use rounded-3xl project cards with thin translucent cream borders.
- Project cards should use Tailwind gradients from the existing palette, generous padding, and a pronounced espresso offset shadow.
- Place project labels near the lower-left edge and supporting badges near the upper-left edge.
- Use large, low-opacity technology marks or type as decorative card elements.
- Social links are circular, 3rem controls with centered icons.

## Motion and interaction

- Keep motion subtle but playful: cards can scale slightly and increase contrast on hover; decorative marks and labels can translate, rotate, or scale.
- Preserve clear hover/focus affordances and do not rely on motion alone to communicate information.
- Respect reduced-motion preferences when adding substantial new animation.

## Implementation rules

- Implement all visual changes with Tailwind utility classes.
- Do not add custom CSS classes, inline styles, or arbitrary color values.
- When the design evolves, update this document and add any new custom colors to `input.css`'s `@theme` block.
