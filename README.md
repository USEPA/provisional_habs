
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
(e.g. R, python, etc.).  The easiest way to download files is right click on the 
links below and select "Save link as...".

- [2021 HABs Data for Shubael and Hamblin Ponds](cc_hab_provisional_data_2021.csv?raw=true)
- [2022 HABs Data for Shubael and Hamblin Ponds](cc_hab_provisional_data_2022.csv?raw=true)

These data are made available with the [Creative Commons Zero Public Domain Dedication](LICENSE.md).

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

# Disclaimer

The United States Environmental Protection Agency (EPA) GitHub project code is provided on an "as is" basis and the user assumes responsibility for its use.  EPA has relinquished control of the information and no longer has responsibility to protect the integrity , confidentiality, or availability of the information.  Any reference to specific commercial products, processes, or services by service mark, trademark, manufacturer, or otherwise, does not constitute or imply their endorsement, recommendation or favoring by EPA.  The EPA seal and logo shall not be used in any manner to imply endorsement of any commercial product or activity by EPA or the United States Government.
