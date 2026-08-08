# Product Requirements Document (PRD)

## Project Overview
This project involves translating a static HTML/CSS/JS prototype of the Purelane homepage into dynamic, merchant-editable Shopify sections compatible with the Shopify Dawn Theme.

## Objectives
- Achieve a 1:1 pixel-perfect visual match with the provided `purelane-homepage.html`.
- Ensure all content (text, images, collections) is fully editable via the Shopify Theme Editor.
- Populate data dynamically using Shopify objects (`product`, `collection`, etc.).
- Maintain or exceed existing performance and accessibility standards.

## User Stories
1. **As a Merchant**, I want to change the hero heading, description, and button text without touching code.
2. **As a Merchant**, I want to select a collection for the "Best Selling Combos" section, and have the section dynamically render the products in that collection.
3. **As a Merchant**, I want to manage customer reviews through Theme Editor blocks (add, edit, reorder).
4. **As a Customer**, I want to see accurate prices, compare-at prices, and stock availability on all product cards.
5. **As a Customer**, I want the site to load quickly and be fully usable on my mobile device.

## Section Breakdown
1. **Hero Section**: Includes a dynamic 3-stage product animation. Must support custom headings, backgrounds, and block-based product selection.
2. **Shop Grid**: A standard grid displaying a selected collection, utilizing reusable product cards.
3. **Best Selling Combos**: A horizontal scrolling rail of bundled products, displaying savings and included items.
4. **Bundles**: A tiered layout for starter kits and bundles, highlighting savings and features.
5. **Reviews Rail**: An auto-scrolling marquee of reviews, managed via blocks.

## Component Breakdown
- **Product Card (`product-card.liquid`)**: Standardized card displaying product image, title, review rating, price, compare-at price, and savings badge. Handles sold-out states.
- **Combo Card (`combo-card.liquid`)**: Specialized card for the combo rail showing a stack of included products.
- **Review Card (`review-card.liquid`)**: Standardized card for user reviews.

## Acceptance Criteria
- All 5 sections are present in the Theme Editor.
- Changes made in the Theme Editor reflect immediately in the preview.
- All product information is driven by Shopify data.
- The layout matches the HTML prototype across all specified breakpoints (375px to 1920px).

## Responsive Behaviour
- The UI must adapt seamlessly across breakpoints: 375px, 390px, 414px, 768px, 1024px, 1280px, 1440px, 1920px.
- Specialized mobile layouts (e.g., horizontally scrolling product rails) must be preserved.

## CMS Requirements
- Use Shopify Section Schemas to expose settings.
- Avoid hardcoded values in Liquid templates.

## Performance Goals
- Use `loading="lazy"` on all images below the fold.
- Defer non-critical JavaScript.
- Avoid layout shifts (CLS) by setting aspect ratios on images where possible.

## Accessibility Goals
- Semantic HTML tags.
- Proper `alt` text bindings (e.g., `product.featured_image.alt`).
- Focus states for keyboard navigation.
- Respect `prefers-reduced-motion` for animations.
