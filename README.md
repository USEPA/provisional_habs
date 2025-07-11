
# Provisional Harmful Algal Bloom research data

<!-- badges: start -->
<!-- badges: end -->

This repository houses provisional water quality monitoring datasets collected 
from Lake Archer in Wrentham, MA and Mashapaug Pond in Providence, RI.  These 
data are collected to help track, understand and eventually forecast potential 
Harmful Algal Blooms (HABs).  We use several data sources for this effort which 
include: data buoys, an on-board, flow-through system, aka FLAMe, and water 
samples that are processed in a lab for various measurements.  The data from 
these sources are provided here as provisional data and they may change. While 
the data provided here have had quality control checks applied, these data are 
considered provisional in nature. Quality checks may be updated during the 
course of the research study based upon new findings about the measurement 
technology. Final data versions may incorporate additional quality control 
checks after further analysis.

# Provisional Data Access

The provisional data are provided as comma delimited files and are suitable for 
use with spreadsheets or easily read into many common programming languages 
(e.g., R, Python).  The easiest way to download files is follow the 
links below and when you see the data, right click and  select "Save as...".

- [2025 Provisional Data File](https://github.com/USEPA/provisional_habs/raw/main/hab_provisional_data_2025.csv)
- [2024 Provisional Data File](https://github.com/USEPA/provisional_habs/raw/main/hab_provisional_data_2024.csv)

These data are made available with the [Creative Commons Zero Public Domain Dedication](LICENSE.md).

Final data associated with publications, after EPA clearance and peer review, are expected to be available through data.gov. We will update this GitHub site to point to final data, when available, which we expect to occur after several years of data collection.

# Data Dictionary

| Field Name| Data Type| Description                                     |Details/Possible Values|
|-----------|----------|-------------------------------------------------|-----------------------|
| date      | date     | The date data were collected                     |YYYY-MM-DD             |
| time      | hms      | The time data were collected                     |Eastern Time, HH::MM:SS|
| waterbody | character| Name of the waterbody                           |archer or mashapaug     |
| site      | character| Site identifier within the waterbody            |1-4 or b for the buoy site|
| depth     | character| Depth, in meters, the measurement was collected |0-20, or integrated    |
| field_dups| numeric  | Field duplicate identifier                      |1-3,                   |
| lab_reps  | numeric  | Lab replicate identifier                        |1-3,                   |  
| device    | character| Identifier for device that collected data       |cb150, turner, flame, plate, cube, scope|
| variable  | character| The name of the variable                        |no3-n, water temperature, ph, specific conductivity, dissolved oxygen sat., dissolved oxygen conc., turbidity, chlorophyll, phycocyanin, barometric pressure, air temperature, wind direction, wind speed|
| units     | character| Units for the variable                          |mg/L, °C, mS/cm, percent, NTU, RFU, in Hg, degrees, knots|
| value     | numeric  | The measured value                              ||
| notes     | character| Notes about the measurement, including QA Flags |value less than historic minimum, value less than minimum detection limit, value greater than sensor maximum, value greater than historic maximum|

# Automated Quality Control Checks

A number of automated quality control (QC) checks will be run on the data as they are added to the dataset.  For these data, we use two different checks.  First, we look for values that exceed historic maximums and minimums; second, we identify values that exceed the sensor manufacturer reported detection limits for the sensors we are using.  The purpose of the historic range checks are to highlight potentially unusual numbers and do not necessarily mean the values should be removed.  Values outside of the sensor capabilities would either indicate data that should be removed or data that should be set to the sensor minimums and maximums.  For the provisional datasets, we have made no changes to data but instead have flagged these data in the "notes" column.  The historic and sensor manufacturer reported detection limits for the sensors we are using are listed below.

| Variable             | Units  | Historic Range Check | Sensor Manufacturer Detection Limits |
|----------------------|--------|----------------------|------------------|
|no3-n                 | mg/L   | 0.05 - 6             | 0.05 - 6         |
|water temperature     | °C     | 6.6 - 29.0           | -5.0 - 50        |
|ph                    |        | 6.2 - 8.6            | 0-14             |
|specific conductivity | mS/cm  | 0 - 0.14             | 0 - 1            |
|dissolved oxygen conc.| mg/L   | 7.9 - 13.9           | 0 - 50           |
|dissolved oxygen sat. | percent| 78.1 - 115.3         | 0 - NA           |
|turbidity             | NTU    | 0.01 - 712.4         | 0 - 4000         |
|chlorophyll           | RFU    | 0.1 - 100            | 0 - 100          |
|phycocyanin           | RFU    | 0.1 - 35.4           | 0 - 100          |
|barometric pressure   | in Hg  | 28.8 - 30.5          | 8.9 - 32.4       |
|air temperature       | °C     | -0.9 - 31.4          | -40 - 80         |
|wind speed            | knots  | 0 - 45.7             | 0 - 77           |
|wind direction        | degrees| 0-360                | 0-360            |

# Disclaimer

The United States Environmental Protection Agency (EPA) GitHub project code is provided on an "as is" basis and the user assumes responsibility for its use.  EPA has relinquished control of the information and no longer has responsibility to protect the integrity, confidentiality, or availability of the information.  Any reference to specific commercial products, processes, or services by service mark, trademark, manufacturer, or otherwise, does not constitute or imply their endorsement, recommendation or favoring by EPA.  The EPA seal and logo shall not be used in any manner to imply endorsement of any commercial product or activity by EPA or the United States Government.

The spatial and temporal HAB provisional data are not fully verified and validated through the quality assurance procedures and, therefore, cannot be used to formulate or support regulation, guidance or any other Agency decision or position.