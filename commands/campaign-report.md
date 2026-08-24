---
description: Analyze the performance of a Customer.io automation, broadcast, or newsletter
argument-hint: [automation name or id, and optional time window]
---

Produce a performance report for the Customer.io automation/campaign the user
named: $ARGUMENTS

1. Call `cio_prime` if you haven't this session.
2. Read `cio_skills_read` path `recipes/analyzing_automations.md` and follow it —
   it defines the metrics workflow. Read `fly-api/automation_metrics.md` for
   endpoint specifics.
3. If no automation was named, list active automations with `cio_read_api` and
   ask the user to pick one.
4. Deliver: sends, delivery/open/click/conversion rates against the stated time
   window, notable trends, and 2–3 concrete recommendations. State the actual
   date range analyzed.
