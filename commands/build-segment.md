---
description: Build a Customer.io segment from a plain-English audience description
argument-hint: [audience description, e.g. "users inactive 90 days who purchased before"]
---

Build a Customer.io segment for this audience: $ARGUMENTS

1. Call `cio_prime` if you haven't this session.
2. Read `cio_skills_read` path `fly-api/segments.md` and
   `fly-api/segment_conditions.md` — condition syntax is non-obvious; do not
   guess it. For goal-driven segments also read `recipes/goal_segments.md`.
3. Confirm attribute/event names actually exist in the workspace
   (`cio_read_api`) before referencing them in conditions.
4. Preview the create with `cio_write_api` and `dry_run: true`, show the user
   the exact segment definition, and only create after they confirm.
5. After creation, report the segment id and current membership count.
