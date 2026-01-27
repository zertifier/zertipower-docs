---
title: Baterías
sidebar_label: Baterías
---

## Descripción

Esta vista proporciona detalles técnicos sobre las baterías registradas, tales como marca, modelo, precio, capacidad energética nominal, ciclos de vida y límites de temperatura y carga.

## Estructura (upc_batteries)

| Campo | Descripción |
| --- | --- |
| `id` | Identificador único de la batería |
| `model` | Modelo de la batería |
| `brand` | Marca de la batería |
| `price` | Precio de la unidad (€) |
| `total_energy_kwh` | Capacidad energética nominal (kWh) |
| `max_cycles` | Número máximo de ciclos de vida |
| `estimated_cycle_cost` | Coste estimado por ciclo (€) |
| `max_charge_temp_c` | Temperatura máxima permitida durante la carga (°C) |
| `min_charge_temp_c` | Temperatura mínima permitida durante la carga (°C) |
| `max_discharge_temp_c` | Temperatura máxima permitida durante la descarga (°C) |
| `min_discharge_temp_c` | Temperatura mínima permitida durante la descarga (°C) |
| `max_state_of_charge_pct` | Nivel límite de carga máxima (%) |
| `min_state_of_charge_pct` | Nivel límite de descarga mínima (%) |
| `max_charge_power_kw` | Potencia máxima de carga (kW) |
| `min_charge_power_kw` | Potencia mínima de carga (kW) |
| `created_dt` | Fecha de creación del registro |
