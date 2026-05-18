# Design System

## Visual Direction

The interface is light, premium, minimal, and operational. It should feel calm under pressure and designed for repeated daily use.

Reference qualities:

- Stripe clarity
- Linear hierarchy
- Vercel restraint

## Color Tokens

| Token | Value | Usage |
| --- | --- | --- |
| `--color-navy` | `#0F172A` | Primary text, headings |
| `--color-blue` | `#2563EB` | Primary actions, active indicators |
| `--color-soft-blue` | `#DBEAFE` | Active backgrounds, subtle highlights |
| `--color-background` | `#F8FAFC` | App background |
| `--color-card` | `#FFFFFF` | Cards and panels |
| `--color-border` | `#E2E8F0` | Borders and dividers |

No purple.

## Semantic Colors

| Status | Color Intent |
| --- | --- |
| Success | Green |
| Warning | Amber |
| Error | Red |
| Neutral | Slate |
| Active | Blue |

Semantic colors should be used sparingly and never dominate the screen.

## Typography

Font: Inter.

Rules:

- Use navy for primary text.
- Use slate for secondary text.
- Do not use negative letter spacing.
- Do not scale font size with viewport width.
- Use compact headings inside cards and panels.

## Spacing

Base spacing unit: `4px`.

Recommended page spacing:

- Desktop page padding: `32px`
- Tablet page padding: `24px`
- Mobile page padding: `16px`
- Section gap: `24px`
- Card padding: `24px`

## Cards

Cards have:

- One purpose only
- `24px` padding
- `16px` radius
- `1px` subtle border
- No heavy shadow

Do not place cards inside cards.

## Buttons

Button styles:

- Primary: blue background, white text
- Secondary: white background, border
- Ghost: transparent, minimal hover

Use icons for compact tool actions where a familiar symbol exists.

## Tabs

Tabs use:

- Underline active state
- Navy active label
- Slate inactive labels
- No pill-heavy styling

## Charts

Charts are functional, not decorative.

Rules:

- Maximum one main chart per page
- Simple blue line by default
- Minimal grid
- No gradient fills unless needed for readability
- Avoid chart legends when labels can be direct

## Density

This is an operational SaaS product. Use whitespace for hierarchy, not emptiness. Avoid marketing-style hero composition inside the app.

