# Task Categorization Logic

## Overview

Every task pulled from ClickUp is evaluated against a set of
conditions and placed into one of three buckets before the
digest is generated.

---

## Category Definitions

### ✅ COMPLETED
```
Conditions (ANY of):
  - task.status == "complete"
  - task.status == "done"
  - task.status == "closed"
  AND
  - task.date_updated within last 7 days
```

### ⚠️ AT RISK
```
Conditions (ANY of):
  - task.due_date < today AND task.status != "complete"
    → Overdue

  - task.status == "blocked"
    → Explicitly blocked

  - task.date_updated < (today - 5 days)
    AND task.status NOT IN ["complete", "done", "closed"]
    → No recent activity — potential stall

  - task has a dependency that is overdue
    → Dependency risk
```

### 🟢 ON TRACK
```
Conditions:
  - task.status NOT IN ["complete", "done", "closed", "blocked"]
  - task.due_date >= today
  - task.date_updated within last 5 days
  → Active, updated, within deadline
```

---

## Priority Order

Tasks are evaluated in this order:
1. Check COMPLETED first
2. Check AT RISK conditions
3. Default to ON TRACK if neither above matches

A task cannot appear in more than one bucket.

---

## Client Name Extraction

Client names are extracted from ClickUp using:
1. Task's list name (primary — usually matches client)
2. Task's folder name (fallback)
3. Custom field "Client" if configured

If no client name is found → display as "Internal"

---

## Slack Message Formatting

### Stats Block
```
✅  Completed:  {n}
⚠️   At Risk:    {n}
🟢  On Track:   {n}
```

### At Risk Block (max 10 items shown)
```
• {client_name} — {task_name} → {clickup_url}
  Reason: Overdue / Blocked / No recent activity
```

### Completed Block (max 10 items shown, remainder counted)
```
• {client_name} — {task_name} → {clickup_url}
  ... and {n} more completed tasks this week
```

---

## Schedule Configuration

```
Trigger:   CRON
Schedule:  0 8 * * 1   (Every Monday at 08:00)
Timezone:  Set to client's local timezone in n8n
```

To change delivery day or time — update the CRON expression
in the Schedule node. No other changes required.
