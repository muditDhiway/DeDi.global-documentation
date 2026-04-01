# JobStatusProgress


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **int** | Total number of items to process | [optional] 
**processed** | **int** | Number of items processed | [optional] 
**failed** | **int** | Number of items that failed | [optional] 

## Example

```python
from dedi_client.models.job_status_progress import JobStatusProgress

# TODO update the JSON string below
json = "{}"
# create an instance of JobStatusProgress from a JSON string
job_status_progress_instance = JobStatusProgress.from_json(json)
# print the JSON string representation of the object
print(JobStatusProgress.to_json())

# convert the object into a dict
job_status_progress_dict = job_status_progress_instance.to_dict()
# create an instance of JobStatusProgress from a dict
job_status_progress_from_dict = JobStatusProgress.from_dict(job_status_progress_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


