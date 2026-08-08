# Git Commit Plan

A logical sequence for committing this work to a repository.

1. **`chore: Initial Dawn Setup`**
   - Initialize the fresh Shopify Dawn theme.
2. **`feat: Add Global Assets`**
   - Add `purelane-base.css` and `purelane-animations.js`.
   - Update `theme.liquid` to include these assets and the required Google Fonts.
3. **`feat: Add Reusable Snippets`**
   - Create `product-card.liquid` and `review-card.liquid`.
4. **`feat: Hero Section`**
   - Create `hero.liquid` with dynamic product stage and schema settings.
5. **`feat: Shop Grid Section`**
   - Create `shop-grid.liquid` linked to standard collections.
6. **`feat: Best Selling Combos Section`**
   - Create `best-combos.liquid` with horizontal scrolling and specialized combo display.
7. **`feat: Bundles Section`**
   - Create `bundles.liquid` for tiered starter kits.
8. **`feat: Reviews Marquee Section`**
   - Create `reviews.liquid` driven by theme blocks.
9. **`fix: Responsive & Accessibility Adjustments`**
   - Ensure media queries function correctly and ARIA labels are bound to dynamic Liquid outputs.
10. **`docs: Final Cleanup & Documentation`**
    - Add README, PRD, Checklists, and AI workflow notes.
