---
description: Diagnose the health of a Customer.io workspace — deliverability, pipelines, stalled automations
argument-hint: [optional focus area, e.g. "deliverability"]
---

Run a health check on the connected Customer.io workspace. Focus: $ARGUMENTS

1. Call `cio_prime` if you haven't this session, and `cio_auth_status` to
   confirm which workspace you're inspecting.
2. Read `cio_skills_read` path `recipes/diagnosing_workspace_health.md` and
   follow its workflow. Supplement with `fly-api/deliverability.md` and
   `fly-api/pipeline_health.md` as relevant.
3. This is a read-only diagnosis: use `cio_read_api` only. Propose fixes, but
   do not execute writes unless the user asks afterward.
4. Deliver findings ordered by severity, each with the evidence and the
   suggested fix.
