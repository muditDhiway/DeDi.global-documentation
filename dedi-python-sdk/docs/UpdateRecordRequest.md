# UpdateRecordRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**description** | **str** | Updated description | [optional] 
**details** | **object** | Updated record data | [optional] 
**meta** | **object** | Updated metadata | [optional] 
**valid_till** | **datetime** | Updated expiration date in ISO format | [optional] 
**ttl** | **int** | Updated time to live in seconds | [optional] 

## Example

```python
from dedi_client.models.update_record_request import UpdateRecordRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateRecordRequest from a JSON string
update_record_request_instance = UpdateRecordRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateRecordRequest.to_json())

# convert the object into a dict
update_record_request_dict = update_record_request_instance.to_dict()
# create an instance of UpdateRecordRequest from a dict
update_record_request_from_dict = UpdateRecordRequest.from_dict(update_record_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


