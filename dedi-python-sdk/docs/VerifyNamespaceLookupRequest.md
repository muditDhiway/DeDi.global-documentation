# VerifyNamespaceLookupRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**namespace_lookup_response** | **object** | Full response body from namespace lookup API | 

## Example

```python
from dedi_client.models.verify_namespace_lookup_request import VerifyNamespaceLookupRequest

# TODO update the JSON string below
json = "{}"
# create an instance of VerifyNamespaceLookupRequest from a JSON string
verify_namespace_lookup_request_instance = VerifyNamespaceLookupRequest.from_json(json)
# print the JSON string representation of the object
print(VerifyNamespaceLookupRequest.to_json())

# convert the object into a dict
verify_namespace_lookup_request_dict = verify_namespace_lookup_request_instance.to_dict()
# create an instance of VerifyNamespaceLookupRequest from a dict
verify_namespace_lookup_request_from_dict = VerifyNamespaceLookupRequest.from_dict(verify_namespace_lookup_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


