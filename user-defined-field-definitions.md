---
title: User Defined Field Definitions
sidebar: sidebar/users.json
---
# User Defined Field Definitions

User Defined Field (UDF) Definitions allow you to structure and organize your User Defined Fields. With UDF Definitions, you can set data formats, default values, and validation rules for each UDF. This ensures that the data in your UDF fields can be compatible with your ecommerce store. 

UDF Definitions can be set up for Customers, Customer Addresses, Subscriptions, Group Subscriptions, and Products.

Configure a new or edit and existing UDF Definition by navigating to **_Environment Settings > User-Defined Field Definitions > New or Edit_**.

| Field | Requirements |
|-----------|---|
|Field Code| Unique string that must be at least 4 characters long|
|Entity Type| The entity type this rule will be assigned to. UDFs are available on Customer, Customer Address, Subscription, Group Subscription, and Product entities.
|Field Type| The type of field that best supports the data. This is the type of UI element used to input that UDF value. [See available Field- and Data-Type pairings](/users/configuration/user-defined-fields/user-defined-fields-ui/).|
|Data Type| Data type for UDF Value. This controls how the data is sent and received by SubscribePro. [See available Field- and Data-Type pairings](/users/configuration/user-defined-fields/user-defined-fields-ui/).|
|Validate Date| Choose if data will be validated before saving.|
|Default Value| Set a default value for the UDF|
|Populate Default| Choose if UDF will be automatically populated on new instances of the assigned entity. Existing instances will not be updated with the new UDF.|


## Assign UDF Definitions

You can automatically add a User Defined Field to new Customer, Customer Address, Subscription, Group Subscription, and Product entities by selecting the Populate Default Value option. If you specify a default value, it will also be populated on new entities as they are created."

<docs-image src="/images/udf_definition_populate_default.png" title="UDF Definition Populate Default" shadow=true max-width="700px" ></docs-image>

If the Don't Populate Default Value Option is selected, a definition can be added to an entity by using the exact Field Code when adding a new UDF to an inidividual entity.

<docs-image src="/images/udf_definition_list_highlight_field_code.png" title="UDF Definition List Highlight Field Code" shadow=true max-width="700px" ></docs-image>

<docs-image src="/images/add_udf_field_code.png" title="UDF Definition List Highlight Field Code" shadow=true max-width="700px" ></docs-image>

The field type will be assigned and cannot be changed. If a default value exists, it will populate.
<docs-image src="/images/udf_definition_highlight_customer.png" title="UDF Definition on Customer" shadow=true max-width="700px" ></docs-image>

## Defining Select Options

If you are using the Select field type for your User Defined Field, you can set the list of options through the UDF Definition. Select fields must be used with the String data type. For each option, you must set a label and value. There is no limit to the number of options. 

<docs-image src="/images/udf_definition_select_options.png" title="UDF Definition Select Options" shadow=true max-width="700px" ></docs-image>

The value controls how the option will be stored and presented in the API. The label controls how the option appears in the UI.
<docs-image src="/images/udf_select_options.png" title="UDF Select Options" shadow=true max-width="700px" ></docs-image>

You may select one of the options to be the default option. If you don't select a default option, then the first option will be used as the default.
<docs-image src="/images/udf_definition_select_options_default_data.png" title="UDF Definition Select Options Default" shadow=true max-width="700px" ></docs-image>

## User Defined Fields Back-End Data Types

The below table lists the data types and their validation requirements. SubscribePro will only enforce these requirements if you select "true" value for the "Validate Data" setting in the UDF Definition.

| Data Type | Requirements | Examples |
|---|---|---|
| `string` | Null or string value | `"example"`, `"1"` |
| `number` | Integer or float | `1`, `1.1` |
| `date` | String in the date format `Y-m-d` | `"2000-01-15"` |
| `datetime` | String in the ISO 8601 date/time values which include at least hours and minute, date-only is not allowed - negative timezone offset not allowed. | `"2022-05-27T16:01:29"`, `"2022-05-27T16:01:29+0000"` |
| `boolean` | Boolean | `true`, `false` |
| `json_object` | Key/value array, null or empty array | `{}`, `{'key' => 'value'}` |
| `json_array` | Array, null or empty array | `[]`, `[0, 1, 2]` |
