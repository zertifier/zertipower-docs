---
title: Predicciones de Consumo
sidebar_label: Predicciones de Consumo
---

## Descripción

Vista diseñada para comparar el consumo eléctrico real con el esperado. Muestra datos horarios sobre el consumo real (kwh_in) y reserva campos para el consumo esperado y la desviación.

## Estructura (upc_consumption_predictions)

| Campo | Descripción |
| --- | --- |
| `id` | Identificador único del registro |
| `cups_id` | Identificador del punto de suministro (CUPS) |
| `expected_consumption_kwh` | Consumo eléctrico esperado (kWh) |
| `real_consumption_kwh` | Consumo eléctrico real registrado (kWh) |
| `deviation_pct` | Porcentaje de desviación entre lo esperado y lo real |
| `info_dt` | Fecha y hora a la que pertenece la información |
