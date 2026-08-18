# Jira MCP + Claude Code Workflow

A sanitized case study of using a Claude Code agent with a Jira MCP server to turn a concise natural-language instruction into a controlled Jira workflow action.

## Example use case

An engineer provides a one-line instruction such as:

> Move approved security-validation stories from **Ready for Review** to **Done**.

The agent identifies candidate issues, presents the planned updates for review, and performs only the approved status transitions. Authentication, project identifiers, and live Jira data are intentionally excluded.

## Guardrails

- Use least-privilege Jira credentials.
- Require an explicit project, status transition, and approval condition.
- Preview the affected issues before making changes.
- Log the instruction, planned changes, approval, execution result, and failures.
- Keep a human reviewer in the loop for production actions.

## Why it matters

This pattern demonstrates agentic workflow automation with MCP, natural-language task intake, API-integrated execution, human oversight, and auditability.
