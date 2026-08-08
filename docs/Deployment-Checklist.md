# Deployment Checklist

Follow these steps before pushing the Purelane theme sections to a live production environment.

## Pre-Deployment
- [ ] **Code Review**: Ensure all Liquid schemas are valid JSON.
- [ ] **Asset Minification**: Verify that `purelane-base.css` and `purelane-animations.js` do not contain unnecessary bloat. (Shopify will minify automatically, but ensure no large base64 strings remain).
- [ ] **Cross-Browser Testing**: Test on Chrome, Safari, and Firefox. Ensure the CSS `backdrop-filter` rules apply gracefully or have fallbacks.

## Deployment Steps
- [ ] **Theme Push**: Use Shopify CLI (`shopify theme push`) to push the local code to the target theme.
- [ ] **Schema Population**: Navigate to the Shopify Admin -> Online Store -> Customize.
- [ ] **Configure Hero**: Add the Hero section and populate it with 1-3 Product blocks.
- [ ] **Configure Shop Grid**: Create a "Bestsellers" collection in Shopify Admin. Assign it to the Shop Grid section.
- [ ] **Configure Combos**: Create a "Combos" collection and assign it to the Best Selling Combos section.
- [ ] **Configure Bundles**: Set up the Starter, Most Popular, and Whole Home blocks in the Bundles section.
- [ ] **Configure Reviews**: Add review text, reviewer names, and ratings to the Reviews section blocks.

## Post-Deployment Verification
- [ ] Check the live site on a mobile device to verify the horizontal scrolling rails.
- [ ] Verify that the Hero animation functions as expected when scrolling.
- [ ] Verify that clicking an "Add to Cart" or product link directs the user appropriately.
