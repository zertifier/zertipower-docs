---
title: Energía Horaria UPC
sidebar_label: upc_energy_hourly
---

## Descripción

Proporciona un desglose horario de la energía, detallando el consumo (kwh_in), la producción y el excedente (kwh_out) para cada punto de suministro.

## Estructura

| Campo | Descripción |
| --- | --- |
| `id` | Identificador único del registro |
| `cups_id` | Identificador del punto de suministro (CUPS) |
| `consumption_kwh` | Energía consumida de la red (kWh) - kwh_in |
| `production_kwh` | Energía producida (kWh) |
| `surplus_kwh` | Excedente de energía vertido a la red (kWh) - kwh_out |
| `info_dt` | Fecha y hora del registro de energía |

## Definición SQL

```sql
SELECT id,
    cups_id,
    kwh_in AS consumption_kwh,
    production AS production_kwh,
    kwh_out AS surplus_kwh,
    info_dt
   FROM zertipower.energy_hourly eh;
```
