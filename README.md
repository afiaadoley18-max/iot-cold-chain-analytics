# iot-cold-chain-analytics

Temperature monitoring for cold-chain storage: an ESP32 sensor node posts readings to Postgres, SQL views flag temperature excursions, and a Tableau Public dashboard shows the results.

> **Status:** data is currently **simulated**. Real device data will replace it once the hardware is built.

## Architecture
ESP32 + sensor → HTTPS POST (JSON) → Postgres (Supabase) → SQL views → CSV/Google Sheets → Tableau Public

## Repo layout
- `firmware/` – ESP32 code (C/C++)
- `sql/` – schema and analysis queries
- `dashboard/` – exported CSVs and Tableau workbook
- `docs/` – wiring diagram, photos, notes

## Analysis
- Hourly average, min and max per device
- Excursions above threshold (default 4 °C)
- Longest unbroken excursion per day

## Demo
_Video and dashboard link to be added._
