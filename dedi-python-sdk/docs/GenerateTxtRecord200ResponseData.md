# GenerateTxtRecord200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**txt_record** | **str** | DNS TXT record to add to domain | [optional] 

## Example

```python
from dedi_client.models.generate_txt_record200_response_data import GenerateTxtRecord200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of GenerateTxtRecord200ResponseData from a JSON string
generate_txt_record200_response_data_instance = GenerateTxtRecord200ResponseData.from_json(json)
# print the JSON string representation of the object
print(GenerateTxtRecord200ResponseData.to_json())

# convert the object into a dict
generate_txt_record200_response_data_dict = generate_txt_record200_response_data_instance.to_dict()
# create an instance of GenerateTxtRecord200ResponseData from a dict
generate_txt_record200_response_data_from_dict = GenerateTxtRecord200ResponseData.from_dict(generate_txt_record200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


