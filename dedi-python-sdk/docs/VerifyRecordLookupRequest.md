# VerifyRecordLookupRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**record_lookup_response** | **object** | Full response body from record lookup API | 

## Example

```python
from dedi_client.models.verify_record_lookup_request import VerifyRecordLookupRequest

# TODO update the JSON string below
json = "{}"
# create an instance of VerifyRecordLookupRequest from a JSON string
verify_record_lookup_request_instance = VerifyRecordLookupRequest.from_json(json)
# print the JSON string representation of the object
print(VerifyRecordLookupRequest.to_json())

# convert the object into a dict
verify_record_lookup_request_dict = verify_record_lookup_request_instance.to_dict()
# create an instance of VerifyRecordLookupRequest from a dict
verify_record_lookup_request_from_dict = VerifyRecordLookupRequest.from_dict(verify_record_lookup_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


