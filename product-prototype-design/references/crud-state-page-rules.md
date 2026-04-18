# CRUD State Page Rules

Use this file whenever the request is a CRUD backend prototype.

## Required states

1. 查询页
2. 新增页
3. 修改页
4. 删除页

## Generation order

1. build 查询页
2. validate 查询页
3. copy 查询页 to 新增页 / 修改页 / 删除页
4. apply overlays

## Add/Edit rules

- preserve query-page base
- use full-page mask
- use right drawer
- drawer must be topmost

## Delete rules

- preserve query-page base
- use full-page mask
- use centered confirmation layer

## Query-page rules

- real table
- visible pagination
- no fake drawer lane
- full usable width
