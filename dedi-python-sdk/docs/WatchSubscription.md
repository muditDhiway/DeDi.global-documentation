# WatchSubscription


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subscription_id** | **str** | Unique subscription identifier | [optional] 
**watch_type** | **str** | Type of resource being watched | [optional] 
**target_id** | **str** | ID of the watched resource | [optional] 
**target_name** | **str** | Human-readable name of the watched resource | [optional] 
**webhook_url** | **str** | Webhook URL for notifications | [optional] 
**events** | **List[str]** | Events being watched | [optional] 
**created_at** | **datetime** | Subscription creation timestamp | [optional] 
**last_notification** | **datetime** | Last notification sent timestamp | [optional] 
**status** | **str** | Current subscription status | [optional] 
**notification_count** | **int** | Total number of notifications sent | [optional] 

## Example

```python
from dedi_client.models.watch_subscription import WatchSubscription

# TODO update the JSON string below
json = "{}"
# create an instance of WatchSubscription from a JSON string
watch_subscription_instance = WatchSubscription.from_json(json)
# print the JSON string representation of the object
print(WatchSubscription.to_json())

# convert the object into a dict
watch_subscription_dict = watch_subscription_instance.to_dict()
# create an instance of WatchSubscription from a dict
watch_subscription_from_dict = WatchSubscription.from_dict(watch_subscription_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


