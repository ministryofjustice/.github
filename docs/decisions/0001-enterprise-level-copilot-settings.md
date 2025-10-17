# 1. Initial configuration of enterprise level copilot settings

Date: 2025-09-12

## Status

Accepted

## Context

In preperation for the rollout of GitHub CoPilot across MoJ, members from the github administration group paired together to set initial enteprise level settings.
These defaults will then be inherited by each of the organisations within the MoJ Enterprise ([Ministry of Justice](https://github.com/ministryofjustice), [ministryofjustice-test](https://github.com/ministryofjustice-test), [MoJ Analytical Services](https://github.com/moj-analytical-services), [CICA](https://github.com/CriminalInjuriesCompensationAuthority)).

These were set on the Ministry of Justice (UK) Enterprise, at the CoPilot Policy level.

We chose a cautious approach, limiting access to less familiar options upfront rather than granting full access initially and having to revoke it later. Please note, this is not a definitive set of rules and specific policies will likely change over time.


## Key Roles and Responsibilities

| Role                        | Description                                                                                                                                         | Owner/Team                        |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Project Responsible Owner   | Accountable for the system's proper development, compliance, and performance.                                                                       | Rosie Brigham                     |
| Technical Lead              | Responsible for procurement evaluation, integration, configuration, and ongoing technical oversight.                                                 | Rosie Brigham (interim), then Developer Experience Team |
| Risk and Compliance Officer | Conducts risk and impact assessments, determines appropriate levels of human oversight, and ensures adherence to this framework for all AI systems. | Rosie Brigham                     |

---

## Decisions

## Policy Decisions
### Content exclusion
(Prevent Copilot from reading specific files or repositories.)
No pattern currently set

### Models
(Select which models can be used with Copilot Chat and your IDE.)
No model policies currently set, CoPilot default models are currently available. However, please note that this is under review.

### Feature settings

### Copilot in GitHub.com
No policy set - this is under review

### Copilot in the CLI
Disabled - there could be a risk that internal tooling, propriatory scripts or environment secrets could be inadvertantly shared.

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
Disabled - a part of this tool going through the Technical Design Authority process, it was agreed that AI Agents should not be allowed to 'check their own homework'. A human in the loop must always check the work (e.g review pull requests)

### Block Copilot code review in all enterprise repositories
Enabled - If enabled, Copilot code review will be blocked in all repositories in this enterprise for all users, even if they are not assigned a Copilot license by this enterprise.

### Copilot coding agent Preview
Disabled

### Block Copilot coding agent in all repositories owned by Ministry of Justice (UK)
Enabled - When enabled, Copilot coding agent will be blocked from accessing all repositories owned by Ministry of Justice (UK), for all users—including those not managed by this enterprise.

### MCP servers in Copilot
Disabled - initially

### MCP Registry URL (optional)
As specific MCPs are required in developers workflow (for CircleCI or similar), they will be listed here

### Duplicate Detection Filter
Blocked - initially
