# VerifyRegistryLookupRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**registry_lookup_response** | **object** | Full response body from registry lookup API | 

## Example

```python
from dedi_client.models.verify_registry_lookup_request import VerifyRegistryLookupRequest

# TODO update the JSON string below
json = "{}"
# create an instance of VerifyRegistryLookupRequest from a JSON string
verify_registry_lookup_request_instance = VerifyRegistryLookupRequest.from_json(json)
# print the JSON string representation of the object
print(VerifyRegistryLookupRequest.to_json())

# convert the object into a dict
verify_registry_lookup_request_dict = verify_registry_lookup_request_instance.to_dict()
# create an instance of VerifyRegistryLookupRequest from a dict
verify_registry_lookup_request_from_dict = VerifyRegistryLookupRequest.from_dict(verify_registry_lookup_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


