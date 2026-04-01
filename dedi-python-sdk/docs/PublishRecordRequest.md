# PublishRecordRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Unique record name within registry | 
**description** | **str** | Record description | [optional] 
**details** | **object** | Record data conforming to registry schema | 
**meta** | **object** | Additional metadata | [optional] 
**valid_till** | **datetime** | Expiration date in ISO format (optional) | [optional] 
**ttl** | **int** | Time to live in seconds | [optional] 

## Example

```python
from dedi_client.models.publish_record_request import PublishRecordRequest

# TODO update the JSON string below
json = "{}"
# create an instance of PublishRecordRequest from a JSON string
publish_record_request_instance = PublishRecordRequest.from_json(json)
# print the JSON string representation of the object
print(PublishRecordRequest.to_json())

# convert the object into a dict
publish_record_request_dict = publish_record_request_instance.to_dict()
# create an instance of PublishRecordRequest from a dict
publish_record_request_from_dict = PublishRecordRequest.from_dict(publish_record_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


