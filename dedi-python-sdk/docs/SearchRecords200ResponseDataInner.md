# SearchRecords200ResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**record_id** | **str** |  | [optional] 
**record_name** | **str** |  | [optional] 
**registry_name** | **str** |  | [optional] 
**namespace_id** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**details** | **object** | Record data that can contain any fields | [optional] 
**state** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 
**version** | **str** |  | [optional] 
**ttl** | **int** |  | [optional] 

## Example

```python
from dedi_client.models.search_records200_response_data_inner import SearchRecords200ResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of SearchRecords200ResponseDataInner from a JSON string
search_records200_response_data_inner_instance = SearchRecords200ResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(SearchRecords200ResponseDataInner.to_json())

# convert the object into a dict
search_records200_response_data_inner_dict = search_records200_response_data_inner_instance.to_dict()
# create an instance of SearchRecords200ResponseDataInner from a dict
search_records200_response_data_inner_from_dict = SearchRecords200ResponseDataInner.from_dict(search_records200_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


