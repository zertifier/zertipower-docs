---
title: UPC Hourly Energy
sidebar_label: upc_energy_hourly
---

## Description

Provides an hourly breakdown of energy, detailing consumption (kwh_in), production, and surplus (kwh_out) for each supply point.

## Structure

| Field | Description |
| --- | --- |
| `id` | Unique record identifier |
| `cups_id` | Supply point identifier (CUPS) |
| `consumption_kwh` | Energy consumed from the grid (kWh) - kwh_in |
| `production_kwh` | Energy produced (kWh) |
| `surplus_kwh` | Surplus energy exported to the grid (kWh) - kwh_out |
| `info_dt` | Date and time of the energy record |

## SQL Definition

```sql
SELECT id,
    cups_id,
    kwh_in AS consumption_kwh,
    production AS production_kwh,
    kwh_out AS surplus_kwh,
    info_dt
   FROM zertipower.energy_hourly eh;
```
