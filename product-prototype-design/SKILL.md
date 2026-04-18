---
name: product-prototype-design
description: Generate standardized enterprise product prototypes from business requirements, prototype references, `.pen` files, HTML mockups, or design files. Defaults to Element Plus-style admin UI, supports query/add/edit/delete state pages, right-drawer workflows, full-page overlays, true table structures, pagination, business logic notes, and page-state consistency validation. Use when building or normalizing backend management prototypes with Pencil MCP.
---

# Product Prototype Design

## Purpose

Turn business requirements or existing prototype material into consistent, implementation-guiding product prototype pages for enterprise backend systems.

This skill is optimized for:

- Pencil MCP `.pen` generation
- admin CRUD pages
- page-state prototype systems
- Element Plus-style information architecture
- business-logic-aware prototype review

Default desktop canvas:

- `1920 x 1080`

## Core Rules

### 1. Default to Element Plus

Unless the user explicitly overrides the design system:

- use Element Plus visual language
- use Element Plus component semantics
- use enterprise admin density, spacing, and hierarchy
- do not ask again for style reference when the request is a normal admin prototype
- use Element Plus to keep visible component styling consistent, not just to choose structure
- if a reference `.pen` is provided, extract layout structure, information hierarchy, note format, and content organization from it
- do not blindly inherit a reference `.pen` color palette or typography if it conflicts with Element Plus defaults

Read:

- `./references/element-plus-components-full.md`
- `./references/element-plus-prototype-mapping.md`
- `./references/element-plus-layout-rules.md`
- `./references/reference-pen-patterns.md`

### 2. Use page-state modeling for CRUD

For backend CRUD pages, generate these state pages separately:

1. 查询页
2. 新增页
3. 修改页
4. 删除页

### 3. Query page is the base page

The query page is the canonical base.

- build the query page first
- verify it first
- copy it into add/edit/delete state pages

Do not generate four unrelated pages independently.

### 4. Add/Edit are overlays, not rebuilt pages

For 新增页 and 修改页:

- keep the query-page base layout unchanged
- add a full-page mask
- add a right drawer above the mask
- do not change sidebar, header, filter area, or list layout

### 5. Delete is a confirmation state

For 删除页:

- keep the query-page base layout unchanged
- add a full-page mask
- add a centered confirmation layer or warning panel

### 6. Tables must be real

CRUD list pages must use real table structure.

At minimum:

- toolbar row
- header row
- body rows
- cell frames
- visible pagination

Never use a single text line to fake a table.

Visible pagination is mandatory for query/list pages.

### 7. Query page must occupy the full usable width

- do not leave a fake drawer lane on the query page
- filter card and table module should occupy the full usable right-side content width
- compute width from main content width minus page-body horizontal padding
- on `1920x1080`, keep content visually controlled so it does not feel over-stretched
- keep the shell stable: top nav, left navigation, page title, then the main work area
- if the reference `.pen` uses denser list-page composition, absorb its structural hierarchy without copying its non-Element visual tokens directly

### 8. Business logic belongs in notes

If a page contains core business rules:

- add a page-external business note
- keep it secondary to the primary action flow
- place it outside the page canvas, typically to the right side
- use it to explain validation, permissions, status transitions, side effects, and save/delete impact
- do not move it into the page content area unless the user explicitly asks for that
- use Pencil `note` as the default annotation component
- keep the note outside the page frame, not inside the page layout
- for a single page, place the note in the right-side annotation lane
- when no better reference exists, follow the reference `.pen` note pattern:
  page title line + 核心逻辑 + 主操作 + 关键校验
- prefer compact note blocks around `250 x 240` unless the content genuinely needs more space
- if existing note content is trivial or placeholder text, ignore it instead of treating it as a rule source

### 9. Validation is visual, not assumed

Always validate by screenshot:

- whole page
- filter card
- table card
- drawer state
- delete confirmation state

If a page still looks wrong, keep iterating.

### 10. Defaults that should not need repeating in prompts

Unless the user overrides them, assume:

- Element Plus style
- reference `.pen` files contribute structure and copywriting patterns, not mandatory visual tokens
- query/list pages use real tables
- query/list pages have visible pagination
- query pages occupy the full usable width
- query/list modules keep controlled field widths and balanced spacing
- generation proceeds iteratively by section
- output should target the current active editor `.pen` file
- business logic is explained with a page-external note

## Workflow

1. Read the business request and classify the page type.
2. Choose the page shell and navigation.
3. If a reference `.pen` exists, extract reusable page-shell, note, table, drawer-content, and copy patterns from it.
4. Load the relevant Element Plus references.
5. Reconcile the two layers:
   - structure and hierarchy from the reference `.pen`
   - visual language and component semantics from Element Plus
6. Build the query page first.
7. Verify:
   - filter structure
   - table structure
   - full-width layout
   - visible pagination
8. Copy the query page into state pages.
9. Apply overlay states:
   - add/edit: full-page mask + right drawer
   - delete: full-page mask + confirm layer
10. Add business logic notes.
11. Screenshot each state page and verify consistency.

## Required References

- `./references/element-plus-components-full.md`
- `./references/element-plus-prototype-mapping.md`
- `./references/element-plus-layout-rules.md`
- `./references/reference-pen-patterns.md`
- `./references/crud-state-page-rules.md`
- `./references/pencil-mcp-execution-rules.md`

## Quality Bar

The result is acceptable only if:

- query page is complete and independently reviewable
- add/edit states preserve the query-page base layout
- overlay mask covers the full page
- drawer is topmost
- table is structurally real
- pagination is visibly present
- no unnecessary right-side whitespace remains on the query page
- business logic notes explain key behavior
- reference `.pen` structure cues are absorbed where useful, without overriding the Element Plus visual baseline
