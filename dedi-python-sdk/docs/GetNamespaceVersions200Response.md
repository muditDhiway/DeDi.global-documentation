# GetNamespaceVersions200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**data** | [**GetNamespaceVersions200ResponseData**](GetNamespaceVersions200ResponseData.md) |  | [optional] 

## Example

```python
from dedi_client.models.get_namespace_versions200_response import GetNamespaceVersions200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetNamespaceVersions200Response from a JSON string
get_namespace_versions200_response_instance = GetNamespaceVersions200Response.from_json(json)
# print the JSON string representation of the object
print(GetNamespaceVersions200Response.to_json())

# convert the object into a dict
get_namespace_versions200_response_dict = get_namespace_versions200_response_instance.to_dict()
# create an instance of GetNamespaceVersions200Response from a dict
get_namespace_versions200_response_from_dict = GetNamespaceVersions200Response.from_dict(get_namespace_versions200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


