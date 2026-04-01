# QueryNamespaceRegistries200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**namespace_id** | **str** |  | [optional] 
**namespace_name** | **str** |  | [optional] 
**total_registries** | **int** |  | [optional] 
**page_number** | **int** |  | [optional] 
**page_size** | **int** |  | [optional] 
**registries** | [**List[RegistrySummary]**](RegistrySummary.md) |  | [optional] 

## Example

```python
from dedi_client.models.query_namespace_registries200_response_data import QueryNamespaceRegistries200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of QueryNamespaceRegistries200ResponseData from a JSON string
query_namespace_registries200_response_data_instance = QueryNamespaceRegistries200ResponseData.from_json(json)
# print the JSON string representation of the object
print(QueryNamespaceRegistries200ResponseData.to_json())

# convert the object into a dict
query_namespace_registries200_response_data_dict = query_namespace_registries200_response_data_instance.to_dict()
# create an instance of QueryNamespaceRegistries200ResponseData from a dict
query_namespace_registries200_response_data_from_dict = QueryNamespaceRegistries200ResponseData.from_dict(query_namespace_registries200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


