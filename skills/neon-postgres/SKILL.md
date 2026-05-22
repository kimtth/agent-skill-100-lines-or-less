---
name: neon-postgres
description: "Use when: set up, connect, branch, pool, scale, or troubleshoot Neon Serverless Postgres."
---

Goal: help users make Neon Postgres work with current docs and minimal guesswork.

Use for:
- Neon project setup and connection strings
- serverless driver, pooled connections, ORMs, and framework integration
- branching, instant restore, read replicas, autoscaling, and scale-to-zero
- Neon Auth, CLI, MCP, REST API, TypeScript SDK, or Python SDK questions

Docs first:
- index: `https://neon.com/docs/llms.txt`
- markdown page: append `.md` to a Neon docs URL
- prefer current docs over memory for API names and limits

Workflow:
1. Identify language, framework, runtime, ORM, and deployment target.
2. Fetch the relevant Neon docs page when behavior may have changed.
3. Choose direct, pooled, serverless, or CLI/API path based on runtime.
4. Show exact environment variables and connection handling.
5. Verify with a simple query, migration, or branch operation.

Common checks:
- `DATABASE_URL` scope and pooling mode
- serverless runtime compatibility
- SSL requirements
- branch and endpoint names
- connection limits and cold-start behavior

Rules:
- do not print credentials
- do not guess docs URLs; use `llms.txt`
- separate Neon platform behavior from generic Postgres behavior
