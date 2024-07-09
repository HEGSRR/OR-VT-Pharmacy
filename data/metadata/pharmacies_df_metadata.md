- `Title`: All non-staffing pharmacy data (pharmacies_df.gpkg)
- `Abstract`: Same as pharmacies_raw.csv without staffing data. 
- `Spatial Coverage`: Vermont and ten miles within in Vermont state border, encompassing parts of New York, Massachusetts, and New Hampshire. Canada was excluded.
- `Temporal Coverage`: Data was collected over the course of a couple of months, but it theoretically represents a an average or typical week in the fall or early winter of 2023.
- `Temporal Resolution`: The temporal resolution of service is hours. 
- `Lineage`: Data extracted from pharmacies_raw.csv using the code 00_pharmacy_cleaning.Rmd . This R markdown file converted operational hours originally reported on the 24-hour clock to integers for easier analysis and extracted all non-staffing data for analysis. The exported .csv was then converted into a .gpkg file in QGIS. View process in procedure/code/00_pharmacy_cleaning.Rmd 
- `Distribution`: This dataset will be made public and downloadable on a GitHub repository
- `Constraints`: NA
- `Data Quality`: The hours of operations were reported directly from pharmacy staff at each individual pharmacy location. Hours of operations for pharmacies that declined to be surveyed were pulled from online. 
- `Variables`:

| Label | Definition | Type |
| :--: | :--: | :--: | 
| pharmid | unique pharmacy identifier | Text| 
| pharmacy_name | business name | Text | 
| type | chain, independent | Text | 
| address | pharmacy street address | Text |  
| state | state in which pharmacy is located | Text | 
| lat | GPS coordinates. Lat | Decimal | 
| lon | GPS coordinates. Lon | Decimal | 
| week_open | opening time on weekdays | Integer | 
| week_close | closing time on weekdays | Integer |
| sat_open| opening time on Saturdays | Integer | 
| sat_close| closing time on Saturdays | Integer |
| sun_open| opening time on Sundays | Integer | 
| sun_close| closing time on Sundays | Integer |

  - `Accuracy`: We have confidence in the quality of the data on hours of operations for VT pharmacies since we collected the data by surveying all pharmacies. Hours of operations for non-VT pharmacies were pulled from online. The spatial accuracy of the dataset is further confirmed as we ensured that the point coordinates for the pharmacies were within the building footprint polygon on the OSM map layer in QGIS. 
  - `Domain`:  The expected range of all of the pharmacy operational hours is from roughly 7 am to 10 pm. 
  - `Missing Data Value(s)`: There is no missing data for hours of operations, as operational hours for non-surveyed out-of-state pharmacies were pulled from online. 
  - `Missing Data Frequency`: No missing data for hours of operations. 
