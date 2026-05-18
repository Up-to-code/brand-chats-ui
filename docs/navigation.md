# Navigation

## Navigation Principles

Navigation should make the operating model obvious: global workspace first, then connected channels, then channel-specific work. Avoid duplicate routes, nested sidebars, and hidden primary actions.

## Global Navigation Structure

| Label | Route | Purpose |
| --- | --- | --- |
| Home | `/app/home` | Global workspace overview |
| Analytics | `/app/analytics` | Cross-channel performance |
| AI Agents | `/app/ai-agents` | Manage all AI agents |
| Channel item | `/app/channels/[channelSlug]/overview` | Open a channel workspace |

## Header Navigation

The top header is minimal by design and may contain only:

- Organization switcher
- Settings icon

Do not add global search, notifications, create buttons, banners, or marketing content to the header.

## Channel Workspace Tabs

Channel workspaces use horizontal tabs below the channel page header:

| Tab | Route |
| --- | --- |
| Overview | `/app/channels/[channelSlug]/overview` |
| Chats | `/app/channels/[channelSlug]/chats` |
| Analytics | `/app/channels/[channelSlug]/analytics` |
| AI Settings | `/app/channels/[channelSlug]/ai-settings` |
| Automations | `/app/channels/[channelSlug]/automations` |
| Integrations | `/app/channels/[channelSlug]/integrations` |
| Knowledge Base | `/app/channels/[channelSlug]/knowledge-base` |
| Team Access | `/app/channels/[channelSlug]/team-access` |

Tabs use an underline active state. They must remain horizontally scrollable on small screens.

## Settings Navigation

Settings pages are organization-level and reached from the header settings icon.

Recommended settings sections:

- General
- Team
- Billing
- Usage
- API Keys
- Security

Settings may use a local settings navigation because it is a dedicated settings area, not a channel workspace.

## Active State Rules

Primary nav active states use:

- Small blue left indicator
- Light blue background
- Navy text
- No heavy borders
- No large filled pills

Channel active state should highlight the selected channel and keep the status dot visible.

## Breadcrumb Usage

Use breadcrumbs only on deep detail pages such as an individual AI agent, automation editor, or billing invoice. Do not show breadcrumbs on the main dashboard pages or channel tab pages.

