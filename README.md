<h1 align="center">MinYi Xie</h1>

<p align="center">
  <strong>AI Security Researcher · Open Source Contributor · Taiwan</strong>
</p>

<p align="center">
  <a href="https://www.npmjs.com/package/prompt-defense-audit"><img src="https://img.shields.io/npm/v/prompt-defense-audit?style=flat&label=prompt-defense-audit&color=8A5CFF" alt="npm"></a>
  <a href="https://www.npmjs.com/package/@ppcvote/prompt-shield"><img src="https://img.shields.io/npm/v/@ppcvote/prompt-shield?style=flat&label=prompt-shield&color=CE4DFF" alt="npm"></a>
  <a href="https://github.com/marketplace/actions/prompt-defense-audit"><img src="https://img.shields.io/badge/GitHub_Action-Marketplace-purple?style=flat&logo=github" alt="Action"></a>
  <a href="https://github.com/ppcvote/prompt-defense-audit/actions"><img src="https://github.com/ppcvote/prompt-defense-audit/actions/workflows/ci.yml/badge.svg" alt="CI"></a>
</p>

---

I build tools that protect AI systems from prompt injection attacks. My code is merged into Cisco and Microsoft's open-source security projects.

I run **[Ultra Lab](https://ultralab.tw/en)** — an AI product company with 4 autonomous agents handling content, security scans, and community management.

---

### Open Source Contributions

| Organization | Contribution | Status |
|:------------|:-------------|:------:|
| **Cisco AI Defense** · [mcp-scanner](https://github.com/cisco-ai-defense/mcp-scanner) | PromptDefenseAnalyzer — 12-vector prompt hardening | ✅ Merged |
| **Microsoft** · [agent-governance-toolkit](https://github.com/microsoft/agent-governance-toolkit/pull/854) | PromptDefenseEvaluator — 63 tests, mypy strict, zero deps | ✅ Merged |
| **NVIDIA** · [garak](https://github.com/NVIDIA/garak/issues/1666) | Defense posture probes — methodology discussion | 💬 Active |
| **OWASP** · [LLM Top 10](https://github.com/OWASP/www-project-top-10-for-large-language-model-applications/pull/816) | Red Team Handbook tool listing | 📝 Open |

### Tools

<table>
  <tr>
    <td width="33%" valign="top">
      <h4><a href="https://github.com/ppcvote/prompt-defense-audit">prompt-defense-audit</a></h4>
      <p>Pre-deploy scanner — checks system prompts for missing defenses. 12 attack vectors.</p>
      <code>npx prompt-defense-audit "Your prompt"</code>
      <br><br>
      <img src="https://img.shields.io/badge/tests-84-brightgreen?style=flat" alt="tests">
      <img src="https://img.shields.io/badge/coverage-100%25-brightgreen?style=flat" alt="coverage">
    </td>
    <td width="33%" valign="top">
      <h4><a href="https://github.com/ppcvote/prompt-shield">prompt-shield</a></h4>
      <p>Runtime scanner — blocks injection attacks before they reach your LLM. 8 attack types.</p>
      <code>npm i @ppcvote/prompt-shield</code>
      <br><br>
      <img src="https://img.shields.io/badge/tests-108-brightgreen?style=flat" alt="tests">
      <img src="https://img.shields.io/badge/< 1ms-per_scan-brightgreen?style=flat" alt="speed">
    </td>
    <td width="33%" valign="top">
      <h4><a href="https://github.com/ppcvote/prompt-defense-audit-action">GitHub Action</a></h4>
      <p>CI/CD gate — auto-scans prompt files on every PR. Posts results table.</p>
<pre>- uses: ppcvote/prompt-defense-audit-action@v1</pre>
    </td>
  </tr>
</table>

```
Pre-deploy                    →  CI/CD                →  Runtime
prompt-defense-audit             GitHub Action            prompt-shield
"Does your prompt have           "Block weak prompts      "Is this user input
 defenses?"                       before merge"            an attack?"
```

### Research

Scanned **1,646 production system prompts** from ChatGPT, Claude, Grok, Copilot, and 1,300+ GPT Store apps:

| Finding | Rate |
|:--------|-----:|
| No indirect injection defense | 97.8% |
| No role boundary enforcement | 92.4% |
| No output control | 88.3% |
| Overall grade F (score < 45) | 78.3% |
| Average defense score | 36/100 |

Data: [gap-20260405.json](https://github.com/ppcvote/prompt-defense-audit/blob/master/research/gap-20260405.json) · Paper: [DOI 10.5281/zenodo.19410475](https://doi.org/10.5281/zenodo.19410475)

---

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=ppcvote&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&hide_title=true" height="150" alt="stats">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=ppcvote&layout=compact&theme=tokyonight&hide_border=true&hide_title=true&langs_count=6" height="150" alt="languages">
</p>

<p align="center">
  <a href="https://ultralab.tw/en">Website</a> · <a href="https://ultralab.tw/en/blog">Blog</a> · <a href="https://discord.gg/ewS4rWXvWk">Discord (270+ members)</a>
</p>
