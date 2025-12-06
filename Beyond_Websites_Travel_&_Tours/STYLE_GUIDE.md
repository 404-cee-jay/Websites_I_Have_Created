# Beyond Travels — Style Guide

This lightweight style guide documents the main design tokens, layout rules and component usages for the project. It is intentionally short and practical so you can use it while developing or updating the site.

## Design tokens

- Primary color: `--primary-color: #2887ff` (used for primary actions, highlights)
- Primary color (dark): `--primary-color-dark: #2476da` (hover states)
- Text dark: `--text-dark: #0a0a0a`
- Text light: `--text-light: #737373`
- Extra light (surface): `--extra-light: #f3f4f6`
- White: `--white: #ffffff`

## Typography

- Font-family: `DM Sans` (google font imported in `style.css`).
- Heading sizes: large hero `h1` uses ~4.5rem on desktop; section headers use ~2.5rem.
- Body text: readable sizes around 1rem with 1.4 line-height (kept in CSS defaults).

## Spacing & Layout

- The main content container: `--max-width: 1200px` with `.section__container` providing 5rem vertical padding.
- Grid patterns are used across the site (`display: grid`) and adapt with media queries at 540px, 768px and 1200px.

## Components

- Navigation (`nav`, `.nav__links`, `.nav__menu__btn`)

  - Desktop: normal horizontal menu. Mobile: transformed into a full-width column menu using `.nav__links.open`.

- Header / Hero (`header`, `.header__image`, `.header__content`)

  - Background image uses `header::before` and the hero image sits in `.header__image`.

- Destination cards (`.destination__card`, `.destination__rating`)

  - Card images have rounded corners and shadow. Rating chips use `--primary-color`.

- Journey cards (`.journey__card`) — interactive hover that slides content up using `top` transition.

- Showcase (`.showcase__container`) — image + content composition; call-to-action uses textured background.

- Testimonials / Clients (swiper) — Use the `.swiper` container and `.client__card` for slides. Avatar images are circular (`.client__details img`).

## Accessibility notes

- Buttons use visible focus via native outlines (no override). Keep color contrast for primary actions.
- Ensure `alt` attributes are meaningful for images (already present for assets).

## How to extend

- Add variables to `:root` for new colors or spacing.
- Create component-specific classes and add a short comment above them in `style.css` for clarity.

---

This guide is intentionally brief. For larger projects, consider adding token maps, a component inventory, and usage examples.
