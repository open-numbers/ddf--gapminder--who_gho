# Selected indicators from GHO

Selected Indicators from GHO

To get started with DDF and learn how to use the dataset, please read the
[introduction to DDF][1] and [DDFcsv format document][2].

[1]: https://open-numbers.github.io/ddf.html
[2]: https://docs.google.com/document/d/1aynARjsrSgOKsO1dEqboTqANRD1O9u7J_xmxy8m5jW8

## Indicators

- List of indicators in this repo

## Definition of indicator


## Unit of measurement


## Versions


### Revision history


## Data sources summary


## TODO

### Missing Indicators

The following indicators are requested but could not be found in the source data:

**From mort_100 (total deaths):**

1. **all_causes_deaths_in_children_1_59_months_total_deaths** - No "all causes" entity exists in childcause dimension. May need to be calculated by summing all causes.
2. **all_causes_deaths_in_newborn_total_deaths** - No "all causes" entity exists in childcause dimension. May need to be calculated by summing all causes.
3. **pertussis_deaths_in_children_1_59_months_total_deaths** - No pertussis entity found in childcause dimension. Pertussis might be included in another category or requires a different source indicator.

**From mort_200 (death rates per 1000 births):**

1. **all_causes_deaths_in_children_1_59_months_per_1000_births** - No "all causes" entity exists in childcause dimension. May need to be calculated by summing all causes.
2. **all_causes_deaths_in_newborn_per_1000_births** - No "all causes" entity exists in childcause dimension. May need to be calculated by summing all causes.
3. **pertussis_deaths_in_children_1_59_months_per_1000_births** - No pertussis entity found in childcause dimension. Pertussis might be included in another category or requires a different source indicator.
4. **other_deaths_in_newborn_per_1000_births** - `childcause_ch19` (Other Group 1 and Other noncommunicable) exists in mort_100 (total deaths) but does NOT exist in mort_200 (death rates) for the newborn age group. This is a data availability issue in the source dataset.

**From geo_convention_only (health expenditure indicators):**

1. **ghed_che_pc_ppp_sha2011** - Current health expenditure (CHE) per capita in PPP - Not available in source dataset. Only the US$ version (ghed_che_pc_us_sha2011) exists.
2. **ghed_gghe_d_pc_ppp_sha2011** - Domestic general government health expenditure (GGHE-D) per capita in PPP - Not available in source dataset. Only the US$ version (ghed_gghe_d_pc_us_sha2011) exists.

## Specific information about this indicator

### BMI Indicators (body_mass_index_bmi_men_kgperm2, body_mass_index_bmi_women_kgperm2)

**Important Note on Age Group Selection:**

The source data (ncd_bmi_meanc from WHO GHO) does not contain a standardized "all ages" category. Available age groups in the source data are:
- `agegroup_age20_plus` - 20+ years
- `agegroup_years05_09` - 5-9 years
- `agegroup_years05_19` - 5-19 years
- `agegroup_years10_19` - 10-19 years
- `agegroup_years18_plus` - 18+ years

For this dataset, we use **`agegroup_years18_plus` (18+ years)** as the standardized age group for adult BMI measurements. This is NOT "all ages" but rather represents the adult population (18 years and older).

This choice was made because:
1. BMI is typically measured and interpreted differently for children vs adults
2. The 18+ age group represents a clinically meaningful population for adult BMI assessment
3. No true "all ages" aggregate exists in the source data
