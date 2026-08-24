# Publish later

Do this in a separate pass. Do not submit until `customerio/claude-plugin` is
public — the Claude plugin directory only accepts public GitHub repos.

1. Make **https://github.com/customerio/claude-plugin** public.
2. Validate from the repo root: `claude plugin validate .`
3. Optional: soak internally first — teammates run
   `/plugin marketplace add customerio/claude-plugin` in Claude Code.
4. Submit the repo URL in the Directory portal:
   https://claude.ai/admin-settings/directory/submissions/plugins/new
   (requires Team/Enterprise directory management access — the same permission
   as the MCP connector listing). Console alternative:
   https://platform.claude.com/plugins/submit
5. Anthropic runs automated screening; "Anthropic Verified" is a deeper,
   optional review. Track status at
   https://claude.ai/admin-settings/directory/submissions
6. After publication, pushes to `main` are picked up automatically — no
   re-submission. Keep playbooks on the MCP server, not in git, so content
   updates don't wait on screening.
