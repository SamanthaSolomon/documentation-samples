# User Defined Field Example Scenario

You are a supplement distributor for animal athletes. You want to include the type of animal the product is for on all subscriptions. Most of your customer-base owns horses. 

Since you want to include the animal-type on every subscription entity, you set up a [UDF Definition](/user-defined-field-definitions.md). The Field Name is "Animal Type", the Entity Type is "Subscription"

<docs-image src="/images/udf_definition_field_code_entity_type.png" title="UDF Definition with Field Code and Entity Type" shadow=true max-width="800px" rounded-corners=true></docs-image>

You know that the majority of your products are used on horses, but are occassionaly bought for other animals. You don't want to limit the value that can be entered, but you do want to ensure it is a short description of the animal type. You set the Field Type to "Text", the Data Type to "String", and choose to "Validate UDF Data", preventing non-string values from being entered.

<docs-image src="/images/udf_definition_field_type_data_type_validate_data.png" title="UDF Definition with Field Type, Data Type, Validate Data" shadow=true max-width="800px" rounded-corners=true></docs-image>

Then you set the Default Value to "horse" and choose to populate the Default Value.

<docs-image src="/images/udf_definition_default_data_populate.png" title="UDF Definition with Default Data and P" shadow=true max-width="800px" rounded-corners=true></docs-image>

Everytime a new subscription is created, this UDF will be populated. The Field Code and Field Type cannot be altered on the subscription, but the value can.

<docs-image src="/images/udf_on_create_subscription.png" title="UDF on Create Subscription" shadow=true max-width="800px" rounded-corners=true></docs-image>





