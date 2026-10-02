# PROJECT REGISTRY AUDIT — 2026-10-02

**Repository:** `botbikamordehai2-sketch/memory-for-all`  
**Purpose:** non-destructive project-memory audit and gap report.  
**Mode:** READ/AUDIT + documentation only. No workflow execution, Publish, deployment, external write, or APPROVED status mutation.

## 1. Audit scope

This audit checked:
- the current `memory-for-all` repository tree;
- the imported `github-sync/` governance snapshot;
- `github-sync/PROJECT_INDEX.md`, `REPOSITORIES.md`, `PLATFORM_MAP.md`, `STATUS.md`;
- the current GitHub connector repository inventory (100 repositories returned by the installed account scope);
- explicit repository searches for current project names including memory, GitHub sync, Shopify, Trinity, MCP, Slack, Forex, SEO, content and agents;
- the current CONCERT2 architecture memory already stored in `inbox/CONCERT2_4_WORKFLOW_ARCHITECTURE.md`.

## 2. Important finding

The old `github-sync/PROJECT_INDEX.md` is dated **2026-09-13** and is no longer complete enough to be the only current project registry.

Do **not** delete it. Treat it as an imported historical baseline until a canonical replacement is approved.

## 3. Verified/current project families

### Governance / shared memory
- **memory-for-all** — verified GitHub repository; unified team-memory/governance repository.
- **github-sync** — verified GitHub repository; imported snapshot also exists under `memory-for-all/github-sync/`.
- **Sync-GitHub-** — separate private repository found; do not silently merge with `github-sync` without review.
- **Multi-Agent Coordination** — documented inside the imported governance snapshot.

### CONCERT2 / research orchestration
- **CONCERT2** — current project memory exists in `inbox/CONCERT2_4_WORKFLOW_ARCHITECTURE.md`.
- Four n8n workflow domains are documented:
  - Shopify / Site Maintenance
  - Forex Research
  - Social Media
  - Blog / SEO
- Shared architecture: Models → MCP → Tools/Apps/Sources, with n8n orchestration and HOLD/HITL/Audit.

### Shopify / commerce
- **shopify-store** — verified public GitHub repository.
- **ai-commerce** — repository present; relationship to Shopify project must be reviewed before merging identities.
- **mega-store** — private repository; repository presence verified.
- **dropship-machine** — private repository; repository presence verified.
- **ebay-scorecard** — private repository; repository presence verified.
- **publify** — repository present; project role needs validation.

### Forex / trading research
- **commotiai-forex** — verified GitHub repository found by explicit search.
- **trinity-trading** — private repository.
- **trading-system** — repository present.
- **signalforge** — private repository.
- **smc-authority** — repository present.
- **ai-wealth-engine-** — repository present.
- **-prop-trade-hacks** — repository present but empty/near-empty inventory status should be reviewed.
- **Scout-FX** — known project/workstream from project memory; no dedicated repo was verified in this audit. Keep RESEARCH_ONLY.
- **FX Strength / Hermes local work** — historical project documentation exists, but the current GitHub repo mapping needs re-verification before canonical status changes.

### Content / SEO / social
- **content-engine** — private GitHub repository exists. Do not automatically equate it with the old deprecated “Content Engine (DeepSeek)” record; identity needs review.
- **signalforge-seo** — private repository.
- **signalforge-outreach** — private repository.
- **--ict-blog--** — repository present.
- **Blog / SEO** — active CONCERT2 workflow domain.
- **Social Content** — active CONCERT2 workflow domain.

### Trinity / MCP / model infrastructure
- **trinity-core** — private repository.
- **trinity-os-core** — public repository.
- **trinity-trading** — private repository.
- **trinity-slack-gateway** — private repository found by explicit search.
- **ocean-quartz-crane-clear-MCP** — private verified repository.
- **Trinity MCP course implementation / trinity-queue** — current project/workstream documented in learning/project memory; repository identity is not assumed unless explicitly mapped.
- **trinity-funnel** — archived repository.

### Agents / jobs / automation
- **JOB-SCOUT-AGENT** — private GitHub repository now exists. This corrects the old registry statement that it was “not a repo”.
- **job-agent-dashboard** — private repository.
- **octocode-bot** — private repository.
- **commoti-os** — public repository; description identifies a local-first project cockpit with built-in AI agents.
- **Morning Brief (Dana)** — documented historical active agent; dedicated repository not verified in this audit.

### Cyber / security
- **bug-bounty-lab** — private repository.
- **security-scanner-** — repository present.

### Design / bridge
- **Figma Bridge / trinity-figma-bridge** — known project/workstream from prior project records, but no repository with exact `trinity-figma-bridge` name was found in explicit GitHub search. Keep as **NEEDS_REPO_VALIDATION**, not missing/deleted.

## 4. Standard command model already agreed

For project families that have an approved command pair in current project memory:

| Project | Shared memory command | n8n/task command |
|---|---|---|
| CONCERT2 | `PROJECT_SYNC: CONCERT2` | `TASK: CONCERT2_RUN` |
| Shopify | `PROJECT_SYNC: SHOPIFY` | `TASK: SITE_MAINTENANCE` |
| Scout-FX / Forex | `PROJECT_SYNC: SCOUT_FX` | `TASK: FOREX_RESEARCH` |
| Social Content | `PROJECT_SYNC: SOCIAL_CONTENT` | `TASK: SOCIAL_CONTENT` |
| Blog / SEO | `PROJECT_SYNC: BLOG_SEO` | `TASK: BLOG_RESEARCH` |
| memory-for-all | `PROJECT_SYNC: MEMORY_FOR_ALL` | `TASK: MEMORY_SYNC` |
| Trinity / MCP | `PROJECT_SYNC: TRINITY_MCP` | `TASK: MCP_CHECK` |
| Slack Gateway | `PROJECT_SYNC: SLACK_GATEWAY` | `TASK: SLACK_GATEWAY_CHECK` |
| Job Scout | `PROJECT_SYNC: JOB_SCOUT` | `TASK: JOB_SCOUT_SCAN` |

