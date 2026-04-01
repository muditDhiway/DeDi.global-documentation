# User


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_id** | **str** | Unique user identifier | [optional] 
**email** | **str** | User email address | [optional] 
**name** | **str** | User display name | [optional] 
**created_at** | **datetime** | User registration timestamp | [optional] 
**updated_at** | **datetime** | Last update timestamp | [optional] 
**verified** | **bool** | Email verification status | [optional] 
**last_login** | **datetime** | Last login timestamp | [optional] 

## Example

```python
from dedi_client.models.user import User

# TODO update the JSON string below
json = "{}"
# create an instance of User from a JSON string
user_instance = User.from_json(json)
# print the JSON string representation of the object
print(User.to_json())

# convert the object into a dict
user_dict = user_instance.to_dict()
# create an instance of User from a dict
user_from_dict = User.from_dict(user_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


