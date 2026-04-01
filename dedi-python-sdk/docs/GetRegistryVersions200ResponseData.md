# GetRegistryVersions200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**registry_name** | **str** |  | [optional] 
**created_by** | **str** |  | [optional] 
**var_schema** | **object** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 
**total_versions** | **int** |  | [optional] 
**versions** | **List[str]** |  | [optional] 
**ttl** | **int** |  | [optional] 

## Example

```python
from dedi_client.models.get_registry_versions200_response_data import GetRegistryVersions200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of GetRegistryVersions200ResponseData from a JSON string
get_registry_versions200_response_data_instance = GetRegistryVersions200ResponseData.from_json(json)
# print the JSON string representation of the object
print(GetRegistryVersions200ResponseData.to_json())

# convert the object into a dict
get_registry_versions200_response_data_dict = get_registry_versions200_response_data_instance.to_dict()
# create an instance of GetRegistryVersions200ResponseData from a dict
get_registry_versions200_response_data_from_dict = GetRegistryVersions200ResponseData.from_dict(get_registry_versions200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


