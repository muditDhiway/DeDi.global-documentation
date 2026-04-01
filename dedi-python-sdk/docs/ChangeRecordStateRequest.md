# ChangeRecordStateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**state** | **str** | New state for the record | 

## Example

```python
from dedi_client.models.change_record_state_request import ChangeRecordStateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ChangeRecordStateRequest from a JSON string
change_record_state_request_instance = ChangeRecordStateRequest.from_json(json)
# print the JSON string representation of the object
print(ChangeRecordStateRequest.to_json())

# convert the object into a dict
change_record_state_request_dict = change_record_state_request_instance.to_dict()
# create an instance of ChangeRecordStateRequest from a dict
change_record_state_request_from_dict = ChangeRecordStateRequest.from_dict(change_record_state_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


