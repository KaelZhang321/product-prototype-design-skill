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

## Core Rules

### 1. Default to Element Plus

Unless the user explicitly overrides the design system:

- use Element Plus visual language
- use Element Plus component semantics
- use enterprise admin density, spacing, and hierarchy

Read:

- `./references/element-plus-components-full.md`
- `./references/element-plus-prototype-mapping.md`
- `./references/element-plus-layout-rules.md`

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

### 7. Query page must occupy the full usable width

- do not leave a fake drawer lane on the query page
- filter card and table module should occupy the full usable right-side content width
- compute width from main content width minus page-body horizontal padding

### 8. Business logic belongs in notes

If a page contains core business rules:

- add an in-page business rule block
- keep it secondary to the primary action flow
- place it inside the page content area, typically above filters or above the main list/detail module
- use it to explain validation, permissions, status transitions, side effects, and save/delete impact
- do not place business logic outside the page as an external annotation by default

### 9. Validation is visual, not assumed

Always validate by screenshot:

- whole page
- filter card
- table card
- drawer state
- delete confirmation state

If a page still looks wrong, keep iterating.

## Workflow

1. Read the business request and classify the page type.
2. Choose the page shell and navigation.
3. Load the relevant Element Plus references.
4. Build the query page first.
5. Verify:
   - filter structure
   - table structure
   - full-width layout
   - visible pagination
6. Copy the query page into state pages.
7. Apply overlay states:
   - add/edit: full-page mask + right drawer
   - delete: full-page mask + confirm layer
8. Add business logic notes.
9. Screenshot each state page and verify consistency.

## Required References

- `./references/element-plus-components-full.md`
- `./references/element-plus-prototype-mapping.md`
- `./references/element-plus-layout-rules.md`
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
