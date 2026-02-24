# QuantBitRealm

> AI-powered multi-agent development studio — autonomous agents that code, build bots, create content, and manage clients.

## Overview

QuantBitRealm is a self-running AI development studio built on **OpenClaw** and powered by **Kimi K2.5**. Five specialized agents work together via Discord, each handling a different part of the business — from finding freelance work to delivering finished projects.

## Architecture

```
                    QuantBitRealm Discord Server
                    ============================
                    
  #admin          #coding-tasks    #bot-workshop    #content-lab    #client-intake
     |                 |                |                |                |
  Admin            Dev Coder       Bot Builder     Content Creator  Client Manager
  Orchestrator                                                      
     |                 |                |                |                |
     +------------ OpenClaw Gateway (localhost:18789) -------------------+
                           |
                      Kimi K2.5 (Moonshot AI)
```

## Agents

| Agent | Channel | Heartbeat | Purpose |
|-------|---------|-----------|---------|
| **Admin Orchestrator** | #admin | 6h | Finds bounties, coordinates agents, tracks revenue |
| **Dev Coder** | #coding-tasks | 24h | Takes freelance coding jobs, builds full-stack projects |
| **Bot Builder** | #bot-workshop | — | Creates Discord & Telegram bots for sale |
| **Content Creator** | #content-lab | 12h | Writes blog posts, tweets, YouTube scripts |
| **Client Manager** | #client-intake | 24h | Handles client communication & proposals |

## Tech Stack

- **Agent Framework**: OpenClaw v2026.2
- **LLM**: Kimi K2.5 by Moonshot AI (Agent Swarm capable)
- **Communication**: Discord (guild channels + DM pairing)
- **Inter-Agent**: sessions_spawn / sessions_send (ping-pong, max 5 turns)

## Getting Started

1. Install OpenClaw: `npm i -g openclaw`
2. Copy `openclaw.json` to `~/.openclaw/openclaw.json`
3. Set your Discord bot token and Moonshot API key
4. Run: `openclaw gateway`
5. DM the bot in Discord to pair your account

## Status

- [x] OpenClaw gateway configured and running
- [x] 5 agents with workspace files (SOUL.md, AGENTS.md, USER.md, TOOLS.md, HEARTBEAT.md)
- [x] Discord bot online in QuantBitRealm server
- [x] Channel routing via root-level bindings
- [x] Inter-agent communication enabled
- [ ] First revenue milestone

## License

MIT

---

*Built by [quantbitrealmSimon](https://github.com/quantbitrealmSimon) — "Let the machines work while you sleep."*
