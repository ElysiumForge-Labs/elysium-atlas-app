# elysium-atlas-app

**Elysium Atlas** frontend — build chat agents on your own data, manage knowledge bases, tools, and plugins, and deploy an embeddable visitor widget. Teams, leads, live sessions, and human handover settings are managed from the dashboard.

Part of [ElysiumForge Labs](https://github.com/ElysiumForge-Labs). Companion backend: [elysium-atlas-backend](https://github.com/ElysiumForge-Labs/elysium-atlas-backend).

> **Independent research repository.** Not affiliated with, endorsed by, or sponsored by Kinetiq or Hyperliquid. Point the app at a trusted Atlas API; never commit secrets.

## Overview

| Area | Routes / features |
| --- | --- |
| Auth | Login, verify, forgot / reset password |
| Agents | List, build, per-agent settings (`my-agents`) |
| Knowledge | Team knowledge library and agent attachments |
| Tools & plugins | Custom HTTP tools and sandboxed Python plugins |
| Chat | Chat-with-agent and live visitor sessions |
| Leads | Captured lead tables |
| Team | Members, invites, account settings |
| Dashboard | Session / message performance charts |

Frontend integration guides live under `documentation/` (auth, agents, KB, tools, plugins, handover, leads, Socket.IO).

## Stack

| Layer | Technology |
| --- | --- |
| Framework | Next.js (App Router), TypeScript |
| UI | React, Tailwind, shadcn-style components |
| State | Redux store under `src/store` |

## Development

```bash
npm install
npm run dev
npm run build
npm run lint
```

Configure the Atlas API base URL per your deployment environment. API paths typically use `/elysium-atlas` and `/elysium-agents` prefixes as documented in `documentation/`.
