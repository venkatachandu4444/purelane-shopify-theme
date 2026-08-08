# HTML Review Notes

## Overview
This document outlines the analysis of the provided `purelane-homepage.html` prototype and details the necessary architectural changes for a production Shopify implementation.

## Issues Identified & Solutions

### 1. Hardcoded Content
- **Problem**: The prototype hardcodes product names, prices, reviews, and UI copy.
- **Solution**: Replaced hardcoded text with Liquid objects (`{{ product.title }}`, `{{ product.price | money }}`) and section settings (`{{ section.settings.heading }}`).

### 2. Base64 Image Assets
- **Problem**: The prototype relies heavily on inline Base64 SVG backgrounds defined in `:root` CSS (e.g., `--p-combo2`). This is inefficient for a CMS, blows up stylesheet size, and prevents merchants from updating images.
- **Solution**: Shifted from CSS background images to standard `<img>` tags populated dynamically via Shopify's image filters (`{{ product.featured_image | image_url: width: 600 | image_tag }}`).

### 3. Non-Modular CSS/JS
- **Problem**: All styles and scripts were placed in a single file inside `<style>` and `<script>` blocks.
- **Solution**: Separated CSS into `assets/purelane-base.css` and scoped section-specific styles within the Liquid sections. Moved JS to `assets/purelane-animations.js` and ensured it relies on robust DOM querying.

### 4. Accessibility Gaps
- **Problem**: While some ARIA attributes were present, interactive elements often lacked context for screen readers, and image `alt` texts were hardcoded descriptions rather than dynamic.
- **Solution**: Bound dynamic `alt` text to all Shopify images. Ensured buttons and links have proper focus states.

### 5. Code Duplication
- **Problem**: The product card HTML and review card HTML were duplicated repeatedly.
- **Solution**: Abstracted these into Liquid snippets (`product-card.liquid`, `review-card.liquid`) to adhere to DRY principles and simplify maintenance.
