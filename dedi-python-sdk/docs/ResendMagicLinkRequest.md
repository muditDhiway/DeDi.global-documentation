# ResendMagicLinkRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**action** | **str** | Should be &#39;register&#39; | 
**email** | **str** | Email address of the account | 
**name** | **str** | User&#39;s name | 
**password** | **str** | User&#39;s password | 

## Example

```python
from dedi_client.models.resend_magic_link_request import ResendMagicLinkRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ResendMagicLinkRequest from a JSON string
resend_magic_link_request_instance = ResendMagicLinkRequest.from_json(json)
# print the JSON string representation of the object
print(ResendMagicLinkRequest.to_json())

# convert the object into a dict
resend_magic_link_request_dict = resend_magic_link_request_instance.to_dict()
# create an instance of ResendMagicLinkRequest from a dict
resend_magic_link_request_from_dict = ResendMagicLinkRequest.from_dict(resend_magic_link_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


