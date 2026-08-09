# dammc.github.io

This repository is intended to become a minimalist personal technical and analytical blog published with GitHub Pages. At present it contains only the project-scoped Codex agentic development environment. The blog application, visual design, content system, framework, deployment, and articles have deliberately not been implemented yet.

## What this setup does

The Codex environment gives future development sessions a small set of persistent project principles, a repeatable blog-development workflow, three specialized agents, conservative command safeguards, and a place for lifecycle hooks if a real need emerges.

```text
User request
    │
    ├── AGENTS.md: durable rules applied to every repository task
    │
    └── blog-development skill: task workflow
            │
            ├── blog_architect: read-only investigation and recommendations
            ├── blog_implementer: scoped workspace changes
            └── blog_reviewer: read-only findings and validation gaps
                    │
                    └── primary Codex agent integrates results and reports

Command execution remains governed by the active sandbox and approval policy,
with additional prompts for selected remote Git/GitHub mutations.
```

The primary Codex session remains responsible for understanding the request, deciding whether delegation adds value, integrating agent results, validating the final state, and communicating with the user. The custom agents are focused helpers, not an autonomous hierarchy.

## Repository structure

| File | Responsibility |
| --- | --- |
| [`AGENTS.md`](AGENTS.md) | Durable repository-wide engineering and design guidance that Codex loads for every task. |
| [`.agents/skills/blog-development/SKILL.md`](.agents/skills/blog-development/SKILL.md) | Repeatable workflow for architecture, implementation, testing, review, and maintenance of the blog platform. |
| [`.codex/config.toml`](.codex/config.toml) | Minimal project configuration for multi-agent behavior and concurrency. |
| [`.codex/agents/blog_architect.toml`](.codex/agents/blog_architect.toml) | Read-only architecture and research specialist. |
| [`.codex/agents/blog_implementer.toml`](.codex/agents/blog_implementer.toml) | Main code-writing specialist for clearly scoped platform work. |
| [`.codex/agents/blog_reviewer.toml`](.codex/agents/blog_reviewer.toml) | Read-only reviewer for material risks and validation gaps. |
| [`.codex/hooks.json`](.codex/hooks.json) | Valid lifecycle-hook configuration with no active handlers. |
| [`.codex/rules/default.rules`](.codex/rules/default.rules) | Experimental command-execution rules for consequential remote mutations. |

## Quick start in VS Code

1. Open the repository root in VS Code and start a new Codex chat from this workspace.
2. Trust the repository if Codex asks. Project-local `.codex` configuration, hooks, and rules are ignored for untrusted projects.
3. Describe the desired outcome and constraints. Codex loads the root `AGENTS.md` automatically.
4. For blog-platform work, explicitly invoke `$blog-development` or use a request that clearly matches its description. In Codex CLI or the IDE extension, `/skills` can be used to inspect available skills.
5. Ask for a specialized agent when it would be useful, or allow the skill workflow to recommend one. The primary session should delegate only bounded work that benefits from specialization.
6. Review requested command approvals carefully. Agent instructions never replace the active sandbox, approval policy, or the user's judgment.

After changing `AGENTS.md`, agent files, project configuration, hooks, or rules, begin a new Codex session so all startup configuration is reloaded. Skill changes are normally detected automatically; restart Codex if an updated skill does not appear.

## How to use the development workflow

The `blog-development` skill is intended for platform work such as choosing an architecture, building or changing layouts, modifying rendering behavior, improving accessibility or performance, adding technical-writing support, testing, and maintenance. It is not intended to generate substantive blog articles.

The workflow asks Codex to:

1. Inspect the repository and preserve existing work.
2. Clarify the requested result and keep platform development separate from article authorship.
3. Investigate architectural uncertainty only when necessary.
4. Choose the simplest viable approach without assuming a framework.
5. Implement the smallest coherent change.
6. Preserve an original, restrained, content-first visual direction.
7. Validate build behavior, responsiveness, accessibility, routes, assets, and performance as relevant.
8. Obtain a focused review for non-trivial changes.
9. Report changes, checks, tradeoffs, and anything that remains unverified.

