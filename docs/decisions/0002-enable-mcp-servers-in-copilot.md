# 2. Enable MCP Servers in Copilot

Date: 2025-10-21

## Status

Proposed

Amends [ADR-0001](0001-enterprise-level-copilot-settings.md)

## Context

In [ADR-0001](0001-enterprise-level-copilot-settings.md), MCP (Model Context Protocol) servers in Copilot were initially disabled as part of a cautious rollout approach for GitHub Copilot across MoJ.

Since the initial configuration:

- [Add context: What has changed? E.g., developer needs, specific use cases identified, security review completed, etc.]
- [Add context: What prompted this review?]

MCP servers allow Copilot to integrate with external tools and services (such as CircleCI, documentation systems, or other development tools) to provide more contextual assistance to developers.

## Decision

We will **enable MCP servers in Copilot** at the enterprise level.

Specific MCPs approved for use will be explicitly listed in the MCP Registry URL configuration to maintain security and governance oversight.

### Initial Approved MCPs

- [List specific MCPs to be enabled, e.g., CircleCI]
- [Add more as needed]

## Consequences

### Positive

- Developers can leverage approved integrations to improve productivity
- Better contextual assistance from Copilot based on project-specific tools
- Controlled rollout through explicit registry management

### Negative

- Increased surface area for potential data exposure
- Additional governance overhead to maintain approved MCP list
- Requires ongoing review of new MCP requests

### Risks and Mitigations

- **Risk**: Unauthorized MCPs could access sensitive data
  - **Mitigation**: Use explicit MCP Registry URL with approved list only
- **Risk**: MCPs may change functionality over time
  - **Mitigation**: Periodic review of enabled MCPs (suggest quarterly)

## Review

This decision should be reviewed:

- When new MCPs are requested
- Quarterly to assess usage and security posture
- If security incidents occur related to MCP usage
