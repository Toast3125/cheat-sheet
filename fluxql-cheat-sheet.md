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
| <!-- -->      | <!-- -->        |
|:-------------:|:---------------:|
| from(): Source data from a specified bucket or location | ```from(bucket: "example_bucket")``` |
| range(): Define the time range for data retrieval | ```range(start: v.timeRangeStart, stop: v.timeRangeStop) ``` |
| filter(): Filter data based on specified conditions | ```filter(fn: (r) => r["_measurement"] == "measurement_name")``` |
| group(): Group data based on specific criteria. | ```group(columns: ["column_name"])``` |
| map(): Modify or transform data. | ```map(fn: (r) => ({ r with new_field: r.old_field * 2 }))``` |
| yield(): Output or present the final result. | ``` yield()``` |

## Selecting Data
| <!-- -->      | <!-- -->        |
|:-------------:|:---------------:|
| from(): Select data from a specific measurement or bucket | ```from(bucket: "example_bucket")``` |
| filter() - Measurement: Filter data based on a specific measurement | ```filter(fn: (r) => r["_measurement"] == "measurement_name")``` |
| filter() - Field: Filter data based on a specific field within a measurement. | ```filter(fn: (r) => r["_field"] == "field_name")``` |
| filter() - Tag: Filter data based on a specific tag. | ```filter(fn: (r) => r["tag_key"] == "tag_value")``` |

# Data filtering
## Filtering data
## Conditional query

# Transformationen
## Aggregation
## Time manipulation
