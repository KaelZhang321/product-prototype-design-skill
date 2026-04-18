# Reference Pen Patterns

Use this file when the user provides a reference `.pen` and asks to absorb its layout, copy, or component organization into the skill.

This file is based on the local reference prototype corpus in `参考.pen`.

Important:

- treat the reference `.pen` as a structural and copywriting source
- keep Element Plus as the default visual and component-semantic baseline
- do not blindly copy the reference `.pen` deep-blue palette, custom token names, or font choices when they conflict with Element Plus

## 1. What To Learn From The Reference `.pen`

Absorb these patterns:

- page-shell hierarchy
- information density
- note writing format
- card segmentation
- filter and toolbar ordering
- table width distribution strategy
- drawer content grouping
- action-bar composition

Do not absorb these blindly:

- exact color palette
- project-specific variable names
- custom brand styling
- any business module names that are irrelevant to the user request

## 2. Canonical Page Shell Learned From The Reference

The reference `.pen` repeatedly uses this shell:

- top nav
- body
- sidebar
- content
- page title
- main work area

Recommended dimensions for standard pages:

- desktop canvas: `1920 x 1080`
- top nav height: `64`
- sidebar width: `240`
- content padding: around `12,16`
- content vertical gap: around `12`

Rule:

- keep the shell stable across related pages
- sidebar and top nav should not be rebuilt differently from page to page without a business reason

## 3. Query/List Page Pattern

The reference list pages consistently use:

- page title
- main card
- filter toolbar
- table container
- table header
- structural table rows
- pagination or bottom summary area

Preferred hierarchy:

- `TopNav`
- `Body`
- `Sidebar`
- `Content`
- `PageTitle`
- `MainCard`
- `FilterToolbar`
- `Table`

Rule:

- keep filters and actions in one visible toolbar above the table
- left side is for filters/search
- right side is for primary and secondary actions

## 4. Filter Toolbar Pattern

The reference `.pen` uses a compact filter bar:

- toolbar height near `44`
- search input first
- short select/status filters next
- action buttons aligned right
- controls usually `32-34` high
- control corner radius around `6`

Use this structurally with Element Plus equivalents:

- search input -> `Input`
- level/status selectors -> `Select`
- date constraints if needed -> `DatePicker`
- primary action -> primary `Button`
- export/reset -> secondary `Button`

Rule:

- search field is usually the widest control
- short categorical filters should not consume excessive width
- do not scatter filters into multiple unrelated rows unless the business fields force it

## 5. Table Pattern

The reference `.pen` demonstrates a real table layout:

- a dedicated header row
- each header cell is a frame
- each data row is a frame
- each data cell is a frame
- row content uses compact text or tags

Learn these behaviors:

- columns are intentionally sized by business importance
- identifier columns are narrower than descriptive text columns
- status columns use short semantic labels
- operations live in the final cell and stay compact

Do not do this:

- one-line text pretending to be a table
- equal-width columns for obviously unequal data
- overly compressed columns that make important fields unreadable

## 6. Form / Create Page Pattern

The reference create page uses:

- a title/header card with instruction text
- multiple white section cards
- section title first
- form rows beneath
- each field group is label above, control below
- control height around `34`

Use this structurally when building add/edit forms:

- section card
- section title
- form rows
- stacked label + control groups

Rule:

- prefer 2-4 fields per row depending on business complexity
- required marks and helper copy should be concise
- section grouping should reflect business domains, not arbitrary visual splitting

## 7. Drawer Content Pattern

The reference `.pen` has dedicated drawer-style pages whose internal drawer content is useful even though the overall composition is not the same as the required CRUD overlay rule.

Absorb:

- drawer width around `560-620`
- drawer title at top
- grouped sections inside the drawer
- each section has a title and content block
- bottom action row aligned right

Do not change the CRUD state rule:

- add/edit still derive from the query page base
- add/edit still require full-page mask plus topmost right drawer

Interpretation:

- learn the inside of the drawer from the reference `.pen`
- keep the overlay behavior from the skill's CRUD rules

## 8. Note Pattern

The reference `.pen` uses compact page-external notes very consistently.

Default note structure:

- first line: page identifier + page name
- second line: `【核心逻辑】...`
- third line: `【主操作】...`
- fourth line: `【关键校验】...`

Default note shape:

- width around `250`
- height around `240`
- positioned to the right of the page

Rule:

- notes summarize business meaning, not UI layout
- note text should be concise and review-oriented
- keep note outside the page frame

## 9. Naming And Hierarchy Conventions

The reference `.pen` repeatedly uses readable node names such as:

- `TopNav`
- `Body`
- `Sidebar`
- `Content`
- `PageTitle`
- `FilterToolbar`
- `ActionsRight`
- `ActionBar`
- `MainCard`

Use simple structural names when building reusable page sections.

Rule:

- name major sections clearly
- avoid meaningless random names for page-level containers

## 10. How To Reconcile With Element Plus

When both this file and the Element Plus references are loaded:

- shell, hierarchy, and note pattern come from this file
- colors, button semantics, tag semantics, input behavior, spacing discipline, and state styling come from Element Plus references

Priority rule:

1. business requirement
2. CRUD state rules
3. Element Plus visual/component semantics
4. reference `.pen` structural patterns

This means:

- keep Element Plus as the visual default
- use the reference `.pen` to improve organization and page realism
- do not let a non-Element custom brand style override the default system unless the user explicitly asks for it
