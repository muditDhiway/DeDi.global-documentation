# SubscribeToWatch201ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subscription_id** | **str** | Unique subscription ID for management | [optional] 
**watch_type** | **str** |  | [optional] 
**target_id** | **str** |  | [optional] 
**webhook_url** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from dedi_client.models.subscribe_to_watch201_response_data import SubscribeToWatch201ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of SubscribeToWatch201ResponseData from a JSON string
subscribe_to_watch201_response_data_instance = SubscribeToWatch201ResponseData.from_json(json)
# print the JSON string representation of the object
print(SubscribeToWatch201ResponseData.to_json())

# convert the object into a dict
subscribe_to_watch201_response_data_dict = subscribe_to_watch201_response_data_instance.to_dict()
# create an instance of SubscribeToWatch201ResponseData from a dict
subscribe_to_watch201_response_data_from_dict = SubscribeToWatch201ResponseData.from_dict(subscribe_to_watch201_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


