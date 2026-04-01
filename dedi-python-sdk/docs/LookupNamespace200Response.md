# LookupNamespace200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**data** | [**Namespace**](Namespace.md) |  | [optional] 

## Example

```python
from dedi_client.models.lookup_namespace200_response import LookupNamespace200Response

# TODO update the JSON string below
json = "{}"
# create an instance of LookupNamespace200Response from a JSON string
lookup_namespace200_response_instance = LookupNamespace200Response.from_json(json)
# print the JSON string representation of the object
print(LookupNamespace200Response.to_json())

# convert the object into a dict
lookup_namespace200_response_dict = lookup_namespace200_response_instance.to_dict()
# create an instance of LookupNamespace200Response from a dict
lookup_namespace200_response_from_dict = LookupNamespace200Response.from_dict(lookup_namespace200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


