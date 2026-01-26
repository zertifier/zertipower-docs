---
title: Prediccions de Producció UPC
sidebar_label: upc_production_predictions
---

## Descripció

Vista per comparar la producció d'energia real amb l'esperada. Mostra la producció real i reserva camps per a la producció esperada i el percentatge de desviació.

## Estructura

| Camp | Descripció |
| --- | --- |
| `id` | Identificador únic del registre |
| `cups_id` | Identificador del punt de subministrament (CUPS) |
| `expected_production_kwh` | Producció d'energia esperada (kWh) |
| `real_production_kwh` | Producción d'energia real registrada (kWh) |
| `deviation_pct` | Percentatge de desviació entre l'esperat i el real |
| `info_dt` | Data i hora a la qual pertany la informació |

## Definició SQL

```sql
SELECT id,
    cups_id,
    NULL::numeric AS expected_production_kwh,
    production AS real_production_kwh,
    NULL::numeric AS deviation_pct,
    info_dt
   FROM zertipower.energy_hourly eh;
```
