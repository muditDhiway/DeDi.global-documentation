# GenerateTxtRecord200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**data** | [**GenerateTxtRecord200ResponseData**](GenerateTxtRecord200ResponseData.md) |  | [optional] 

## Example

```python
from dedi_client.models.generate_txt_record200_response import GenerateTxtRecord200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GenerateTxtRecord200Response from a JSON string
generate_txt_record200_response_instance = GenerateTxtRecord200Response.from_json(json)
# print the JSON string representation of the object
print(GenerateTxtRecord200Response.to_json())

# convert the object into a dict
generate_txt_record200_response_dict = generate_txt_record200_response_instance.to_dict()
# create an instance of GenerateTxtRecord200Response from a dict
generate_txt_record200_response_from_dict = GenerateTxtRecord200Response.from_dict(generate_txt_record200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


