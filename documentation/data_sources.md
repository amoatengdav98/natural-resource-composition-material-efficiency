# Data sources and indicators

## UNEP International Resource Panel

**Database:** Global Material Flows Database

**Primary access point:** https://www.resourcepanel.org/global-material-flows-database

**Dataset record:** https://energydata.info/en/dataset/world-unep-irp-global-material-flows-database

The study uses material-flow data to construct domestic material consumption per unit of GDP (DMC/GDP) and GDP per unit of material footprint (GDP/MF). The original UNEP-IRP export used during analysis was named mfa_totals_ratios_export.csv.

That source export is not redistributed in this repository. Users can obtain source data through the UNEP-IRP database or the dataset record above, subject to the applicable access, attribution, and reuse terms. The ENERGYDATA.INFO record indicates a CC BY 4.0 licence; users should consult the record and its associated resource details to confirm the terms applicable to the specific data files they access.

## World Bank World Development Indicators

**Database:** World Development Indicators  
**Access point:** https://databank.worldbank.org/source/world-development-indicators  
**API documentation:** https://datahelpdesk.worldbank.org/knowledgebase/articles/889392-about-the-indicators-api-documentation

The analysis uses the following indicator families:

| Variable | Description | WDI indicator code |
|---|---|---|
| Total natural-resource rents (`NRR`) | Total natural resources rents (% of GDP) | `NY.GDP.TOTL.RT.ZS` |
| Oil rents (`Oil`) | Oil rents (% of GDP) | `NY.GDP.PETR.RT.ZS` |
| Natural gas rents (`Gas`) | Natural gas rents (% of GDP) | `NY.GDP.NGAS.RT.ZS` |
| Coal rents (`Coal`) | Coal rents (% of GDP) | `NY.GDP.COAL.RT.ZS` |
| Mineral rents (`Mineral`) | Mineral rents (% of GDP) | `NY.GDP.MINR.RT.ZS` |
| Forest rents (`Forest`) | Forest rents (% of GDP) | `NY.GDP.FRST.RT.ZS` |
| GDP per capita (`GDPpc`) | GDP per capita (constant 2015 US$) | `NY.GDP.PCAP.KD` |
| Industry (`Industry`) | Industry, value added (% of GDP) | `NV.IND.TOTL.ZS` |
| Trade (`Trade`) | Trade (% of GDP) | `NE.TRD.GNFS.ZS` |
| Urban population (`Urban`) | Urban population (% of total population) | `SP.URB.TOTL.IN.ZS` |
| Renewable energy (`Renewable`) | Renewable energy consumption (% of total final energy consumption) | `EG.FEC.RNEW.ZS` |
| Foreign direct investment (`FDI`) | Foreign direct investment, net inflows (% of GDP) | `BX.KLT.DINV.WD.GD.ZS` |

The study period is 2000–2021, reflecting the common period used in the merged analysis and the availability of the resource-rent series. The repository contains derived analysis data rather than the original World Bank indicator exports. Indicator definitions and availability may be updated by the source providers over time.


## Source exports included in this release

The following source exports are preserved in `data/raw/`:

- `unep_irp/mfa_totals_ratios_export.csv` — UNEP-IRP Global Material Flows Database export.
- `world_bank/` — World Bank WDI CSV exports for total natural-resource rents, oil, natural gas, coal, mineral and forest rents, GDP per capita, industry value added, trade openness, urban population, renewable energy consumption, and FDI net inflows.
- `material_flow_indicators/DMC_per_unit_of_GDP_source_export.csv` — additional DMC-per-unit-of-GDP export supplied with the project files. Its original filename is recorded in the file manifest; its exact provenance and relationship to the UNEP-IRP export should be checked against the original download page or metadata before using it as a substitute for the UNEP-IRP series.

Raw files are preserved as supplied and are not silently revised to match the cleaned master dataset.
