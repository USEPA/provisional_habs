
# USEPA Provisional HABs Data for Shubael and Hamblin Ponds

<!-- badges: start -->
<!-- badges: end -->

This repository houses provisional water quality monitoring datasets collected 
from two ponds in Barnstable, MA.  These data are collected to help track, 
understand and eventually forecast potential Harmful Algal Blooms (HABs).  We
use several data sources for this effort which include: data buoys, an on-board,
flow-through system, aka FLAMe, and water samples that are processed in a lab
for various measurements.  The data from these sources are provided here as 
provisional data and they may change.

# Data Access

The provisional data are provided as comma delimited files and are suitable for 
use with spreadsheets or easily read into many common programming languages 
(e.g. R, python, etc.).  The easiest way to download files is follow the 
links below and when you see the data, right click and  select "Save as...".

- [2021 HABs Data for Shubael and Hamblin Ponds](cc_hab_provisional_data_2021.csv?raw=true)
- [2022 HABs Data for Shubael and Hamblin Ponds](cc_hab_provisional_data_2022.csv?raw=true)

These data are made available with the [Creative Commons Zero Public Domain Dedication](LICENSE.md).

As these data are finalized, we expect to make them available via GitHub and as a Zenodo archive.  Additional data papers may be published on these data as well.  Any archives and final data will be documented here.  We expect this to occur once we have 3-4 years of data collected.

# Data Dictionary

| Field Name | Data Type                     | Details                                         |
|------------|-------------------------------|-------------------------------------------------|
| date       | Date                          | The date data was collected: YYYY-MM-DD         |
| time       | Hours, Minutes, Seconds (hms) | The time data was collected: Eastern Time, HH::MM:SS|
| waterbody  | Character                     | Name of the waterbody: shubael or hamblin|
| site       | Character                     | Site identifier within the waterbody: 1-4 or b for the buoy site|
| depth      | Numeric                       | The depth, in meters, the mmeasurement was collected|
| field_dups | Character                     | Field duplicate identifier                      |
| lab_reps   | Character                     | Lab replicate identifier                       |
| device     | Character                     | Identifier for device that collected data       |
| variable   | Character                     | The name of the variable                        |
| units      | Character                     | Units for the variable                          |
| value      | Numeric                       | The measured value                              |
| notes      | Character                     | Notes about the measurement, including QA Flags |

# Automated Quality Control Checks

A number of automated quality control (QC) checks will be run on the data as they are added to the dataset.  As of 2022-11-02, these are limited to data being collected via two water quality buoys.  For these data we use two different checks.  First, we look for values that exceed historic maximums and minimums and second, we identify values that exceed the published ranges of the sensors we are using  The purpose of the historic range checks are to highlight potentially unusual numbers and do not necessarily mean the values should be removed.  We expect hone these checks over time. Values outside of the sensor capabilities would either indicate data that should be removed or data that should be set to the sensor minimums and maximums.  For the provisional datasets we have made no changes to data but instead have flagged these data in the "notes" column.  The historic and published senors ranges are listed below.

| Parameter                      | Units   | Historic Range Check | Detection Limits |
|--------------------------------|---------|----------------------|------------------|
| Nitrate as Nitrogen            | mg/L    | 0.05 - 6             | 0.05 - 6         |
| Water Temperature              | °C      | 6.6 - 29.0           | -5.0 - 50        |
| pH                             |         | 6.2 - 8.6            | 0-14             |
| specific conductivity          | mS/cm   | 0 - 0.14             | 0 - 1            |
| dissolved oxygen concentration | mg/L    | 7.9 - 13.9           | 0 - 50           |
| dissolved oxygen saturation    | percent | 78.1 - 115.3         | 0 - NA           |
| turbidity                      | NTU     | 0.01 - 712.4         | 0 - 4000         |
| chlorophyll                    | RFU     | 0.1 - 100            | 0 - 100          |
| phycocyanin                    | RFU     | 0.1 - 35.4           | 0 - 100          |
| barometric pressure            | in Hg   | 28.8 - 30.5          | 8.9 - 32.4       |
| air temperature                | °C      | -0.9 - 31.4          | -40 - 80         |
| wind speed                     | knots   | 0 - 45.7             | 0 - 77           |
| magnetic wind direction        | degrees | 0-360                | 0-360            |

# Disclaimer

The United States Environmental Protection Agency (EPA) GitHub project code is provided on an "as is" basis and the user assumes responsibility for its use.  EPA has relinquished control of the information and no longer has responsibility to protect the integrity , confidentiality, or availability of the information.  Any reference to specific commercial products, processes, or services by service mark, trademark, manufacturer, or otherwise, does not constitute or imply their endorsement, recommendation or favoring by EPA.  The EPA seal and logo shall not be used in any manner to imply endorsement of any commercial product or activity by EPA or the United States Government.
