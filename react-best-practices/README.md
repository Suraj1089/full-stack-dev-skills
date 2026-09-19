# React Best Practices (Agent Skill)

An agent skill that gives AI coding assistants practical React and Next.js guidance.

When an agent writes, refactors, or reviews React code, this skill checks for stale closures, missing keys, wasted renders, and barrel-file bloat.

## What it covers

The rules cover 12 common problem areas:

1. **Closures & Stale State** - cached callbacks that silently freeze old values
2. **Reconciliation & Keys** - React reusing the wrong component instances
3. **Server Components & RSC** - data fetching without shipping code to the client
4. **Re-render Causes** - why your tree keeps rendering when nothing changed
5. **Composition & Context** - solving performance problems with component structure, not memoization
6. **Suspense & Streaming** - loading states that don't block the whole page
7. **Bundle Optimization** - lazy loading and tree-shaking mistakes
8. **Concurrent Features** - `useTransition` and `useDeferredValue` for responsive UIs
9. **Memoization Usage** - when `React.memo` helps vs. when it's a waste
10. **Refs & Imperative APIs** - DOM access without fighting the framework
11. **DOM Sync & Effects** - `useLayoutEffect` vs `useEffect` and SSR gotchas
12. **Rendering Performance** - virtualization and avoiding unnecessary DOM depth

## Project structure

- `SKILL.md` - The activation manifest and workflow
- `AGENTS.md` - All rules in one file
- `rules/` - One file per topic, with the problem, a wrong example, and a corrected example
- `react-best-practices.skill` - Packaged archive of everything above

## Quality scoring

The skill uses four dimensions that help registries and agents find and apply it:

- **Discovery** - File globs (`**/*.jsx`, etc.) and trigger phrases tell agents exactly when to load this skill
- **Implementation** - A workflow with specific failure modes to scan for
- **Structure** - Standard frontmatter, clear sections, and a `tool-wrapper` design pattern
- **Expertise** - Concrete traps such as stale closures, reconciliation bugs, and waterfall fetching
