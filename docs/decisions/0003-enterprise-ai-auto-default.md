# 3. GitHub Copilot Default Model Selection

Date: 2026-07-02

Last Updated: 2026-07-02

## Status

Accepted

## Context

GitHub Copilot Enterprise billing has moved from Premium Request Units (PRU) to AI Credits (AIC).

On 2026-07-01, GitHub introduced a new enterprise control to default users to Auto model selection: [Enterprises can default to auto model selection](https://github.blog/changelog/2026-07-01-enterprises-can-default-to-auto-model-selection/).

Within MOJ, users work across varied tasks (chat, code generation, refactoring, test authoring, and explanation). A single fixed default model is often suboptimal across these task types and requires users to manually switch models to get better outcomes.

This ADR complements [0002](./0002-enterprise-ai-controls.md), which defines model availability and enterprise guardrails.

## Decision

Set the enterprise default for GitHub Copilot to Auto model selection.

This means:

1. Users receive a recommended model automatically for general workflows without needing to choose one first.
2. Existing enterprise controls remain in place, including allowed/disallowed models and feature policies from ADR 0002.
3. Where a workflow needs determinism or model-specific behaviour, teams may still choose an explicit model for that task.

## Consequences

### Positive

- Improves developer experience by reducing model-selection overhead at the start of tasks.
- Increases the likelihood of matching model capability to task type without requiring deep model knowledge from every user.
- Supports change resilience as model availability evolves; Auto can adapt without repeated retraining or policy churn.
- Aligns with AI Credits usage by encouraging efficient use of available model capacity.

### Risks

- Lower predictability for users who expect the same model response profile every time.
- Some workflows may require specific model behaviour for repeatability, tone, latency, or output shape.
- Future changes to Auto routing behaviour may affect user expectations if not communicated.

### Mitigations

- Keep enterprise model governance in place via ADR 0002 (only approved models are available).
- Require teams with high-assurance workflows to explicitly select and document a fixed model where needed.
- Continue human review, testing, and security controls regardless of selected model.
- Monitor usage, quality feedback, and spend through existing enterprise reporting, and revisit this decision if outcomes deteriorate.

### Alternatives considered

- Keep a fixed enterprise default model: rejected, because it creates avoidable friction and is less effective across mixed task types.
- Let each organisation define its own default only: rejected for now, to preserve a consistent enterprise-wide baseline while allowing task-level overrides.
