# GetUserWatchSubscriptions200ResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subscription_id** | **str** |  | [optional] 
**watch_type** | **str** |  | [optional] 
**target_id** | **str** |  | [optional] 
**target_name** | **str** | Human-readable name of the watched resource | [optional] 
**webhook_url** | **str** |  | [optional] 
**events** | **List[str]** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**last_notification** | **datetime** |  | [optional] 
**status** | **str** |  | [optional] 

## Example

```python
from dedi_client.models.get_user_watch_subscriptions200_response_data_inner import GetUserWatchSubscriptions200ResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetUserWatchSubscriptions200ResponseDataInner from a JSON string
get_user_watch_subscriptions200_response_data_inner_instance = GetUserWatchSubscriptions200ResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(GetUserWatchSubscriptions200ResponseDataInner.to_json())

# convert the object into a dict
get_user_watch_subscriptions200_response_data_inner_dict = get_user_watch_subscriptions200_response_data_inner_instance.to_dict()
# create an instance of GetUserWatchSubscriptions200ResponseDataInner from a dict
get_user_watch_subscriptions200_response_data_inner_from_dict = GetUserWatchSubscriptions200ResponseDataInner.from_dict(get_user_watch_subscriptions200_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


