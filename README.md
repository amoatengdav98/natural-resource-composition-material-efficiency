# Does the Composition of Natural-Resource Dependence Matter for Material Efficiency? Evidence from a Global Panel

Research data and analysis materials for a cross-country panel study of natural-resource rent composition and material efficiency over 2000–2021.

## Study overview

The study combines material-flow indicators from the United Nations Environment Programme International Resource Panel (UNEP-IRP) Global Material Flows Database with macroeconomic and natural-resource-rent indicators from the World Bank's World Development Indicators (WDI).

The principal outcome is domestic material consumption per unit of GDP (`DMC/GDP`), where higher values indicate greater material intensity. An alternative outcome is GDP per unit of material footprint (`GDP/MF`), where higher values indicate greater material productivity. The analysis compares aggregate natural-resource rents with five components: oil, gas, coal, mineral, and forest rents.

## Repository contents

- `data/processed/` — cleaned master panel dataset.
- `data/analysis_samples/` — exported analysis samples and model-input datasets for baseline, resource-composition, and material-footprint specifications.
- `notebooks/` — Jupyter notebook documenting data checks, diagnostics, fixed-effects regressions, and robustness analyses.
- `results/audits/` — data audit and country-availability audit workbooks.
- `documentation/` — source descriptions, sample-selection rules, and a file manifest.
- `requirements.txt` — Python package dependencies.

## Data coverage and sample sizes

The merged master dataset contains 4,390 country-year observations for 201 countries/economies over 2000–2021. Estimation samples are specification-specific:

| Specification | Observations | Countries |
|---|---:|---:|
| DMC/GDP baseline | 3,120 | 143 |
| DMC/GDP resource composition | 3,004 | 138 |
| GDP/material-footprint aggregate | 2,821 | 129 |
| GDP/material-footprint resource composition | 2,727 | 125 |

The sample-selection documentation explains complete-case selection, the minimum of 18 usable annual observations per country, and the exclusion of non-positive `DMC/GDP` values from models that take its natural logarithm.

## Data sources

- UNEP-IRP Global Material Flows Database: https://www.resourcepanel.org/global-material-flows-database
- World Bank World Development Indicators: https://databank.worldbank.org/source/world-development-indicators
- World Bank indicator metadata and API: https://datahelpdesk.worldbank.org/knowledgebase/articles/889392-about-the-indicators-api-documentation

The repository includes the cleaned master dataset, analysis samples, model-input datasets, audit workbooks, and the source-export files supplied for this release. The original World Bank WDI indicator exports are in `data/raw/world_bank/`; the UNEP-IRP Global Material Flows Database export is in `data/raw/unep_irp/`; and the separate DMC-per-unit-of-GDP export is in `data/raw/material_flow_indicators/`. File-level checksums and tabular dimensions are recorded in `documentation/file_manifest.csv`. Source files are preserved as received. Their inclusion does not imply that every current online observation is identical to the historical download used in the original analysis; see `documentation/data_verification.md`.

## Analysis environment

Python 3.10 or later is recommended. Install the packages listed in `requirements.txt`, then launch Jupyter from the repository root and open:

`notebooks/Natural_Resource_Dependence_Material_Efficiency_Analysis.ipynb`

The notebook uses project-relative paths for repository files. The UNEP-IRP source export is referenced in an optional source-validation cell; if the original export is not present locally, the notebook reports that source-level validation is skipped and continues using the included cleaned master dataset.

## Data treatment

The documented workflow does not use interpolation or mean imputation. Legitimate zero natural-resource rents are retained. Complete-case requirements are applied by model specification. Non-positive `DMC/GDP` observations are not eligible for logarithmic dependent-variable regressions.

## Citation

When using this repository, cite the study as:

Amoateng, D. (2026). *Does the Composition of Natural-Resource Dependence Matter for Material Efficiency? Evidence from a Global Panel*. Research data and analysis repository.

A DOI can be added to the citation metadata when a version is archived with a DOI-issuing repository.
