---
title: Precio Energía Horaria UPC
sidebar_label: upc_energy_price_hourly
---

## Descripción

Esta vista muestra el precio de la energía consumida (kwh_in_price) por hora. Filtra los registros donde el precio está disponible.

## Estructura

| Campo | Descripción |
| --- | --- |
| `id` | Identificador único del registro |
| `kwh_price` | Precio del kWh consumido (Moneda local/kWh) |
| `info_dt` | Fecha y hora correspondiente al precio |

## Definición SQL

```sql
SELECT id,
    kwh_in_price AS kwh_price,
    info_dt
   FROM zertipower.energy_hourly eh
  WHERE kwh_in_price IS NOT NULL;
```
