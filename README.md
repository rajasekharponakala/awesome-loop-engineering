# Awesome Loop Engineering [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

Loop engineering is the practice of designing systems that prompt, check, remember, and
re-run AI coding agents for you, instead of prompting them by hand, turn after turn.

This list covers only that meaning of the term. It does not cover software event loops,
UI or game loops, growth loops, or generic workflow automation.

## Contents

- [Start Here](#start-here)
- [The Lineage](#the-lineage)
- [Papers & Research](#papers--research)
- [Long-form Guides](#long-form-guides)
- [Runtimes & Harnesses](#runtimes--harnesses)
- [Verification & Guardrails](#verification--guardrails)
- [State, Memory & Persistence](#state-memory--persistence)
- [Cost, Observability & Evals](#cost-observability--evals)
- [Patterns & Templates](#patterns--templates)
- [Skeptics, Critiques & Related Lists](#skeptics-critiques--related-lists)

## Start Here

- 📝 [Loop Engineering](https://addyosmani.com/blog/loop-engineering/) — The essay that named the field: five building blocks, mapped onto Claude Code and Codex.
- 📖 [Getting Started with Loops](https://claude.com/blog/getting-started-with-loops) — Official taxonomy of loop types by trigger and stop condition, from turn-based to proactive.
- 📝 [What Is Loop Engineering?](https://www.ibm.com/think/topics/loop-engineering) — Learn the loop lifecycle from trigger to verification to persisted state in plain terms.
- 📝 [The Art of Loop Engineering](https://www.langchain.com/blog/the-art-of-loop-engineering) — Stacks four loops, agent through verification to hill climbing, into one production design.
- 📝 [Stop Prompting. Design the Loop.](https://www.pulumi.com/blog/stop-prompting-design-the-loop/) — Practical breakdown of loop building blocks with tests and builds as verification oracles.
- 📝 [Peter Steinberger on X: "You shouldn't be prompting coding agents anymore"](https://x.com/steipete/status/2063697162748260627) — The two sentences that started the June 2026 shift from prompting agents to designing loops.
- 📝 [Boris Cherny on X: five tips for running Opus autonomously](https://x.com/bcherny/status/2063792263067754658) — Claude Code's creator shares his working recipe: auto mode, /goal, cloud runs, self-verification.
- 🎥 [Boris Cherny: Claude Code & the Future of Engineering (Acquired Unplugged)](https://www.youtube.com/watch?v=RkQQ7WEor7w) — Hear Claude Code's creator explain why engineers build loops instead of writing prompts.

## The Lineage

- 📖 [Building effective agents](https://www.anthropic.com/engineering/building-effective-agents) — Workflows versus agents, and the evaluator-optimizer pattern that loops later formalize.
- 📖 [Effective context engineering for AI agents](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents) — Treat context as runtime state: compaction, just-in-time retrieval, sub-agent isolation.
- 📝 [Context Engineering](https://simonwillison.net/2025/Jun/27/context-engineering/) — Where context engineering came from and what it controls beneath your loop.
- 📖 [Harness engineering for coding agent users](https://martinfowler.com/articles/harness-engineering.html) — Feedforward and feedback: design what surrounds one agent run before designing the loop.
- 📝 [Harness Engineering for Self-Improvement](https://lilianweng.github.io/posts/2026-07-04-harness/) — Why the system around the model, not intelligence alone, decides recursive self-improvement outcomes.
- 📝 [Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/) — Apply OpenAI's harness lessons on legibility, constraints, and feedback loops.
- 📝 [Agent Harness Engineering](https://addyosmani.com/blog/agent-harness-engineering/) — Catalogues harness mechanisms: compaction, planner/generator/evaluator splits, hooks, ratchet rules.
- 📄 [The Prompt Report: A Systematic Survey of Prompt Engineering Techniques](https://arxiv.org/abs/2406.06608) — The prompt-engineering layer made systematic: 58 techniques, shared vocabulary, best practices.

## Papers & Research

- 📄 [Loop Engineering: Building Blocks, Adoption, and Impact](https://arxiv.org/abs/2608.21884) — The first academic survey: what well-engineered loops contain, plus a 36,710-repository adoption study.
- 📄 [Stop Hand-Holding Your Coding Agent: Engineering the Loops that Replace Step-by-Step Prompting](https://arxiv.org/abs/2607.00038) — Formalizes the loop specification: trigger, verification, stopping rule, memory, and a verification ladder.
- 📄 [ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629) — The reason-act-observe cycle every agent loop still descends from.
- 📄 [Reflexion: Language Agents with Verbal Reinforcement Learning](https://arxiv.org/abs/2303.11366) — Turns environment feedback into stored reflections the next attempt reads.
- 📄 [SWE-agent: Agent-Computer Interfaces Enable Automated Software Engineering](https://arxiv.org/abs/2405.15793) — Agent-computer interface design: how tool surfaces shape autonomous software engineering.
- 📄 [Measuring AI Ability to Complete Long Software Tasks](https://arxiv.org/abs/2503.14499) — METR's time horizons: the empirical grounding for loop budgets, checkpoints, and escalation.
- 📄 [Inside the Scaffold: A Source-Code Taxonomy of Coding Agent Architectures](https://arxiv.org/abs/2604.03515) — Dissects 13 open-source coding-agent scaffolds into five composable loop primitives.
- 📄 [The Kitchen Loop: User-Spec-Driven Development for a Self-Evolving Codebase](https://arxiv.org/abs/2603.25697) — Production loop report: 285+ self-correcting iterations and 1,000+ merged PRs behind ground-truth tests.
- 📄 [From Question Answering to Task Completion: A Survey on Agent System and Harness Design](https://arxiv.org/abs/2606.20683) — Survey decomposing the agent harness into six runtime responsibilities, verification included.
- 📄 [A Survey on Evaluation of LLM-based Agents](https://arxiv.org/abs/2503.16416) — How to evaluate trajectories and tool use, not just final answers.

## Long-form Guides

- 📖 [Run long horizon tasks with Codex](https://developers.openai.com/blog/run-long-horizon-tasks-with-codex) — Official runbook for plan-edit-test-observe-repair loops: specs, status logs, validation gates.
- 📖 [Writing Loops, Not Prompts, Explained](https://rico.codes/loops-not-prompts) — Break-even model for when a loop beats prompting, plus stop conditions and evidence collection.
- 📖 [Loop Engineering: Design Coding Agent Loops That Run While You Sleep](https://explainx.ai/blog/loop-engineering-coding-agents-claude-code-guide-2026) — Walks from ReAct and Ralph to /goal and cron, with worked Claude Code examples.
- 📖 [AI Loop Engineering: Build Autonomous Agents with Claude Code /goal + Routines](https://www.sabrina.dev/p/loop-engineering-claude-code-goal-routines) — Five worked loops with verifiable end states; shows why the checker is the hard part.
- 📖 [How I AI: How to Write AI Agent Loops in Claude Code and Codex](https://www.lennysnewsletter.com/p/how-i-ai-how-to-write-ai-agent-loops) — A Mozilla engineer's daily PR-review loop with per-PR subagents, in copyable detail.

## Runtimes & Harnesses

- 📖 [Claude Code Overview](https://code.claude.com/docs/en/overview) — The reference runtime for loop writing: tools, skills, hooks, sessions, and agent surfaces.
- 📖 [Keep Claude working toward a goal](https://code.claude.com/docs/en/goal) — The goal-condition loop: a separate model judges completion after every turn.
- 📖 [Create custom subagents](https://code.claude.com/docs/en/sub-agents) — Isolated context, model choice, and tool permissions: the maker/checker mechanism.
- 📖 [Run prompts on a schedule](https://code.claude.com/docs/en/scheduled-tasks) — Session-scoped /loop plus cloud, desktop, and CI scheduling options, compared.
- 📖 [Scheduled tasks (Codex automations)](https://learn.chatgpt.com/docs/automations) — Codex's scheduled automations: recurring cloud runs that resume prior threads.
- 📝 [Harness Design for Long-Running Application Development](https://www.anthropic.com/engineering/harness-design-long-running-apps) — Maker/checker in practice: planning, generation, and evaluation split so the critic never authors.
- 📝 [Engineering for Agents That Never Sleep](https://nader.substack.com/p/engineering-for-agents-that-never) — Designs triggers, constraints, and quality gates for agents that start themselves.
- 🛠 [Model Context Protocol](https://modelcontextprotocol.io) — Connect your loop to outside tools and data through one open standard.
- 📖 [LangGraph overview](https://docs.langchain.com/oss/python/langgraph) — Orchestration runtime mixing deterministic and agentic steps, with durable execution built in.
- 🛠 [superpowers](https://github.com/obra/superpowers) — Skills framework enforcing TDD, subagent review, and worktrees inside your loop.
- 🛠 [GitHub Agentic Workflows](https://github.github.com/gh-aw/) — Markdown-defined repository automations that run coding agents in Actions, with guardrails.
- 🛠 [OpenClaw](https://github.com/openclaw/openclaw) — Self-host a personal agent runtime by the author who named the trend.

## Verification & Guardrails

- 📄 [Proof-or-Stop: Don't Trust the Agent, Trust the Evidence — Loop Engineering for Verifiable Evidence-Gated Lifecycle Control](https://arxiv.org/abs/2607.14890) — Evidence-gated lifecycle control: zero false-DONE outcomes across ten scenarios and eighteen tampering classes.
- 📄 [SWE-bench: Can Language Models Resolve Real-World GitHub Issues?](https://arxiv.org/abs/2310.06770) — The executable-test benchmark: real GitHub issues resolved under fail-to-pass test gates.
- 📄 [LLMs-as-Judges: A Comprehensive Survey on LLM-based Evaluation Methods](https://arxiv.org/abs/2412.05579) — Maps judge biases like position, verbosity, and self-preference before trusting model-based gates.
- 📝 [Loop Engineering Without Verification Is Just Automation](https://www.sonarsource.com/blog/loop-engineering-without-verification-is-just-automation/) — Two-tier exit gates: LLM judge for intent, deterministic analysis as the hard halt.
- 📝 [Verifying Agentic Development at Scale](https://cognition.com/blog/testing-development) — The verification stack behind majority-async Devin sessions: test plans, reusable skills, video receipts.
- 📝 [Agentic Code Review](https://addyosmani.com/blog/agentic-code-review/) — Review is the bottleneck: risk-tiered verification depth and heterogeneous AI reviewers.
- 📝 [Agentic coding](https://danluu.com/ai-coding/) — Field benchmarks arguing fuzzing and randomized testing, not human review, let agent code ship.
- 📝 [The lethal trifecta for AI agents](https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/) — Security rule for unattended loops: private data, untrusted input, and exfiltration channels never combine.
- 📖 [The Tests-First AI Agent Loop for Autonomous Coding](https://micheallanham.substack.com/p/the-tests-first-ai-agent-loop-for) — Tests as the loop's spine and a diff budget capping what each cycle may touch.
- 📦 [Red/green TDD — Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/red-green-tdd/) — A tight test feedback loop that makes agent progress measurable each cycle.
- 📖 [Automate actions with hooks](https://code.claude.com/docs/en/hooks-guide) — Deterministic lifecycle control: your own scripts gate every model action.
- 📖 [agent-qa coding-agent verification workflow](https://vostride.com/docs/agent-qa/guides/coding-agent-workflow) — Verify app changes through MCP, inspect evidence, repair failures, and rerun.

## State, Memory & Persistence

- 📝 [The spine of the loop](https://markmhendrickson.com/posts/the-spine-of-the-loop/) — Why durable state makes loops work, and what a markdown state file must deliver.
- 📝 [Long-Running Agents](https://addyo.substack.com/p/long-running-agents) — Three walls, finite context, missing state, unreliable self-verification, and the patterns through them.
- 📖 [Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents) — Durable progress artifacts, environment setup, and self-verification across many context windows.
- 📖 [Persistence](https://docs.langchain.com/oss/python/langgraph/persistence) — Checkpoint state at every super-step; resume, replay, and time-travel interrupted runs.
- 📄 [The Log Is the Agent: Event-Sourced Reactive Graphs for Auditable, Forkable Agentic Systems](https://arxiv.org/abs/2605.21997) — Append-only event log as source of truth: deterministic replay, cheap forking, causal lineage.
- 📄 [Filesystem-Based Memory for LLM Agents: Organization, Evolution, and Sustainability](https://arxiv.org/abs/2607.26637) — First systematic study of the markdown-files-on-disk memory pattern loops already run.
- 📄 [Always-On Agents: A Survey of Persistent Memory, State, and Governance in LLM Agents](https://arxiv.org/abs/2606.30306) — Survey of durable state across runs, scored on governance, recovery, and deletion.
- 📝 [Agentics: Memorizing Session Transcripts Isn't Useful](https://12gramsofcarbon.com/p/agentics-memorizing-session-transcripts) — Evidence that loop state belongs in distilled artifacts, not searchable session transcripts.
- 📝 [An open-source spec for Codex orchestration: Symphony](https://openai.com/index/open-source-codex-orchestration-symphony/) — Issue-driven orchestration for Codex fleets that preserves harness context across runs.
- 📝 [Unlocking the Codex harness: how we built the App Server](https://openai.com/index/unlocking-the-codex-harness/) — How Codex preserves threads and agent state across clients, sessions, and restarts.
- 🛠 [kanban-md](https://github.com/antopolskiy/kanban-md) — File-based kanban board giving agent loops a durable, inspectable work queue.

## Cost, Observability & Evals

- 📖 [Demystifying Evals for AI Agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents) — Combine code, model, and human graders; start from production failures, wire into CI.
- 📝 [Better Harness: A Recipe for Harness Hill-Climbing with Evals](https://www.langchain.com/blog/better-harness-a-recipe-for-harness-hill-climbing-with-evals) — Uses evals as the learning signal to hill-climb your harness, not just your prompts.
- 📄 [Token Reduction Is Not Cost Reduction](https://arxiv.org/abs/2607.12161) — Prompt-cache traffic drives most billed cost; optimize success-adjusted spend, not token counts.
- 📄 [Token Budgets: An Empirical Catalog of 63 LLM-Agent Budget-Overrun Incidents](https://arxiv.org/abs/2606.04056) — Documented budget-overrun incidents with an eight-cluster failure taxonomy and mitigations.
- 📄 [LoopsBench: From Harness Engineering to Loop Engineering in Coding Agent Evaluation](https://arxiv.org/abs/2608.00267) — Benchmarks sustained execution: tests release along a dependency frontier as standing regression obligations.
- 📖 [Manage costs effectively](https://code.claude.com/docs/en/costs) — Cap loop spend: organization limits, usage behavior, practical budget controls.
- 📖 [OpenTelemetry Semantic Conventions for Generative AI Systems](https://opentelemetry.io/docs/specs/semconv/gen-ai/) — Portable tracing conventions for model and tool calls across your loop stack.
- 🛠 [LangSmith](https://www.langchain.com/langsmith) — Inspect and grade loop runs across iterations with shared tracing and evals.
- 📦 [Build an Agent Improvement Loop with Traces, Evals, and Codex](https://developers.openai.com/cookbook/examples/agents_sdk/agent_improvement_loop) — Trace runs, convert failures into evals, let Codex patch the harness, remeasure.

## Patterns & Templates

- 📝 [Ralph Wiggum as a software engineer](https://ghuntley.com/ralph/) — The bare while-loop: fresh agent each pass, filesystem and specs as memory.
- 🛠 [ralph-loop-agent](https://github.com/vercel-labs/ralph-loop-agent) — Run Ralph loops with verifier feedback plus iteration, token, and cost limits.
- 📖 [12 Factor Agents](https://github.com/humanlayer/12-factor-agents) — Operating principles for production agents: own your state, pause and resume cleanly.
- 📦 [Agent Loop Hub](https://agentloophub.com) — Copy-paste loops in a seven-field format with measured token cost per cycle.
- 📝 [Unrolling the Codex agent loop](https://openai.com/index/unrolling-the-codex-agent-loop/) — A production loop traced turn by turn: model, tools, context, and approval transitions.

## Skeptics, Critiques & Related Lists

- 📝 [The Coming Loop](https://lucumr.pocoo.org/2026/6/23/the-coming-loop/) — What re-driving agents past their natural stopping points does to code quality and review capacity.
- 📝 [Understanding Is the New Bottleneck](https://www.geoffreylitt.com/2026/07/02/understanding-is-the-new-bottleneck.html) — Comprehension, not verification, is the real ceiling; literate diffs and quizzes as regulators.
- 📄 [(Im)Paired Programming: Coding Agents Improve Productivity but Harm Understanding](https://arxiv.org/abs/2607.26375) — Controlled study: agents raise completion speed while lowering comprehension and independent extension.
- 📄 [Looping Is Not Reliability: State-Bound Evidence and Typed Revision Contracts for Agentic Code Repair](https://arxiv.org/abs/2607.24604) — Shows correctness can drop across revisions: the loop finds a patch, then loses it.
- 📄 [The Illusion of Multi-Agent Advantage](https://arxiv.org/abs/2606.13003) — Auto-generated multi-agent systems underperform self-consistency at up to 10x the cost.
- 📝 [Most Developers Do Not Need Agent Loops Yet](https://alphasignalai.substack.com/p/most-developers-do-not-need-agent) — A readiness check: adopt loops only when task, signal, and economics justify them.
- 📝 [Why Software Factories Fail (or: Harness Engineering Is Not Enough)](https://github.com/humanlayer/advanced-context-engineering-for-coding-agents/blob/main/wsff.md) — RL rewards passing tests with no penalty for eroding maintainability; human judgment gates the fix.
- 📝 [Loop engineering, latest AI buzzword, still needs humans in the loop](https://www.theregister.com/ai-and-ml/2026/06/24/loop-engineering-latest-ai-buzzword-still-needs-humans-in-the-loop/5261735) — Collects the founding quotes and the token-bill incentives underneath the trend.
- 📝 [Why Agent Loops Fail in Production (and the Database Patterns That Fix Them)](https://www.cockroachlabs.com/blog/agent-loops-production-database-patterns/) — Diagnoses production loop failures; ties reliability to database-level safeguards.
- 📚 [invincible04/awesome-loop-engineering](https://github.com/invincible04/awesome-loop-engineering) — Learn loops by doing: chapters, copy-paste prompts, portable skill, runnable Python example.
- 📚 [ChaoYue0307/awesome-loop-engineering](https://github.com/ChaoYue0307/awesome-loop-engineering) — Dataset-scale reference: 1,025 resources, 22 patterns, schema-checked contracts, runtime starters.
- 📚 [rudy2steiner/awesome-agent-loops](https://github.com/rudy2steiner/awesome-agent-loops) — Broad loop-engineering list: patterns, runtimes, templates; updates itself via agent loop.
- 📚 [snwfdhmp/awesome-ralph](https://github.com/snwfdhmp/awesome-ralph) — Find Ralph implementations, playbooks, and community channels to copy working loops.
- 📚 [Awesome Context Engineering](https://github.com/Meirtz/Awesome-Context-Engineering) — Borrow context-engineering tactics that keep your loops supplied with the right context.
- 📚 [A Coding-Agent Reading List: Behind the Loops](https://insights.ml4trading.io/p/a-coding-agent-reading-list-behind) — 60+ sources organized by evidence type, from practitioner discourse to control theory.
