# Channel Workspace

## Purpose

A channel workspace is the operational control room for one connected messaging channel. It should answer: what is happening on this channel, how is the AI behaving, and what needs human attention?

## URL Pattern

```text
/app/channels/[channelSlug]/[tab]
```

Example:

```text
/app/channels/alpha-real-estate-whatsapp/overview
```

## Header

The channel page header contains:

- Channel icon
- Channel name
- Connection status
- Small metadata line

Metadata examples:

- `WhatsApp Business API`
- `Connected 18 days ago`
- `Assigned to Leasing Assistant`
- `Last sync 4 min ago`

## Tabs

Tabs:

1. Overview
2. Chats
3. Analytics
4. AI Settings
5. Automations
6. Integrations
7. Knowledge Base
8. Team Access

Use tabs only. Do not add a second sidebar or dock.

## Overview

Purpose: show what matters now.

Components:

- Channel summary header
- Up to four metric cards
- One simple trend chart
- Channel status card
- Assigned AI agent card
- Quick actions card

Metric cards:

- Conversations
- AI resolution rate
- Avg response time
- Human takeover rate

## Chats

Purpose: operate the inbox.

Layout: three columns.

Left column:

- Conversation list
- Conversation filters
- Unread badges
- AI handled or human takeover status

Center column:

- Chat thread
- Message bubbles
- Assignment state
- Reply composer
- AI suggested reply

Right column:

- Customer context
- AI context
- Assigned teammate
- Conversation metadata
- Relevant knowledge sources

## Channel Analytics

Purpose: inspect the performance of this one channel.

Use the same KPI language as global analytics, scoped to the selected channel. Keep one main chart maximum.

## AI Settings

Purpose: configure agent behavior for this channel.

Sections:

- Personality
- Instructions
- Tone
- Prompt rules
- Knowledge sources
- Escalation rules
- Fallback behavior
- Memory

This page should feel like configuring an AI operating system. Use textareas, rule cards, toggles, select fields, and a persistent save bar.

## Automations

Purpose: create channel-specific workflows.

Sections:

- Automation list
- Create automation
- Triggers
- Conditions
- Actions

Example automations:

- If customer asks for pricing, send brochure.
- If lead is hot, notify sales team.
- If AI confidence is low, request human takeover.

## Integrations

Purpose: manage external tools for this channel.

Sections:

- Connected integrations
- Available integrations
- API keys
- Webhooks

Examples:

- CRM
- Google Sheets
- Zapier
- Make
- Meta
- WhatsApp Business API

## Knowledge Base

Purpose: manage AI knowledge for this channel.

Sections:

- Uploaded files
- Synced URLs
- Data sources
- Indexing status
- Last training update

Components:

- Upload area
- File table
- Status badges
- Sync button

## Team Access

Purpose: manage channel-specific permissions.

Sections:

- Team members
- Roles
- Permissions
- Invite member

Roles:

- Owner
- Admin
- Agent
- Viewer

