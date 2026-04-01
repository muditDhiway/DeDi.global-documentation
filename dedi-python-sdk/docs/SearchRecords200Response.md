# SearchRecords200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**data** | [**List[SearchRecords200ResponseDataInner]**](SearchRecords200ResponseDataInner.md) |  | [optional] 

## Example

```python
from dedi_client.models.search_records200_response import SearchRecords200Response

# TODO update the JSON string below
json = "{}"
# create an instance of SearchRecords200Response from a JSON string
search_records200_response_instance = SearchRecords200Response.from_json(json)
# print the JSON string representation of the object
print(SearchRecords200Response.to_json())

# convert the object into a dict
search_records200_response_dict = search_records200_response_instance.to_dict()
# create an instance of SearchRecords200Response from a dict
search_records200_response_from_dict = SearchRecords200Response.from_dict(search_records200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


