# LookupRecord200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**data** | [**Record**](Record.md) |  | [optional] 

## Example

```python
from dedi_client.models.lookup_record200_response import LookupRecord200Response

# TODO update the JSON string below
json = "{}"
# create an instance of LookupRecord200Response from a JSON string
lookup_record200_response_instance = LookupRecord200Response.from_json(json)
# print the JSON string representation of the object
print(LookupRecord200Response.to_json())

# convert the object into a dict
lookup_record200_response_dict = lookup_record200_response_instance.to_dict()
# create an instance of LookupRecord200Response from a dict
lookup_record200_response_from_dict = LookupRecord200Response.from_dict(lookup_record200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


