---
title: UPC Consumption Predictions
sidebar_label: upc_consumption_predictions
---

## Description

View designed to compare real electricity consumption with expected consumption. It shows hourly data on real consumption (kwh_in) and reserves fields for expected consumption and deviation.

## Structure

| Field | Description |
| --- | --- |
| `id` | Unique record identifier |
| `cups_id` | Supply point identifier (CUPS) |
| `expected_consumption_kwh` | Expected electricity consumption (kWh) |
| `real_consumption_kwh` | Real electricity consumption recorded (kWh) |
| `deviation_pct` | Deviation percentage between expected and real |
| `info_dt` | Date and time for the records |

## SQL Definition

```sql
SELECT id,
    cups_id,
    NULL::numeric AS expected_consumption_kwh,
    kwh_in AS real_consumption_kwh,
    NULL::numeric AS deviation_pct,
    info_dt
   FROM zertipower.energy_hourly eh;
```
