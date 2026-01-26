---
title: UPC Production Predictions
sidebar_label: upc_production_predictions
---

## Description

View to compare real energy production with expected production. It shows real production and reserves fields for expected production and deviation percentage.

## Structure

| Field | Description |
| --- | --- |
| `id` | Unique record identifier |
| `cups_id` | Supply point identifier (CUPS) |
| `expected_production_kwh` | Expected energy production (kWh) |
| `real_production_kwh` | Real energy production recorded (kWh) |
| `deviation_pct` | Deviation percentage between expected and real |
| `info_dt` | Date and time for the records |

## SQL Definition

```sql
SELECT id,
    cups_id,
    NULL::numeric AS expected_production_kwh,
    production AS real_production_kwh,
    NULL::numeric AS deviation_pct,
    info_dt
   FROM zertipower.energy_hourly eh;
```
