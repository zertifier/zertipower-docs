---
title: CUPS
sidebar_label: CUPS
---

## Description

This view aggregates information about supply points (CUPS), including their type and contracted power for different periods (P1 to P6).

## Structure (upc_cups)

| Field | Description |
| --- | --- |
| `id` | Unique CUPS identifier in the system |
| `cups` | Universal Supply Point Code |
| `type` | Supply type or tariff |
| `category` | CUPS category (Residential, Public lighting, Commercial, Swimming pool...) |
| `p1_contracted_power_kw` | Contracted power in period P1 (kW) |
| `p2_contracted_power_kw` | Contracted power in period P2 (kW) |
| `p3_contracted_power_kw` | Contracted power in period P3 (kW) |
| `p4_contracted_power_kw` | Contracted power in period P4 (kW) |
| `p5_contracted_power_kw` | Contracted power in period P5 (kW) |
| `p6_contracted_power_kw` | Contracted power in period P6 (kW) |
| `created_dt` | Record creation date |
