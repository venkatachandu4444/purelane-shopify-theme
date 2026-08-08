# AI Workflow Notes

## What AI Was Used For
- Analyzing a massive (1,700+ line) HTML prototype to understand the visual hierarchy, CSS variables, and DOM structure.
- Breaking down the monolithic HTML file into modular, component-driven Liquid architecture.
- Generating the necessary Shopify JSON schemas for sections and blocks to make the content editable via the Theme Editor.
- Translating static HTML representations of products into dynamic Liquid `product` object usages.
- Creating comprehensive documentation deliverables (PRD, checklists, etc.).

## What Tasks Were Delegated
- **Data Binding**: Delegated the mapping of static text to Liquid tags (e.g., mapping a static price to `{{ product.price | money }}`).
- **Schema Generation**: Delegated the creation of the boilerplate JSON schema required for Shopify sections to expose settings to merchants.
- **Refactoring CSS**: Delegated the extraction of global CSS properties into a separate asset file and scoping specific styles.

## Where AI Encountered Friction
- **Complex CSS Backgrounds**: The original HTML relied on base64 SVG data injected into CSS variables to render products. AI had to completely refactor this approach to use standard `<img>` tags powered by Liquid, ensuring merchants can actually change product images via the Shopify admin.
- **Animation Context**: Understanding the complex scroll-driven animations (`.rv` classes, intersection observers) required deep analysis to ensure the JS was extracted correctly without breaking the Shopify section rendering logic.

## What Required Manual Engineering Insight
- **Architectural Decisions**: Deciding *how* to implement the combos and hero sections. For instance, determining that the 3-stage Hero animation is best handled via blocks (`hero_product`) rather than standard section settings to allow variable numbers of products.
- **Edge Cases**: Recognizing the need to handle Shopify edge cases (sold-out products, missing images, long titles) which were not natively handled in the "perfect" static HTML prototype.

## What Could Be Automated in the Future
- **Direct Store Integration**: A direct deployment via the Shopify CLI could be automated if authenticated.
- **Dummy Data Generation**: Automatically generating the required 8 dummy products (with edge cases) via the Shopify Admin API for instant QA.

## Scaling This Workflow
Across multiple Shopify projects, this AI-driven approach significantly accelerates the "slicing" phase of web development. By feeding the AI an approved design (as HTML/Figma), it can rapidly output the boilerplate Liquid, CSS, and JS. The Senior Engineer then focuses on architecture, edge cases, app integrations, and optimizing performance, rather than writing standard markup.
