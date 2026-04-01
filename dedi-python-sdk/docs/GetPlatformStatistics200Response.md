# GetPlatformStatistics200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_users** | **int** | Total number of registered user accounts | [optional] 
**total_namespaces** | **int** | Total number of namespaces across all users | [optional] 
**total_registries** | **int** | Total number of registries across all namespaces | [optional] 
**total_records** | **int** | Total number of records across all registries | [optional] 

## Example

```python
from dedi_client.models.get_platform_statistics200_response import GetPlatformStatistics200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetPlatformStatistics200Response from a JSON string
get_platform_statistics200_response_instance = GetPlatformStatistics200Response.from_json(json)
# print the JSON string representation of the object
print(GetPlatformStatistics200Response.to_json())

# convert the object into a dict
get_platform_statistics200_response_dict = get_platform_statistics200_response_instance.to_dict()
# create an instance of GetPlatformStatistics200Response from a dict
get_platform_statistics200_response_from_dict = GetPlatformStatistics200Response.from_dict(get_platform_statistics200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


