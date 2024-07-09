- `Title`: Staffing Interpolated (staffing_interpolated.csv)
- `Abstract`: This dataset is primary data that was collected through surveying all VT pharmacies about their staffing levels. It contains information on the number of pharmacists and pharmacy technicians that typically work on a given day at each retail pharmacy in VT (117). It also includes data on the staffing levels of the 75 pharmacies within 10 miles of the VT border (NY, MA, NH). Staffing data was not collected for pharmacies outside of Vermont. Instead, staffing data was interpolated for all out-of-state pharmacies and pharmacies in Vermont for which data could not be collected. There were 192 pharmacies included in our study area in total. Staffing was interpolated for all 75-out-of-state pharmacies and 15 of the 117 in-state pharmacies. 
- `Spatial Coverage`: Vermont and ten miles within in Vermont state border, encompassing parts of New York, Massachusetts, and New Hampshire. Canada was excluded.
- `Spatial Resolution`: NA
- `Spatial Reference System`: NA
- `Temporal Coverage`: Data was collected over the course of a couple of months, but it theoretically represents an average or typical week in the fall or early winter of 2023.
- `Temporal Resolution`: A week. Differential data was collected for weekdays, Saturdays, and Sundays of a typical week.
- `Lineage`: Staffing data extracted from pharmacies_raw.csv. This dataset was created using the 00_pharmacy_cleaning.Rmd, which ultimately interpolated missing staffing data and extracted a dataframe with just the staffing levels. All department store and chain grocery store pharmacies were grouped with pharmacy chains like CVS, as these had more similar staffing models. The number of pharmacists and technicians was then averaged by day of the week and used to fill-in missing data. Hospital / clinic and independent pharmacies were aggregated as they had similar staffing models. We had to aggregate since sample size was too small for each pharmacy type individually. View process in procedure/code/00_pharmacy_cleaning.Rmd . 
- `Distribution`: This staffing data will not be made public due to the proprietary nature of this information; however, the staffing data may be available upon request.
- `Constraints`: We have agreed not to publicly release staffing levels of the pharmacy locations due to the proprietary nature of this data for some of the larger pharmacy chains.
- `Data Quality`: Staffing data was interpolated for fifteen of 117 pharmacies in VT. Staffing data was interpolated for all 75 out-of-state pharmacies. The staffing data were reported directly from pharmacy staff at each individual pharmacy location or regional headquarters. Therefore, the quality is unknown but is presumed to be high.
- `Variables`:

| Label | Definition | Type |
| :--: | :--: | :--: |
| pharmid | unique pharmacy identifier | Text|
| week_pharm| Typical # pharmacists on weekday | Integer |
| week_tech| Typical # pharm. techs on weekdays  | Integer |
| sat_pharm| Typical # pharmacists on Saturday | Integer|
| sat_tech| Typical # pharm. techs on Saturdays  | Integer|
| sun_pharm| Typical # pharmacists on Sundays | Integer |
| sun_tech| Typical # pharm. techs on Sundays| Integer|


  - `Accuracy`: Data was interpolated for 15 of the 117 retail pharmacies in VT, and all 75 out-of-state pharmacies. Data accuracy for out-of-state pharmacies is less important since these pharmacies were just included to minimize edge effects in our study (they are less utilized by VT residents). 
  - `Domain`: The expected range of pharmacists and technicians is from one to ten for weekdays, Saturdays, and Sundays.
  - `Missing Data Value(s)`: For any missing data on the number of pharmacists and pharmacy technicians at a given pharmacy location, the values are interpolated based on collected data for pharmacies of the same type. There is no missing data for hours of operations, as operational hours for non-surveyed out-of-state pharmacies were pulled from online.
  - `Missing Data Frequency`: We were able to collect staffing data for 102 of 117 pharmacies in Vermont.
