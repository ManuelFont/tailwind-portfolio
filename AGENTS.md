# Project instructions

These instructions apply to the entire repository.

## Styling requirements

- Use 100% Tailwind CSS utility classes for all styling. Do not add custom CSS selectors, component classes, style attributes, `<style>` blocks, CSS modules, Sass, or other custom styling systems.
- Keep styling in the markup through Tailwind classes. If an existing custom selector must be changed, migrate its usage to Tailwind utilities instead of extending the selector.
- All custom colors must be declared in the `@theme` block in `input.css` before they are used. Do not use arbitrary color values such as `bg-[#...]`, `text-[#...]`, `border-[rgb(...)]`, or inline color declarations.
- Reuse the existing theme tokens whenever possible. If a new color is genuinely needed, add a clearly named `--color-*` token to `input.css` and use the generated Tailwind utility.
- Use the existing Tailwind build scripts to verify styling changes. Do not edit generated `assets/output.css` directly.

## Design consistency

- Read `DESIGN.md` before making visual or UI changes. It is the source of truth for the website's visual style, color palette, typography, layout, and interaction conventions.
- Preserve the existing personality and palette. Do not introduce unrelated colors, gradients, typography, spacing systems, or visual patterns without updating `DESIGN.md` first.
- Prefer existing patterns and theme tokens over one-off values. Keep the responsive, compact portfolio layout and playful card interactions intact.

## Verification

- After styling changes, run `npm run build:styles` and inspect the resulting page/classes for obvious regressions.
- Keep accessibility in mind: preserve meaningful link labels, visible focus states, readable contrast, and responsive behavior.
