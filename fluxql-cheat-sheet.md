# Basic of FluxQL
## Syntax
```
from(bucket: "Bucket Name")
  |> range(start: v.timeRangeStart, stop: v.timeRangeStop)
  |> filter(fn: (r) => r["_measurement"] == "Measurement Name")
  |> filter(fn: (r) => r["_field"] == "Field Name")
```
We select data from the bucket "Bucket Name". ```from(bucket: "Bucket Name")``` <br>
We only select data which is in the set time range. ```|> range(start: v.timeRangeStart, stop: v.timeRangeStop)``` <br>
We filter the selected data for the Measurement "Measurement Name". ```|> filter(fn: (r) => r["_measurement"] == "Measurement Name")``` <br>
We filter the selcted data for the field "Field Name". ```|> filter(fn: (r) => r["_field"] == "Field Name")``` <br>

## Definition
| <!-- -->      | <!-- -->        |
|:-------------:|:---------------:|
| Measurement | Category of data, similar to tables in a database (set in telegraf) |
| Field | Actual data within a measurement, like columns in a table (set in telegraf) |
| Tag | Extra metadata adding context to measurements for better categorization and filtering |

## Data flow
## Selection of measurements, fields and tags

# Data filtering and selection
## Filtering data
## Conditional query

# Transformationen
## Aggregation
## Time manipulation
