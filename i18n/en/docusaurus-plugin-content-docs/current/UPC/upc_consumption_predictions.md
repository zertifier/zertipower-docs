---
title: Consumption Predictions
sidebar_label: Consumption Predictions
---

## Description

View designed to compare real electricity consumption with expected consumption. It shows hourly data on real consumption (kwh_in) and reserves fields for expected consumption and deviation.

## Structure (upc_consumption_predictions)

| Field | Description |
| --- | --- |
| `id` | Unique record identifier |
| `cups_id` | Supply point identifier (CUPS) |
| `expected_consumption_kwh` | Expected electricity consumption (kWh) |
| `real_consumption_kwh` | Real electricity consumption recorded (kWh) |
| `deviation_pct` | Deviation percentage between expected and real |
| `info_dt` | Date and time for the records |
