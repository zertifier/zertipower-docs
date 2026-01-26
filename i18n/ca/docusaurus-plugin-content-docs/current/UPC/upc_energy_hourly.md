---
title: Energia Horària UPC
sidebar_label: upc_energy_hourly
---

## Descripció

Proporciona un desglossament horari de l'energia, detallant el consum (kwh_in), la producció i l'excedent (kwh_out) per a cada punt de subministrament.

## Estructura

| Camp | Descripció |
| --- | --- |
| `id` | Identificador únic del registre |
| `cups_id` | Identificador del punt de subministrament (CUPS) |
| `consumption_kwh` | Energia consumida de la xarxa (kWh) - kwh_in |
| `production_kwh` | Energia produïda (kWh) |
| `surplus_kwh` | Excedent d'energia abocat a la xarxa (kWh) - kwh_out |
| `info_dt` | Data i hora del registre d'energia |

## Definició SQL

```sql
SELECT id,
    cups_id,
    kwh_in AS consumption_kwh,
    production AS production_kwh,
    kwh_out AS surplus_kwh,
    info_dt
   FROM zertipower.energy_hourly eh;
```
