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

## Table rules

- query-page tables must be structural
- one-line text tables are forbidden
- each row and cell should be its own frame when possible
- visible pagination is mandatory

## Annotation rules

- use an in-page business rule block for core business logic
- keep the business rule block inside the page content area
- do not default to top-level external notes
