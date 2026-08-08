# Folder Structure

This project follows a standard Shopify Theme structure, mimicking how the files would integrate into an existing Dawn theme.

```text
purelane-shopify-theme/
├── assets/
│   ├── purelane-base.css        # Global CSS variables, typography, and utility classes
│   └── purelane-animations.js   # Global JavaScript for scroll reveals and dynamic UI
├── sections/
│   ├── hero.liquid              # Hero section with dynamic product stage
│   ├── shop-grid.liquid         # Standard product grid section
│   ├── best-combos.liquid       # Horizontal scrolling rail for combos
│   ├── bundles.liquid           # Tiered layout for bundles
│   └── reviews.liquid           # Auto-scrolling reviews marquee
├── snippets/
│   ├── product-card.liquid      # Reusable snippet for standard product cards
│   └── review-card.liquid       # Reusable snippet for review cards
├── docs/
│   ├── PRD.md                   # Product Requirements Document
│   ├── HTML-Review-Notes.md     # Critique of the original HTML
│   ├── Git-Commit-Plan.md       # Suggested commit history
│   ├── Setup-Instructions.md    # Guide for installing the code
│   ├── AI-Workflow-Notes.md     # Notes on AI generation
│   ├── QA-Checklist.md          # Quality Assurance checklist
│   └── Deployment-Checklist.md  # Final deployment checks
└── README.md                    # Project overview
```
