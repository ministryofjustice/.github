# 2. GitHub Copilot Enterprise AI Controls

Date: 2026-06-18

Last Updated: 2026-07-01

## Status

Accepted

## Context

This ADR is an enhancement of the previous ADR [0001](./0001-enterprise-level-copilot-settings.md).

GitHub Copilot Enterprise has been continuously improving, with new features added and some existing features deprecated. This ADR provides an overview of the current GitHub Copilot Enterprise settings, including features and changes introduced since ADR 0001.

This ADR is intended to be both a governance record (what settings are in place and why) and a current-state reference.

Controls documented in ADR 0001 that are no longer present in current enterprise settings are intentionally omitted from this document.

---

## Key roles and responsibilities

| Role                        | Description                                                                                                                                         | Owner/Team                |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------- |
| Project Responsible Owner   | Accountable for the system's proper development, compliance, and performance.                                                                       | Rosie Brigham             |
| Technical Lead              | Responsible for procurement evaluation, integration, configuration, and ongoing technical oversight.                                                | Developer Experience Team |
| Risk and Compliance Officer | Conducts risk and impact assessments, determines appropriate levels of human oversight, and ensures adherence to this framework for all AI systems. | Rosie Brigham             |

---

## Access management

Access to GitHub Copilot is delegated to business units. They are responsible for managing access using GitHub Teams. This is done at an Organisation level.

## Content Exclusion

GitHub Copilot context exclusion is delegated to repository owners. They are responsible for managing content exclusion using the GitHub Copilot settings in their repositories. This is done at a repository level.

## Allowed models

### Default models

_Selected Copilot models are available across every organization in Ministry of Justice (UK)_

_Model status is documented at enterprise level. Copilot is enabled through one organization, so separate per-organization model variance is not tracked in this ADR._

| Model                                           | Status   |
| ----------------------------------------------- | -------- |
| Anthropic Claude Haiku 4.5                      | Optional |
| Anthropic Claude Opus 4.5                       | Optional |
| Anthropic Claude Opus 4.6                       | Optional |
| Anthropic Claude Opus 4.6 (fast mode) (Preview) | Optional |
| Anthropic Claude Opus 4.7                       | Optional |
| Anthropic Claude Opus 4.8                       | Optional |
| Anthropic Claude Sonnet 4.5                     | Optional |
| Anthropic Claude Sonnet 4.6                     | Optional |
| Anthropic Claude Sonnet 5                       | Optional |
| Google Gemini 2.5 Pro                           | Optional |
| Google Gemini 3.1 Pro (Preview)                 | Optional |
| Google Gemini 3.5 Flash                         | Optional |
| Google Gemini 3 Flash (Preview)                 | Optional |
| OpenAI GPT-5 mini                               | Optional |
| OpenAI GPT-5.4                                  | Optional |
| OpenAI GPT-5.4 mini                             | Optional |
| OpenAI GPT-5.5                                  | Optional |

## Privacy

### Suggestions matching public code

