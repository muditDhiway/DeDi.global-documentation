# GetUserJobs200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**data** | [**List[JobStatus]**](JobStatus.md) |  | [optional] 

## Example

```python
from dedi_client.models.get_user_jobs200_response import GetUserJobs200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetUserJobs200Response from a JSON string
get_user_jobs200_response_instance = GetUserJobs200Response.from_json(json)
# print the JSON string representation of the object
print(GetUserJobs200Response.to_json())

# convert the object into a dict
get_user_jobs200_response_dict = get_user_jobs200_response_instance.to_dict()
# create an instance of GetUserJobs200Response from a dict
get_user_jobs200_response_from_dict = GetUserJobs200Response.from_dict(get_user_jobs200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


