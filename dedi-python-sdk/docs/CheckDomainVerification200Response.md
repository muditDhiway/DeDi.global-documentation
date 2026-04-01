# CheckDomainVerification200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**data** | [**CheckDomainVerification200ResponseData**](CheckDomainVerification200ResponseData.md) |  | [optional] 

## Example

```python
from dedi_client.models.check_domain_verification200_response import CheckDomainVerification200Response

# TODO update the JSON string below
json = "{}"
# create an instance of CheckDomainVerification200Response from a JSON string
check_domain_verification200_response_instance = CheckDomainVerification200Response.from_json(json)
# print the JSON string representation of the object
print(CheckDomainVerification200Response.to_json())

# convert the object into a dict
check_domain_verification200_response_dict = check_domain_verification200_response_instance.to_dict()
# create an instance of CheckDomainVerification200Response from a dict
check_domain_verification200_response_from_dict = CheckDomainVerification200Response.from_dict(check_domain_verification200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


