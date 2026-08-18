# Example Workflow Contract

## Instruction

Move approved security-validation stories from `Ready for Review` to `Done`.

## Agent plan

1. Query Jira through the MCP server for issues in the specified project and status.
2. Filter to issues tagged `security-validation` with an approved validation record.
3. Display the issue keys and proposed transition for human review.
4. Execute the approved transitions only.
5. Return an audit-friendly summary of successes and failures.

## Non-negotiable controls

- Never infer project scope or approval status.
- Never perform irreversible workflow actions without review.
- Do not expose Jira tokens, user data, or proprietary issue content in logs.
