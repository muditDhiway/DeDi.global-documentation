# VerifyEmail200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | [optional] 
**data** | [**VerifyEmail200ResponseData**](VerifyEmail200ResponseData.md) |  | [optional] 

## Example

```python
from dedi_client.models.verify_email200_response import VerifyEmail200Response

# TODO update the JSON string below
json = "{}"
# create an instance of VerifyEmail200Response from a JSON string
verify_email200_response_instance = VerifyEmail200Response.from_json(json)
# print the JSON string representation of the object
print(VerifyEmail200Response.to_json())

# convert the object into a dict
verify_email200_response_dict = verify_email200_response_instance.to_dict()
# create an instance of VerifyEmail200Response from a dict
verify_email200_response_from_dict = VerifyEmail200Response.from_dict(verify_email200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


