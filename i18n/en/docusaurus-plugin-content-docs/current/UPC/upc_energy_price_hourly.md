---
title: UPC Hourly Energy Price
sidebar_label: upc_energy_price_hourly
---

## Description

This view shows the price of consumed energy (kwh_in_price) per hour. It filters records where the price is available.

## Structure

| Field | Description |
| --- | --- |
| `id` | Unique record identifier |
| `kwh_price` | Price per kWh consumed (Local currency/kWh) |
| `info_dt` | Date and time corresponding to the price |

## SQL Definition

```sql
SELECT id,
    kwh_in_price AS kwh_price,
    info_dt
   FROM zertipower.energy_hourly eh
  WHERE kwh_in_price IS NOT NULL;
```
