---
title: Predicciones de Producción UPC
sidebar_label: upc_production_predictions
---

## Descripción

Vista para comparar la producción de energía real con la esperada. Muestra la producción real y reserva campos para la producción esperada y el porcentaje de desviación.

## Estructura

| Campo | Descripción |
| --- | --- |
| `id` | Identificador único del registro |
| `cups_id` | Identificador del punto de suministro (CUPS) |
| `expected_production_kwh` | Producción de energía esperada (kWh) |
| `real_production_kwh` | Producción de energía real registrada (kWh) |
| `deviation_pct` | Porcentaje de desviación entre lo esperado y lo real |
| `info_dt` | Fecha y hora a la que pertenece la información |

## Definición SQL

```sql
SELECT id,
    cups_id,
    NULL::numeric AS expected_production_kwh,
    production AS real_production_kwh,
    NULL::numeric AS deviation_pct,
    info_dt
   FROM zertipower.energy_hourly eh;
```
