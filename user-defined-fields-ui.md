# User Defined Fields in the UI

UDFs are currently available on the following entities:

* Customers
  * Details
  * Addresses
* Subscription Details
* Group Subscription Details
* Products 
* Group Subscription Templates

<docs-image src="/images/udf_on_customer.png" title="UDF on Cutomer Entity" shadow=true max-width="500px" rounded-corners=true></docs-image>

## Field Types, Data Types, and Values

UDFs accept a unique Field Code (or UDF name), a Field Type, and a value. Values must be one of the data types accepted by the Field Type. See the chart below for all accepted Field Type and Data Type pairings.

|Field Type|Accepted Data Types|Specifications|
|------|------|-----|
|Input|string, number, boolean| Single line input|
|Text Area|string, number| Multi line input|
|Number|string, number| Only integers accepted|
|Currency| string, number| Only integers accepted|
|Select| string |Drop down options must be defined in a UDF Definition first|
|Date|date| Enter date through datepicker|
|Date-Time|datetime| Enter date and time through datepicker|
|Checkbox|boolean| Stored as true/false|
|JSON| JSON object, JSON array| Formating and error validation available|

## Validation

If the UDF field has a been configured through a [UDF Definition](/user-defined-field-definitions.md) with the "Validate Data" setting, SubscribePro will check that the data is in a valid format before allowing you to save.


