# Proposed SAP Solution by Business Unit

## CropCo — Proposed Solution

**Requirement:** Farmer's Agenda, Crop Planner, central financial reporting.

- **SAP S/4HANA Finance (FI/CO)** — replaces paper-based accounting with a central ledger, covering revenue tracking and management reporting.
- **SAP S/4HANA Plant Maintenance (PM)** — machinery maintenance planning for processing centers, supporting Crop Planner optimization.
- **SAP Analytics Cloud (SAC)** — replaces Excel-based reporting with dashboards for account managers, integrating crop yield data from EnvoData.
- **SAP BTP Integration Suite** — connects CropCo with EnvoData's data feeds and TransCrop's fleet data to power the Farmer's Agenda.

**Open questions:** How are account manager KPIs tracked today? What local plant data needs to be migrated to the central system?

**Readiness: LOW** — Excel and paper-based reporting today, no ERP system in place, data scattered across plants with local retention policies.

## TransCrop — Proposed Solution

**Requirement:** Fleet Calendar, Shipments Planner, Farmer Bookkeeper.

- **SAP Transportation Management (TM)** — replaces the legacy 1980s SCM system, enabling real-time shipment tracking, re-routing, and cost updates across all operating countries.
- **SAP Analytics Cloud Planning** — powers the Farmer Bookkeeper with commodity market data feeds and revenue forecasting based on EnvoData yield estimates.
- **SAP BTP Integration Suite** — feeds GPS data (where available) into the Shipments Planner and integrates with the existing commodities trading system.

**Open questions:** GPS coverage is currently absent in some operating regions, is a rollout timeline confirmed? Should the existing commodities trading system be retained or replaced?

**Readiness: MEDIUM** — legacy SCM system needs replacement, GPS coverage is partial, coordination currently relies on phone and email.

## EnvoData — Proposed Solution

**Requirement:** Farming Planner with GIS, drone imagery, weather forecasting, and carbon impact tracking.

EnvoData already runs SAP S/4HANA and serves as the central capability provider for the other two business units.

- **SAP HANA Spatial Services** — GIS integration for field mapping and drone data ingestion alongside the existing HANA environment.
- **SAP Predictive Analytics Library (PAL)** — machine learning for crop yield prediction, pest risk, and extreme weather alerts.
- **SAP Analytics Cloud Stories** — visual land, weather, and yield dashboards with simulation and carbon impact reporting.
- **SAP BTP AI Core** — for deploying custom machine learning models on drone and satellite imagery.

**Readiness: HIGH** — S/4HANA is up to date, SAP Solution Manager is configured with change and business process management, and data cleansing processes are already in place. Remaining gaps: data provisioning tooling not yet in place, and the BW on HANA end-of-life migration noted in the gap analysis.

## Summary

The three business units sit at very different points on the SAP maturity curve, from CropCo's paper-based processes to EnvoData's established S/4HANA environment. This is a common pattern in multi-entity implementations: the technical design has to account for bringing units onto a shared landscape at different starting points, not assume a uniform baseline.
