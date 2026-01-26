---
title: Preu Energia Horària UPC
sidebar_label: upc_energy_price_hourly
---

## Descripció

Aquesta vista mostra el preu de l'energia consumida (kwh_in_price) per hora. Filtra els registres on el preu està disponible.

## Estructura

| Camp | Descripció |
| --- | --- |
| `id` | Identificador únic del registre |
| `kwh_price` | Preu del kWh consumit (Moneda local/kWh) |
| `info_dt` | Data i hora corresponent al preu |

## Definició SQL

```sql
SELECT id,
    kwh_in_price AS kwh_price,
    info_dt
   FROM zertipower.energy_hourly eh
  WHERE kwh_in_price IS NOT NULL;
```
