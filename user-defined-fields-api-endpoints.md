# User Defined Fields with the API

Several API resources for our [v2 REST API](https://api.subscribepro.com/docs/rest) have a `user-defined-fields` attribute. You can make GET requests to find UDFs and POST/PATCH requests to set or update UDFs:

- Customer Address  
    - GET `/services/v2/addresses`
    - GET/POST `/services/v2/addresses/{id}`
- Customer 
    - POST `/services/v2/customer`
    - GET `/services/v2/customers`
    - GET/POST `/services/v2/customers/{id}`
- Group Subscription 
    - POST `/services/v2/group-subscription`
    - GET/PATCH/POST `/services/v2/group-subscriptions`
    - GET/PATCH/POST `/services/v2/group-subscriptions/{id}`
- Group Subscription Template 
    - POST `/services/v2/group-subscription-template`
    - GET/PATCH/POST `/services/v2/group-subscription-templates`
    - GET/PATCH/POST `/services/v2/group-subscription-templates/{id}`
- Product 
    - GET/PATCH/POST `/services/v2/products`
    - GET/PATCH/POST `/services/v2/products/{id}`
- Subscription 
    - POST `/services/v2/subscription`
    - GET/PATCH/POST `/services/v2/subscriptions`
    - GET/PATCH/POST `/services/v2/subscriptions/{id}`

## Examples:

For example, let's say you wanted to update the `birthday` user defined field on a customer's address. You could make an API call like this

```bash
curl -X PATCH "https://api.subscribepro.com/services/v2/addresses/123" \
-H 'Authorization: Bearer XXXXXX' \
-d '[{"op": "add","path": "/user_defined_fields/birthday","value": "1985-01-01"}]' 
```

Then, you could get the customer's address data including that UDF value with an API request like this:

```bash
curl -X GET "https://api.subscribepro.com/services/v2/addresses/123" \
-H 'Authorization: Bearer XXXXXX' 
```

# Validation

When User Defined Fields are set or updated via the API, we only validate that the UDF data is valid JSON. When UDF fields with the "Validate Data" setting are edited through the SubscribePro application, we will enforce the validation rules for that field.
