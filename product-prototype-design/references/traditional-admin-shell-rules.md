# Traditional Admin Shell Rules

Use this file to build the default shell for backend CRUD pages.

This shell is the expected default unless the user explicitly requests another pattern.

## 1. Canonical Shell Order

For a standard CRUD page, build this order:

1. top system bar
2. left navigation
3. content header strip
4. query/filter toolbar
5. action area
6. real table
7. bottom-right pagination

## 2. Top System Bar

Expected characteristics:

- light background
- shallow height, usually around `48-64`
- system name/logo at left
- utility actions and user area at right
- not visually heavy

Rule:

- the top bar should read as infrastructure, not branding theater

## 3. Left Navigation

Expected characteristics:

- narrow width, usually around `220-240`
- grouped text navigation
- subtle active state
- light border separation from the content area

Rule:

- side navigation is a work menu, not a visual centerpiece
- if the menu is long, keep items compact and evenly spaced

## 4. Content Header Strip

Use one of:

- compact tabs strip
- breadcrumb strip
- tabs plus breadcrumb when the business context truly needs both

Rule:

- keep this area thin and operational
- do not turn it into a hero banner

## 5. Query Toolbar

Expected behavior:

- appears before the table
- compact single-row first
- widest control is search
- shorter filters follow
- query/reset buttons stay aligned right or near the filter cluster
- each condition should render as `label text + component`, not a naked component by itself

Rule:

- try one row before expanding to two rows
- if two rows are necessary, still keep them compact and grid-like
- unless explicitly requested otherwise, search placeholders are supplementary text, not a replacement for visible labels

## 6. Action Area

Action buttons should usually appear:

- above the table
- aligned to the left or split left/right with bulk actions

Preferred composition:

- primary create button
- secondary export/import or batch actions
- no oversized action band

## 7. Table Area

Expected characteristics:

- occupies the main body
- uses true table structure
- has a clear operation column
- leaves room for pagination

Rule:

- table is the center of the page, not a decorative card inside a card stack

## 8. Pagination

Expected characteristics:

- bottom-right placement by default
- compact size
- adjacent page-size selector if needed
- total count nearby but secondary

Rule:

- pagination must look like a normal admin list footer, not a detached widget

## 9. Add/Edit Overlay States

Default expectation:

- copy the query page first
- dim the whole page with a full-page mask
- place a right drawer above the mask
- keep the base layout unchanged

Rule:

- the user should still clearly recognize the original query page underneath

## 10. Delete State

Default expectation:

- copy the query page first
- add a full-page mask
- add a centered confirmation panel or dialog

Rule:

- the delete state should feel like a standard admin confirmation, not a redesign of the whole page
