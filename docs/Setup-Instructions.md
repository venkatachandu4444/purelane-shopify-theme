# Setup Instructions

Follow these steps to integrate the Purelane sections into your Shopify store using the Dawn theme.

## 1. Theme Preparation
1. Create a new development store or use an existing one.
2. Install a fresh copy of the **Dawn Theme**.
3. Create a duplicate of the theme to act as your working branch.

## 2. Global Assets
1. Open the code editor for the theme.
2. Under the `assets/` directory, add two new files:
   - `purelane-base.css`
   - `purelane-animations.js`
3. Paste the provided code into these files.
4. Open `layout/theme.liquid`.
5. Before `</head>`, link the new CSS file:
   ```html
   {{ 'purelane-base.css' | asset_url | stylesheet_tag }}
   ```
6. Before `</body>`, link the new JS file:
   ```html
   <script src="{{ 'purelane-animations.js' | asset_url }}" defer="defer"></script>
   ```
7. Ensure the Outfit and Inter fonts are loaded in `theme.liquid`:
   ```html
   <link rel="preconnect" href="https://fonts.googleapis.com">
   <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
   <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@500;600;700;800&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
   ```

## 3. Snippets
1. Under the `snippets/` directory, create two new files:
   - `product-card.liquid`
   - `review-card.liquid`
2. Paste the provided Liquid code into these snippets.

## 4. Sections
1. Under the `sections/` directory, create the following new files:
   - `hero.liquid`
   - `shop-grid.liquid`
   - `best-combos.liquid`
   - `bundles.liquid`
   - `reviews.liquid`
2. Paste the provided Liquid code into their respective files.

## 5. Store Data Setup
1. Create at least 8 products. Ensure one is sold out, one lacks an image, and one has a very long title to test edge cases.
2. Create collections (e.g., "Bestsellers", "Combos") and assign the products.
3. Open the Shopify Theme Editor (Customize).
4. Add the new Purelane sections to the Homepage.
5. Configure the sections by selecting the collections and products you created.
6. Populate the Reviews section using blocks.
