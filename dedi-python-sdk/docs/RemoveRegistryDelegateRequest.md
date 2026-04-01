# RemoveRegistryDelegateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**delegate_email** | **str** | Email of delegate user to remove | 

## Example

```python
from dedi_client.models.remove_registry_delegate_request import RemoveRegistryDelegateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RemoveRegistryDelegateRequest from a JSON string
remove_registry_delegate_request_instance = RemoveRegistryDelegateRequest.from_json(json)
# print the JSON string representation of the object
print(RemoveRegistryDelegateRequest.to_json())

# convert the object into a dict
remove_registry_delegate_request_dict = remove_registry_delegate_request_instance.to_dict()
# create an instance of RemoveRegistryDelegateRequest from a dict
remove_registry_delegate_request_from_dict = RemoveRegistryDelegateRequest.from_dict(remove_registry_delegate_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


