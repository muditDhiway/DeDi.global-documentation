# GetUserWatchSubscriptions200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**data** | [**List[GetUserWatchSubscriptions200ResponseDataInner]**](GetUserWatchSubscriptions200ResponseDataInner.md) |  | [optional] 

## Example

```python
from dedi_client.models.get_user_watch_subscriptions200_response import GetUserWatchSubscriptions200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetUserWatchSubscriptions200Response from a JSON string
get_user_watch_subscriptions200_response_instance = GetUserWatchSubscriptions200Response.from_json(json)
# print the JSON string representation of the object
print(GetUserWatchSubscriptions200Response.to_json())

# convert the object into a dict
get_user_watch_subscriptions200_response_dict = get_user_watch_subscriptions200_response_instance.to_dict()
# create an instance of GetUserWatchSubscriptions200Response from a dict
get_user_watch_subscriptions200_response_from_dict = GetUserWatchSubscriptions200Response.from_dict(get_user_watch_subscriptions200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


