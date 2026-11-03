# Cloud Migration AI Repo

GitLab Duo agents, flows, prompts and rules for a multi-application cloud migration. One folder per asset; every asset is built to run in **GitLab Duo** (AI Catalog / Duo Chat).

## Catalog

| Asset | Type | Migration phase | Status | What it does |
|---|---|---|---|---|
| [confluence-app-extractor](agents/confluence-app-extractor/) | Agent | Discover & assess | Draft v0.1 | Fills the application template page from existing Confluence pages, with citations |

## Layout

```
.
├── agents/<agent-name>/     # agent.md (AI Catalog fields + system prompt + evals), prompt.md, README.md
├── flows/<flow-name>/       # multi-step flows (YAML) + README
├── prompts/<category>/      # copy-paste Duo Chat prompts
├── rules/                   # AGENTS.md / Duo rule templates to copy into app repos
├── confluence/              # Confluence page drafts (playbooks, guides)
└── ide/                     # shared IDE config (mcp.json for Confluence Cloud)
```

## Adding a new asset

1. Create `agents/<kebab-case-name>/` (or `flows/...`, `prompts/...`).
2. Include `README.md`, `agent.md` (purpose, AI Catalog fields, system prompt, guardrails, evals) and `prompt.md`.
3. Add a row to the **Catalog** table above.
4. Run the evals before sharing with the team.
