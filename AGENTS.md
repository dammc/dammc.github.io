# Repository guidance

This repository is for a personal technical and analytical blog published with GitHub Pages. Keep the platform static-first, lightweight, portable, and easy for one person to maintain.

- Inspect the existing architecture, conventions, and build commands before changing them. Do not assume a framework or static-site generator.
- Prefer the smallest coherent, reversible change. Avoid speculative abstractions, unrelated refactors, and dependencies without a concrete benefit.
- Preserve GitHub Pages compatibility, reproducible builds, and a simple local-development path.
- Treat content as primary: favor original, restrained, typography-led design, generous whitespace, readable line lengths, and excellent long-form reading. External sites may inspire principles, never copied layouts, CSS, or distinctive visual elements.
- Build accessible, responsive, semantic pages with keyboard usability, visible focus, sufficient contrast, meaningful structure and alternative text, and reduced-motion handling where relevant.
- Prefer static HTML, minimal CSS and JavaScript, progressive enhancement, optimized assets, and no tracking, analytics, or web fonts by default.
- Keep blog infrastructure separate from substantive article content. Tiny rendering fixtures are acceptable when technically necessary; do not author real posts unless explicitly asked.
- Preserve the ability to support technical Markdown, code, mathematics, figures, charts, tables, citations, footnotes, captions, links, and optional taxonomy without implementing features prematurely.
- Validate changes in proportion to risk using the repository's documented checks. Include build behavior plus relevant accessibility, responsive, link/route/asset, and performance checks; review the final diff before reporting completion.

Complexity must earn its place. Do not add features merely because a chosen tool makes them easy.
