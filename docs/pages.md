# Pages

## Home

Purpose: show the global state of the workspace and what needs attention now.

Primary action: `Add Channel`.

Sections:

- Welcome and workspace summary
- Active channels
- AI agents summary
- Recent important system events
- Usage summary

Recommended layout:

- Page header with workspace name and one-sentence operational summary
- Compact metric row with no more than four cards
- Active channels table or list
- Two-column lower area for AI agents summary and recent events
- Usage summary as a compact card

Avoid placing multiple charts on Home.

## Analytics

Purpose: understand performance across all connected channels.

Primary action: export or inspect channel comparison, depending on product maturity.

Sections:

- Conversations
- Resolution rate
- Response time
- Human handoff rate
- Channel comparison

Rules:

- Maximum one main chart
- Use compact metric cards for top-level KPIs
- Keep comparison table scannable
- Use a simple blue line or grouped bars only when comparison is required

## AI Agents

Purpose: manage every AI agent and understand where each agent is deployed.

Primary action: `Create Agent`.

Sections:

- Agents list
- Status
- Assigned channels
- Model and config summary
- Create new agent button

Agent card includes:

- Name
- Role
- Assigned channels
- Status
- Last updated
- Edit action

Recommended empty state: explain that agents are reusable operators that can be assigned to one or more channels, then offer `Create Agent`.

## Agent Detail

Purpose: edit the reusable agent configuration that can be assigned across channels.

Sections:

- Agent identity
- Model and runtime settings
- Global instructions
- Channel assignments
- Evaluation and recent changes

Channel-specific behavior belongs in channel `AI Settings`, not the global agent page.

## Settings

Purpose: configure organization-level account, security, team, billing, and platform settings.

Settings should be calm and form-led. Use local navigation only inside the settings area.

## Billing

Purpose: show plan, usage, invoices, and upgrade controls.

Billing should include:

- Current plan
- Usage against limits
- Payment method
- Invoice history
- Upgrade or manage plan action

## Team Management

Purpose: manage organization-level access.

Channel-specific permissions belong in the channel `Team Access` tab.

