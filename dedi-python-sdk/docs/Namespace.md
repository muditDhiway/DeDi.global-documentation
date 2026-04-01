# Namespace


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**namespace_id** | **str** | Unique namespace identifier | [optional] 
**name** | **str** | Namespace name | [optional] 
**description** | **str** | Namespace description | [optional] 
**digest** | **str** | Cryptographic digest of namespace data | [optional] 
**meta** | **object** | Additional metadata | [optional] 
**version** | **str** | Current version | [optional] 
**version_count** | **int** | Total number of versions | [optional] 
**created_at** | **datetime** | Creation timestamp | [optional] 
**updated_at** | **datetime** | Last update timestamp | [optional] 
**created_by** | **str** | Creator user ID | [optional] 
**domain** | **str** | Verified domain (if any) | [optional] 
**state** | **str** | Current namespace state | [optional] 
**ttl** | **int** | Time to live in seconds | [optional] 

## Example

```python
from dedi_client.models.namespace import Namespace

# TODO update the JSON string below
json = "{}"
# create an instance of Namespace from a JSON string
namespace_instance = Namespace.from_json(json)
# print the JSON string representation of the object
print(Namespace.to_json())

# convert the object into a dict
namespace_dict = namespace_instance.to_dict()
# create an instance of Namespace from a dict
namespace_from_dict = Namespace.from_dict(namespace_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


