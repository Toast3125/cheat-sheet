# Basic of FluxQL

from(bucket: "MeinBucket")
  |> range(start: -1h) 
  |> filter(fn: (r) => r._measurement == "Cisco" and r._field == "SG300")
