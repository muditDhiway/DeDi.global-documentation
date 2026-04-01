# VerifyDomainRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**namespace** | **str** | Namespace ID | 
**domain** | **str** | Domain to verify | 

## Example

```python
from dedi_client.models.verify_domain_request import VerifyDomainRequest

# TODO update the JSON string below
json = "{}"
# create an instance of VerifyDomainRequest from a JSON string
verify_domain_request_instance = VerifyDomainRequest.from_json(json)
# print the JSON string representation of the object
print(VerifyDomainRequest.to_json())

# convert the object into a dict
verify_domain_request_dict = verify_domain_request_instance.to_dict()
# create an instance of VerifyDomainRequest from a dict
verify_domain_request_from_dict = VerifyDomainRequest.from_dict(verify_domain_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


