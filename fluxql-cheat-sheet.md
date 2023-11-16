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
## What is an FIeld and what is a Measurement
## Data flow
## Selection of measurements, fields and tags

# Data filtering and selection
## Filtering data
## Conditional query

# Transformationen
## Aggregation
## Time manipulation
