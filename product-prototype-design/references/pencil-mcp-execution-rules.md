# Pencil MCP Execution Rules

Use this file for stable generation behavior in Pencil MCP.

## Reliability rules

- use very small `batch_design` blocks, usually `<= 3-8` operations
- split strictly by page section
- never try to build an entire CRUD page in one block
- use this execution order:
  1. shell
  2. filter
  3. table header
  4. one row pattern
  5. more rows
  6. pagination
  7. overlay
  8. note
- validate with screenshots after each meaningful stage
- prefer node creation first and style refinement second
- when a block fails, do not retry the same large block; shrink the block and continue
- if a reference `.pen` is available, inspect it before building so page-shell, note, and section patterns are grounded in evidence

This matches the official Pencil AI-integration guidance:

- be specific
- iterate
- inspect every stage
- refine incrementally

## Overlay rules

- copied CRUD overlay pages should switch to absolute composition mode when needed
- numerically size copied sidebar/main containers if `fill_container` conflicts with absolute overlays
- full-page mask must cover the entire copied page
- drawer must be moved after the mask so it remains topmost
- reference `.pen` drawer pages may guide internal drawer sectioning, but must not replace the overlay-state requirement

## Table rules

- query-page tables must be structural
- one-line text tables are forbidden
- each row and cell should be its own frame when possible
- visible pagination is mandatory
- if a reference `.pen` provides a credible table pattern, reuse its column grouping logic while translating visuals back to Element Plus semantics

## Annotation rules

- use a page-external `note` for core business logic by default
- keep the note outside the page canvas
- only switch to in-page explanation when the user explicitly requests it
- note position should default to the right-side annotation lane
- note must remain outside the page frame boundaries
- when no user-specific note format is given, prefer the compact 4-line note structure learned from the reference `.pen`:
  page title / 核心逻辑 / 主操作 / 关键校验

## Default assumptions for prompt simplification

Do not force the user to restate these every time:

- Element Plus is the default visual system
- traditional admin shell is the default page appearance
- reference `.pen` files are default structural evidence when present
- query/list pages require real tables
- query/list pages require visible pagination
- query pages should occupy the full usable width
- generation should proceed iteratively by section
- output should target the current active editor `.pen` file
- business logic should default to an external note