The skill discourages speculative abstractions, unrelated redesigns, unnecessary JavaScript, bloated CSS frameworks, unjustified dependencies, premature optimization, and features added only because a framework exposes them.

### Example prompts

Architecture investigation:

```text
$blog-development Evaluate the simplest architecture for this blog. Use
blog_architect to compare viable options against the current repository and
GitHub Pages constraints. Return a recommendation and tradeoffs, but do not
implement anything yet.
```

Scoped implementation after an architecture has been selected:

```text
$blog-development Implement the agreed home-page structure. Use
blog_implementer for the scoped changes, validate the existing build and
responsive behavior, and leave article content untouched.
```

Independent review:

```text
Have blog_reviewer review the current diff. Prioritize correctness, GitHub
Pages compatibility, accessibility, broken routes or assets, responsive
behavior, performance, and unnecessary complexity. Do not edit files.
```

Small changes do not require delegation. For a narrow documentation correction or obvious local fix, the primary Codex agent can follow the repository guidance and skill directly.

## Custom agents

### `blog_architect`

Use this agent when a task depends on understanding repository structure, evaluating a static-site approach, checking framework or GitHub Pages constraints, or considering a dependency or build-system decision.

It defaults to a read-only sandbox and must not implement changes. Its recommendations should remain framework-neutral until repository evidence and requirements justify a choice. It weights GitHub Pages compatibility, complexity, technical-content support, maintainability, dependency count, performance, customization, and long-term stability.

Expected output: a concise evidence-based recommendation, relevant file and primary-documentation references, explicit assumptions, and meaningful tradeoffs.

### `blog_implementer`

Use this agent after the outcome is clear and any necessary architectural decision has been made. It has workspace-write access because it is the designated implementation role.

It should produce the smallest defensible diff; favor semantic HTML, accessible behavior, responsive layouts, lightweight CSS, minimal JavaScript, and progressive enhancement; preserve GitHub Pages compatibility; and avoid unrelated refactors. It may not publish, deploy, push, change remote repository state, or author substantive articles.

Expected output: scoped file changes, proportionate validation, a reviewed diff, and a report of checks and unresolved tradeoffs.

### `blog_reviewer`

Use this agent after a non-trivial implementation or whenever an independent review is requested. It defaults to a read-only sandbox and must report findings rather than fix them.

It reviews correctness, links, routes, assets, build and GitHub Pages compatibility, regression risk, unnecessary dependencies or complexity, accessibility, semantics, keyboard and focus behavior, responsive behavior, typography, long-form readability, performance, maintainability, platform/content separation, and evidence of copied external design elements.

Expected output: material findings ordered by severity with precise file locations and remediation advice, followed by important validation gaps. It should explicitly say when it finds no material issues.

## Persistent project guidance

`AGENTS.md` is the always-on policy layer. It establishes that the eventual site should be static-first, lightweight, accessible, responsive, typography-led, original, and maintainable by one person. It also requires agents to inspect the existing architecture before changing it, justify dependencies, keep changes small and reversible, validate in proportion to risk, and keep platform engineering separate from article content.

Keep this file concise. Put durable principles in `AGENTS.md`, repeatable task steps in the skill, and role-specific behavior in agent TOML files. One-off task requirements belong in the current prompt rather than in persistent configuration.

## Configuration and concurrency

The project configuration enables multi-agent tools and permits at most three concurrently open subagent threads, excluding the primary thread:

```toml
[agents]
enabled = true
max_concurrent_threads_per_session = 3
```

Three is enough to make the project agents available without encouraging unnecessary parallelism. No model or reasoning level is pinned, so each custom agent inherits the parent session's model defaults and remains portable as model availability changes.

Agent sandbox values are role defaults. The active Codex session's permission mode and runtime overrides still govern what can actually run, and commands that require additional authority may still prompt or fail.

## Hooks

`hooks.json` intentionally contains an empty `hooks` object. Hooks are best reserved for deterministic lifecycle automation that provides concrete value, such as a necessary mechanical safeguard that ordinary instructions cannot reliably express.

There are currently no hook scripts, logging, analytics, generated summaries, session-memory automation, or commands that run after every tool call. Add an active hook only when the repository has a demonstrated requirement, then document its trigger, command, runtime cost, trust implications, and failure behavior here.

