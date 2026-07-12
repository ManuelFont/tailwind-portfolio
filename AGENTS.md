# Repository Guidelines

## Project Structure & Module Organization

This is a small static portfolio built with Tailwind CSS. The main page lives in `index.html`; update content, links, layout, and styling through Tailwind utility classes there. `input.css` is reserved for Tailwind imports, the local `Inter` font face, and theme tokens only.

Generated and static assets live in `assets/`. `assets/output.css` is the compiled stylesheet consumed by `index.html`, `assets/sprite.svg` stores reusable icons, and font/image files are referenced from the page or CSS. Keep new public assets in this directory and use relative paths such as `./assets/name.ext`.

## Build, Test, and Development Commands

- `npm run build:styles`: compiles `input.css` into `assets/output.css`.
- `npm run watch:styles`: watches Tailwind sources and rebuilds `assets/output.css` during local editing.
- `npx prettier --write index.html input.css`: formats edited files and sorts Tailwind classes through `prettier-plugin-tailwindcss`.

There is no app server required; open `index.html` directly in a browser after building styles.

## Coding Style & Naming Conventions

Use two-space indentation for HTML and CSS. This repository should remain 100% Tailwind for styling: do not add custom CSS selectors, component classes, inline `style` attributes, or handwritten CSS rules for layout or visuals. Express changes with Tailwind utilities in `index.html`. Do not hardcode color values in HTML, including arbitrary color utilities with hex, RGB, HSL, or OKLCH values; add custom colors to the `@theme` block first, then use the generated Tailwind color utilities. Keep token names descriptive and consistent with the existing `portrait-*` color pattern.

Use lowercase, hyphenated file names for assets, for example `me-3.webp` or `project-icon.svg`. Keep accessibility attributes on interactive elements, including `aria-label`, `title`, `target="_blank"`, and `rel="noopener noreferrer"` for external links.

## Testing Guidelines

No automated test framework is currently configured. Before submitting changes, run `npm run build:styles` and manually inspect `index.html` in a browser. Check responsive behavior at mobile and desktop widths, verify links and mail/WhatsApp actions, and confirm icons from `assets/sprite.svg` render correctly.

## Commit & Pull Request Guidelines

Recent commits use short Conventional Commit-style messages, mainly `feat: ...` and `fix: ...`. Continue that pattern, for example `feat: add project card` or `fix: update linkedin url`.

Pull requests should include a brief summary, screenshots for visual changes, and notes about manual browser checks performed. Link related issues when available and call out any generated asset changes, especially updates to `assets/output.css`.

## Agent-Specific Instructions

Agents may read repository files and may create or edit files in this repository when requested. Do not run shell commands, build commands, test commands, package-manager commands, formatter commands, dev servers, or any other commands in this repository. Do not edit `assets/output.css` by hand. Do not add new custom CSS to `input.css`; limit it to Tailwind imports, `@font-face`, and `@theme` tokens. Any new project color must be defined in `@theme` before it is used in markup. Make visual changes in `index.html` with Tailwind utilities; leave generated CSS updates to the project owner.
