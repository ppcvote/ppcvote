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

I build tools that protect AI systems from prompt injection attacks. **15 PRs merged across seven organizations**: Microsoft, NVIDIA, Cisco, NIST, OWASP, the UK AI Security Institute, and the Casualty Actuarial Society.

Before this I spent ten years as a financial adviser (MDRT), which is why the actuarial and finance rows below exist: I read insurance code as a practitioner, not a tourist. I run **[Ultra Lab](https://ultralab.tw/en)**, an AI products company in Taiwan.

My niche is unglamorous: I develop on Windows with a Traditional Chinese (cp950) locale, an environment almost no OSS contributor uses. Bugs that are invisible on Linux CI live there for years. Most of the merges below started that way.

---

### Open Source Contributions

Every row links to the merged work; verify any of it with `gh pr list --author ppcvote --state merged`.

| Organization | Merged | What |
|:------------|:------:|:-----|
| **Microsoft** · [PyRIT](https://github.com/microsoft/PyRIT/pulls?q=is%3Apr+author%3Appcvote+is%3Amerged) / [agent-governance-toolkit](https://github.com/microsoft/agent-governance-toolkit/pulls?q=is%3Apr+author%3Appcvote+is%3Amerged) | 5 | OWASP LLM02 output-scorer pack; PromptDefenseEvaluator |
| **OWASP** · [regression harness](https://github.com/OWASP/Agent-Security-Regression-Harness/pulls?q=is%3Apr+author%3Appcvote+is%3Amerged) / [AI testing guide](https://github.com/OWASP/www-project-ai-testing-guide/pulls?q=is%3Apr+author%3Appcvote+is%3Amerged) | 3 | Agent-security scenarios; testing-guide mapping |
| **NVIDIA** · [SkillSpector](https://github.com/NVIDIA/SkillSpector/pulls?q=is%3Apr+author%3Appcvote+is%3Amerged) | 2 | Windows silent file-skip race; LP3 remediation guidance |
| **UK AI Security Institute** · [inspect_evals](https://github.com/UKGovernmentBEIS/inspect_evals/pulls?q=is%3Apr+author%3Appcvote+is%3Amerged) / [inspect_k8s_sandbox](https://github.com/UKGovernmentBEIS/inspect_k8s_sandbox/pulls?q=is%3Apr+author%3Appcvote+is%3Amerged) | 2 | Eval config migration; K8sError diagnostics |
| **Casualty Actuarial Society** · [chainladder-python](https://github.com/casact/chainladder-python/pulls?q=is%3Apr+author%3Appcvote+is%3Amerged) | 1 | Quarterly/semiannual premium on-leveling crash |
| **Cisco AI Defense** · [mcp-scanner](https://github.com/cisco-ai-defense/mcp-scanner/pulls?q=is%3Apr+author%3Appcvote+is%3Amerged) | 1 | PromptDefenseAnalyzer prompt hardening |
| **NIST** · [dioptra](https://github.com/usnistgov/dioptra/pulls?q=is%3Apr+author%3Appcvote+is%3Amerged) | 1 | Task-plugin path convention docs |

In review: [NASA](https://github.com/nasa/hds-core/pull/185) (forced-colors focus ring) · [MITRE](https://github.com/mitre-attack/mitreattack-python/pull/246) (UTF-8 changelog) · [CERT/CC](https://github.com/CERTCC/SSVC/pull/1225) (approved) · [FINOS](https://github.com/finos/git-proxy/pull/1676) (gitleaks range corruption on Windows) · [De Nederlandsche Bank](https://github.com/DeNederlandscheBank/name_matching/pull/52) (input-frame mutation) · [OpenSSF](https://github.com/ossf/cve-bin-tool/pull/5872) (17/18 language checkers dead on Windows)

### Tools

<table>
  <tr>
    <td width="33%" valign="top">
      <h4><a href="https://github.com/ppcvote/prompt-defense-audit">prompt-defense-audit</a></h4>
      <p>Pre-deploy scanner — checks system prompts for missing defenses. 17 attack vectors, SARIF 2.1.0 output.</p>
      <code>npx prompt-defense-audit "Your prompt"</code>
      <br><br>
      <img src="https://img.shields.io/badge/tests-196-brightgreen?style=flat" alt="tests">
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
  <a href="https://ultralab.tw/en">Website</a> · <a href="https://ultralab.tw/en/blog">Blog</a> · <a href="https://discord.gg/ewS4rWXvWk">Discord</a>
</p>
