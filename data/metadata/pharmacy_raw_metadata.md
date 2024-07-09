- `Title`: Pharmacy raw data (pharmacies_raw)
- `Abstract`: This dataset is primary data that was collected through surveying all VT pharmacies about their staffing levels and hours of operations. It contains information on each VT pharmacy's (117) location, hours of operations on weekdays, Saturdays, and Sundays, and the number of pharmacists and pharmacy technicians that typically work on a given day. It also includes data on the hours of operations of the 75 pharmacies within 10 miles of the VT border (NY, MA, NH). Staffing data was not collected for pharmacies outside of Vermont. Instead, staffing data was interpolated for all out-of-state pharmacies and pharmacies in Vermont for which data could not be collected. There were 192 pharmacies included in our study area in total.
- `Spatial Coverage`: Vermont and ten miles within in Vermont state border, encompassing parts of New York, Massachusetts, and New Hampshire. Canada was excluded.
- `Temporal Coverage`: Data was collected over the course of a couple of months, but it theoretically represents a an average or typical week in the fall or early winter of 2023.
- `Temporal Resolution`: The temporal resolution of service is hours while the temporal resolution of staffing levels is a typical work week. 
- `Lineage`: Initial pharmacy list of 127 pharmacies was downloaded from the Vermont Office of Professional Regulation (https://secure.professionals.vermont.gov/prweb/PRServletCustom?UserIdentifier=LicenseLookupGuestUser) and modified to exclude no longer active pharmacies and non-retail pharmacies. 10 pharmacies on the list were removed, totaling 117 VT pharmacies.  The pharmacy locations were checked against Google Maps and a national pharmacy dataset from the Department of Homeland Security (DHS) to ensure all pharmacies in the state were included. Pharmacy locations outside of Vermont but within study area were included through querying pharmacies from OSM in QGIS, Google Maps searches, and the DHS pharmacy dataset. Pharmacies that had been closed were omitted from the data. Data on hours of operations and staffing were sourced through surveys and manually inputted by the authors. Staffing data was collected for 87% of pharmacies in VT, which was used to interpolate staffing for out-of-state pharmacies. This protocol was approved by the Middlebury College Institutional Review Board (#264). 
- `Distribution`: The majority of this dataset will be made public and downloadable on a GitHub repository. The staffing data will not be made public due to the proprietary nature of this information; however, the staffing data may be available upon request. 
- `Constraints`: We have agreed not to publicly release staffing levels of the pharmacy locations due to the proprietary nature of this data for some of the larger pharmacy chains.
- `Data Quality`: The staffing levels were reported directly from pharmacy staff at each individual pharmacy location or regional headquarters. Therefore, the quality is unknown but is presumed to be high.
- `Variables`:

| Label | Definition | Type |
| :--: | :--: | :--: | 
| pharmid | unique pharmacy identifier | Text| 
| pharmacy_name | business name | Text | 
| type | chain, independent, grocery, department, hospital | Text | 
| address | pharmacy street address | Text |  
| state | state in which pharmacy is located | Text | 
| lat | GPS coordinates. Lat | Decimal | 
| lon | GPS coordinates. Lon | Decimal | 
| week_open | opening time on weekdays | Integer | 
| week_close | closing time on weekdays | Integer |
| sat_open| opening time on Saturdays | Integer | 
| sat_close| closing time operations on Saturdays | Integer |
| sun_hours| opening time on Sundays | Integer | 
| sun_hours| closing time on Sundays | Integer |
| week_pharm| Typical # pharmacists on weekday | Integer | 
| week_tech| Typical # pharm. techs on weekdays  | Integer | 
| sat_pharm| Typical # pharmacists on Saturday | Integer| 
| sat_tech| Typical # pharm. techs on Saturdays  | Integer| 
| sun_pharm| Typical # pharmacists on Sundays | Integer | 
| sun_tech| Typical # pharm. techs on Sundays| Integer| 

  - `Accuracy`: We are confident in the accuracy of the pharmacy list in Vermont. Our confidence in the out-of-state retail pharmacy locations is slightly diminished since these pharmacy locations are not based on a recent dataset from the respective states. We have confidence in the quality of the data on pharmacy staffing and hours of operations for VT pharmacies since we collected the data by surveying all pharmacies. Hours of operations for non-VT pharmacies were pulled from online. The spatial accuracy of the dataset is further confirmed as we ensured that the point coordinates for the pharmacies were within the building footprint polygon on the OSM map layer in QGIS. 
  - `Domain`:  The expected range of all of the pharmacy operational hours is from roughly 7 am to 10 pm. The expected range of pharmacists and technicians is from one to ten for weekdays, Saturdays, and Sundays. 
  - `Missing Data Value(s)`: For any missing data on the number of pharmacists and pharmacy technicians at a given pharmacy location, the values are interpolated based on collected data for pharmacies of the same type. There is no missing data for hours of operations, as operational hours for non-surveyed out-of-state pharmacies were pulled from online. 
  - `Missing Data Frequency`: We were able to collect staffing data for 102 of 117 pharmacies in Vermont.
