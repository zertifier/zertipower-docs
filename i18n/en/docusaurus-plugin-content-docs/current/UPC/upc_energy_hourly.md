---
title: Hourly Energy
sidebar_label: Hourly Energy
---

## Description

Provides an hourly breakdown of energy, detailing consumption (kwh_in), production, and surplus (kwh_out) for each supply point.

## Structure (upc_energy_hourly)

| Field | Description |
| --- | --- |
| `id` | Unique record identifier |
| `cups_id` | Supply point identifier (CUPS) |
| `consumption_kwh` | Energy consumed from the grid (kWh) - kwh_in |
| `production_kwh` | Energy produced (kWh) |
| `surplus_kwh` | Surplus energy exported to the grid (kWh) - kwh_out |
| `info_dt` | Date and time of the energy record |
