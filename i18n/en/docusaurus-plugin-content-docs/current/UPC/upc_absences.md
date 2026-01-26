---
title: UPC Absences
sidebar_label: upc_absences
---

## Description

This view shows information related to user absences, including the ID, reason (if available), and the time period (start and end).

## Structure

| Field | Description |
| --- | --- |
| `id` | Unique record identifier |
| `cups_id` | Related supply point identifier (CUPS) |
| `reason` | Reason for absence (can be 'Unknown') |
| `start_dt` | Start date and time of absence |
| `end_dt` | End date and time of absence |

## SQL Definition

```sql
SELECT id,
    cups_id,
    COALESCE(reference, 'Unknown'::character varying) AS reason,
    start_dt,
    end_dt
   FROM zertipower.vacations v;
```
