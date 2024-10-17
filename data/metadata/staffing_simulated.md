- `Title`: staffing_simulated
- `Abstract`: This synthetic dataset was created to closely mimic the statistical properties of the primary data contained in staffing_interpolated.csv used in the Spatio-Temporal Accessibility of Pharmacy Care in Vermont, USA project (https://doi.org/10.17605/OSF.IO/BCQ9S). The staffing levels of pharmacies in that primary dataset could not be publicly released due to the proprietary nature of this data for some of the larger pharmacy chains. Data were simulated for pharmacists and technician staffing by fiting Poisson generalized linear models with a log link function and identity mean-variance relationship using the package rstanarm v2.21.1. A Bayesian statistical framework was used with models given weakly informed priors. Posterior predictions were then made for the staffing level of each pharmacy using the posterior distibutions for the coefficients and errors of the fitted models.
- `Spatial Coverage`: Vermont and ten miles within in Vermont state border, encompassing parts of New York, Massachusetts, and New Hampshire. Canada was excluded.
- `Spatial Resolution`: NA
- `Spatial Reference System`: NA
- `Temporal Coverage`: Simulated data were created in August 2024. Original staffing data was collected over the course of several of months, but theoretically represents an average or typical week in the fall or early winter of 2023. 
- `Temporal Resolution`: Differential data was collected for weekdays, Saturdays, and Sundays of a typical week. This data is not longitudinal.
- `Lineage`: Phamacy location data were derived from the pharmacy_raw data available on the Spatio-Temporal Accessibility of Pharmacy Care in Vermont, USA project (https://doi.org/10.17605/OSF.IO/BCQ9S). Staffing data used as the basis for simulation were sourced from the restricted staffing_interpolated data of same project. Complete information on both files is contained in their accompanying metadata. Details on the statistical procedures used to generate the dataset and their implementation are available in simulate_pharmacy_staffing.Rmd.  
- `Distribution`: Simulated dataset publicly available on an Open Science Project (https://doi.org/10.17605/OSF.IO/BCQ9S) and GitHub repository (https://github.com/HEGSRR/OR-VT-Pharmacy)
- `Constraints`: There are not contraints on the release and use of this data. The data carries a BSD 3-Clause "New" or "Revised" license.
- `Data Quality`: The regression models informing the simulation achieved moderate model (R^2 of 0.3 to 0.5). Statistical properties (e.g., mean, median, range) and geographic patterns were similar for the simulated and original data. Original staffing data were reported directly from pharmacy staff at each individual pharmacy location or regional headquarters. Therefore, the original quality is unknown but is presumed to be high. Original staffing levels were interpolated for fifteen of 117 pharmacies in VT and all 75 out-of-state pharmacies. 
- `Variables`: For each variable, enter the following information. If you have two or more variables per data source, you may want to present this information in table form (shown below)
  - `Accuracy`: Simulated data is purposely inaccurate, but retains statistical and geogrphic properities similar to those of the original dataset.
  - `Domain`: The expected range of pharmacists and technicians is from one to ten for weekdays, Saturdays, and Sundays.
  - `Missing Data Value(s)`: The file contains no missing data values.
  - `Missing Data Frequency`: The simulated data contain no missing data. However, the original data collected data on 102 of 117 pharmacies in Vermont. The remaining 15 values were interpolated.

| Label | Alias | Definition | Type | Accuracy | Domain | Missing Data Value(s) | Missing Data Frequency |
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |
| pharmid | pharmacy | unique pharmacy identifier | Text | ... | ... | NA | 0 |
| pharmacy_name | name | pharmacy name | Text | ... | ... | NA | 0 |
| address | address | pharmacy address | Text | ... | ... | NA | 0 |
| state | state | state | Text | ... | ... | ... | NA |
| lat | latitude | pharmacy latitude | Double | ... | ... | NA | 0 |
| long | longitude | pharmacy longitude | Double | ... | ... | NA | 0 |
| week_open | ... | weekday opening time | Time | ... | ... | NA | 0 |
| week_close | ... | weekday closing time | Time | ... | ... | NA | 0 |
| sat_open | ... | Saturday opening time | Time | ... | ... | NA | 0 |
| sat_close | ... | Saturday closing time | Time | ... | ... | NA | 0 |
| sun_open | ... | Sunday opening time | Time | ... | ... | NA | 0 |
| sun_close | ... | Sunday closing time | Time | ... | ... | NA | 0 |
| week_sim_staff| weekday-staff | Typical # of staff on weekday | Integer | ... | 0-10 | NA | 0 |
| sat_sim_staff | saturday_staff | Typical # of staff on Saturday | Integer | ... | 0-10 | NA | 0 |
| sun_sim_staff | sunday_staff | Typical # of staff on Sunday | Integer | ... | 0-10 | NA | 0 |