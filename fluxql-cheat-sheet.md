# Basic of FluxQL
## Syntax
```
from(bucket: "Bucket Name")
  |> range(start: v.timeRangeStart, stop: v.timeRangeStop)
  |> filter(fn: (r) => r["_measurement"] == "Measurement Name")
  |> filter(fn: (r) => r["_field"] == "Field Name")
```
Select Data: Fetch data from the "Bucket Name" bucket. <br>
Set Time Range: Define the time range using v.timeRangeStart and v.timeRangeStop.
Filter by Measurement: Filter data where _measurement is "Measurement Name".
Filter by Field: Further filter data by _field "Field Name".

## Data flow
## Selection of measurements, fields and tags

# Data filtering and selection
## Filtering data
## Conditional query

# Transformationen
## Aggregation
## Time manipulation
