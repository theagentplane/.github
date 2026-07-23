<div align="center">
  <a href="https://theagentplane.github.io">
    <img src="https://theagentplane.github.io/assets/logo-mark.png" alt="AgentPlane" width="72" />
  </a>

  <h2>AgentPlane</h2>
  <p><strong>The layer AI agents need underneath them.</strong></p>

  <p>
    <a href="https://www.youtube.com/watch?v=Lc8zRh9muoY">
      <img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="YouTube" />
    </a>
    &nbsp;
    <a href="https://www.linkedin.com/in/susheemkoul/">
      <img src="https://img.shields.io/badge/Susheem-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="Susheem on LinkedIn" />
    </a>
    &nbsp;
    <a href="https://in.linkedin.com/in/tisha-chawla">
      <img src="https://img.shields.io/badge/Tisha-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="Tisha on LinkedIn" />
    </a>
    &nbsp;
    <a href="https://theagentplane.github.io">
      <img src="https://img.shields.io/badge/theagentplane.github.io-111111?style=for-the-badge&logoColor=white" alt="Website" />
    </a>
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

<a href="https://github.com/theagentplane/chronicle">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api/pin/?username=theagentplane&repo=chronicle&theme=dark&hide_border=true&bg_color=0d1117" />
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=theagentplane&repo=chronicle&hide_border=true" />
  </picture>
</a>
&nbsp;
<a href="https://github.com/theagentplane/tokenops">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api/pin/?username=theagentplane&repo=tokenops&theme=dark&hide_border=true&bg_color=0d1117" />
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=theagentplane&repo=tokenops&hide_border=true" />
  </picture>
</a>

<br /><br />

**[Chronicle](https://github.com/theagentplane/chronicle)** &nbsp;`pip install agent-chronicle`

Record-and-replay for agent decision graphs. Chronicle instruments every LLM call, tool call, and routing decision as an immutable Envelope. When something breaks in production, that incident becomes a committed regression test — replayable without a single live model call.

**[TokenOps](https://github.com/theagentplane/tokenops)** &nbsp;`pip install agent-tokenops`

Run-aware token governance for multi-agent systems. A shared ledger and control plane enforce spend policies across every agent, model call, and tool hop in a workflow — before the next LLM call executes, not after.

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
