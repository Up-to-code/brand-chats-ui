# App Architecture

## Product Positioning

This app is a multi-channel AI chatbot management platform for teams that operate AI agents across WhatsApp, website chat, Telegram, Instagram, Messenger, and future messaging surfaces.

The product should feel like AI communication infrastructure: operational, precise, quiet, and trustworthy. The reference quality bar is Stripe for clarity, Linear for speed and hierarchy, and Vercel for developer-grade simplicity.

## App Map

```text
/
├─ auth
│  ├─ sign-in
│  ├─ sign-up
│  ├─ forgot-password
│  └─ reset-password
├─ onboarding
│  ├─ workspace
│  ├─ organization
│  ├─ first-agent
│  ├─ first-channel
│  └─ complete
├─ app
│  ├─ home
│  ├─ analytics
│  ├─ ai-agents
│  │  ├─ new
│  │  └─ [agentId]
│  ├─ channels
│  │  └─ [channelSlug]
│  │     ├─ overview
│  │     ├─ chats
│  │     ├─ analytics
│  │     ├─ ai-settings
│  │     ├─ automations
│  │     ├─ integrations
│  │     ├─ knowledge-base
│  │     └─ team-access
│  ├─ settings
│  │  ├─ general
│  │  ├─ team
│  │  ├─ billing
│  │  ├─ usage
│  │  ├─ api-keys
│  │  └─ security
│  └─ billing
```

## Route Groups

Auth routes use a centered, low-friction layout with no app sidebar. Onboarding uses a focused setup layout with progress and one decision per step. App routes use the shared dashboard shell with sidebar, minimal top header, and dynamic content area.

Channel workspace routes share the app shell and use horizontal tabs inside the channel page. They must not introduce a nested sidebar or dock.

## Core Product Objects

| Object | Purpose | Key Fields |
| --- | --- | --- |
| Organization | Billing and team ownership boundary | name, plan, usage, members |
| Workspace | Operating environment within an organization | name, slug, channels, agents |
| Channel | Connected customer messaging surface | name, type, status, metadata, agentId |
| AI Agent | Configurable AI operator | name, role, model, behavior, status |
| Conversation | Customer interaction thread | channelId, customer, status, assignee, messages |
| Knowledge Source | Indexed material used by agents | type, status, lastIndexedAt |
| Automation | Rule-based workflow | trigger, conditions, actions, status |
| Integration | External connected system | provider, status, credentials, webhooks |

## App Shell Contract

Every authenticated app page uses the same structural contract:

- `AppShell` owns the full viewport layout.
- `Sidebar` owns primary navigation and connected channels.
- `Header` owns only the organization switcher and settings icon.
- `PageContainer` owns page width, vertical rhythm, and responsive spacing.
- Page components own their content, primary action, and empty states.

## Primary Navigation

Primary navigation is intentionally small:

- Home
- Analytics
- AI Agents
- Connected channel list

Secondary organization-level areas, such as Settings, Billing, and Team, are accessed from the settings icon or relevant page links. They should not inflate the main sidebar.

## Data Loading Boundaries

The shell should load organization, workspace, current user, usage summary, and connected channels. Individual pages should load only their page-specific data.

Channel workspace pages should resolve the channel from `channelSlug`, then load tab-specific data independently so switching tabs remains fast.

## App States

Every page and major component must account for:

- Loading
- Empty
- Ready
- Error
- Permission denied
- Integration disconnected

These states should be quiet and actionable. Avoid generic error banners without a suggested next step.

