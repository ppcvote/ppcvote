## Hey, I'm MinYi

Insurance advisor turned AI builder. Based in Taiwan.

4 months ago I couldn't write a line of code. I started building with Claude, broke things constantly, and somehow ended up contributing to Microsoft and OWASP. Still figuring things out tbh, but shipping every day.

I run [Ultra Lab](https://ultralab.tw/en) — a one-person AI company with 4 agents doing most of the work while I sleep.

---

### Things I've built

- **[prompt-defense-audit](https://github.com/ppcvote/prompt-defense-audit)** — scans LLM system prompts for missing defenses. 12 attack vectors, pure regex, < 5ms. `npx prompt-defense-audit "your prompt"`
- **[UltraProbe](https://ultralab.tw/en/probe)** — AI visibility scanner (SEO + AEO + agent accessibility)
- **[openclaw-claude-proxy](https://github.com/ppcvote/openclaw-claude-proxy)** — run Opus 4.6 on Telegram via Claude Max
- **[discord-lobster](https://github.com/ppcvote/discord-lobster)** — AI community manager bot, $0/month to run

### PRs out in the wild

| Where | What | Status |
|-------|------|--------|
| [Microsoft / agent-governance-toolkit](https://github.com/microsoft/agent-governance-toolkit/pull/854) | PromptDefenseEvaluator (1,110 lines, 58 tests) | Under review |
| [OWASP / LLM Top 10](https://github.com/OWASP/www-project-top-10-for-large-language-model-applications/pull/816) | Red Team Handbook tool listing | Open |
| [Anthropic / claude-cookbooks](https://github.com/anthropics/claude-cookbooks/pull/502) | Prompt defense audit recipe | Open |
| [NVIDIA / garak](https://github.com/NVIDIA/garak/pull/1669) | Defense posture patterns | Closed |

### Research stuff

Scanned **1,646 production system prompts** from ChatGPT, Claude, Grok, Copilot, and 1,300+ GPT Store apps. The short version: most AI apps have basically zero defense. [Full write-up here.](https://ultralab.tw/en/blog/ai-prompt-defense-study-1646/)

Also made an open standard for AI visibility scoring (AVS) — it has a [DOI](https://doi.org/10.5281/zenodo.19410475) and everything, which felt very official for someone who learned what DOI means like 2 months ago.

---

I write about all of this on my [blog](https://ultralab.tw/en/blog) and hang out with ~270 people on [Discord](https://discord.gg/ewS4rWXvWk). If you're into AI security or building solo, come say hi.
