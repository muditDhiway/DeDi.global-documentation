# RegisterLoginRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**name** | **str** | Required for registration, optional for login | [optional] 
**action** | **str** |  | 
**password** | **str** | Password with at least 6 characters and one special character (@$!%*?&amp;) | 

## Example

```python
from dedi_client.models.register_login_request import RegisterLoginRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RegisterLoginRequest from a JSON string
register_login_request_instance = RegisterLoginRequest.from_json(json)
# print the JSON string representation of the object
print(RegisterLoginRequest.to_json())

# convert the object into a dict
register_login_request_dict = register_login_request_instance.to_dict()
# create an instance of RegisterLoginRequest from a dict
register_login_request_from_dict = RegisterLoginRequest.from_dict(register_login_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


