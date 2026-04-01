# SaveRecordAsDraftRequest


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
from dedi_client.models.save_record_as_draft_request import SaveRecordAsDraftRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SaveRecordAsDraftRequest from a JSON string
save_record_as_draft_request_instance = SaveRecordAsDraftRequest.from_json(json)
# print the JSON string representation of the object
print(SaveRecordAsDraftRequest.to_json())

# convert the object into a dict
save_record_as_draft_request_dict = save_record_as_draft_request_instance.to_dict()
# create an instance of SaveRecordAsDraftRequest from a dict
save_record_as_draft_request_from_dict = SaveRecordAsDraftRequest.from_dict(save_record_as_draft_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


