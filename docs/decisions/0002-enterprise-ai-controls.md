# 2. GitHub Copilot Enterprise AI Controls

Date: 2026-06-18

Last Updated: 2026-09-30

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

## Administration and Privacy

### Access management

Access to GitHub Copilot is delegated to agencies. They are responsible for managing access using GitHub Teams. This is done at an Organisation level.

### Content Exclusion

GitHub Copilot context exclusion is delegated to repository owners. They are responsible for managing content exclusion using the GitHub Copilot settings in their repositories. This is done at a repository level.

### Suggestions matching public code

_Allow organizations to receive [code suggestions](https://docs.github.com/en/copilot/using-github-copilot/finding-public-code-that-matches-github-copilot-suggestions) that match publicly available code._

Status: Blocked

## Models

### Default availability for released models

_Controls the default state for [models you haven't explicitly configured.](https://docs.github.com/en/copilot/concepts/models/default-availability)_

Status: Disabled everywhere

### Enabled models

| Model                                                                               | Status   |
| ----------------------------------------------------------------------------------- | -------- |
| Anthropic Claude Fable 5                                                            | Disabled |
| Anthropic Claude Fable 5.1                                                          | Disabled |
| Anthropic Claude Haiku 4.5                                                          | Enabled  |
| Anthropic Claude Opus 4.8                                                           | Enabled  |
| Anthropic Claude Opus 4.8 (fast mode) (Preview)                                     | Disabled |
| Anthropic Claude Opus 5                                                             | Enabled  |
| Anthropic Claude Opus 5.5                                                           | Enabled  |
| Anthropic Claude Sonnet 5                                                           | Enabled  |
| Anthropic Claude Sonnet 5.5                                                         | Enabled  |
| Google Gemini 3.7 Flash                                                             | Enabled  |
| Google Gemini 3.8 Flash                                                             | Enabled  |
| Microsoft MAI-Code-1.1-Flash                                                        | Enabled  |
| Moonshot AI Kimi K3                                                                 | Disabled |
| OpenAI GPT-5 Mini                                                                   | Enabled  |
| OpenAI GPT-5.3 Codex (GitHub Copilot uses GPT-5.3 Codex as the base fallback model) | Enabled  |
| OpenAI GPT-5.4                                                                      | Enabled  |
| OpenAI GPT-5.4 Mini                                                                 | Enabled  |
| OpenAI GPT-5.5                                                                      | Enabled  |
| OpenAI GPT-5.6 Luna                                                                 | Enabled  |
| OpenAI GPT-5.6 Sol                                                                  | Enabled  |
| OpenAI GPT-5.6 Terra                                                                | Enabled  |
| OpenAI GPT-6 Astra                                                                  | Enabled  |
| OpenAI GPT-6 Luna                                                                   | Enabled  |
| OpenAI GPT-6 Sol                                                                    | Enabled  |
| OpenAI GPT-6.1 Sol                                                                  | Enabled  |
| xAI Grok 4.5                                                                        | Disabled |
| xAI Grok 4.6                                                                        | Disabled |
| xAI Grok 4.7                                                                        | Disabled |

## Features and Clients

### Default policy for new features and clients

_When GitHub ships new Copilot features and clients, this policy is applied automatically. You can override individual features and clients below. Learn more about default availability_

Status: Disabled

### Clients

#### Copilot cloud agent (coming soon)

_Enables access to Copilot in the cloud, including GitHub.com and GitHub Mobile. This policy replaces previous Copilot Chat and Copilot cloud agent policies._

Status: Enabled everywhere

#### Copilot in GitHub.com

_Organizations can use Copilot Chat in GitHub.com and knowledge base search._

Status: Enabled everywhere

#### Copilot in GitHub Desktop

_Organizations can use GitHub Copilot for assistance in GitHub Desktop._

Status: Enabled everywhere

#### Copilot Chat in the IDE

_Organizations can use Copilot Chat for code editors._

Status: Enabled everywhere

#### Copilot Agent Mode in IDE Chat

_If enabled, organizations may use Agent Mode within their IDE to interact with Copilot for the purpose of reasoning through requests, planning tasks, and making changes to the codebase._

Status: Enabled everywhere

#### Copilot CLI

_If enabled, organizations can use GitHub Copilot CLI as an assistant in the terminal_

Status: Enabled everywhere

#### Allow use of Copilot CLI billed to the organization (Preview)

_Allow use of the Copilot CLI for automations and other uses not linked to a specific user. AI credits used will be billed directly to the organization, using the shared pool first, and then incurring additional usage, subject to budgets._

Status: Enabled

#### Store local sessions in the Cloud

_If enabled, CLI and VSCode sessions are stored in the cloud._

Status: View from cloud


#### Copilot Chat in GitHub Mobile

_If enabled, organizations can use GitHub Copilot Chat in GitHub Mobile personalized to a codebase._

Status: Disabled everywhere

#### GitHub Copilot app

_If enabled, members of organizations in your enterprise can use the GitHub Copilot app. Enforcement begins July 27th, 2026 in version 1.1 of the GitHub Copilot app. The Copilot CLI policy continues to govern the GitHub Copilot App until version 1.1._

Status: Enabled everywhere

#### Agent apps (Preview)

_If enabled, enterprise admins can turn on agentic features provided by GitHub Apps._

Status: Disabled everywhere

### Features

#### Copilot can search the web

_Copilot can answer questions about new trends and give improved answers, via Bing. See [Microsoft Privacy Statement](https://privacy.microsoft.com/en-us/privacystatement)._

Status: Enabled everywhere


#### Copilot can search the web using model native search (Preview)

_If enabled, Copilot can answer questions using a model's built-in search capabilities._

Status: Enabled everywhere

#### Copilot-generated commit messages

_If enabled, Copilot will [suggest commit messages](https://docs.github.com/en/copilot/responsible-use/copilot-commit-message-generation) for changes made on GitHub.com._

Status: Enabled everywhere

#### Editor preview features

_Organizations can have access to editor preview features._

Status: Enabled everywhere

#### Copilot Memory (Preview)

_Members can use [Copilot Memory](https://docs.github.com/copilot/concepts/agents/copilot-memory) to store facts about repositories and personal preferences about how they want to interact with Copilot. These are available to agents in future sessions. Users can turn this off at any time, regardless of enterprise or organization policy. Learn more in the [Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement). This preview is governed by [GitHub's pre-release terms](https://docs.github.com/en/site-policy/github-terms/github-pre-release-license-terms)._

Status: Disabled everywhere

#### Semantic indexing for Non-GitHub Repositories (Preview)

_If enabled, members of this business will have access to upload non-GitHub repositories for semantic indexing._

Status: Disabled everywhere

#### Bring Your Own Language Model Key in Select IDEs

_Enable the use of your own third-party language model API keys for VS Code and JetBrains. [Learn more](https://code.visualstudio.com/docs/copilot/customization/language-models#_bring-your-own-language-model-key)._

Status: Enabled everywhere

### Copilot Spaces

_If enabled, organization members can view and create [Copilot Spaces](https://docs.github.com/en/copilot/how-tos/provide-context/use-copilot-spaces). When disabled, users cannot view or create any Copilot Spaces._

Status: Disabled everywhere

### Copilot Spaces Individual Access

_If enabled, organization members can create individually owned Copilot Spaces. When disabled, users cannot create individual spaces._

Status: Disabled everywhere

### Copilot Spaces Individual Sharing

_If enabled, organization members can share individually owned Copilot Spaces that do not contain enterprise data. When disabled, users cannot share individual spaces._

Status: Disabled everywhere

## Billing

### AI credit paid usage

_If enabled, all organizations in your enterprise will be billed for AI credit paid usage [Set a budget to control your maximum spend](https://github.com/enterprises/ministry-of-justice-uk/billing/budgets)._

Status: Disabled

## Metrics

### Copilot metrics API

_If enabled, enterprise and organization administrators can query the [Copilot metrics API](https://docs.github.com/en/rest/copilot/copilot-metrics?apiVersion=2022-11-28) for insights into Copilot usage._

Status: Enabled everywhere

### Copilot usage metrics

_If enabled, enterprise admins, billing managers, and authorized users can view Copilot usage metrics in a [dashboard](https://docs.github.com/en/copilot/concepts/copilot-metrics) and access the [Copilot Usage API](https://docs.github.com/en/enterprise-cloud@latest/rest/copilot/copilot-metrics?apiVersion=2022-11-28#get-copilot-enterprise-usage-metrics-for-a-specific-day)._

Status: Enabled everywhere

## MCP

### MCP servers in Copilot

_Users can configure Model Context Protocol (MCP) servers for Copilot in all Copilot editors and Copilot cloud agent. See MCP docs for [Copilot Chat](https://docs.github.com/en/copilot/customizing-copilot/extending-copilot-chat-with-mcp) and [Copilot cloud agent](https://docs.github.com/en/copilot/customizing-copilot/extending-copilot-coding-agent-with-mcp)._

Status: Enabled everywhere

## Agents

### Configuration source

_Select the organization that provides enterprise-managed settings, plugins, and custom agents._

Source: ministryofjustice

### Copilot cloud agent

_If enabled, users assigned a Copilot license from this enterprise will have access to Copilot cloud agent in repositories where it is enabled. This feature may use models which are not enabled on your "Models" settings page. [Learn more](https://gh.io/assigncopilot)._

Status: Enabled for selected organizations

Enabled organisations:

- ministryofjustice

### Block Copilot cloud agent in all repositories owned by Ministry of Justice (UK)

_When enabled, Copilot cloud agent will be blocked from accessing all repositories owned by Ministry of Justice (UK), for all users—including those not managed by this enterprise._

Status: Off

### Copilot code review

_If enabled, members who are licensed through organizations within this enterprise can use [Copilot code review](https://docs.github.com/en/enterprise-cloud@latest/copilot/using-github-copilot/code-review/using-copilot-code-review) and [Copilot for pull requests](https://docs.github.com/enterprise-cloud@latest/copilot/github-copilot-enterprise/copilot-pull-request-summaries/creating-a-pull-request-summary-with-github-copilot) in any repository they belong to._

Status: Let organizations decide

### Default review effort level

_The depth of analysis Copilot uses for repositories that have not selected their own review effort level.
Applies to repositories owned by organizations in this enterprise. Organizations and repositories can override this default._

Level: Balanced

### Allow Copilot to approve pull requests

_Choose which organizations can allow Copilot to approve pull requests._

Status: Disabled everywhere

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

### 09/07/2026 ([source](https://github.com/ministryofjustice/.github/pull/50))

- Enable Microsoft MAI-Code-1-Flash

- Enable OpenAI GPT-5.6 Luna, Sol, and Terra

### 30/09/2026

- Enable OpenAI GPT-6.1 Sol

### 07/10/2026

- Update ADR with current enterprise AI control settings and models
