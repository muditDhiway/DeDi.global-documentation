# CreateRegistryRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Unique registry name within namespace | 
**description** | **str** | Registry description | 
**var_schema** | **object** | JSON Schema for record validation | 
**tag** | **str** | Schema tag for categorization | [optional] [default to 'custom']
**meta** | **object** | Additional metadata | [optional] 

## Example

```python
from dedi_client.models.create_registry_request import CreateRegistryRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateRegistryRequest from a JSON string
create_registry_request_instance = CreateRegistryRequest.from_json(json)
# print the JSON string representation of the object
print(CreateRegistryRequest.to_json())

# convert the object into a dict
create_registry_request_dict = create_registry_request_instance.to_dict()
# create an instance of CreateRegistryRequest from a dict
create_registry_request_from_dict = CreateRegistryRequest.from_dict(create_registry_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


