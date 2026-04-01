# BulkUploadRecords202Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**data** | [**BulkUploadRecords202ResponseData**](BulkUploadRecords202ResponseData.md) |  | [optional] 

## Example

```python
from dedi_client.models.bulk_upload_records202_response import BulkUploadRecords202Response

# TODO update the JSON string below
json = "{}"
# create an instance of BulkUploadRecords202Response from a JSON string
bulk_upload_records202_response_instance = BulkUploadRecords202Response.from_json(json)
# print the JSON string representation of the object
print(BulkUploadRecords202Response.to_json())

# convert the object into a dict
bulk_upload_records202_response_dict = bulk_upload_records202_response_instance.to_dict()
# create an instance of BulkUploadRecords202Response from a dict
bulk_upload_records202_response_from_dict = BulkUploadRecords202Response.from_dict(bulk_upload_records202_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


