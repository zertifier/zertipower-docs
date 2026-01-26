---
title: Predicciones de Consumo UPC
sidebar_label: upc_consumption_predictions
---

## Descripción

Vista diseñada para comparar el consumo eléctrico real con el esperado. Muestra datos horarios sobre el consumo real (kwh_in) y reserva campos para el consumo esperado y la desviación.

## Estructura

| Campo | Descripción |
| --- | --- |
| `id` | Identificador único del registro |
| `cups_id` | Identificador del punto de suministro (CUPS) |
| `expected_consumption_kwh` | Consumo eléctrico esperado (kWh) |
| `real_consumption_kwh` | Consumo eléctrico real registrado (kWh) |
| `deviation_pct` | Porcentaje de desviación entre lo esperado y lo real |
| `info_dt` | Fecha y hora a la que pertenece la información |

## Definición SQL

```sql
SELECT id,
    cups_id,
    NULL::numeric AS expected_consumption_kwh,
    kwh_in AS real_consumption_kwh,
    NULL::numeric AS deviation_pct,
    info_dt
   FROM zertipower.energy_hourly eh;
```
