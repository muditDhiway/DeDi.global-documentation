# RecordSummary


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**record_id** | **str** |  | [optional] 
**record_name** | **str** |  | [optional] 
**digest** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 
**state** | **str** |  | [optional] 
**ttl** | **int** |  | [optional] 

## Example

```python
from dedi_client.models.record_summary import RecordSummary

# TODO update the JSON string below
json = "{}"
# create an instance of RecordSummary from a JSON string
record_summary_instance = RecordSummary.from_json(json)
# print the JSON string representation of the object
print(RecordSummary.to_json())

# convert the object into a dict
record_summary_dict = record_summary_instance.to_dict()
# create an instance of RecordSummary from a dict
record_summary_from_dict = RecordSummary.from_dict(record_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


