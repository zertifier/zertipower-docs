---
title: Absències
sidebar_label: Absències
---

## Descripció

Aquesta vista mostra informació relacionada amb les absències dels usuaris, incloent l'identificador, el motiu (si està disponible) i el període de temps (inici i final).

## Estructura (upc_absences)

| Camp | Descripció |
| --- | --- |
| `id` | Identificador únic del registre |
| `cups_id` | Identificador del punt de subministrament (CUPS) relacionat |
| `reason` | Motiu de l'absència (pot ser 'Unknown') |
| `start_dt` | Data i hora d'inici de l'absència |
| `end_dt` | Data i hora de fi de l'absència |
