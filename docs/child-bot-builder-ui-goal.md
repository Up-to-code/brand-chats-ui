# Child Bot Builder App UI Build Goal

Source pattern: [Using Goals in Codex](https://raw.githubusercontent.com/openai/openai-cookbook/main/examples/codex/using_goals_in_codex.ipynb)

## Purpose

Use this document as the implementation goal for building the Child Bot Builder app UI. It adapts the Codex Goals pattern into a concrete product-building contract: what must be true when the UI is complete, how completion is verified, which constraints must stay intact, and how to continue when the next step depends on what is discovered during implementation.

## Product Definition

Child Bot Builder is a focused app for creating, configuring, testing, and managing safe AI chatbots for children. The UI must help parents, educators, and administrators build child-appropriate bots with clear guardrails, age settings, content boundaries, knowledge sources, and review controls.

The app should feel:

- Calm
- Trustworthy
- Simple
- Safety-first
- Operational
- Premium, not playful clutter

The interface should avoid noisy cartoon styling. It can be warm, but it must communicate control, safety, and clarity.

## Codex Goal

```text
/goal Build the Child Bot Builder app UI as an implementation-ready product system, verified by completed routes, reusable components, responsive layouts, and a local visual QA pass, while preserving the existing project conventions and design constraints. Use the repository's current Next.js, component, and styling patterns. Between iterations, inspect the current UI, implement the next highest-value screen or component, verify it in browser, and continue until all core flows are represented. If blocked by missing product decisions or technical constraints, stop with the completed work, evidence gathered, blocker, and the exact decision needed.
```

## Success Criteria

The UI is complete when the app includes:

- Auth and onboarding entry points
- Main dashboard shell
- Left sidebar navigation
- Minimal top header
- Bot builder workspace
- Bot management pages
- Safety and guardrail configuration
- Knowledge source management
- Conversation testing interface
- Analytics overview
- Settings, billing, and team access surfaces
- Reusable component library primitives
- Responsive desktop, tablet, and mobile behavior

Completion must be based on evidence, not impression. The UI should be considered done only after routes render, navigation works, key states are represented, and screenshots confirm the layout is not broken.

## Verification Surface

Use the following evidence to verify progress:

- Local build or typecheck result
- Local dev server rendering
- Browser screenshots for primary pages
- Desktop and mobile viewport checks
- Component reuse across pages
- No obvious text overflow or layout overlap
- Navigation routes open the expected screens
- Empty, loading, and error states exist where needed

Recommended checks:

```bash
npm run lint
npm run build
npm run dev
```

Use the in-app browser to inspect the running UI after meaningful frontend changes.

## Constraints

The build must preserve these constraints:

- Light mode only
- No purple
- No decorative clutter
- No marketing landing page as the primary app surface
- No nested sidebars
- No global notification spam
- No search bar unless a real search workflow exists
- Cards must have one purpose
- Tabs use underline active state
- Header contains only organization switcher and settings icon
- Sidebar remains quiet and operational
- UI must remain accessible and responsive

## App Map

```text
/
├─ auth
│  ├─ sign-in
│  ├─ sign-up
│  └─ reset-password
├─ onboarding
│  ├─ welcome
│  ├─ child-profile
│  ├─ first-bot
│  ├─ safety-baseline
│  └─ complete
└─ app
   ├─ home
   ├─ bots
   │  ├─ new
   │  └─ [botId]
   │     ├─ overview
   │     ├─ builder
   │     ├─ safety
   │     ├─ knowledge
   │     ├─ test-chat
   │     ├─ analytics
   │     └─ access
   ├─ conversations
   ├─ analytics
   ├─ knowledge
   ├─ settings
   ├─ billing
   └─ team
```

## Primary Layout

The authenticated app uses one shell:

- Left sidebar
- Minimal top header
- Main content area

The top header includes only:

- Organization or workspace switcher
- Settings icon

The sidebar includes:

- Product logo
- Workspace name
- Home
- Bots
- Conversations
- Analytics
- Knowledge
- Bot list
- Create Bot button
- Usage progress bar
- Compact user profile

## Core Pages

### Home

Purpose: show the state of the child bot workspace.

Sections:

- Welcome summary
- Active bots
- Safety status summary
- Recent review events
- Usage summary

Primary action: `Create Bot`.

### Bots

Purpose: manage all child-safe bots.

Sections:

- Bot list
- Bot status
- Assigned child profile or classroom
- Safety profile
- Last updated
- Edit action

Primary action: `Create Bot`.

### Bot Overview

Purpose: show what matters for one bot.

Sections:

- Bot summary
- Safety status
- Recent conversations needing review
- Knowledge health
- Quick actions

### Bot Builder

Purpose: configure the bot identity and behavior.

Sections:

- Bot name
- Role
- Age range
- Personality
- Allowed topics
- Blocked topics
- Response style
- Conversation goals

### Safety

Purpose: configure child safety rules.

Sections:

- Age controls
- Content filters
- Escalation rules
- Blocked topics
- Personal information handling
- Parent or teacher review rules
- Emergency fallback behavior

This page is the most important trust surface in the product.

### Knowledge

Purpose: manage what the bot can know.

Sections:

- Uploaded files
- Approved URLs
- Learning materials
- Indexing status
- Last training update

### Test Chat

Purpose: safely test the bot before publishing.

Layout:

- Left: scenario presets
- Center: chat thread
- Right: safety evaluation and bot reasoning summary

Features:

- Simulated child messages
- AI response preview
- Safety flags
- Suggested rule improvements

### Conversations

Purpose: review real conversations.

Sections:

- Conversation list
- Review status
- Safety flags
- Transcript
- Parent or teacher notes

### Analytics

Purpose: understand usage and safety performance.

Sections:

- Conversations
- Safe completion rate
- Escalation count
- Blocked topic attempts
- Review queue volume

Use one main chart maximum.

### Settings

Purpose: manage workspace-level configuration.

Sections:

- General
- Child profiles
- Team
- Billing
- Data retention
- Security

## Component Library

### Layout

- `AppShell`
- `Sidebar`
- `Header`
- `PageHeader`
- `PageContainer`
- `Section`
- `SplitLayout`

### Navigation

- `SidebarItem`
- `BotNavItem`
- `Tabs`
- `Breadcrumb`
- `WorkspaceSwitcher`

### Data Display

- `MetricCard`
- `StatusCard`
- `SafetyStatusCard`
- `TrendChart`
- `DataTable`
- `EmptyState`
- `ActivityItem`

### Forms

- `Input`
- `Textarea`
- `Select`
- `Toggle`
- `Checkbox`
- `FormSection`
- `SaveBar`

### Bot Builder

- `BotCard`
- `BotProfileEditor`
- `AgeRangeSelector`
- `TopicRuleCard`
- `SafetyRuleCard`
- `EscalationRuleCard`
- `KnowledgeSourceCard`

### Chat

- `ConversationList`
- `ConversationItem`
- `ChatThread`
- `MessageBubble`
- `TestReplyComposer`
- `SafetyEvaluationPanel`

### Modals

- `CreateBotModal`
- `ConfirmDialog`
- `InviteMemberModal`
- `UploadKnowledgeModal`

## Design Rules

Use these base tokens:

| Token | Value | Usage |
| --- | --- | --- |
| Navy | `#0F172A` | Headings, primary text |
| Blue | `#2563EB` | Primary actions, active state |
| Soft Blue | `#DBEAFE` | Active backgrounds |
| Background | `#F8FAFC` | App background |
| Card | `#FFFFFF` | Cards and panels |
| Border | `#E2E8F0` | Dividers and outlines |

Typography:

- Inter
- Clear hierarchy
- No negative letter spacing
- No viewport-scaled font sizes

Cards:

- One purpose only
- `24px` padding
- `16px` radius
- Subtle border
- No heavy shadows

Buttons:

- Primary blue
- Secondary white
- Ghost minimal

Tabs:

- Underline active state
- No pill-heavy styling

## UX Rules

Every page must answer one question:

```text
What is the adult trying to configure, review, or trust here?
```

Safety controls must be explicit. Avoid vague labels like `Smart Safety` unless the behavior is visible and configurable.

Use direct labels:

- Allowed topics
- Blocked topics
- Escalate to adult
- Require review
- Do not answer
- Ask a parent or teacher

## Iteration Policy

When implementing, work in this order:

1. Build the app shell and navigation.
2. Build the Home and Bots pages.
3. Build the Bot workspace tabs.
4. Build Safety and Bot Builder pages.
5. Build Knowledge and Test Chat pages.
6. Build Conversations and Analytics.
7. Add empty, loading, and error states.
8. Verify responsive behavior.
9. Run build and browser QA.

After each iteration, check:

- What route or component was completed?
- What evidence proves it works?
- What is the next highest-value missing surface?
- Did any layout, accessibility, or design rule regress?

## Blocked Stop Condition

Stop and report if:

- Required product decisions are missing and would materially change the UI
- The app cannot build because of unrelated existing repository issues
- Required package behavior conflicts with the current Next.js version
- Browser verification cannot run
- The UI cannot meet the safety requirements without additional backend state

When blocked, report:

- Completed work
- Evidence gathered
- Exact blocker
- Decision or input needed
- Best next step after unblock

