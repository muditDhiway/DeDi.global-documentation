# GetApiKey200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**api_key** | **str** | Generated API key for Bearer authentication | [optional] 

## Example

```python
from dedi_client.models.get_api_key200_response_data import GetApiKey200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of GetApiKey200ResponseData from a JSON string
get_api_key200_response_data_instance = GetApiKey200ResponseData.from_json(json)
# print the JSON string representation of the object
print(GetApiKey200ResponseData.to_json())

# convert the object into a dict
get_api_key200_response_data_dict = get_api_key200_response_data_instance.to_dict()
# create an instance of GetApiKey200ResponseData from a dict
get_api_key200_response_data_from_dict = GetApiKey200ResponseData.from_dict(get_api_key200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


