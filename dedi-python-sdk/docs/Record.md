# Record


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**record_id** | **str** | Unique record identifier | [optional] 
**record_name** | **str** | Record name | [optional] 
**registry_id** | **str** | Parent registry ID | [optional] 
**registry_name** | **str** | Parent registry name | [optional] 
**namespace_id** | **str** | Parent namespace ID | [optional] 
**namespace** | **str** | Parent namespace name | [optional] 
**description** | **str** | Record description | [optional] 
**digest** | **str** | Cryptographic digest of record data | [optional] 
**details** | **object** | Record data conforming to registry schema | [optional] 
**meta** | **object** | Additional metadata | [optional] 
**version** | **str** | Current version | [optional] 
**version_count** | **int** | Total number of versions | [optional] 
**genesis** | **str** | Original version digest | [optional] 
**created_at** | **datetime** | Creation timestamp | [optional] 
**updated_at** | **datetime** | Last update timestamp | [optional] 
**created_by** | **str** | Creator user ID | [optional] 
**state** | **str** | Current record state | [optional] 
**valid_till** | **datetime** | Record expiration timestamp | [optional] 
**ttl** | **int** | Time to live in seconds | [optional] 

## Example

```python
from dedi_client.models.record import Record

# TODO update the JSON string below
json = "{}"
# create an instance of Record from a JSON string
record_instance = Record.from_json(json)
# print the JSON string representation of the object
print(Record.to_json())

# convert the object into a dict
record_dict = record_instance.to_dict()
# create an instance of Record from a dict
record_from_dict = Record.from_dict(record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


