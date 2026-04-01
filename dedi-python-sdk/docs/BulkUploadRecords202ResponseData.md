# BulkUploadRecords202ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**job_id** | **str** | Job ID for tracking progress | [optional] 

## Example

```python
from dedi_client.models.bulk_upload_records202_response_data import BulkUploadRecords202ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of BulkUploadRecords202ResponseData from a JSON string
bulk_upload_records202_response_data_instance = BulkUploadRecords202ResponseData.from_json(json)
# print the JSON string representation of the object
print(BulkUploadRecords202ResponseData.to_json())

# convert the object into a dict
bulk_upload_records202_response_data_dict = bulk_upload_records202_response_data_instance.to_dict()
# create an instance of BulkUploadRecords202ResponseData from a dict
bulk_upload_records202_response_data_from_dict = BulkUploadRecords202ResponseData.from_dict(bulk_upload_records202_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


