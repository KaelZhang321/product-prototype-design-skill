# Traditional Admin Visual Tokens

Use this file to keep generated pages aligned with a classic backend management system rather than a stylized SaaS page.

This file defines the default visual density and shell appearance for normal admin CRUD work.

## 1. Overall Style Intent

Target look:

- traditional operations console
- classic admin system
- dense but readable
- light shell with thin borders
- restrained color usage

Avoid:

- oversized card layouts
- hero sections
- large-radius modern SaaS styling
- strong gradients
- colorful dashboard aesthetics
- exaggerated shadows

## 2. Canvas And Density

- default canvas: `1920 x 1080`
- page shell should feel compact and operational
- controls should be visually smaller than generic design-system demos
- information density should be medium-high, not sparse

## 3. Typography

Preferred sizing:

- top nav/system title: `16-18`
- page title: `16-20`
- table/filter/body text: `12-14`
- helper text: `12`
- table header text: `12`
- operation links: `12-13`

Preferred weights:

- page title: `600-700`
- section title: `600`
- table header: `600-700`
- body: `400-500`

Rule:

- do not use oversized page titles
- do not create big visual contrast jumps between shell text and page text

## 4. Control Heights

Default control sizing:

- compact controls: `28`
- standard controls: `32`
- toolbar height: `40-44`
- table header height: `40-44`
- table row height: `40-48`

Rule:

- prefer `28-32` controls for ordinary backend pages
- avoid large `40+` buttons unless the user explicitly asks for a strong CTA

## 5. Radius

- input/button/select radius: `2-6`
- cards/container radius: `4-8`
- pagination/button chips: `2-4`

Rule:

- keep corners small
- prefer `4` as the safe default
- do not use soft consumer-app rounding

## 6. Borders And Shadows

Preferred surfaces:

- white content surface
- very light gray page background
- thin gray borders
- minimal or no shadow

Rule:

- border-first, shadow-second
- use shadows only where layering needs explanation, such as drawers or dialogs

## 7. Colors

Use Element Plus semantics, but keep the traditional admin balance:

- page background: very light gray-blue or neutral light gray
- content background: white
- primary button: medium blue
- secondary button: white with light border
- table header background: very light gray
- selected nav: light-tint background or subtle text emphasis

Rule:

- color should support structure, not dominate it
- avoid deep branded sidebars by default unless the user explicitly wants that

## 8. Table Look

Traditional admin tables should feel:

- grid-based
- lightly bordered
- compact
- mostly monochrome

Preferred signals:

- light header fill
- thin row separators
- small text
- operation column as inline text actions

Avoid:

- chunky cards pretending to be rows
- oversized row heights
- large colorful status widgets unless business states require them

## 9. Navigation Look

Shell expectation:

- top system bar is shallow and light
- left sidebar is narrow and ordered
- selected item is subtle, not loud
- tabs or breadcrumb strip should be compact

Rule:

- shell chrome should frame the work area, not compete with it

## 10. Negative Constraints

Do not generate these by default:

- glassmorphism
- dark mode
- colorful KPI-first dashboard headers
- marketing banners
- oversized iconography
- rounded bento-grid layouts
- floating multi-card hero compositions
