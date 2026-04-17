# product-prototype-design

Business-first product prototype design skill for AI coding agents and prototype-generation workflows.

This skill helps agents build standardized enterprise backend prototypes with:

- Element Plus-style admin UI
- query/add/edit/delete state pages
- query-page-as-base modeling
- right-drawer add/edit states
- delete confirmation states
- real table structures
- visible pagination
- business logic notes for prototype review

## Why this skill exists

Many generated prototypes fail in the same way:

- random left navigation
- fake tables made from text
- add/edit pages that rebuild the layout instead of overlaying the query page
- query pages that leave unexplained whitespace
- missing pagination
- no visible business logic annotations

This skill forces those issues into a consistent prototype workflow.

## Installation

After publishing publicly to GitHub, install with:

```bash
npx skills add https://github.com/<owner>/product-prototype-design-skill
```

Or:

```bash
npx skills add <owner>/product-prototype-design-skill
```

## What the skill does

The skill tells the agent to:

1. Use Element Plus as the default design system.
2. Build query pages first.
3. Use the query page as the base for add/edit/delete state pages.
4. Use full-page masks for overlay states.
5. Use right drawers for add/edit by default.
6. Require real table structures and visible pagination.
7. Add business logic notes when needed.
8. Validate each page state visually.

## Recommended use cases

Use this skill when:

- generating backend management prototypes
- standardizing `.pen` admin pages
- converting HTML mocks to consistent prototype rules
- making CRUD state pages
- aligning prototype output with Element Plus conventions
- building repeatable prototype-generation workflows

## Example prompts

### Example 1

```text
Use the product-prototype-design skill to generate a user management prototype with query/add/edit/delete states.
```

### Example 2

```text
Use the product-prototype-design skill to normalize this .pen admin prototype to Element Plus style and fix the table, pagination, and drawer states.
```

### Example 3

```text
Use the product-prototype-design skill to generate a patient management query page, then derive add/edit/delete overlay pages from it.
```

## Repository structure

This is a single-skill repository recognized by the skills CLI because the root contains `SKILL.md`.

```text
product-prototype-design-skill/
├── README.md
├── SKILL.md
└── references/
    ├── element-plus-components-full.md
    ├── element-plus-prototype-mapping.md
    ├── element-plus-layout-rules.md
    ├── crud-state-page-rules.md
    └── pencil-mcp-execution-rules.md
```

## License

MIT
