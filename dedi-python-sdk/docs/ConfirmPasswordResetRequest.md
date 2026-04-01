# ConfirmPasswordResetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **str** | Reset token from email link | 
**new_password** | **str** | New password meeting requirements | 

## Example

```python
from dedi_client.models.confirm_password_reset_request import ConfirmPasswordResetRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ConfirmPasswordResetRequest from a JSON string
confirm_password_reset_request_instance = ConfirmPasswordResetRequest.from_json(json)
# print the JSON string representation of the object
print(ConfirmPasswordResetRequest.to_json())

# convert the object into a dict
confirm_password_reset_request_dict = confirm_password_reset_request_instance.to_dict()
# create an instance of ConfirmPasswordResetRequest from a dict
confirm_password_reset_request_from_dict = ConfirmPasswordResetRequest.from_dict(confirm_password_reset_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


