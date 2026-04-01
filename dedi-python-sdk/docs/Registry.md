# Registry


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**registry_id** | **str** | Unique registry identifier | [optional] 
**registry_name** | **str** | Registry name | [optional] 
**namespace_id** | **str** | Parent namespace ID | [optional] 
**description** | **str** | Registry description | [optional] 
**digest** | **str** | Cryptographic digest of registry data | [optional] 
**var_schema** | **object** | JSON Schema for record validation | [optional] 
**meta** | **object** | Additional metadata | [optional] 
**version** | **str** | Current version | [optional] 
**version_count** | **int** | Total number of versions | [optional] 
**created_at** | **datetime** | Creation timestamp | [optional] 
**updated_at** | **datetime** | Last update timestamp | [optional] 
**created_by** | **str** | Creator user ID | [optional] 
**state** | **str** | Current registry state | [optional] 
**ttl** | **int** | Time to live in seconds | [optional] 

## Example

```python
from dedi_client.models.registry import Registry

# TODO update the JSON string below
json = "{}"
# create an instance of Registry from a JSON string
registry_instance = Registry.from_json(json)
# print the JSON string representation of the object
print(Registry.to_json())

# convert the object into a dict
registry_dict = registry_instance.to_dict()
# create an instance of Registry from a dict
registry_from_dict = Registry.from_dict(registry_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


