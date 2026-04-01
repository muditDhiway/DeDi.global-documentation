# QueryNamespaceRegistries200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**data** | [**QueryNamespaceRegistries200ResponseData**](QueryNamespaceRegistries200ResponseData.md) |  | [optional] 

## Example

```python
from dedi_client.models.query_namespace_registries200_response import QueryNamespaceRegistries200Response

# TODO update the JSON string below
json = "{}"
# create an instance of QueryNamespaceRegistries200Response from a JSON string
query_namespace_registries200_response_instance = QueryNamespaceRegistries200Response.from_json(json)
# print the JSON string representation of the object
print(QueryNamespaceRegistries200Response.to_json())

# convert the object into a dict
query_namespace_registries200_response_dict = query_namespace_registries200_response_instance.to_dict()
# create an instance of QueryNamespaceRegistries200Response from a dict
query_namespace_registries200_response_from_dict = QueryNamespaceRegistries200Response.from_dict(query_namespace_registries200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


