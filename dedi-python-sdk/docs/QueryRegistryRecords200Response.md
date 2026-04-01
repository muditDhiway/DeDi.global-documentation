# QueryRegistryRecords200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**data** | [**QueryRegistryRecords200ResponseData**](QueryRegistryRecords200ResponseData.md) |  | [optional] 

## Example

```python
from dedi_client.models.query_registry_records200_response import QueryRegistryRecords200Response

# TODO update the JSON string below
json = "{}"
# create an instance of QueryRegistryRecords200Response from a JSON string
query_registry_records200_response_instance = QueryRegistryRecords200Response.from_json(json)
# print the JSON string representation of the object
print(QueryRegistryRecords200Response.to_json())

# convert the object into a dict
query_registry_records200_response_dict = query_registry_records200_response_instance.to_dict()
# create an instance of QueryRegistryRecords200Response from a dict
query_registry_records200_response_from_dict = QueryRegistryRecords200Response.from_dict(query_registry_records200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


