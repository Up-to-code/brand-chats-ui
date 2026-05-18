# Add Channel Flow

## Entry Point

The `+ Add Channel` button in the sidebar opens `AddChannelModal`.

The modal is a four-step flow:

1. Select channel type
2. Basic information
3. Connection setup
4. Review and connect

## Step 1: Select Channel Type

Show channel cards:

- WhatsApp
- Website Chat
- Telegram
- Instagram
- Messenger

Each card includes:

- Channel icon
- Channel name
- Short setup note
- Availability status when relevant

Future integrations can appear as disabled cards with `Coming soon` only when the product needs to preview roadmap.

## Step 2: Basic Information

Fields:

- Channel name
- Business name
- Assigned AI agent

Rules:

- Channel name should be user-facing inside the app.
- Business name should match the customer-facing identity.
- Assigned AI agent may be optional only if the platform supports human-only inbox mode.

## Step 3: Connection Setup

Fields depend on channel type.

Common fields:

- API key
- Phone number
- Webhook
- Verification token

Channel-specific examples:

| Channel | Fields |
| --- | --- |
| WhatsApp | Business account, phone number, API key, webhook |
| Website Chat | Domain, install snippet, verification token |
| Telegram | Bot token, webhook |
| Instagram | Meta account, page, permissions |
| Messenger | Meta page, app credentials, webhook |

## Step 4: Review and Connect

Show:

- Channel type
- Channel name
- Business name
- Assigned AI agent
- Connection fields summary
- Permissions or scopes

Primary action: `Connect Channel`.

After success:

- Add the channel to the sidebar under Connected Channels.
- Navigate to `/app/channels/[channelSlug]/overview`.
- Show a quiet success toast.

## Validation

Validate each step before continuing.

Connection setup should verify credentials where possible before final review.

## Failure States

Common failures:

- Invalid API key
- Webhook unreachable
- Verification token mismatch
- Missing provider permissions
- Channel already connected

Failure messages should be specific and include the next fix.

