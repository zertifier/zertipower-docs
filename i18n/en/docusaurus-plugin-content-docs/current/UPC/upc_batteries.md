---
title: Batteries
sidebar_label: Batteries
---

## Description

This view provides technical details about registered batteries, such as brand, model, price, nominal energy capacity, life cycles, and temperature/charge limits.

## Structure (upc_batteries)

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
