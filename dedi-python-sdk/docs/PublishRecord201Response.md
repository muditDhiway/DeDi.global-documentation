# PublishRecord201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**data** | [**Record**](Record.md) |  | [optional] 

## Example

```python
from dedi_client.models.publish_record201_response import PublishRecord201Response

# TODO update the JSON string below
json = "{}"
# create an instance of PublishRecord201Response from a JSON string
publish_record201_response_instance = PublishRecord201Response.from_json(json)
# print the JSON string representation of the object
print(PublishRecord201Response.to_json())

# convert the object into a dict
publish_record201_response_dict = publish_record201_response_instance.to_dict()
# create an instance of PublishRecord201Response from a dict
publish_record201_response_from_dict = PublishRecord201Response.from_dict(publish_record201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


