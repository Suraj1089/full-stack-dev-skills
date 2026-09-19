# Django Best Practices Skill

An AI agent skill for Django, Django REST Framework, WebSockets (Channels), and asynchronous code.

Use this skill in an AI-agent workspace such as Claude Code, Cursor, Copilot, or Windsurf. It covers architecture, N+1 queries, security, and database performance.

---

## What it does

The rules give an AI agent a current baseline for Django code and call out advice that often leads to slow or unsafe applications.

It helps agents avoid:
- **Performance bottlenecks:** Unpaginated querysets, missing `select_related`/`prefetch_related`, loading millions of rows into RAM.
- **Architectural Mistakes:** Overloaded views, using plain classes when service layer functions are better, putting deep validation logic in generic views instead of DRF serializers.
- **Security Flaws:** Auto-incrementing primary IDs in web URLs (IDOR attacks), misconfigured CSRF/XSS strategies, hardcoding `SECRET_KEY` inside `settings.py`.
- **Concurrency issues:** Failing to use Database Row Locks (`select_for_update`) during queue polling or financial data mutations.

---

## Internal Structure

The rules are split into focused files in the `rules/` directory so an agent can load only the relevant material.

- `rules/admin.md`: Django admin optimizations (`autocomplete_fields`).
- `rules/architecture.md`: Services Layer, Data Selectors, DRY principles.
- `rules/async-and-tasks.md`: Handling Celery edge cases and async views.
- `rules/caching.md`: Guarding against cache stampedes.
- `rules/channels.md`: Safe Redis usage, ASGI auth.
- `rules/database-locks.md`: Stopping race conditions using Postgres/MySQL row locks.
- `rules/logging.md`: Enforcing standard JSON logging over `print()`.
- `rules/migrations.md`: Zero-downtime database changes.
- `rules/models.md`: Modernized `Meta.indexes`, database constraints, and Fat Models.
- `rules/orm-advanced.md`: Explicit database annotations and using `bulk_create`.
- `rules/orm-queries.md`: Fixing N+1 queries.
- `rules/security.md`: Hardening servers against IDOR and enumerations.
- `rules/signals.md`: Why you should avoid implicit signals for business logic.
- `rules/testing.md`: Enforcing PyTest over unittest, asserting query counts, and using factory_boy.
- `rules/views-and-apis.md`: Separating FBVs from CBVs and optimizing DRF endpoints.

---

## Usage & Setup

1. Copy this skill directory into your agent workspace.
2. If your agent has a skill registry, register `SKILL.md` there.
3. Use `AGENTS.md` when the agent needs all rules in one file.

These rules help agents produce Django code with fewer performance, correctness, and security mistakes.
