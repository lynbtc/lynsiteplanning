# CLAUDE.md — LYN Site Planning Tool

## What this is
The site planning configurator for LYN's sauna project. Lives at siteplanning.lyn.page. Evaluates M4 thermal module feasibility per site based on thermal demand, electricity cost, and climate.

LYN is jsb's operating firm. Bitcoin-native. The sauna project is LYN's first venture — 2,100 numbered outdoor units + bespoke indoor installations.

## Deployment — CRITICAL
This repo auto-deploys to Netlify on push to main. **This is a live production site.**

### Rules
1. **Claude Code never pushes or commits.** Only make local file changes.
2. jsb reviews changes locally, commits and pushes to main himself.
3. If unsure about a change, **ask before editing.**

## Stack
- Pure HTML / CSS / JS
- No frameworks, no build tools, no dependencies
- Google Fonts loaded via CDN (IBM Plex Sans, IBM Plex Mono, Inter)
- Netlify hosting

## Design system
- **Body text:** IBM Plex Sans 300
- **Labels/mono:** IBM Plex Mono 400
- **Logo/nav:** Inter 600
- **Background:** #fafafa
- **Layout:** Minimal. No cards, no boxes. Whitespace over borders. Lowercase labels.

## Copy and code philosophy
Every word earns its place. Every line of code earns its place. If it doesn't add value, cut it.

### Copy
- Factual. No sell lines. No filler.
- The live lyn.page is the tone reference — match it.
- Lowercase on labels.

### Code
- Open-source clean. Readable, minimal.
- HTML should read like a document. Semantic, obvious structure.
- CSS: as few rules as needed. Whitespace does most of the work.
- JS: only when static HTML can't do it.

## M4 thermal module context
- **Optional.** Not in every unit. Configured per site.
- At a LYN site, M4 IS the heating system. Electricity = heating cost. Bitcoin = upside.
- Positioning: "hard asset for your savings" (NOT "bitcoin for your savings").
- Commercial = "revenue for the project". Private = "hard asset for your savings".

## Key user flows
1. User selects private or professional
2. Selects outdoor or indoor
3. Configures site constraints (crane, power, foundation)
4. Selects modules
5. M4 thermal step — skip or add
6. Summary with configuration and pricing
7. Request site review (Netlify Forms submission)

## Nav pattern
Contextual nav shared across lyn.page ecosystem. No border on `.nav-menu`. Uses `.nav-group` class for grouped `<ul>` lists (margin-separated, no dividers). Trigger is en dash `–`. Links use clean URLs (e.g. `https://lyn.page/sauna`, no `.html`).

Siteplanning nav groups:
1. Site pages: sauna, product sheet, documents
2. Contextual actions: download pdf (`window.print()`), email (`mailto:julius@lyn.page`)
3. Theme toggle (`.nav-muted` class)

## Working conventions
- Show proposed text copy before implementing in code.
- Deliver code changes as specific edits, not full file rewrites.
- Don't rewrite files unnecessarily. Minimal diffs.
