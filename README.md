# elysium-atlas-app

**Elysium Atlas** frontend — build chat agents on your own data, manage knowledge bases, tools, and plugins, and deploy an embeddable visitor widget. Teams, leads, live sessions, and human handover are managed from the dashboard.

Part of [ElysiumForge Labs](https://github.com/ElysiumForge-Labs). Companion backend: [elysium-atlas-backend](https://github.com/ElysiumForge-Labs/elysium-atlas-backend).

> **Independent research repository.** Not affiliated with, endorsed by, or sponsored by Kinetiq or Hyperliquid. Point the app at a trusted Atlas API. Never commit secrets.

## Features

| Area | Routes / capabilities |
| --- | --- |
| Auth | Login, verify, forgot / reset password |
| Agents | List, build, per-agent settings (`my-agents`) |
| Knowledge | Team knowledge library and agent attachments |
| Tools & plugins | Custom HTTP tools and sandboxed Python plugins |
| Chat | Chat-with-agent and live visitor sessions |
| Leads | Captured lead tables |
| Team | Members, invites, account settings |
| Dashboard | Session and message performance charts |
| Widget | Embeddable visitor chat widget |

Frontend integration guides live under `documentation/` (auth, agents, KB, tools, plugins, handover, leads, Socket.IO).

## Stack

| Layer | Technology |
| --- | --- |
| Framework | Next.js (App Router), TypeScript |
| UI | React, Tailwind, Radix / shadcn-style components |
| State | Redux Toolkit (`src/store`) |
| HTTP | Axios |
| Version | `0.1.71` |

## Getting started

### Prerequisites

- Node.js 20+
- npm
- A running [elysium-atlas-backend](https://github.com/ElysiumForge-Labs/elysium-atlas-backend) instance

### Install and run

```bash
npm install
npm run dev      # http://127.0.0.1:3000
npm run build
npm run lint
```

Configure the Atlas API base URL for your deployment environment. API paths typically use `/elysium-atlas` and `/elysium-agents` prefixes as documented in `documentation/`.

## Layout

| Path | Role |
| --- | --- |
| `src/` | App Router pages, components, store, API clients |
| `public/` | Static assets and widget embeds |
| `documentation/` | Frontend integration guides |
| `components.json` | shadcn-style component config |

## Security

- Use HTTPS and trusted origins for production embeds.
- Keep auth cookies and API tokens out of client logs.
- Align CORS and Socket.IO origins with the companion backend settings.
