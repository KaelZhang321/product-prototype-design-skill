# Element Plus Layout Rules

Use this file for page shell and width rules.

## Query Page

- default desktop frame: `1920 x 1080`
- sidebar + header + right main content
- top nav height should usually stay near `64`
- left sidebar width should usually stay near `240`
- right main content must use the full available width
- filter card and table module must occupy the usable width
- visible pagination is required
- content should not feel over-stretched on the wide canvas
- filter controls should keep reasonable widths
- filter items should use visible text labels before controls by default
- table columns should be intentionally distributed
- preferred page flow is:
  top nav -> sidebar/content body -> page title -> main card -> filter toolbar -> table/pagination
- for normal backend pages, prefer a traditional admin shell over a stylized SaaS composition

## Add/Edit Page

- query-page base copied first
- full-page mask added above base
- right drawer added above mask
- base layout remains unchanged
- the drawer internals may use section grouping inspired by a reference `.pen`, but the page composition must still behave like an overlay state

## Delete Page

- query-page base copied first
- full-page mask added above base
- centered confirmation layer added above mask

## Width Rules

- usable content width = main content width - horizontal padding * 2
- do not leave artificial whitespace on query pages
- reserve overlay behavior only for copied state pages
- if the business fields create too many columns, widen column distribution intentionally instead of compressing all columns into equal narrow cells
- use the reference `.pen` for structural distribution ideas, not for replacing the Element Plus visual baseline

## Validation Rules

- whole page screenshot
- filter card screenshot
- table card screenshot
- drawer state screenshot
- delete state screenshot
