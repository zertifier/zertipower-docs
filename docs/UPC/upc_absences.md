---
title: Ausencias UPC
sidebar_label: upc_absences
---

## Descripción

Esta vista muestra la información relacionada con las ausencias de los usuarios, incluyendo el identificador, el motivo (si está disponible) y el periodo de tiempo (inicio y fin).

## Estructura

| Campo | Descripción |
| --- | --- |
| `id` | Identificador único del registro |
| `cups_id` | Identificador del punto de suministro (CUPS) relacionado |
| `reason` | Motivo de la ausencia (puede ser 'Unknown') |
| `start_dt` | Fecha y hora de inicio de la ausencia |
| `end_dt` | Fecha y hora de fin de la ausencia |

## Definición SQL

```sql
SELECT id,
    cups_id,
    COALESCE(reference, 'Unknown'::character varying) AS reason,
    start_dt,
    end_dt
   FROM zertipower.vacations v;
```
