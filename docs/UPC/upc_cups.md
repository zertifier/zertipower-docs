---
title: CUPS UPC
sidebar_label: upc_cups
---

## Descripción

Esta vista agrega información sobre los puntos de suministro (CUPS), incluyendo su tipo y las potencias contratadas para los diferentes periodos (P1 a P6).

## Estructura

| Campo | Descripción |
| --- | --- |
| `id` | Identificador único del CUPS en el sistema |
| `cups` | Código Universal de Punto de Suministro |
| `type` | Tipo de suministro o tarifa |
| `p1_contracted_power_kw` | Potencia contratada en periodo P1 (kW) |
| `p2_contracted_power_kw` | Potencia contratada en periodo P2 (kW) |
| `p3_contracted_power_kw` | Potencia contratada en periodo P3 (kW) |
| `p4_contracted_power_kw` | Potencia contratada en periodo P4 (kW) |
| `p5_contracted_power_kw` | Potencia contratada en periodo P5 (kW) |
| `p6_contracted_power_kw` | Potencia contratada en periodo P6 (kW) |
| `created_dt` | Fecha de creación del registro |

## Definición SQL

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
