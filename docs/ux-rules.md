# UX Rules

## Core Rule

Every page must answer: what is the user trying to do here?

If a component does not support the page purpose, remove it.

## Page Rules

Each page should have:

- Clear purpose
- One primary action
- Obvious hierarchy
- Minimal distractions
- Predictable navigation

## Avoid

- Too many charts
- Too many cards
- Nested sidebars
- Colorful dashboards
- Generic SaaS clutter
- Decorative components that do not communicate product state
- Notification spam
- Global search unless there is a real search product

## Operational Clarity

Important operational states must be visible:

- Channel disconnected
- AI confidence low
- Human takeover needed
- Knowledge indexing failed
- Automation disabled
- Usage limit approaching

These states should be visible near the related object, not hidden in a global notification center.

## Primary Action Rules

Each page gets one primary action. Examples:

| Page | Primary Action |
| --- | --- |
| Home | Add Channel |
| Analytics | Export report |
| AI Agents | Create Agent |
| Channel Overview | Open Chats |
| Chats | Send Reply |
| AI Settings | Save Changes |
| Automations | Create Automation |
| Integrations | Connect Integration |
| Knowledge Base | Upload Source |
| Team Access | Invite Member |

## Empty States

Empty states should include:

- What is missing
- Why it matters
- One next action

Do not use large decorative empty-state artwork.

## Error States

Error states should include:

- What failed
- Whether data is safe
- How to retry or fix it

## AI UX Rules

AI behavior controls must feel explicit and inspectable.

Users should be able to understand:

- What the AI is instructed to do
- Which knowledge sources it can use
- When it escalates
- How it behaves when uncertain
- Which channels it is assigned to

Avoid vague AI labels such as `Smart Mode` unless the behavior is defined nearby.

