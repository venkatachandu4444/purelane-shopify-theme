# Purelane Shopify Theme Implementation

## Project Overview
This project converts a static, non-production-ready HTML prototype of the Purelane homepage into a set of production-quality, dynamic, and merchant-editable Shopify sections built for the Dawn theme.

## Folder Structure
- `sections/`: Contains the dynamic Liquid sections (`hero.liquid`, `shop-grid.liquid`, `best-combos.liquid`, `bundles.liquid`, `reviews.liquid`).
- `snippets/`: Reusable Liquid components (`product-card.liquid`, `review-card.liquid`).
- `assets/`: Global CSS and JavaScript files (`purelane-base.css`, `purelane-animations.js`).
- `docs/`: Project documentation including the PRD, AI Workflow Notes, and Checklists.

## Setup Instructions
Please refer to `docs/Setup-Instructions.md` for a detailed guide on how to integrate this code into a fresh Shopify Dawn theme.

## Features
- **Fully Merchant Editable**: All text, images, and collections can be modified via the Shopify Theme Editor without touching code.
- **Dynamic Product Data**: Sections pull real product prices, titles, variants, and availability states directly from Shopify.
- **Componentized**: Common UI elements (like product cards) are extracted into reusable snippets to adhere to DRY principles.

## Performance
- All CSS and JS have been modularized and separated from the Liquid structure.
- Redundant styles and inline definitions have been minimized.
- Heavy animations are gated behind `prefers-reduced-motion` media queries for accessibility and performance.

## Accessibility
- Proper heading hierarchy is enforced.
- Semantic HTML tags are used (`<article>`, `<section>`, `<nav>`).
- ARIA labels and `aria-hidden` attributes are appropriately applied to interactive elements and decorative animations.

## Known Limitations
- The provided code assumes standard Shopify object schemas (e.g., `product.price`, `product.featured_image`). Custom metafields may need to be mapped if non-standard data (like a short description) is required.