Newly discovered repositories are **not** automatically assigned commands. Their project identity must be confirmed first.

## 5. Duplicates / identity conflicts requiring review

Do not merge or delete automatically:
- `memory-for-all` vs `github-sync` vs `Sync-GitHub-`
- `content-engine` vs historical “Content Engine (DeepSeek)”
- `shopify-store` vs `ai-commerce` vs `mega-store` vs `dropship-machine`
- `trinity-core` vs `trinity-os-core` vs `trinity-trading`
- `signalforge` vs `signalforge-seo` vs `signalforge-outreach` vs `signalforge-debug`
- `commotiai-forex` vs Scout-FX vs historical FX Strength/Hermes records

## 6. Installed GitHub repository inventory

The connected GitHub installation returned the following **100 repositories**. Presence here means “repository accessible to the connector”; it does **not** automatically mean “active project”.

- `ai-wealth-engine-` — public
- `smc-authority` — public
- `-prop-trade-hacks` — public
- `trading-system` — public
- `--ict-blog--` — public
- `publify` — public
- `ai-commerce` — public
- `project-6a3ebdcd-15ff-47e1-8c1` — public
- `botbikamordehaik2-sketch-commotai` — public
- `security-scanner-` — public
- `signalforge` — private
- `commoti-os` — public
- `JOB-SCOUT-AGENT` — private
- `trinity-trading` — private
- `content-engine` — private
- `ebay-scorecard` — private
- `mega-store` — private
- `octocode-bot` — private
- `bug-bounty-lab` — private
- `trinity-core` — private
- `signalforge-outreach` — private
- `signalforge-seo` — private
- `canva-assets` — private
- `signalforge-debug` — private
- `bet-scanner` — private
- `diamond-scanner` — private
- `dropship-machine` — private
- `portfolio` — private
- `job-agent-dashboard` — private
- `trinity-os-core` — public
- `trinity-funnel` — private · ARCHIVED
- `smart-money-concepts` — public
- `yoman` — public
- `blankly` — public
- `talipp` — public
- `AlphaPy` — public
- `qf-lib` — public
- `MachineLearningStocks` — public
- `uniswap-python` — public
- `python-poloniex` — public
- `cryptofeed` — public
- `alpaca-py` — public
- `python3-krakenex` — public
- `coinbasepro-python` — public
- `open-rarity` — public
- `xian-contracting` — public
- `client-python` — public
- `WebSocket-for-Python` — public
- `hydrogram` — public
- `interactions.py` — public
- `pottery` — public
- `kink` — public
- `lagom` — public
- `luminaire` — public
- `pyFTS` — public
- `authomatic` — public
- `oauthlib` — public
- `pydantic-settings` — public
- `meilisearch-python` — public
- `python-twitch-client` — public
- `tunesynctool` — public
- `adcp-client-python` — public
- `vllm-plugin-FL` — public
- `scikit-learn` — public
- `mempalace` — public
- `TensorRT-Edge-LLM` — public
- `pageTurnerLibrary` — public
- `mergework` — public
- `poe2-mcp` — public
- `agents` — public
- `rucio` — public
- `naturo` — public
- `PraisonAI` — public
- `mcp-context-forge` — public
- `issue-history` — public
- `cognee` — public
- `bandit` — public
- `AIOS` — public
- `flashcards-python` — public
- `litellm` — public
- `mloader` — public
- `newrelic-python-agent` — public
- `factorgraph-st` — public
- `ras-commander` — public
- `sir` — public
- `sd-forge-deforum` — public
- `lumina-st` — public
- `observability-demo` — public
- `linux-profile` — public
- `unsloth` — public
- `FlagGems` — public
- `flagsmith` — public
- `linkml` — public
- `news-template` — public
- `earth2studio` — public
- `academicOps` — public
- `freecad-addon-robust-mcp-server` — public
- `ngdevkit` — public
- `mcp-for-splunk` — public
- `Adapt` — public

## 7. Repositories found by explicit current-name search in addition to the installed 100-list

- `memory-for-all`
- `github-sync`
- `Sync-GitHub-`
- `shopify-store`
- `ocean-quartz-crane-clear-MCP`
- `commotiai-forex`
- `trinity-slack-gateway`

These are important because the 100-item installation inventory is not sufficient by itself as the canonical project list.

## 8. Governance

- No project is deleted because it looks duplicated.
- Repo presence and project identity are separate facts.
- No status is upgraded to ACTIVE/PRODUCTION solely because a repo exists.
- FX remains RESEARCH_ONLY unless explicitly changed by the human owner.
- APPROVED remains human-only.
- No Publish / Production without explicit human approval.
- Secrets, API keys and credentials must never be stored in this registry.

## 9. Next canonicalization step

This file is an audit snapshot in `inbox/`.  
Recommended next step: after human review, promote confirmed entries into a canonical `PROJECT_REGISTRY.md` and create `projects/<project>/` memory folders without deleting historical files.
