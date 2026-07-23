<div align="center">
  <a href="https://theagentplane.github.io">
    <img src="https://theagentplane.github.io/assets/logo-mark.png" alt="AgentPlane" width="72" />
  </a>

  <h2>AgentPlane</h2>
  <p><strong>The layer AI agents need underneath them.</strong></p>

  <p>
    <a href="https://www.youtube.com/watch?v=Lc8zRh9muoY"><img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&amp;logo=youtube&amp;logoColor=white" alt="YouTube" /></a><a href="https://www.linkedin.com/in/susheemkoul/"><img src="https://img.shields.io/badge/Susheem-0A66C2?style=for-the-badge&amp;logo=linkedin&amp;logoColor=white" alt="Susheem on LinkedIn" /></a><a href="https://in.linkedin.com/in/tisha-chawla"><img src="https://img.shields.io/badge/Tisha-0A66C2?style=for-the-badge&amp;logo=linkedin&amp;logoColor=white" alt="Tisha on LinkedIn" /></a><a href="https://theagentplane.github.io"><img src="https://img.shields.io/badge/theagentplane.github.io-111111?style=for-the-badge&amp;logo=github&amp;logoColor=white" alt="Website" /></a>
  </p>
</div>

---

Frameworks move fast. Agents are going to production before the infrastructure to operate them exists. The industry spent decades building reliability primitives for services — observability, cost governance, regression testing. For the agentic stack, that work is just beginning.

**We build that layer. Open source, shipped in the open as we learn.**

---

## 🔍 The problem

A production agent fails mid-run. The prompt, state, and tool chain that caused it are gone.

A multi-agent workflow burns 10× its token budget because each agent caps spend locally.

You ship a fix for a regression — but without a committed test, nothing stops it from coming back silently.

Monitoring built for stateless services doesn't transfer. Testing frameworks built for deterministic code break on probabilistic outputs. Something purpose-built for agents is needed.

---

## 📦 Projects

### [chronicle](https://github.com/theagentplane/chronicle) &nbsp; [![Stars](https://img.shields.io/github/stars/theagentplane/chronicle?style=flat-square&color=gold)](https://github.com/theagentplane/chronicle/stargazers) [![PyPI](https://img.shields.io/pypi/v/agent-chronicle?style=flat-square)](https://pypi.org/project/agent-chronicle/)

**Record-and-replay for agent decision graphs.** &nbsp; `pip install agent-chronicle`

Chronicle instruments every LLM call, tool call, and routing decision as an immutable Envelope. When something breaks in production, that incident becomes a committed regression test — replayable without a single live model call.

### [tokenops](https://github.com/theagentplane/tokenops) &nbsp; [![Stars](https://img.shields.io/github/stars/theagentplane/tokenops?style=flat-square&color=gold)](https://github.com/theagentplane/tokenops/stargazers) [![PyPI](https://img.shields.io/pypi/v/agent-tokenops?style=flat-square)](https://pypi.org/project/agent-tokenops/)

**Run-aware token governance for multi-agent systems.** &nbsp; `pip install agent-tokenops`

TokenOps governs the *run*, not the request. A shared ledger and control plane enforce spend policies across every agent, model call, and tool hop in a workflow — before the next LLM call executes, not after.

> Chronicle and TokenOps compose: Chronicle records decision boundaries; TokenOps attaches as the cost and governance observer on live crossings.

---

## 🔭 What comes next

Chronicle and TokenOps solve two problems we hit first. The agentic stack needs more:

- **Memory** that doesn't hallucinate past state and survives context windows
- **Evaluation** built for behavior, not output strings
- **Retrieval** that gives agents accurate, scalable perception of large codebases
- **Observability** at the workflow level, not the request level

We're building in that direction and publishing the thinking as we go.

---

## 📝 Writing & talks

| | |
|---|---|
| 🎥 [Your Agent Failed in Prod](https://www.youtube.com/watch?v=Lc8zRh9muoY) | Why replayability beats bitwise determinism — Chronicle walkthrough |
| ✍️ [Your Agent Failed in Prod](https://dev.to/tisha/your-agent-failed-in-prod-good-luck-reproducing-it-56ci) | The nondeterminism problem and what record-and-replay actually gives you |
| ✍️ [From Validating Code to Evaluating Behavior](https://susheemk.substack.com/p/from-validating-code-to-evaluating) | Why traditional testing assumptions break for agentic systems |
| ✍️ [Why Agents Forget](https://dev.to/tisha/why-agents-forget-5b46) | How memory works in AI agents, and what it takes to make them learn |
| ✍️ [Beyond Prompt Caching](https://susheemk.substack.com/p/beyond-prompt-caching-architecting) | AST-aware indexing, multi-modal search, and codebase perception for coding agents |
| ✍️ [Spec-Driven Development](https://dev.to/tisha/spec-driven-development-when-structure-helps-and-when-it-becomes-tax-1f66) | Token economics and when structure helps vs. becomes tax for AI agents |

All writing and talks → [theagentplane.github.io/media](https://theagentplane.github.io/media.html)

---

<div align="center">
  Built by <a href="https://github.com/susheem-k">Susheem Koul</a> and <a href="https://github.com/tishachawla-jg">Tisha Chawla</a>
  &nbsp;·&nbsp; MIT licensed &nbsp;·&nbsp; Python 3.10+
  <br /><br />
  Issues and PRs welcome on any of our repos.
</div>
