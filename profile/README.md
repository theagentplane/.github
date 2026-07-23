<div align="center">

# AgentPlane

**The layer AI agents need underneath them.**

</div>

---

Frameworks move fast. Agents are being deployed into production before the infrastructure to operate them exists. The industry spent decades building primitives for reliable services — observability, cost governance, regression testing, reproducibility. The agentic stack is starting from zero.

We're building that layer. Open source, in the open, shipped as we learn.

---

## The problem space

Running a production AI agent means operating something you can't fully inspect, can't deterministically reproduce, and can't account for by request. The failure modes don't have names yet:

- A production agent fails mid-run. The prompt, state, and tool chain that caused it are gone.
- A multi-agent workflow burns 10× its token budget because each agent caps spend locally.
- You ship a fix for a regression — but without a committed test, nothing stops it from coming back silently.

Monitoring and cost tooling built for stateless services don't transfer. Testing frameworks built for deterministic code break on probabilistic outputs. Something purpose-built is needed.

---

## What we've built

### [Chronicle](https://github.com/theagentplane/chronicle) &nbsp;·&nbsp; `pip install agent-chronicle`

**Record-and-replay for agent decision graphs.**

Chronicle captures every LLM call, tool call, and routing decision as an immutable Envelope. When something breaks in production, you extract the incident as a committed fixture and replay it — deterministically, without a single live model call.

The target is one specific, real problem: control-flow and tool-safety regressions that are invisible until they happen in prod and impossible to reproduce after.

```
record → envelope → committed fixture → cut-point replay → pytest
```

### [TokenOps](https://github.com/theagentplane/tokenops) &nbsp;·&nbsp; `pip install agent-tokenops`

**Run-aware token governance for multi-agent systems.**

TokenOps governs the *run*, not the request. A shared ledger and control plane enforce spend policies across every agent, model call, and tool hop in a workflow — before the next LLM call executes, not after.

One `run_id`. One budget. In-path enforcement: HALT · MUTATE · INJECT.

```
register run → shared ledger → pre-call detect/decide/apply → governed workflow
```

Chronicle and TokenOps are designed to work together: Chronicle records decision boundaries; TokenOps attaches as the cost and governance observer on live crossings.

---

## What comes next

Chronicle and TokenOps solve two problems we hit first. The agentic stack has more:

- **Memory** that doesn't hallucinate past state and survives context windows
- **Evaluation** frameworks built for behavior, not output strings
- **Retrieval** that gives agents accurate, scalable perception of large codebases and corpora
- **Observability** at the workflow level, not the request level

We're building in that direction and publishing the thinking as we go.

---

## Writing & talks

We document what we learn from building in this space:

| | |
|---|---|
| [Your Agent Failed in Prod](https://www.youtube.com/watch?v=Lc8zRh9muoY) · Video | Why replayability beats bitwise determinism; Chronicle walkthrough |
| [Your Agent Failed in Prod](https://dev.to/tisha/your-agent-failed-in-prod-good-luck-reproducing-it-56ci) · Article | The full written version: nondeterminism, reproducibility, and what record-and-replay actually gives you |
| [From Validating Code to Evaluating Behavior](https://susheemk.substack.com/p/from-validating-code-to-evaluating) | Why traditional testing assumptions break for agentic systems |
| [Why Agents Forget](https://dev.to/tisha/why-agents-forget-5b46) | How memory works in AI agents, and what it will take to make them learn |
| [Beyond Prompt Caching](https://susheemk.substack.com/p/beyond-prompt-caching-architecting) | AST-aware indexing, multi-modal search, and codebase perception for coding agents |
| [Spec-Driven Development](https://dev.to/tisha/spec-driven-development-when-structure-helps-and-when-it-becomes-tax-1f66) | When structure helps and when it becomes tax: token economics and SDD for AI agents |

All writing and talks → [theagentplane.github.io/media](https://theagentplane.github.io/media.html)

---

## Built by

[Susheem Koul](https://github.com/susheem-k) and [Tisha Chawla](https://github.com/tishachawla-jg) — software engineers building agent infrastructure in the open.

[theagentplane.github.io](https://theagentplane.github.io) &nbsp;·&nbsp; MIT licensed &nbsp;·&nbsp; Issues and PRs welcome
