---
title: CUPS UPC
sidebar_label: upc_cups
---

## Descripció

Aquesta vista agrega informació sobre els punts de subministrament (CUPS), incloent el seu tipus i les potències contractades per als diferents períodes (P1 a P6).

## Estructura

| Camp | Descripció |
| --- | --- |
| `id` | Identificador únic del CUPS al sistema |
| `cups` | Codi Universal de Punt de Subministrament |
| `type` | Tipus de subministrament o tarifa |
| `p1_contracted_power_kw` | Potència contractada en període P1 (kW) |
| `p2_contracted_power_kw` | Potència contractada en període P2 (kW) |
| `p3_contracted_power_kw` | Potència contractada en període P3 (kW) |
| `p4_contracted_power_kw` | Potència contractada en període P4 (kW) |
| `p5_contracted_power_kw` | Potència contractada en període P5 (kW) |
| `p6_contracted_power_kw` | Potència contractada en període P6 (kW) |
| `created_dt` | Data de creació del registre |

## Definició SQL

```sql
SELECT c.id,
    c.cups,
    c.type::character varying AS type,
    COALESCE(cnt.p1_power, 0::numeric) AS p1_contracted_power_kw,
    COALESCE(cnt.p2_power, 0::numeric) AS p2_contracted_power_kw,
    COALESCE(cnt.p3_power, 0::numeric) AS p3_contracted_power_kw,
    COALESCE(cnt.p4_power, 0::numeric) AS p4_contracted_power_kw,
    COALESCE(cnt.p5_power, 0::numeric) AS p5_contracted_power_kw,
    COALESCE(cnt.p6_power, 0::numeric) AS p6_contracted_power_kw,
    c.created_dt
   FROM zertipower.cups c
     LEFT JOIN zertipower.contracts cnt ON c.id = cnt.cups_id;
```
