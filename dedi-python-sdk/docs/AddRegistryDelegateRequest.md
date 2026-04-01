# AddRegistryDelegateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**delegate_email** | **str** | Email of user to add as delegate | 

## Example

```python
from dedi_client.models.add_registry_delegate_request import AddRegistryDelegateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AddRegistryDelegateRequest from a JSON string
add_registry_delegate_request_instance = AddRegistryDelegateRequest.from_json(json)
# print the JSON string representation of the object
print(AddRegistryDelegateRequest.to_json())

# convert the object into a dict
add_registry_delegate_request_dict = add_registry_delegate_request_instance.to_dict()
# create an instance of AddRegistryDelegateRequest from a dict
add_registry_delegate_request_from_dict = AddRegistryDelegateRequest.from_dict(add_registry_delegate_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


