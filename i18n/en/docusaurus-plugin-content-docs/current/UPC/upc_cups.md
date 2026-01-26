---
title: UPC CUPS
sidebar_label: upc_cups
---

## Description

This view aggregates information about supply points (CUPS), including their type and contracted power for different periods (P1 to P6).

## Structure

| Field | Description |
| --- | --- |
| `id` | Unique CUPS identifier in the system |
| `cups` | Universal Supply Point Code |
| `type` | Supply type or tariff |
| `p1_contracted_power_kw` | Contracted power in period P1 (kW) |
| `p2_contracted_power_kw` | Contracted power in period P2 (kW) |
| `p3_contracted_power_kw` | Contracted power in period P3 (kW) |
| `p4_contracted_power_kw` | Contracted power in period P4 (kW) |
| `p5_contracted_power_kw` | Contracted power in period P5 (kW) |
| `p6_contracted_power_kw` | Contracted power in period P6 (kW) |
| `created_dt` | Record creation date |

## SQL Definition

```sql
SELECT c.id,
    c.cups,
    c.type::character varying AS type,
    COALESCE(cnt.p1_power, 0::numeric) AS p1_contracted_power_kw,
    COALESCE(cnt.p2_power, 0::numeric) AS p2_contracted_power_kw,
    COALESCE(cnt.p3_power, 0::numeric) AS p3_contracted_power_kw,
    COALESCE(cnt.p4_power, 0::numeric) AS p4_contracted_power_kw,
    COALESCE(cnt.p5_power, 0::numeric) AS p5_contracted_power_kw,
    COALESCE(cnt.p6_power, 0::numeric) AS p6_contracted_power_kw,
    c.created_dt
   FROM zertipower.cups c
     LEFT JOIN zertipower.contracts cnt ON c.id = cnt.cups_id;
```
