---
title: User Defined Field Mapping Rules
sidebar: sidebar/users.json
---
# User Defined Field Mapping Rules

If you use Sales Force Commerce Cloud (SFCC), Subscribe Pro provides UDF Mapping Rules to integrate UDF's with SFCC. These mapping rules allow you copy UDF data from SubscribePro into record attributes in SFCC. Navigate to **_Environment Settings > User-Defined Mapping Rules > New or Edit_** to create a new rule.

## Configure

Configuring a Mapping Rule has two parts:

1. Choose the UDF to map by configuring the Entity the UDF appears on and the Field Code.

<docs-image src="/images/udf_mapping_udf_details.png" title="UDF Mapping UDF Details" shadow=true max-width="700px" ></docs-image>

2. Identify the Destination Field in SFCC by configuring the Desination Record, Destination Data Type, and the Destination Field.
   
<docs-image src="/images/udf_mapping_destination.png" title="UDF Mapping Destination" shadow=true max-width="700px" ></docs-image>

The UDF will appear in the specified Destination Field in SFCC.

## Validation

Mapping rules are validated to ensue the chosen Entity can map to the chosen Destination Record.
