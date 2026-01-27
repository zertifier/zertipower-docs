---
title: Prediccions de Consum
sidebar_label: Prediccions de Consum
---

## Descripció

Vista dissenyada per comparar el consum elèctric real amb l'esperat. Mostra dades horàries sobre el consum real (kwh_in) i reserva camps per al consum esperat i la desviació.

## Estructura (upc_consumption_predictions)

| Camp | Descripció |
| --- | --- |
| `id` | Identificador únic del registre |
| `cups_id` | Identificador del punt de subministrament (CUPS) |
| `expected_consumption_kwh` | Consum elèctric esperat (kWh) |
| `real_consumption_kwh` | Consum elèctric real registrat (kWh) |
| `deviation_pct` | Percentatge de desviació entre l'esperat i el real |
| `info_dt` | Data i hora a la qual pertany la informació |
