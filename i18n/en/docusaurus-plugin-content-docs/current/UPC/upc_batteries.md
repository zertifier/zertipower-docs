---
title: UPC Batteries
sidebar_label: upc_batteries
---

## Description

This view provides technical details about registered batteries, such as brand, model, price, nominal energy capacity, life cycles, and temperature/charge limits.

## Structure

| Field | Description |
| --- | --- |
| `id` | Unique battery identifier |
| `model` | Battery model |
| `brand` | Battery brand |
| `price` | Unit price |
| `total_energy_kwh` | Nominal energy capacity (kWh) |
| `max_cycles` | Maximum life cycles |
| `estimated_cycle_cost` | Estimated cost per cycle (Numeric) |
| `max_charge_temp_c` | Maximum charge temperature (°C) |
| `min_charge_temp_c` | Minimum charge temperature (°C) |
| `max_discharge_temp_c` | Maximum discharge temperature (°C) |
| `min_discharge_temp_c` | Minimum discharge temperature (°C) |
| `max_state_of_charge_pct` | Maximum charge limit (%) |
| `min_state_of_charge_pct` | Minimum discharge limit (%) |
| `max_charge_power_kw` | Maximum charge power (kW) |
| `min_charge_power_kw` | Minimum charge power (kW) |
| `created_dt` | Record creation date |

## SQL Definition

```sql
SELECT id,
    model,
    brand,
    price,
    nominal_energy_kwh AS total_energy_kwh,
    cycles_life AS max_cycles,
    NULL::numeric AS estimated_cycle_cost,
    max_charge_temperature_c AS max_charge_temp_c,
    min_charge_temperature_c AS min_charge_temp_c,
    max_discharge_temperature_c AS max_discharge_temp_c,
    min_discharge_temperature_c AS min_discharge_temp_c,
    charge_limit_level AS max_state_of_charge_pct,
    discharge_limit_level AS min_state_of_charge_pct,
    NULL::numeric AS max_charge_power_kw,
    NULL::numeric AS min_charge_power_kw,
    created_dt
   FROM zertipower.batteries b;
```
