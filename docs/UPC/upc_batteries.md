---
title: Baterías UPC
sidebar_label: upc_batteries
---

## Descripción

Esta vista proporciona detalles técnicos sobre las baterías registradas, tales como marca, modelo, precio, capacidad energética nominal, ciclos de vida y límites de temperatura y carga.

## Estructura

| Campo | Descripción |
| --- | --- |
| `id` | Identificador único de la batería |
| `model` | Modelo de la batería |
| `brand` | Marca de la batería |
| `price` | Precio de la unidad |
| `total_energy_kwh` | Capacidad energética nominal (kWh) |
| `max_cycles` | Número máximo de ciclos de vida |
| `estimated_cycle_cost` | Coste estimado por ciclo (Numérico) |
| `max_charge_temp_c` | Temperatura máxima permitida durante la carga (°C) |
| `min_charge_temp_c` | Temperatura mínima permitida durante la carga (°C) |
| `max_discharge_temp_c` | Temperatura máxima permitida durante la descarga (°C) |
| `min_discharge_temp_c` | Temperatura mínima permitida durante la descarga (°C) |
| `max_state_of_charge_pct` | Nivel límite de carga máxima (%) |
| `min_state_of_charge_pct` | Nivel límite de descarga mínima (%) |
| `max_charge_power_kw` | Potencia máxima de carga (kW) |
| `min_charge_power_kw` | Potencia mínima de carga (kW) |
| `created_dt` | Fecha de creación del registro |

## Definición SQL

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
