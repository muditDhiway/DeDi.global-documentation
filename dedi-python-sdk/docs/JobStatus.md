# JobStatus


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**job_id** | **str** | Unique job identifier | [optional] 
**job_type** | **str** | Type of job (e.g., bulk_upload) | [optional] 
**status** | **str** | Current job status | [optional] 
**progress** | [**JobStatusProgress**](JobStatusProgress.md) |  | [optional] 
**result** | **object** | Job result data (when completed) | [optional] 
**error** | **str** | Error message (if failed) | [optional] 
**created_at** | **datetime** | Job creation timestamp | [optional] 
**updated_at** | **datetime** | Last update timestamp | [optional] 

## Example

```python
from dedi_client.models.job_status import JobStatus

# TODO update the JSON string below
json = "{}"
# create an instance of JobStatus from a JSON string
job_status_instance = JobStatus.from_json(json)
# print the JSON string representation of the object
print(JobStatus.to_json())

# convert the object into a dict
job_status_dict = job_status_instance.to_dict()
# create an instance of JobStatus from a dict
job_status_from_dict = JobStatus.from_dict(job_status_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


