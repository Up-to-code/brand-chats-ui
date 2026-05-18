# Responsive Rules

## Breakpoints

Recommended breakpoints:

| Name | Width |
| --- | --- |
| Mobile | `< 640px` |
| Tablet | `640px - 1023px` |
| Desktop | `1024px+` |
| Wide | `1440px+` |

## App Shell

Desktop:

- Sidebar fixed at `240px`
- Header spans main content only
- Main content scrolls

Tablet and mobile:

- Sidebar becomes a sheet or drawer
- Header remains minimal
- Organization switcher and settings icon stay visible

## Page Container

Padding:

- Desktop: `32px`
- Tablet: `24px`
- Mobile: `16px`

Content should use responsive constraints rather than viewport-scaled typography.

## Channel Tabs

Tabs remain horizontal and scrollable on smaller screens. Do not convert channel tabs into a second sidebar.

## Chats Layout

Desktop:

- Three columns
- Left conversation list
- Center thread
- Right context panel

Tablet:

- Conversation list and thread can use a master-detail pattern
- Context panel moves into a drawer or collapsible panel

Mobile:

- One primary pane visible at a time
- Conversation list opens thread
- Customer context opens as a sheet
- Reply composer remains anchored to the bottom of the thread

## Cards and Tables

Metric cards wrap into two columns on tablet and one column on mobile.

Tables should become:

- Horizontally scrollable when columns are essential
- Stacked rows when content is simple

## Modals

Desktop modals are centered.

Mobile modals use full-width sheets with comfortable touch targets.

## Touch Targets

Minimum interactive size: `40px`.

Icon-only buttons require tooltips on desktop and accessible labels on all viewports.

