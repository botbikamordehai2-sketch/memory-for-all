# CONCERT2 — Project Memory: 4-Workflow Architecture

Date: 2026-10-02
Status: DESIGN_ONLY / RESEARCH_ONLY
Execution: No Publish, no production activation, no external execution.

## Core architecture

```text
Models
  ↓
MCP
  ↓
Tools / Apps / Sources
```

MCP is the common connection layer between models and tools.
n8n is the orchestration layer.
HOLD / HITL is the approval and safety layer.

## Four separate n8n workflows

### 1. Shopify / Site Maintenance
Command: `SITE_MAINTENANCE`

Purpose:
- Maintain and inspect the Shopify site.
- Review products, collections, theme/SEO-related issues and proposed changes.
- Produce recommendations before any write action.

Flow:
```text
Trigger / SITE_MAINTENANCE
→ Load Project Context
→ Load Allowed Sources
→ Inspect Shopify/site context
→ Validate / deduplicate
→ Generate proposed fixes/report
→ Audit
→ HOLD
→ Human Approval
→ Optional Sync/Action only after approval
```

### 2. Forex Research
Command: `FOREX_RESEARCH`

Purpose:
- Research-only market analysis.
- Normalize data and timestamps.
- Separate FACT / OBSERVATION / UNSUPPORTED.
- No trading execution.

Flow:
```text
Trigger / FOREX_RESEARCH
→ Load market context
→ Load approved research sources
→ Normalize
→ Cross-check sources
→ FACT / OBSERVATION / UNSUPPORTED
→ Generate research brief
→ Audit
→ HOLD
```

### 3. Social Media
Command: `SOCIAL_CONTENT`

Purpose:
- Research trends, competitors and prior brand content.
- Generate Hebrew content ideas/drafts.
- No automatic publishing.

Flow:
```text
Trigger / SOCIAL_CONTENT
→ Load Brand Context
→ Load Trends / Competitors / Existing Content
→ Research
→ Validate Claims
→ Generate Content Ideas / Drafts
→ Audit
→ HOLD
→ Human Approval before publishing
```

### 4. Blog / SEO
Command: `BLOG_RESEARCH`

Purpose:
- Research blog topics, search intent, SEO and competitors.
- Build outline and draft with source validation.
- No automatic publishing.

Flow:
```text
Trigger / BLOG_RESEARCH
→ Search Intent
→ Sources / Competitors / Course Material
→ Keyword + Topic Research
→ Outline
→ Draft
→ Fact Check
→ Audit
→ HOLD
→ Human Approval
```

## Shared rules

All four workflows use the same architectural principles:
- Separate workflow per project/use case.
- MCP provides controlled access to tools and applications.
- n8n decides which workflow runs.
- Models perform research/analysis/drafting.
- Read-only first.
- Least privilege.
- Fail-closed.
- Existing HOLD, HITL and Audit controls remain.
- No automatic APPROVED writes.
- No Publish / Production without explicit human approval.

## Current direction

Build and test the tool/MCP layer first, then connect models gradually.
Initial model connection sequence discussed: Perplexity first, followed by additional models later.
