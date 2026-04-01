# RegistrySummary


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**registry_id** | **str** |  | [optional] 
**registry_name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**digest** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 
**state** | **str** |  | [optional] 
**record_count** | **int** |  | [optional] 
**ttl** | **int** |  | [optional] 

## Example

```python
from dedi_client.models.registry_summary import RegistrySummary

# TODO update the JSON string below
json = "{}"
# create an instance of RegistrySummary from a JSON string
registry_summary_instance = RegistrySummary.from_json(json)
# print the JSON string representation of the object
print(RegistrySummary.to_json())

# convert the object into a dict
registry_summary_dict = registry_summary_instance.to_dict()
# create an instance of RegistrySummary from a dict
registry_summary_from_dict = RegistrySummary.from_dict(registry_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


