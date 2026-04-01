# CheckDomainVerification200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**verified** | **bool** | Whether domain is verified | [optional] 
**domain** | **str** | Verified domain | [optional] 

## Example

```python
from dedi_client.models.check_domain_verification200_response_data import CheckDomainVerification200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of CheckDomainVerification200ResponseData from a JSON string
check_domain_verification200_response_data_instance = CheckDomainVerification200ResponseData.from_json(json)
# print the JSON string representation of the object
print(CheckDomainVerification200ResponseData.to_json())

# convert the object into a dict
check_domain_verification200_response_data_dict = check_domain_verification200_response_data_instance.to_dict()
# create an instance of CheckDomainVerification200ResponseData from a dict
check_domain_verification200_response_data_from_dict = CheckDomainVerification200ResponseData.from_dict(check_domain_verification200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


