# product-prototype-design

Business-first product prototype design skill for AI coding agents and prototype-generation workflows.

This skill helps agents build standardized enterprise backend prototypes with:

- Element Plus-style admin UI
- traditional admin-console shell by default
- structure learned from reference `.pen` files when available
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
npx skills add https://github.com/<owner>/product-prototype-design-skill --skill product-prototype-design
```

Or:

```bash
npx skills add <owner>/product-prototype-design-skill --skill product-prototype-design
```

## What the skill does

The skill tells the agent to:

1. Use Element Plus as the default design system.
2. Use a traditional backend-management shell as the default page appearance.
3. Extract page-shell and note patterns from a reference `.pen` if one is provided.
4. Build query pages first.
5. Use the query page as the base for add/edit/delete state pages.
6. Use full-page masks for overlay states.
7. Use right drawers for add/edit by default.
8. Require real table structures and visible pagination.
9. Add page-external business logic notes when needed.
10. Validate each page state visually against a traditional-admin checklist.

## Recommended use cases

Use this skill when:

- generating backend management prototypes
- standardizing `.pen` admin pages
- converting HTML mocks to consistent prototype rules
- making CRUD state pages
- aligning prototype output with Element Plus conventions
- building repeatable prototype-generation workflows

## Example prompts

### Minimal prompt

```text
Use the product-prototype-design skill to generate a [业务页面名称] backend prototype.
```

Example:

```text
Use the product-prototype-design skill to generate a 通知公告 management backend prototype.
```

### CRUD minimal prompt

```text
Use the product-prototype-design skill to generate a [业务对象] management prototype with query/add/edit/delete states.
```

Example:

```text
Use the product-prototype-design skill to generate a 用户 management prototype with query/add/edit/delete states.
```

### Strong-constraint prompt

Use this when you want to force the most predictable result:

```text
Use the product-prototype-design skill to generate a [业务对象] backend CRUD prototype.
Default to a traditional admin-console shell.
Use Element Plus semantics.
Generate 查询页、新增页、修改页、删除页.
Use the query page as the base.
Add/edit must use full-page mask + right drawer.
Delete must use full-page mask + centered confirmation.
Use a real table and visible pagination.
Place business logic in page-external notes.
Canvas size 1920x1080.
```

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

## Recommended real-world usage

For most cases, you only need:

```text
Use the product-prototype-design skill to generate a [业务页面名称] backend prototype.
```

If the page is CRUD-heavy, use:

```text
Use the product-prototype-design skill to generate a [业务对象] management prototype with query/add/edit/delete states.
```

Do not keep repeating these unless you want to override the defaults:

- traditional backend-management shell
- Element Plus semantics
- real table
- visible pagination
- query page as base page
- add/edit with right drawer
- business note outside the page
- canvas `1920 x 1080`

## Repository structure

This repository is organized in installable skill-directory form.

```text
product-prototype-design-skill/
├── README.md
├── LICENSE
└── product-prototype-design/
    ├── SKILL.md
    └── references/
        ├── element-plus-components-full.md
        ├── element-plus-prototype-mapping.md
        ├── element-plus-layout-rules.md
        ├── reference-pen-patterns.md
        ├── traditional-admin-visual-tokens.md
        ├── traditional-admin-shell-rules.md
        ├── traditional-admin-checklist.md
        ├── crud-state-page-rules.md
        └── pencil-mcp-execution-rules.md
```

## Skill name

The installable skill directory name is:

```text
product-prototype-design
```

## License

MIT
