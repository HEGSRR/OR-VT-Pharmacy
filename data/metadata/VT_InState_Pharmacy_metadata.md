- `Title`: VT In-State Pharmacy List
- `Abstract`: 2023 list of active retail pharmacies in Vermont. 
- `Spatial Coverage`: Vermont state
- `Date`: Appears to be last updated in the summer of 2023
- `Lineage`: Data is maintained by Vermont Office of Professional Regulation (OPR). Data is based on professional licenses. 
- `Distribution`: We used the Vermont Secretary of State Office of Professional Regulation feature to Find a Professional, available at this URL: https://sos.vermont.gov/opr/find-a-professional/
From there, we used a Profession Roster Download query with the following parameters:
    - Profession: Pharmacy
    - Profession type: Instate Pharmacy
    - Status: active
The data was downloaded on 9/25/23 in the format of a Microsoft excel .xlsx spreadsheet and contained records for 125 pharmacies.
- `Variables`: Although no metadata is available with the downloaded file, we used the following intuitively named fields for our research:
        - BusinessName
        - Branch Name
        - AddressLine 1
        - AddressLine 2
        - City
        - State
        - ZipCode
