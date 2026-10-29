# Data verification and updates

This repository documents the data and analysis used for the study *Does the Composition of Natural-Resource Dependence Matter for Material Efficiency? Evidence from a Global Panel*.

## Verification principles

- Original source exports are preserved as downloaded and are not overwritten by cleaned or harmonised files.
- Each source file is documented with its provider, dataset or indicator name, access date, download date when known, and original filename.
- Derived datasets are generated separately from raw inputs.
- Country/economy identifiers and years are checked before merging; duplicate country-year keys and unexpected changes in row counts are investigated.
- Variable definitions, units, missing-value conventions, and zero values are checked against source metadata.
- Sample sizes are compared with the documented analysis samples and regression outputs.
- Transformations and exclusions, including the exclusion of non-positive `DMC/GDP` values from logarithmic models, are documented.
- Changes to source data, indicator metadata, code, or sample definitions are recorded in version-control history and summarised in release notes.

## Updating source data

Source databases may revise historical observations or metadata. A newer download should therefore be stored as a new, dated source version rather than silently replacing the file used for an earlier analysis. Re-running the data pipeline against a newer version may change country coverage, observations, estimates, or reported sample sizes. Such changes should be assessed and documented before the updated data are treated as a new analysis release.

## Current release scope

The repository now includes the source exports supplied for this release, including the UNEP-IRP material-flow export, World Bank indicator exports, and a separate DMC-per-unit-of-GDP export. The source-to-master workflow has not yet been fully rerun end to end from these raw files. Accordingly, this release includes raw and derived data together, but the master dataset should not be described as independently reproduced from raw inputs until that pipeline has been executed and its outputs reconciled.
