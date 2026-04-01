# QueryRegistryRecords200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**namespace_id** | **str** |  | [optional] 
**namespace_name** | **str** |  | [optional] 
**registry_id** | **str** |  | [optional] 
**registry_name** | **str** |  | [optional] 
**total_records** | **int** |  | [optional] 
**page_number** | **int** |  | [optional] 
**page_size** | **int** |  | [optional] 
**records** | [**List[RecordSummary]**](RecordSummary.md) |  | [optional] 

## Example

```python
from dedi_client.models.query_registry_records200_response_data import QueryRegistryRecords200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of QueryRegistryRecords200ResponseData from a JSON string
query_registry_records200_response_data_instance = QueryRegistryRecords200ResponseData.from_json(json)
# print the JSON string representation of the object
print(QueryRegistryRecords200ResponseData.to_json())

# convert the object into a dict
query_registry_records200_response_data_dict = query_registry_records200_response_data_instance.to_dict()
# create an instance of QueryRegistryRecords200ResponseData from a dict
query_registry_records200_response_data_from_dict = QueryRegistryRecords200ResponseData.from_dict(query_registry_records200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


