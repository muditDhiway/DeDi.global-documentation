# GetRegistryVersions200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**data** | [**GetRegistryVersions200ResponseData**](GetRegistryVersions200ResponseData.md) |  | [optional] 

## Example

```python
from dedi_client.models.get_registry_versions200_response import GetRegistryVersions200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetRegistryVersions200Response from a JSON string
get_registry_versions200_response_instance = GetRegistryVersions200Response.from_json(json)
# print the JSON string representation of the object
print(GetRegistryVersions200Response.to_json())

# convert the object into a dict
get_registry_versions200_response_dict = get_registry_versions200_response_instance.to_dict()
# create an instance of GetRegistryVersions200Response from a dict
get_registry_versions200_response_from_dict = GetRegistryVersions200Response.from_dict(get_registry_versions200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


