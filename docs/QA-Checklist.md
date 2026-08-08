# QA Checklist

Use this checklist to verify the implementation of the Purelane sections.

## Visual Fidelity
- [ ] Hero section matches the HTML prototype on desktop and mobile.
- [ ] Product Grid cards match the styling, including shadows and rounded corners.
- [ ] Combo cards display the "stack" of included products correctly.
- [ ] Bundle tiers match the design, with the "Most Popular" tier highlighted.
- [ ] Reviews marquee scrolls smoothly and matches styling.

## Responsive Design
- [ ] Layouts stack correctly at `768px` and below.
- [ ] Horizontal scrolling rails (Combos, Full Range) function correctly on touch devices (`375px`, `390px`, `414px`).
- [ ] Typography scales appropriately across breakpoints up to `1920px`.

## Shopify Data Integration
- [ ] Product Titles render correctly (including handling very long titles).
- [ ] Prices render correctly (`{{ product.price | money }}`).
- [ ] Compare-at prices render correctly (`{{ product.compare_at_price | money }}`) and savings badges calculate appropriately.
- [ ] "Sold Out" badge appears when `product.available` is false.
- [ ] Missing images fallback gracefully to a placeholder or remain blank without breaking the layout.
- [ ] Add to Cart buttons function correctly or link to the Product Display Page.

## Theme Editor Integration
- [ ] All 5 new sections can be added, moved, and deleted in the Theme Editor.
- [ ] Changes to section settings (headings, descriptions) reflect immediately.
- [ ] Adding/removing blocks in the Hero and Reviews sections works without breaking layout.
- [ ] Theme Editor inspector mode highlights the correct elements.

## Accessibility
- [ ] All interactive elements (buttons, links) are keyboard accessible (Tab navigation).
- [ ] Focus states are visible (`:focus-visible`).
- [ ] Product images have dynamic `alt` text.
- [ ] Animations pause or are disabled when `prefers-reduced-motion` is active.
- [ ] Contrast ratios meet WCAG standards on light backgrounds.

## Performance
- [ ] Non-hero images use `loading="lazy"`.
- [ ] No layout shifts occur during initial page load.
- [ ] The `purelane-animations.js` script handles `requestAnimationFrame` efficiently for scroll events.
