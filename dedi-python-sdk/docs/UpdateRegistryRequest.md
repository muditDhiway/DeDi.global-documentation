# UpdateRegistryRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**description** | **str** | Updated description | [optional] 
**var_schema** | **object** | Updated JSON Schema (must be backward compatible) | [optional] 
**meta** | **object** | Updated metadata | [optional] 

## Example

```python
from dedi_client.models.update_registry_request import UpdateRegistryRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateRegistryRequest from a JSON string
update_registry_request_instance = UpdateRegistryRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateRegistryRequest.to_json())

# convert the object into a dict
update_registry_request_dict = update_registry_request_instance.to_dict()
# create an instance of UpdateRegistryRequest from a dict
update_registry_request_from_dict = UpdateRegistryRequest.from_dict(update_registry_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


