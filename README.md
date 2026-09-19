# Full Stack Dev Skills

A collection of practical AI agent skills and development guidance for common full-stack work.

Each module gives an AI coding assistant focused rules for a particular part of the stack.

## 🛠️ Available Skills

### 🐍 [Django Best Practices](./django-best-practices/)
Django and Django REST API guidance covering:
- Advanced ORM usage, QuerySet optimisations, and Database Locks
- Architectural patterns (services, selectors)
- Security, Caching, and Asynchronous tasks (Celery/Channels)
- View structure, Serializers, and Testing methodologies

### ⚛️ [React Best Practices](./react-best-practices/)
React and frontend guidance covering:
- React 19 patterns (Server Components, Suspense, Actions, Transitions)
- Idiomatic component design and decoupling state securely
- Strict typing (TypeScript) boundaries and performance optimisations
- Forms, Fetching architectures, and accessibility considerations

### 🕵️ [Change Critic](./change-critic/)
A review skill for analysing code changes, testing assumptions, and checking diffs before deployment.

### 🎨 [AI Slop Remover](./ai-slop-remover/)
A design critique and refinement skill for removing generic AI-generated patterns from websites, product interfaces, dashboards, and marketing visuals while preserving intentional product-specific design.

## 🚀 How to Use

Each directory is a self-contained skill module with its own `SKILL.md` or `README.md`. Import a module into the agent framework you use, such as OpenClaw, Cursor, or Vercel v0.

1. Navigate into any specific skill directory (e.g., `react-best-practices/`).
2. Read the `SKILL.md` for specific AI prompts and configuration steps.
3. Import the system descriptions or rules into your agent's custom instructions / context window.
