# LookupRegistry200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**data** | [**Registry**](Registry.md) |  | [optional] 

## Example

```python
from dedi_client.models.lookup_registry200_response import LookupRegistry200Response

# TODO update the JSON string below
json = "{}"
# create an instance of LookupRegistry200Response from a JSON string
lookup_registry200_response_instance = LookupRegistry200Response.from_json(json)
# print the JSON string representation of the object
print(LookupRegistry200Response.to_json())

# convert the object into a dict
lookup_registry200_response_dict = lookup_registry200_response_instance.to_dict()
# create an instance of LookupRegistry200Response from a dict
lookup_registry200_response_from_dict = LookupRegistry200Response.from_dict(lookup_registry200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


