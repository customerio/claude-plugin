---
description: Draft an email in Customer.io Design Studio
argument-hint: [what the email is for, e.g. "re-engagement email for dormant users"]
---

Draft an email in Design Studio: $ARGUMENTS

1. Call `cio_prime` if you haven't this session.
2. Read `cio_skills_read` path `design-studio`, then `design-studio/nodes.md`
   and the matching pattern file under `design-studio/email_patterns/` (e.g.
   `re_engagement.md`, `welcome.md`, `promotion_sale.md`).
3. Use existing global styles and components from the workspace rather than
   inventing new ones — audit them first with `cio_read_api`.
4. Create the draft with `cio_write_api` (`dry_run: true` first), then run the
   email review flow (`design-studio/email_review.md`) and report the readiness
   score and any QA findings.
5. Do not publish or wire the email into an automation unless the user asks —
   that step is Journeys (`fly-api`).
