---
title: Bateries
sidebar_label: Bateries
---

## Descripció

Aquesta vista proporciona detalls tècnics sobre les bateries registrades, com ara marca, model, preu, capacitat energètica nominal, cicles de vida i límits de temperatura i càrrega.

## Estructura (upc_batteries)

| Camp | Descripció |
| --- | --- |
| `id` | Identificador únic de la bateria |
| `model` | Model de la bateria |
| `brand` | Marca de la bateria |
| `price` | Preu unitari |
| `total_energy_kwh` | Capacitat energètica nominal (kWh) |
| `max_cycles` | Nombre màxim de cicles de vida |
| `estimated_cycle_cost` | Cost estimat per cicle (Numèric) |
| `max_charge_temp_c` | Temperatura màxima permesa durant la càrrega (°C) |
| `min_charge_temp_c` | Temperatura mínima permesa durant la càrrega (°C) |
| `max_discharge_temp_c` | Temperatura màxima permesa durant la descàrrega (°C) |
| `min_discharge_temp_c` | Temperatura mínima permesa durant la descàrrega (°C) |
| `max_state_of_charge_pct` | Nivell límit de càrrega màxima (%) |
| `min_state_of_charge_pct` | Nivell límit de descàrrega mínima (%) |
| `max_charge_power_kw` | Potència màxima de càrrega (kW) |
| `min_charge_power_kw` | Potència mínima de càrrega (kW) |
| `created_dt` | Data de creació del registre |
