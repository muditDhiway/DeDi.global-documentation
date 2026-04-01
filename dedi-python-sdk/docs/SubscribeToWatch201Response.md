# SubscribeToWatch201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**data** | [**SubscribeToWatch201ResponseData**](SubscribeToWatch201ResponseData.md) |  | [optional] 

## Example

```python
from dedi_client.models.subscribe_to_watch201_response import SubscribeToWatch201Response

# TODO update the JSON string below
json = "{}"
# create an instance of SubscribeToWatch201Response from a JSON string
subscribe_to_watch201_response_instance = SubscribeToWatch201Response.from_json(json)
# print the JSON string representation of the object
print(SubscribeToWatch201Response.to_json())

# convert the object into a dict
subscribe_to_watch201_response_dict = subscribe_to_watch201_response_instance.to_dict()
# create an instance of SubscribeToWatch201Response from a dict
subscribe_to_watch201_response_from_dict = SubscribeToWatch201Response.from_dict(subscribe_to_watch201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


