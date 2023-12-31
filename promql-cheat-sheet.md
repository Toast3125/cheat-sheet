# Basics of PromQL
PromQL enables querying time series data using the following basic syntax
```
<metric_name>{<label_name>=<label_value>}
```
For example, in this query, we retrieve all services from the Windows server
```
windows_service_state
```
We can add a filter to show only the service named "cyserver" when it's in the "running" state
```
windows_service_state{name=~cyserver, state=~running}
```

# Functions
| <!-- -->      | <!-- -->        |
|:-------------:|:---------------:|
| sum | Calculates the total sum of matching time series |
| avg | Determines the average value of matching time series |
| min | Provides the minimum value from all matching time series |
| max | Provides the maximum value from all matching time series |
| rate | Calculates the per-second average rate of growth for a time series |
| increase | Calculates the growth in the value of a time series over a specified time range |
| irate | Similar to rate, but promptly adjusts if the metric resets, because of restart as example |

# Operators
| <!-- -->      | <!-- -->        |
|:-------------:|:---------------:|
| = | Is the value equal to another value |
| != | Is the value not equal to another value |
| =~ | Is the value equal to multipul values |
| !~ | Is the value not equal to multipul values |

# Parenthesis
| <!-- -->      | <!-- -->        |
|:-------------:|:---------------:|
| () | Are used to show the logical sequence |
| {} | Are used to filter in metrics |
| [] | Are used to set a time range |
