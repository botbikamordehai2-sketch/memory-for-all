# Model Room Extension Publishing — Project Memory

Date: 2026-10-02
Project ID: MR-PUB-001
Status: HOLD
Mode: DESIGN_ONLY / PREP_ONLY

## Goal

Prepare the "חדר המודלים" browser extension for publication in browser extension stores while keeping the final developer-account actions, payment, and store submission under human control.

## Canonical command pair

- Shared memory sync: `PROJECT_SYNC: MODEL_ROOM_EXTENSION`
- n8n preparation workflow: `TASK: EXTENSION_PUBLISH_PREP`

Important: `EXTENSION_PUBLISH_PREP` prepares artifacts and checks only. It does not submit/publish the extension.

## Target stores documented in Notion

- Chrome Web Store
- Microsoft Edge Add-ons

## Roles documented in Notion

- Gemini — task owner / orchestration of publication materials
- DeepSeek — ZIP preparation and technical checks
- Grok — QA only
- Moti — developer account, payment, final submission

## Required publication materials

- Privacy policy
- Store copy in Hebrew and English
- Screenshot plan
- Permissions explanation
- ZIP package
- Technical validation / QA

## Dependency

- Test with a real OpenRouter key before publication.

## Governance

- Current task remains HOLD.
- No publication without a separate explicit human approval.
- No automatic creation of developer accounts.
- No automatic payment.
- No automatic store submission.
- OpenRouter key belongs to the extension scope only.
- Do not reuse or expose secrets in project memory or workflow JSON.
- This publishing project is separate from n8n AI activation decisions.

## Intended high-level flow

```text
PROJECT_SYNC: MODEL_ROOM_EXTENSION
        ↓
TASK: EXTENSION_PUBLISH_PREP
        ↓
Load extension/project context
        ↓
Prepare store copy + privacy + screenshots plan
        ↓
Build/validate ZIP
        ↓
Technical QA
        ↓
Audit
        ↓
HOLD
        ↓
Human review
        ↓
Manual developer-account/payment/submission by Moti
```

## Source

Notion task: "פרסום ״חדר המודלים״ בחנויות תוספים — MR-PUB-001"
Current Notion status observed on 2026-10-02: HOLD.
