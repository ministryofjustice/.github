# 1. Initial configuration of enterprise level copilot settings

Date: 2025-09-12
Last Updated: 2025-11-25

## Status

Accepted

## Context

In preperation for the rollout of GitHub CoPilot across MoJ, members from the github administration group paired together to set initial enteprise level settings.
These defaults will then be inherited by each of the organisations within the MoJ Enterprise ([Ministry of Justice](https://github.com/ministryofjustice), [ministryofjustice-test](https://github.com/ministryofjustice-test), [MoJ Analytical Services](https://github.com/moj-analytical-services), [CICA](https://github.com/CriminalInjuriesCompensationAuthority)).

These were set on the Ministry of Justice (UK) Enterprise, at the CoPilot Policy level.

We chose a cautious approach, limiting access to less familiar options upfront rather than granting full access initially and having to revoke it later. Please note, this is not a definitive set of rules and specific policies will likely change over time.

## Key Roles and Responsibilities

| Role                        | Description                                                                                                                                         | Owner/Team                                              |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------- |
| Project Responsible Owner   | Accountable for the system's proper development, compliance, and performance.                                                                       | Rosie Brigham                                           |
| Technical Lead              | Responsible for procurement evaluation, integration, configuration, and ongoing technical oversight.                                                | Rosie Brigham (interim), then Developer Experience Team |
| Risk and Compliance Officer | Conducts risk and impact assessments, determines appropriate levels of human oversight, and ensures adherence to this framework for all AI systems. | Rosie Brigham                                           |

---

## Decisions

## Policy Decisions

### Content exclusion

(Prevent Copilot from reading specific files or repositories.)
No pattern currently set

### Models

| Model                               | Enterprise Setting       | Organisation Setting (ministryofjustice) |
| ----------------------------------- | ------------------------ | ---------------------------------------- |
| Anthropic Claude Sonnet 4           | Disabled everywhere      | Disabled by Enterprise                   |
| Anthropic Claude Sonnet 4.5         | Let organisations decide | Enabled                                  |
| Anthropic Claude Haiku 4.5          | Let organisations decide | Enabled                                  |
| Anthropic Claude Opus 4.1           | Disabled everywhere      | Disabled by Enterprise                   |
| Anthropic Claude Opus 4.5 (Preview) | Let organisations decide | Enabled                                  |
| Google Gemini 2.5 Pro               | Let organisations decide | Enabled                                  |
| Google Gemini 3 Pro (Preview)       | Let organisations decide | Enabled                                  |
| Google Gemini 3 Flash (Preview)     | Let organisations decide | Enabled                                  |
| OpenAI GPT-5                        | Let organisations decide | Enabled                                  |
| OpenAI GPT-5-Codex (Preview)        | Let organisations decide | Enabled                                  |
| OpenAI GPT-5 mini                   | Let organisations decide | Enabled                                  |
| OpenAI GPT-5.1                      | Let organisations decide | Enabled                                  |
| OpenAI GPT-5.1-Codex                | Let organisations decide | Enabled                                  |
| OpenAI GPT-5.1-Codex-Mini (Preview) | Let organisations decide | Enabled                                  |
| OpenAI GPT-5.1-Codex-Max            | Let organisations decide | Enabled                                  |
| OpenAI GPT-5.2                      | Let organisations decide | Enabled                                  |
| OpenAI GPT-5.2-Codex                | Let organisations decide | Enabled                                  |
| xAI Grok Code Fast 1                | Disabled everywhere      | Disabled by Enterprise                   |

### Feature settings

### Copilot in GitHub.com

No policy set - this is under review

### Copilot in the CLI

Enabled

### Copilot in GitHub Desktop

Disabled - See above. In addition - GH suggests this feature is useful for large diffs, but good coding practice favours smaller commits. It was also considered that developers should author their own commit content and messages.

### Copilot Chat in the IDE

No Policy - this was a popular feature during the trial, however we have selected no policy to allow individual organisations to enable or disable this.

### Editor preview features

Disabled

### Copilot Chat in GitHub Mobile

Disabled - There are few instances in MoJ where phone access of Github is required.

### Copilot Extensions

Disabled - outside of initial DPIA remit.

### Copilot can search the web

Initially disabled - this can be reviewed at a later date.

### Copilot Metrics API

Initially disabled - this will be enabled after the onboarding of the Dev Experience team who will utilise these metrics.

### Copilot code review

Enabled

### Block Copilot code review in all enterprise repositories

Enabled - If enabled, Copilot code review will be blocked in all repositories in this enterprise for all users, even if they are not assigned a Copilot license by this enterprise.

### Copilot coding agent Preview

Disabled

### Block Copilot coding agent in all repositories owned by Ministry of Justice (UK)

Enabled - When enabled, Copilot coding agent will be blocked from accessing all repositories owned by Ministry of Justice (UK), for all users—including those not managed by this enterprise.

### MCP servers in Copilot

Enabled

### MCP Registry URL (optional)

As specific MCPs are required in developers workflow (for CircleCI or similar), they will be listed here

### Duplicate Detection Filter

Blocked - initially

### Copilot Usage Metrics Dashboard

Enabled - to facilitate assessment of Copilot usage across the enterprise

### Copilot Spark

Disabled

## Amendments

### 13/11/2025 ([source](https://github.com/ministryofjustice/.github/pull/21))

- Enable GitHub Copilot CLI - Allows similar experience to GitHub Copilot via Visual Studio Code, but is editor agnostic
- Enable MCP servers - MCP enhances agent mode capabilities, see https://github.com/ministryofjustice/modernisation-platform-environments/pull/13738 for experimental usage
- Disable Copilot Spark - Provides a similar capability to Copilot Agents which are disabled

### 25/11/2025 ([source](https://github.com/ministryofjustice/.github/pull/23))

- Document enabled models at enterprise and organisation level

### 25/11/2025 ([source](https://github.com/ministryofjustice/.github/pull/24))

- Enable Claude Opus 4.5

### 15/12/2025 ([source](https://github.com/ministryofjustice/.github/pull/26))

- Adds new OpenAI models
  - OpenAI GPT-5.1-Codex-Max
  - OpenAI GPT-5.2
- Enables all available OpenAI models
- Changes Enterprise setting to "Let organisations decide" for enabled models
- Changes Enterprise setting to "Disabled everywhere" for disabled models

### 17/12/2025 ([source](https://github.com/ministryofjustice/.github/pull/27))

- Enables Google Gemini 3 Flash
- Removes "Preview" status of several OpenAI models

### 14/01/2026 ([source](https://github.com/ministryofjustice/.github/pull/28))

- Enables OpenAI GPT-5.2-Codex 
