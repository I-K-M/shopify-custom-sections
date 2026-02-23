# shopify-custom-sections

A grab-bag of **Shopify (Online Store 2.0) Liquid sections/snippets** I use for building stores: FAQ, slideshow, footer, grids, contact form, product blocks, etc.

## Contents

This repo currently includes (non-exhaustive list from the root):

## Sections

- `custom-2-rows-with-bg.liquid`
- `custom-article-template.liquid`
- `custom-contact-form.liquid`
- `custom-faq-section.liquid`
- `custom-footer.liquid`
- `custom-grid-with-bg.liquid`
- `custom-grid-with-heading.liquid`
- `custom-highlights-section.liquid`
- `custom-image-text-box.liquid`
- `custom-map-split.liquid`
- `custom-product-description.liquid`
- `custom-product-details.liquid`
- `custom-rich-text.liquid`
- `custom-slideshow.liquid`
- `custom-table.liquid`
- `custom-testimonials.liquid`
- `custom-text-and-image.liquid`
- `custom-text-columns.liquid`

## Snippets

- `custom-mega-menu.liquid`

  
## Quick start

1. Open your Shopify theme code:
   - **Online Store → Themes → (⋯) → Edit code**
2. Copy the Liquid file you want into the right folder:
   - Most files here are intended as **sections** → `sections/`
   - `custom-mega-menu.liquid` is intended as a **snippet** → `snippets/`
3. Save, then in the Theme Editor:
   - **Customize → Add section** and pick the new section (it appears from its `schema.presets` when present).

## Usage notes (important)

### Theme dependencies
Several files call common theme snippets/components. Example dependencies seen in this repo:
- FAQ section renders `collapsible-icons-alt`
- Mega menu snippet renders `image-element` and expects `link`, `section`, and optional alignment params 
- Slideshow renders `image-element`
- Article template uses `breadcrumbs`, `social-sharing`, `comment`, and `pagination` 
- Footer renders `footer-*` snippets and `multi-selectors` 

If your theme doesn’t ship these snippets (or uses different classnames/structure), you’ll need to adapt the calls/markup.

### Metafields / content assumptions
Some templates are written to optionally read metafields (example: article hero/background/author info). 

## Suggested repo structure (optional but recommended)

If you want this repo to be “drop-in”:
- Move section files into `/sections`
- Move snippet files into `/snippets` (at least `custom-mega-menu.liquid`)
- Add a `/README` section per file with:
  - required snippets
  - required settings/metafields
  - screenshots/gifs

## Contributing

- PRs welcome: improvements, bugfixes, better defaults, or making sections more theme-agnostic.
- Keep sections OS 2.0 compatible (`{% schema %}` + presets where applicable).
