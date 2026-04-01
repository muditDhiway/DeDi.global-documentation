# GetNamespaceVersions200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_by** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 
**total_versions** | **int** |  | [optional] 
**versions** | **List[str]** |  | [optional] 
**ttl** | **int** |  | [optional] 

## Example

```python
from dedi_client.models.get_namespace_versions200_response_data import GetNamespaceVersions200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of GetNamespaceVersions200ResponseData from a JSON string
get_namespace_versions200_response_data_instance = GetNamespaceVersions200ResponseData.from_json(json)
# print the JSON string representation of the object
print(GetNamespaceVersions200ResponseData.to_json())

# convert the object into a dict
get_namespace_versions200_response_data_dict = get_namespace_versions200_response_data_instance.to_dict()
# create an instance of GetNamespaceVersions200ResponseData from a dict
get_namespace_versions200_response_data_from_dict = GetNamespaceVersions200ResponseData.from_dict(get_namespace_versions200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


