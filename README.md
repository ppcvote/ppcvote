## MinYi Xie

I build open-source AI security tools. One-person operation, 4 AI agents, 5 products in production.

### AI Security & Standards

**[AI Application Security Standard (AASS)](https://github.com/ppcvote/avs-standard)** — Open standard for evaluating AI security, visibility, and data protection. Three dimensions, one score.

**[prompt-defense-audit](https://github.com/ppcvote/prompt-defense-audit)** — LLM system prompt defense scanner. 12 attack vectors, pure regex, < 5ms. `npx prompt-defense-audit "Your prompt"`

**[UltraProbe](https://ultralab.tw/en/probe)** — AI Visibility Scanner. SEO + AEO + Agent Accessibility. 92 checks, deterministic, zero cost.

### Research

**Prompt Defense Posture Study** — 1,646 production system prompts scanned from 4 public datasets
- Scanner v1.1.0: LLM-calibrated regex patterns, 69.6% agreement with gpt-4o-mini (up from 51.8%)
- 97.5% lack multi-language defense, 94.6% lack input validation, 84.8% lack harmful content prevention
- Sources: ChatGPT, Claude, Grok, Perplexity, Cursor, v0, Copilot, 1,300+ GPT Store custom GPTs

**AI Visibility Score Validation** — [DOI: 10.5281/zenodo.19410475](https://doi.org/10.5281/zenodo.19410475)
- 155 queries, 816 AI citations, 721 URLs scanned for SEO + AEO
- Median AVS of AI-cited sites: 77/100 (Grade B)

### Contributing To

| Project | What | Status |
|---------|------|--------|
| **[NVIDIA/garak](https://github.com/NVIDIA/garak/pull/1669)** | 6 defense posture patterns (CP-1001 — CP-1006) | PR open |
| **[Anthropic Cookbook](https://github.com/anthropics/claude-cookbooks/pull/502)** | Prompt defense audit recipe | PR open |
| **[Microsoft Agent Governance](https://github.com/microsoft/agent-governance-toolkit/issues/821)** | Pre-deployment prompt audit | Issue open |
| **[Microsoft Presidio](https://github.com/microsoft/presidio/issues/1933)** | PII prompt defense audit | Issue open |
| **[NVIDIA/NeMo-Guardrails](https://github.com/NVIDIA-NeMo/Guardrails/issues/1764)** | System prompt defense guardrail | Issue open |
| **[Cisco AI Defense](https://github.com/cisco-ai-defense/skill-scanner/issues/81)** | Prompt defense rule pack | Issue open |
| **[OWASP LLM Top 10](https://github.com/OWASP/www-project-top-10-for-large-language-model-applications/pull/816)** | Tool reference | PR open |

### Open Source

| Repo | What |
|------|------|
| [avs-standard](https://github.com/ppcvote/avs-standard) | AASS + AVS spec, validation paper, dataset (CC BY 4.0) |
| [prompt-defense-audit](https://github.com/ppcvote/prompt-defense-audit) | Prompt defense scanner — 12 vectors, CLI + library (MIT) |
| [ultralab-scanners](https://github.com/ppcvote/ultralab-scanners) | SEO + AEO + AAO scanners — zero deps, TypeScript (MIT) |
| [openclaw-claude-proxy](https://github.com/ppcvote/openclaw-claude-proxy) | Claude Opus Telegram bot via OpenClaw |
| [discord-lobster](https://github.com/ppcvote/discord-lobster) | Discord AI community manager |

### Products (Ultra Lab)

| Product | What |
|---------|------|
| **UltraProbe** | AI Visibility Scanner — [ultralab.tw/en/probe](https://ultralab.tw/en/probe) |
| **MindThread** | Threads automation — 27 accounts, 3.3M views |
| **Agent Fleet** | 4 autonomous agents, 105 daily tasks |
| **Ultra Advisor** | Financial planning SaaS — 18 visualization tools |

### Stack

`TypeScript` `React` `Vite` `Tailwind` `Firebase` `Vercel` `Gemini` `Claude` `Ollama`

### Contact

minyi@ultralab.tw — [ultralab.tw](https://ultralab.tw/en/) — [Discord](https://discord.gg/ewS4rWXvWk)
