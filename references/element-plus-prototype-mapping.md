# Element Plus Prototype Mapping

Use this file to map Element Plus component concepts to prototype page structures.

## Query Page

- `Form + Input + Select + DatePicker + Button`
  maps to filter region
- `Card + Table + Pagination`
  maps to main list region

## Add/Edit State

- `Drawer + Form + FormItem + Input + Select + Switch + Button`
  maps to right-side edit state

## Delete State

- `Popconfirm` or `Dialog`
  maps to centered delete confirmation state

## Detail State

- `Descriptions + Card + Tabs + Timeline`
  maps to rich detail pages

## Navigation

- `Menu`
  maps to left navigation
- `Breadcrumb`
  maps to top location bar
- `Tabs`
  maps to peer content switching

## Status / Semantics

- `Tag`
  maps to table statuses and labels
- `Alert`
  maps to important page-level instructions or risks
- `Badge`
  maps to compact counters only when necessary

## Page-state-specific Rules

- Query page must not reserve drawer space
- Add/Edit pages must overlay a full-page mask on top of the query page
- Add/Edit drawers must be topmost
- Delete confirmation should preserve the query-page base underneath

## Business Notes

There is no direct Element Plus component for prototype-review business notes.

Use:

- Pencil `note`

Placement rule:

- right-side annotation lane
- visually secondary
- should not displace the primary UI