_GitHub Copilot can allow or block [code suggestions](https://docs.github.com/en/copilot/using-github-copilot/finding-public-code-that-matches-github-copilot-suggestions) matching public code._

Status: Blocked

## Features

### Policies for enterprise-assigned users

_Enable all Copilot features set to "Let organizations decide" for users with a Copilot license assigned directly from the enterprise._

Status: Disabled everywhere

### Spark (Preview)

_Organizations can have access to [GitHub Spark](https://gh.io/responsible-use-of-github-spark). This preview is governed by GitHub's [pre-release terms](https://docs.github.com/en/site-policy/github-terms/github-pre-release-license-terms)._

Status: Disabled everywhere

### Editor preview features

_Organizations can have access to editor preview features._

Status: Enabled everywhere

### Copilot can search the web

_Copilot can answer questions about new trends and give improved answers, via Bing. See [Microsoft Privacy Statement](https://privacy.microsoft.com/en-us/privacystatement)._

Status: Disabled everywhere

### Copilot can search the web using model native search (Preview)

_If enabled, Copilot can answer questions using a model's built-in search capabilities._

Status: Disabled everywhere

### Copilot-generated commit messages

_If enabled, Copilot will [suggest commit messages](https://docs.github.com/en/copilot/responsible-use/copilot-commit-message-generation) for changes made on GitHub.com._

Status: Disabled everywhere

### Copilot Spaces

_If enabled, organization members can view and create [Copilot Spaces](https://docs.github.com/en/copilot/how-tos/provide-context/use-copilot-spaces). When disabled, users cannot view or create any Copilot Spaces._

Status: Let organizations decide

### Copilot Spaces Individual Access

_If enabled, organization members can create individually owned Copilot Spaces. When disabled, users cannot create individual spaces._

Status: Disabled everywhere

### Copilot Spaces Individual Sharing

_If enabled, organization members can share individually owned Copilot Spaces that do not contain enterprise data. When disabled, users cannot share individual spaces._

Status: Disabled everywhere

### Copilot Memory (Preview)

_Members can use [Copilot Memory](https://docs.github.com/copilot/concepts/agents/copilot-memory) to store facts about repositories and personal preferences about how they want to interact with Copilot. These are available to agents in future sessions. Users can turn this off at any time, regardless of enterprise or organization policy. Learn more in the [Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement). This preview is governed by [GitHub's pre-release terms](https://docs.github.com/en/site-policy/github-terms/github-pre-release-license-terms)._

Status: Disabled everywhere

### Semantic indexing for Non-GitHub Repositories (Preview)

_If enabled, members of this business will have access to upload non-GitHub repositories for semantic indexing._

Status: Disabled everywhere

### Enable custom models (Preview)

_Enable to allow your organizations to configure and use custom models via API key. When using custom models, GitHub is allowed to share your data with third-party services, including Azure and OpenAI, using your provided key._

Status: Disabled

### Bring Your Own Language Model Key in Select IDEs

_Enable the use of your own third-party language model API keys for VS Code and JetBrains. [Learn more](https://code.visualstudio.com/docs/copilot/customization/language-models#_bring-your-own-language-model-key)._

Status: Enabled everywhere

## Billing

### AI credit paid usage

_If enabled, all organizations in your enterprise will be billed for AI credit paid usage [Set a budget to control your maximum spend](https://github.com/enterprises/ministry-of-justice-uk/billing/budgets)._

Status: Disabled

## Metrics

### Copilot metrics API

_If enabled, enterprise and organization administrators can query the [Copilot metrics API](https://docs.github.com/en/rest/copilot/copilot-metrics?apiVersion=2022-11-28) for insights into Copilot usage._

Status: Disabled everywhere

### Copilot usage metrics

_If enabled, enterprise admins, billing managers, and authorized users can view Copilot usage metrics in a [dashboard](https://docs.github.com/en/copilot/concepts/copilot-metrics) and access the [Copilot Usage API](https://docs.github.com/en/enterprise-cloud@latest/rest/copilot/copilot-metrics?apiVersion=2022-11-28#get-copilot-enterprise-usage-metrics-for-a-specific-day)._

Status: Enabled everywhere

## Copilot clients

### Copilot in GitHub.com

_Organizations can use Copilot Chat in GitHub.com and knowledge base search._

Status: Let organizations decide

### Copilot CLI

_Organizations can use GitHub Copilot for assistance in terminal._

Status: Enabled everywhere

### Store local sessions in the Cloud

_Control how CLI and VS Code sessions are stored and accessed from the cloud._

Status: Select a policy (effectively disabled)

### Copilot in GitHub Desktop

_Organizations can use GitHub Copilot for assistance in GitHub Desktop._

Status: Disabled everywhere

### Copilot Chat in GitHub Mobile

_If enabled, organizations can use GitHub Copilot Chat in GitHub Mobile personalized to a codebase._

Status: Disabled everywhere

### Copilot Agent Mode in IDE Chat

_If enabled, organizations may use Agent Mode within their IDE to interact with Copilot for the purpose of reasoning through requests, planning tasks, and making changes to the codebase. [Learn more](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/chat-in-ide?tool=visualstudio#using-agent-mode-1)._

Status: Enabled everywhere

### Agent apps (Preview)

_If enabled, enterprise admins can turn on agentic features provided by GitHub Apps._

Status: Disabled everywhere

## MCP

### MCP servers in Copilot

_Users can configure Model Context Protocol (MCP) servers for Copilot in all Copilot editors and Copilot cloud agent. See MCP docs for [Copilot Chat](https://docs.github.com/en/copilot/customizing-copilot/extending-copilot-chat-with-mcp) and [Copilot cloud agent](https://docs.github.com/en/copilot/customizing-copilot/extending-copilot-coding-agent-with-mcp)._

Status: Enabled everywhere

## Agents

### Copilot cloud agent

_If enabled, users assigned a Copilot license from this enterprise will have access to Copilot cloud agent in repositories where it is enabled. This feature may use models which are not enabled on your "Models" settings page. [Learn more](https://gh.io/assigncopilot)._

Status: Enabled for selected organizations

### Block Copilot cloud agent in all repositories owned by Ministry of Justice (UK)

_When enabled, Copilot cloud agent will be blocked from accessing all repositories owned by Ministry of Justice (UK), for all users—including those not managed by this enterprise._

Status: Off

### Copilot code review

_If enabled, members who are licensed through organizations within this enterprise can use [Copilot code review](https://docs.github.com/en/enterprise-cloud@latest/copilot/using-github-copilot/code-review/using-copilot-code-review) and [Copilot for pull requests](https://docs.github.com/enterprise-cloud@latest/copilot/github-copilot-enterprise/copilot-pull-request-summaries/creating-a-pull-request-summary-with-github-copilot) in any repository they belong to._

Status: Let organizations decide

### Block Copilot code review in all enterprise repositories

_If enabled, Copilot code review will be blocked in all repositories in this enterprise for all users, even if they are not assigned a Copilot license by this enterprise._

Status: Off

## Amendments

### 18/06/2026

- Created ADR 0002 to supersede ADR 0001 and document the current enterprise AI control set.
- Updated structure to reflect current GitHub Copilot Enterprise settings and feature areas.

### 19/06/2026

- Enable "Editor preview features"

### 01/07/2026 ([source](https://github.com/ministryofjustice/.github/pull/46))

- Enable Claude Sonnet 5
