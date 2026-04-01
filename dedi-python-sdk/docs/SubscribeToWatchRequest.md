# SubscribeToWatchRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**watch_type** | **str** | Type of resource to watch | 
**target_id** | **str** | ID of the resource to watch (namespace ID, registry ID, or record ID) | 
**webhook_url** | **str** | Webhook URL to receive notifications | 
**events** | **List[str]** | Specific events to watch (optional, defaults to all) | [optional] 

## Example

```python
from dedi_client.models.subscribe_to_watch_request import SubscribeToWatchRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SubscribeToWatchRequest from a JSON string
subscribe_to_watch_request_instance = SubscribeToWatchRequest.from_json(json)
# print the JSON string representation of the object
print(SubscribeToWatchRequest.to_json())

# convert the object into a dict
subscribe_to_watch_request_dict = subscribe_to_watch_request_instance.to_dict()
# create an instance of SubscribeToWatchRequest from a dict
subscribe_to_watch_request_from_dict = SubscribeToWatchRequest.from_dict(subscribe_to_watch_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


