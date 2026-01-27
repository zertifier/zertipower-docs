---
title: Energia Horària
sidebar_label: Energia Horària
---

## Descripció

Proporciona un desglossament horari de l'energia, detallant el consum (kwh_in), la producció i l'excedent (kwh_out) per a cada punt de subministrament.

## Estructura (upc_energy_hourly)

| Camp | Descripció |
| --- | --- |
| `id` | Identificador únic del registre |
| `cups_id` | Identificador del punt de subministrament (CUPS) |
| `consumption_kwh` | Energia consumida de la xarxa (kWh) - kwh_in |
| `production_kwh` | Energia produïda (kWh) |
| `surplus_kwh` | Excedent d'energia abocat a la xarxa (kWh) - kwh_out |
| `info_dt` | Data i hora del registre d'energia |
