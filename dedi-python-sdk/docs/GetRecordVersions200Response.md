# GetRecordVersions200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**data** | [**GetRecordVersions200ResponseData**](GetRecordVersions200ResponseData.md) |  | [optional] 

## Example

```python
from dedi_client.models.get_record_versions200_response import GetRecordVersions200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetRecordVersions200Response from a JSON string
get_record_versions200_response_instance = GetRecordVersions200Response.from_json(json)
# print the JSON string representation of the object
print(GetRecordVersions200Response.to_json())

# convert the object into a dict
get_record_versions200_response_dict = get_record_versions200_response_instance.to_dict()
# create an instance of GetRecordVersions200Response from a dict
get_record_versions200_response_from_dict = GetRecordVersions200Response.from_dict(get_record_versions200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


