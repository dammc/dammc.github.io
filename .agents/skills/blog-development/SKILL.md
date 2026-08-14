---
name: blog-development
description: Develop, modify, test, or review this GitHub Pages blog platform. Use for architecture choices, implementation work, design-system changes, rendering behavior, accessibility, performance, and maintenance; do not use for authoring substantive articles.
---

# Blog development workflow

Use this workflow for changes to the blog platform.

1. Inspect the repository, active instructions, current architecture, existing conventions, and available build/test commands. Preserve useful work already present.
2. Restate the requested outcome and boundaries. Distinguish platform work from article authorship; use only tiny fixture content when rendering tests genuinely require it.
3. Decide whether the change needs architectural investigation. For framework, GitHub Pages, build, or dependency uncertainty, delegate a bounded read-only investigation to `blog_architect` when agent delegation is available and worthwhile. Do not research settled facts again.
4. Form the simplest viable approach. Keep the project framework-neutral until evidence justifies a choice, weighting GitHub Pages compatibility, low complexity, technical-content support, maintainability, few dependencies, performance, customization, and stability.
5. For a clearly scoped implementation, use `blog_implementer` when delegation materially helps; otherwise implement directly. Make the smallest coherent change and leave unrelated areas alone.
6. Preserve a restrained, original, content-first identity: strong typography, sensible measure, clear hierarchy, whitespace, readable code and tables, accessible links, and mobile readability. Do not copy an inspiration site's layout, CSS, or distinctive elements.
7. Validate the relevant build and behavior. Check responsive layouts, semantic structure, keyboard/focus behavior, contrast and motion where applicable, routes/links/assets, and performance costs. Use the project's existing commands; do not install tools just to expand validation.
8. For non-trivial or user-requested review, ask `blog_reviewer` for a read-only, findings-first review when delegation is available and useful. Resolve material findings, then inspect the complete diff yourself.
9. Report the outcome, validation performed, and any remaining tradeoffs or unverified behavior.

Avoid speculative abstractions, unrelated redesigns, unnecessary client-side JavaScript, bloated CSS frameworks, unjustified dependencies, premature optimization, and features added only because a framework exposes them. Prefer static output and progressive enhancement. Do not select or replace a framework without evidence from the repository and task.
