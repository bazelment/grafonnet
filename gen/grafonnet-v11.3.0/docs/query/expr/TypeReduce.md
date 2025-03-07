# TypeReduce

grafonnet.query.expr.TypeReduce

## Index

* [`fn withDatasource(value)`](#fn-withdatasource)
* [`fn withDatasourceMixin(value)`](#fn-withdatasourcemixin)
* [`fn withExpression(value)`](#fn-withexpression)
* [`fn withHide(value=true)`](#fn-withhide)
* [`fn withIntervalMs(value)`](#fn-withintervalms)
* [`fn withMaxDataPoints(value)`](#fn-withmaxdatapoints)
* [`fn withQueryType(value)`](#fn-withquerytype)
* [`fn withReducer(value)`](#fn-withreducer)
* [`fn withRefId(value)`](#fn-withrefid)
* [`fn withResultAssertions(value)`](#fn-withresultassertions)
* [`fn withResultAssertionsMixin(value)`](#fn-withresultassertionsmixin)
* [`fn withSettings(value)`](#fn-withsettings)
* [`fn withSettingsMixin(value)`](#fn-withsettingsmixin)
* [`fn withTimeRange(value)`](#fn-withtimerange)
* [`fn withTimeRangeMixin(value)`](#fn-withtimerangemixin)
* [`fn withType()`](#fn-withtype)
* [`obj datasource`](#obj-datasource)
  * [`fn withType(value)`](#fn-datasourcewithtype)
  * [`fn withUid(value)`](#fn-datasourcewithuid)
* [`obj resultAssertions`](#obj-resultassertions)
  * [`fn withMaxFrames(value)`](#fn-resultassertionswithmaxframes)
  * [`fn withType(value)`](#fn-resultassertionswithtype)
  * [`fn withTypeVersion(value)`](#fn-resultassertionswithtypeversion)
  * [`fn withTypeVersionMixin(value)`](#fn-resultassertionswithtypeversionmixin)
* [`obj settings`](#obj-settings)
  * [`fn withMode(value)`](#fn-settingswithmode)
  * [`fn withReplaceWithValue(value)`](#fn-settingswithreplacewithvalue)
* [`obj timeRange`](#obj-timerange)
  * [`fn withFrom(value="now-6h")`](#fn-timerangewithfrom)
  * [`fn withTo(value="now")`](#fn-timerangewithto)

## Fields

### fn withDatasource

```jsonnet
withDatasource(value)
```

PARAMETERS:

* **value** (`object`)

Ref to a DataSource instance
### fn withDatasourceMixin

```jsonnet
withDatasourceMixin(value)
```

PARAMETERS:

* **value** (`object`)

Ref to a DataSource instance
### fn withExpression

```jsonnet
withExpression(value)
```

PARAMETERS:

* **value** (`string`)

Reference to single query result
### fn withHide

```jsonnet
withHide(value=true)
```

PARAMETERS:

* **value** (`boolean`)
   - default value: `true`

true if query is disabled (ie should not be returned to the dashboard)
NOTE: this does not always imply that the query should not be executed since
the results from a hidden query may be used as the input to other queries (SSE etc)
### fn withIntervalMs

```jsonnet
withIntervalMs(value)
```

PARAMETERS:

* **value** (`number`)

Interval is the suggested duration between time points in a time series query.
NOTE: the values for intervalMs is not saved in the query model.  It is typically calculated
from the interval required to fill a pixels in the visualization
### fn withMaxDataPoints

```jsonnet
withMaxDataPoints(value)
```

PARAMETERS:

* **value** (`integer`)

MaxDataPoints is the maximum number of data points that should be returned from a time series query.
NOTE: the values for maxDataPoints is not saved in the query model.  It is typically calculated
from the number of pixels visible in a visualization
### fn withQueryType

```jsonnet
withQueryType(value)
```

PARAMETERS:

* **value** (`string`)

QueryType is an optional identifier for the type of query.
It can be used to distinguish different types of queries.
### fn withReducer

```jsonnet
withReducer(value)
```

PARAMETERS:

* **value** (`string`)
   - valid values: `"sum"`, `"mean"`, `"min"`, `"max"`, `"count"`, `"last"`, `"median"`

The reducer
Possible enum values:
 - `"sum"` 
 - `"mean"` 
 - `"min"` 
 - `"max"` 
 - `"count"` 
 - `"last"` 
 - `"median"` 
### fn withRefId

```jsonnet
withRefId(value)
```

PARAMETERS:

* **value** (`string`)

RefID is the unique identifier of the query, set by the frontend call.
### fn withResultAssertions

```jsonnet
withResultAssertions(value)
```

PARAMETERS:

* **value** (`object`)

Optionally define expected query result behavior
### fn withResultAssertionsMixin

```jsonnet
withResultAssertionsMixin(value)
```

PARAMETERS:

* **value** (`object`)

Optionally define expected query result behavior
### fn withSettings

```jsonnet
withSettings(value)
```

PARAMETERS:

* **value** (`object`)

Reducer Options
### fn withSettingsMixin

```jsonnet
withSettingsMixin(value)
```

PARAMETERS:

* **value** (`object`)

Reducer Options
### fn withTimeRange

```jsonnet
withTimeRange(value)
```

PARAMETERS:

* **value** (`object`)

TimeRange represents the query range
NOTE: unlike generic /ds/query, we can now send explicit time values in each query
NOTE: the values for timeRange are not saved in a dashboard, they are constructed on the fly
### fn withTimeRangeMixin

```jsonnet
withTimeRangeMixin(value)
```

PARAMETERS:

* **value** (`object`)

TimeRange represents the query range
NOTE: unlike generic /ds/query, we can now send explicit time values in each query
NOTE: the values for timeRange are not saved in a dashboard, they are constructed on the fly
### fn withType

```jsonnet
withType()
```



### obj datasource


#### fn datasource.withType

```jsonnet
datasource.withType(value)
```

PARAMETERS:

* **value** (`string`)

The plugin type-id
#### fn datasource.withUid

```jsonnet
datasource.withUid(value)
```

PARAMETERS:

* **value** (`string`)

Specific datasource instance
### obj resultAssertions


#### fn resultAssertions.withMaxFrames

```jsonnet
resultAssertions.withMaxFrames(value)
```

PARAMETERS:

* **value** (`integer`)

Maximum frame count
#### fn resultAssertions.withType

```jsonnet
resultAssertions.withType(value)
```

PARAMETERS:

* **value** (`string`)
   - valid values: `""`, `"timeseries-wide"`, `"timeseries-long"`, `"timeseries-many"`, `"timeseries-multi"`, `"directory-listing"`, `"table"`, `"numeric-wide"`, `"numeric-multi"`, `"numeric-long"`, `"log-lines"`

Type asserts that the frame matches a known type structure.
Possible enum values:
 - `""` 
 - `"timeseries-wide"` 
 - `"timeseries-long"` 
 - `"timeseries-many"` 
 - `"timeseries-multi"` 
 - `"directory-listing"` 
 - `"table"` 
 - `"numeric-wide"` 
 - `"numeric-multi"` 
 - `"numeric-long"` 
 - `"log-lines"` 
#### fn resultAssertions.withTypeVersion

```jsonnet
resultAssertions.withTypeVersion(value)
```

PARAMETERS:

* **value** (`array`)

TypeVersion is the version of the Type property. Versions greater than 0.0 correspond to the dataplane
contract documentation https://grafana.github.io/dataplane/contract/.
#### fn resultAssertions.withTypeVersionMixin

```jsonnet
resultAssertions.withTypeVersionMixin(value)
```

PARAMETERS:

* **value** (`array`)

TypeVersion is the version of the Type property. Versions greater than 0.0 correspond to the dataplane
contract documentation https://grafana.github.io/dataplane/contract/.
### obj settings


#### fn settings.withMode

```jsonnet
settings.withMode(value)
```

PARAMETERS:

* **value** (`string`)
   - valid values: `"dropNN"`, `"replaceNN"`

Non-number reduce behavior
Possible enum values:
 - `"dropNN"` Drop non-numbers
 - `"replaceNN"` Replace non-numbers
#### fn settings.withReplaceWithValue

```jsonnet
settings.withReplaceWithValue(value)
```

PARAMETERS:

* **value** (`number`)

Only valid when mode is replace
### obj timeRange


#### fn timeRange.withFrom

```jsonnet
timeRange.withFrom(value="now-6h")
```

PARAMETERS:

* **value** (`string`)
   - default value: `"now-6h"`

From is the start time of the query.
#### fn timeRange.withTo

```jsonnet
timeRange.withTo(value="now")
```

PARAMETERS:

* **value** (`string`)
   - default value: `"now"`

To is the end time of the query.