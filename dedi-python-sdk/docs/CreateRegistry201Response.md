# CreateRegistry201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**data** | [**Registry**](Registry.md) |  | [optional] 

## Example

```python
from dedi_client.models.create_registry201_response import CreateRegistry201Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateRegistry201Response from a JSON string
create_registry201_response_instance = CreateRegistry201Response.from_json(json)
# print the JSON string representation of the object
print(CreateRegistry201Response.to_json())

# convert the object into a dict
create_registry201_response_dict = create_registry201_response_instance.to_dict()
# create an instance of CreateRegistry201Response from a dict
create_registry201_response_from_dict = CreateRegistry201Response.from_dict(create_registry201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


