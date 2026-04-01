# VerifyEmail200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**refresh_token** | **str** | JWT refresh token for session management | [optional] 

## Example

```python
from dedi_client.models.verify_email200_response_data import VerifyEmail200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of VerifyEmail200ResponseData from a JSON string
verify_email200_response_data_instance = VerifyEmail200ResponseData.from_json(json)
# print the JSON string representation of the object
print(VerifyEmail200ResponseData.to_json())

# convert the object into a dict
verify_email200_response_data_dict = verify_email200_response_data_instance.to_dict()
# create an instance of VerifyEmail200ResponseData from a dict
verify_email200_response_data_from_dict = VerifyEmail200ResponseData.from_dict(verify_email200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