## Command safety rules

The rules file adds approval prompts for these command prefixes:

- `git push`
- `gh repo archive`, `delete`, `edit`, or `rename`
- `gh pr close`, `merge`, or `reopen`

These operations modify remote state and therefore require explicit approval. Read-only commands such as `git status`, `gh repo view`, and `gh pr checks` are not broadly allowlisted; they continue through the normal Codex sandbox and approval policy.

Rules are prefix-based execution controls, not coding standards and not a complete security boundary. They do not replace repository permissions, branch protection, GitHub authentication controls, the sandbox, or careful approval review. The `.rules` mechanism is experimental, so keep this file small and retest it after significant Codex upgrades.

Test the rules without executing the target command:

```bash
codex execpolicy check --pretty \
  --rules .codex/rules/default.rules \
  -- git push origin main
```

The expected decision is `prompt`. A negative test such as the following should report no matching project rule:

```bash
codex execpolicy check --pretty \
  --rules .codex/rules/default.rules \
  -- gh pr view 12
```

## Maintenance guide

When the project evolves, change the narrowest appropriate layer:

- Update `AGENTS.md` for durable principles that should apply to nearly every task.
- Update `SKILL.md` when the repeatable development workflow changes.
- Update an agent TOML file when only that role's behavior or sandbox default changes.
- Update `config.toml` only for shared Codex runtime behavior that materially benefits the repository.
- Add a hook only for justified deterministic lifecycle automation.
- Add a rule only for a narrowly matchable command whose outside-sandbox execution needs an explicit decision.

When adding or renaming an agent, keep the filename aligned with its `name`, provide `name`, `description`, and `developer_instructions`, and update every skill or README reference. Prefer inheriting the parent model unless a stable, measured reason justifies pinning one.

After configuration changes:

1. Parse TOML and JSON or start Codex and check for configuration warnings.
2. Run `codex execpolicy check` for matching and non-matching rule examples.
3. Confirm every agent referenced by the skill exists and has the expected sandbox.
4. Check that no absolute machine paths, secrets, credentials, or user-specific settings entered the repository.
5. Start a fresh Codex session and confirm the instructions, skill, and agents are discoverable.

## Troubleshooting

### Project configuration is not loading

Confirm that VS Code opened the Git repository, that Codex is running with this repository as its workspace, and that the project is trusted. Start a new chat after changing project configuration.

### The skill is missing

Confirm that the file is at `.agents/skills/blog-development/SKILL.md` and that its frontmatter still contains `name` and `description`. Codex normally detects skill changes automatically; restart it if the skill list is stale.

### A custom agent is not selected

Name it explicitly in the request, for example, “Use `blog_architect` to investigate this decision.” Confirm that its TOML file exists under `.codex/agents/` and that the `name` matches references in the skill.

### A command rule behaves unexpectedly

Use `codex execpolicy check` with the exact argument sequence Codex intends to run. Prefix rules match command arguments from the beginning, and the strictest matching rule wins. Keep `match` and `not_match` examples in the rule file synchronized with intended behavior.

## Scope boundary

The next development phase may evaluate and choose an architecture, then implement the blog. Until that work is explicitly requested, this repository's Codex environment does not choose among plain HTML/CSS, Jekyll, Hugo, Eleventy, Astro, or another generator; install dependencies; add deployment; create visual assets; or author articles.

Tiny fixture content may be created later when necessary to test rendering, but agents should not generate substantive sociology, economics, software-development, data-science, or technology-and-society posts unless explicitly asked.

## Official Codex documentation

- [Custom instructions with `AGENTS.md`](https://learn.chatgpt.com/docs/agent-configuration/agents-md)
- [Build skills](https://learn.chatgpt.com/docs/build-skills)
- [Subagents and custom agents](https://learn.chatgpt.com/docs/agent-configuration/subagents)
- [Project configuration](https://learn.chatgpt.com/docs/config-file/config-basic)
- [Hooks](https://learn.chatgpt.com/docs/hooks)
- [Command rules](https://learn.chatgpt.com/docs/agent-configuration/rules)
