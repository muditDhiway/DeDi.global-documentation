# GetRecordVersions200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_by** | **str** |  | [optional] 
**var_schema** | **object** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 
**total_versions** | **int** |  | [optional] 
**versions** | **List[str]** |  | [optional] 
**ttl** | **int** |  | [optional] 

## Example

```python
from dedi_client.models.get_record_versions200_response_data import GetRecordVersions200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of GetRecordVersions200ResponseData from a JSON string
get_record_versions200_response_data_instance = GetRecordVersions200ResponseData.from_json(json)
# print the JSON string representation of the object
print(GetRecordVersions200ResponseData.to_json())

# convert the object into a dict
get_record_versions200_response_data_dict = get_record_versions200_response_data_instance.to_dict()
# create an instance of GetRecordVersions200ResponseData from a dict
get_record_versions200_response_data_from_dict = GetRecordVersions200ResponseData.from_dict(get_record_versions200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


