# Pencil MCP Execution Rules

Use this file for stable generation behavior in Pencil MCP.

## Reliability rules

- use small `batch_design` blocks
- split by page section
- validate with screenshots after each meaningful stage

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

- use `note` for core business logic
- keep note out of the primary interaction flow
