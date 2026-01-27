---
title: Ausencias
sidebar_label: Ausencias
---

## Descripción

Esta vista muestra la información relacionada con las ausencias de los usuarios, incluyendo el identificador, el motivo (si está disponible) y el periodo de tiempo (inicio y fin).

## Estructura (upc_absences)

| Campo | Descripción |
| --- | --- |
| `id` | Identificador único del registro |
| `cups_id` | Identificador del punto de suministro (CUPS) relacionado |
| `reason` | Motivo de la ausencia (puede ser 'Unknown') |
| `start_dt` | Fecha y hora de inicio de la ausencia |
| `end_dt` | Fecha y hora de fin de la ausencia |
