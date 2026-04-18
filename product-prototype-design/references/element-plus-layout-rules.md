# Element Plus Layout Rules

Use this file for page shell and width rules.

## Query Page

- sidebar + header + right main content
- right main content must use the full available width
- filter card and table module must occupy the usable width
- visible pagination is required

## Add/Edit Page

- query-page base copied first
- full-page mask added above base
- right drawer added above mask
- base layout remains unchanged

## Delete Page

- query-page base copied first
- full-page mask added above base
- centered confirmation layer added above mask

## Width Rules

- usable content width = main content width - horizontal padding * 2
- do not leave artificial whitespace on query pages
- reserve overlay behavior only for copied state pages

## Validation Rules

- whole page screenshot
- filter card screenshot
- table card screenshot
- drawer state screenshot
- delete state screenshot
