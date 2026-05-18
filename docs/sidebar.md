# Sidebar

## Purpose

The sidebar is the platform map. It should help users switch between global views and connected channels without becoming a secondary dashboard.

## Dimensions

Desktop width: `240px`.

The sidebar is fixed on desktop and collapses behind a menu trigger on tablet and mobile.

## Structure

```text
Sidebar
├─ Top
│  ├─ Product logo
│  └─ Workspace name
├─ Main navigation
│  ├─ Home
│  ├─ Analytics
│  └─ AI Agents
├─ Connected Channels
│  ├─ ChannelNavItem
│  ├─ ChannelNavItem
│  └─ Add Channel button
└─ Bottom
   ├─ Usage progress bar
   └─ User profile compact card
```

## Top Section

The top section contains only the product logo and current workspace name. Keep the logo compact and avoid taglines.

## Main Navigation

Main navigation contains exactly:

1. Home
2. Analytics
3. AI Agents

Each item uses a small icon and label.

## Connected Channels

Connected channels are dynamic and sorted by operational relevance:

1. Channels with active incidents or disconnected status
2. Active channels by recent activity
3. Inactive channels

Each `ChannelNavItem` includes:

- Channel icon
- Channel name
- Channel type label
- Active status dot

Example:

```text
Alpha Real Estate
WhatsApp
```

Status dots:

| Status | Dot |
| --- | --- |
| Active | Green |
| Degraded | Amber |
| Disconnected | Red |
| Setup pending | Slate |

## Add Channel Button

The `+ Add Channel` button appears directly below the connected channel list. It opens `AddChannelModal`.

Use a secondary or ghost style. It should be visible but not louder than primary navigation.

## Bottom Section

The bottom contains only:

- Usage progress bar
- User profile compact card

Do not add explanatory text under usage. The progress label can show a compact value such as `64%`.

## Visual Rules

- White or very light background
- Subtle right border
- 16px internal horizontal padding
- Quiet hover state
- No heavy shadows
- No extra badges beyond channel status and unread count when operationally necessary

