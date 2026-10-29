# Sample selection and model definitions

## Study period and master dataset

The merged master panel covers 2000–2021 and contains 4,390 country-year observations for 201 countries/economies. Country-year keys are unique in the master dataset.

## Analysis samples

The study constructs separate samples for each model family, based on the availability of the outcome, resource-rent variables, and controls required by the relevant specification. Countries are retained when they have at least 18 usable annual observations.

| Specification | Observations | Countries |
|---|---:|---:|
| DMC/GDP baseline | 3,120 | 143 |
| DMC/GDP resource composition | 3,004 | 138 |
| GDP/material-footprint aggregate | 2,821 | 129 |
| GDP/material-footprint resource composition | 2,727 | 125 |

The `FINAL_*_SAMPLE` files preserve the broader country-eligibility samples. For the DMC/GDP baseline and composition samples, these files contain 3,124 and 3,008 rows, respectively. The corresponding logarithmic regressions use 3,120 and 3,004 observations because four rows in each sample have non-positive `DMC/GDP`, which cannot be transformed using the natural logarithm. The `MODEL_*` files are separate exported inputs and may reflect different complete-case criteria; model-specific estimation counts are reported in the analysis notebook and study text.

## Variables and transformations

- `DMC/GDP`: domestic material consumption per unit of GDP; the principal dependent variable is its natural logarithm.
- `GDP/MF`: GDP per unit of material footprint; used as an alternative material-productivity outcome.
- `NRR`: total natural-resource rents as a percentage of GDP.
- `Oil`, `Gas`, `Coal`, `Mineral`, `Forest`: resource-rent components as percentages of GDP.
- `GDPpc`, `Industry`, `Trade`, `Urban`, `Renewable`, `FDI`: macroeconomic and structural controls.

The aggregate-rent specification uses the inverse hyperbolic sine transformation of total rents. The resource-composition specification includes the five rent components separately. The aggregate rent and its components are not entered simultaneously in the same specification.

## Missing values and non-positive observations

The documented analysis does not apply interpolation or mean imputation. Legitimate zero resource-rent values are retained. Complete-case selection is specification-specific. Observations with non-positive `DMC/GDP` are excluded only from models requiring the natural logarithm of that outcome; they remain in the underlying data.
