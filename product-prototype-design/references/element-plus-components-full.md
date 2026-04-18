# Element Plus Components Full

Use this file as the source-backed local component index for prototype generation.

This file is derived from the actual `element-plus` source tree under:

- `packages/components/*`

Important:

- not every source directory should be treated as a first-class prototype component
- some directories are subcomponents, internal building blocks, structural wrappers, or implementation utilities
- prototype generation should prefer the user-facing component layer first, and only use subcomponents/internal pieces when the page genuinely needs them

## 1. Primary User-facing Components

These are the main components that most enterprise prototypes should think in.

### Layout / Structure

- Affix
- Aside
- Container
- Divider
- Footer
- Header
- Main
- Row
- Col
- Space
- Splitter
- SplitterPanel

### Navigation

- Anchor
- Backtop
- Breadcrumb
- BreadcrumbItem
- Dropdown
- DropdownItem
- DropdownMenu
- Menu
- MenuItem
- MenuItemGroup
- SubMenu
- PageHeader
- Pagination
- Steps
- Step
- Tabs
- TabPane

### Buttons / Actions

- Button
- ButtonGroup
- Link
- Popconfirm

### Form Inputs

- Autocomplete
- Cascader
- CascaderPanel
- Checkbox
- CheckboxButton
- CheckboxGroup
- ColorPicker
- DatePicker
- Form
- FormItem
- Input
- InputNumber
- InputOtp
- InputTag
- Mention
- Radio
- RadioButton
- RadioGroup
- Rate
- Segmented
- Select
- SelectV2
- Slider
- Switch
- TimePicker
- TimeSelect
- Transfer
- TreeSelect
- Upload

### Data Display

- Avatar
- AvatarGroup
- Badge
- Calendar
- Card
- Carousel
- CarouselItem
- CheckTag
- Collapse
- CollapseItem
- Countdown
- Descriptions
- DescriptionsItem
- Empty
- Image
- ImageViewer
- Progress
- Result
- Skeleton
- SkeletonItem
- Statistic
- Table
- TableColumn
- TableV2
- Tag
- Text
- Timeline
- TimelineItem
- Tour
- TourStep
- Tree
- TreeV2
- Watermark

### Feedback / Overlay / Notice

- Alert
- Dialog
- Drawer
- Loading
- Message
- MessageBox
- Notification
- Popover
- Tooltip

### Utility / Scroll / Visibility

- Icon
- InfiniteScroll
- Scrollbar
- VirtualList

## 2. Source-level Subcomponents And Internal Building Blocks

These exist in source and matter when reading the library, but should not usually be treated as independent prototype choices.

- AnchorLink
- Base
- Collection
- CollapseTransition
- ColorPickerPanel
- ConfigProvider
- FocusTrap
- Option
- OptionGroup
- Overlay
- Popper
- RovingFocusGroup
- Slot

## 3. Prototype Priority Tiers

## Tier A: Core enterprise admin prototype components

Use these first for backend pages:

- Layout
- Menu
- Breadcrumb
- Form
- Input
- Select
- DatePicker
- Button
- Table
- Tag
- Pagination
- Drawer
- Dialog
- Card
- Tabs
- Tree
- Descriptions
- Alert
- Empty
- Skeleton

## Tier B: Frequent secondary components

- Switch
- Radio
- Checkbox
- Upload
- Progress
- Statistic
- Avatar
- Badge
- Dropdown
- Tooltip
- Popconfirm
- Result
- Timeline

## Tier C: Specialized components

Use only when the business need is real:

- Cascader
- TreeSelect
- SelectV2
- TableV2
- Transfer
- Tour
- Mention
- ColorPicker
- Rate
- Calendar
- Carousel
- Watermark
- InfiniteScroll
- VirtualList
- InputOtp
- InputTag
- Splitter

## 4. Admin-prototype Mapping

### Query page

- Form + Input + Select + DatePicker + Button
- Table + Tag + Pagination

### Add/Edit page

- Drawer + Form + FormItem + Input + Select + Switch + Button

### Delete page

- Popconfirm or Dialog-style confirmation

### Detail page

- Descriptions + Card + Tabs + Timeline + Alert

### Navigation shell

- Menu + Breadcrumb + Tabs + Dropdown

## 5. What To Avoid In Prototypes

- Do not choose internal-only primitives as if they were business-facing widgets.
- Do not overuse source-only helpers such as `overlay`, `popper`, `slot`, `collection`, `base`.
- Do not treat `table-column` or `option` as standalone page modules; they are child structures of a higher-level component.
- Do not let rare components dominate simple CRUD pages.

## 6. Source-backed Notes

The actual source tree contains more entries than the docs overview because:

- some are child subcomponents
- some are infrastructure pieces
- some are structural wrappers

For prototype work, the correct approach is:

1. prefer primary user-facing components
2. use subcomponents only as structure inside a parent pattern
3. keep enterprise admin pages focused on Tier A and Tier B
