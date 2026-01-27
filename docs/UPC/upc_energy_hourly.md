---
title: Energía Horaria
sidebar_label: Energía Horaria
---

## Descripción

Proporciona un desglose horario de la energía, detallando el consumo (kwh_in), la producción y el excedente (kwh_out) para cada punto de suministro.

## Estructura (upc_energy_hourly)

| Campo | Descripción |
| --- | --- |
| `id` | Identificador único del registro |
| `cups_id` | Identificador del punto de suministro (CUPS) |
| `consumption_kwh` | Energía consumida de la red (kWh) - kwh_in |
| `production_kwh` | Energía producida (kWh) |
| `surplus_kwh` | Excedente de energía vertido a la red (kWh) - kwh_out |
| `info_dt` | Fecha y hora del registro de energía |
