# Basic of FluxQL
## Syntax
```
from(bucket: "Bucket Name")
  |> range(start: v.timeRangeStart, stop: v.timeRangeStop)
  |> filter(fn: (r) => r["_measurement"] == "Measurement Name")
  |> filter(fn: (r) => r["_field"] == "Field Name")
```
```from(bucket: "Bucket Name")``` We select data from the bucket "Bucket Name". <br>
```|> range(start: v.timeRangeStart, stop: v.timeRangeStop)``` We only select data which is in the set time range. <br>
```|> filter(fn: (r) => r["_measurement"] == "Measurement Name")``` We filter the selected data for the Measurement "Measurement Name". <br>
```|> filter(fn: (r) => r["_field"] == "Field Name")``` We filter the selcted data for the field "Field Name". <br>
## What is an FIeld and what is a Measurement
## Data flow
## Selection of measurements, fields and tags

# Data filtering and selection
## Filtering data
## Conditional query

# Transformationen
## Aggregation
## Time manipulation
