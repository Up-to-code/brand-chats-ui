# Component Library

## Layout Components

### AppShell

Owns the authenticated application frame: sidebar, header, and main content area.

Props:

- `sidebar`
- `header`
- `children`

Rules:

- Full viewport height
- Sidebar fixed on desktop
- Main area scrolls independently

### Sidebar

Renders product identity, primary navigation, connected channels, usage, and profile card.

### Header

Renders only organization switcher and settings icon.

### PageHeader

Renders page title, optional description, status, and one primary action.

### PageContainer

Constrains content width and applies consistent page padding.

### Section

Groups related content with heading, optional description, and content slot.

### SplitLayout

Creates two or three column workspaces such as the Chats page.

## Navigation Components

### SidebarItem

Used for Home, Analytics, and AI Agents.

### ChannelNavItem

Used for connected channels. Includes icon, name, channel type label, and status dot.

### Tabs

Used for channel workspaces and internal settings sections. Active state is underline only.

### Breadcrumb

Used sparingly on deep detail pages.

### OrgSwitcher

Compact organization selector shown in the top header.

## Data Display Components

### MetricCard

One KPI per card. Supports label, value, optional delta, and short metadata.

### StatusCard

Shows operational status and next action.

### TrendChart

Simple blue line chart with minimal grid and no decorative gradients.

### DataTable

Used for files, members, API keys, and integrations.

### EmptyState

Clear explanation and one action. Avoid illustrations unless they communicate product state.

### ActivityItem

Shows an important system event with timestamp and source.

## Form Components

### Input

Standard text input with label, helper text, and error state.

### Textarea

Used for prompts, instructions, fallback behavior, and notes.

### Select

Used for assigned agent, model, tone, role, and integration type.

### Toggle

Used for binary AI behavior and automation states.

### Checkbox

Used for multi-select permissions and conditions.

### FormSection

Groups related fields with title and optional description.

### SaveBar

Persistent bar for unsaved changes. Includes `Cancel` and `Save changes`.

## AI Components

### AgentCard

Shows agent name, role, assigned channels, status, last updated, and edit action.

### PromptEditor

Textarea-focused editor for instructions and prompt rules. May include variable hints and validation.

### RuleCard

Displays one behavioral, escalation, fallback, or automation rule.

### ConfidenceBadge

Shows AI confidence state: high, medium, low, or unknown.

### KnowledgeSourceCard

Shows source type, indexing state, last update, and sync action.

## Chat Components

### ConversationList

Owns filters and list of `ConversationItem`.

### ConversationItem

Shows customer, last message, timestamp, unread badge, status, and assignee.

### ChatThread

Displays chronological messages with day separators and status markers.

### MessageBubble

Differentiates customer, AI, and teammate messages.

### ReplyComposer

Text composer with send, internal note mode, and AI suggested reply insertion.

### CustomerContextPanel

Shows customer details, channel metadata, AI context, and relevant knowledge.

## Modal Components

### AddChannelModal

Four-step modal for connecting a new channel.

### ConfirmDialog

Used for destructive or irreversible actions.

### InviteMemberModal

Used for organization or channel-level invitations.

### IntegrationSetupModal

Used to configure API keys, OAuth, webhooks, and provider-specific settings.

