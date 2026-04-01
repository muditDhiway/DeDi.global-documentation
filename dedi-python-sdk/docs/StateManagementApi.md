# dedi_client.StateManagementApi

All URIs are relative to *https://api.dedi.global*

Method | HTTP request | Description
------------- | ------------- | -------------
[**archive_registry**](StateManagementApi.md#archive_registry) | **POST** /dedi/{namespace}/{registry_name}/archive-registry | Archive registry
[**change_record_state**](StateManagementApi.md#change_record_state) | **POST** /dedi/{namespace}/{registry_name}/{record_name}/change-record-state | Change record state
[**reinstate_record**](StateManagementApi.md#reinstate_record) | **POST** /dedi/{namespace}/{registry_name}/{record_name}/reinstate-record | Reinstate record
[**reinstate_registry**](StateManagementApi.md#reinstate_registry) | **POST** /dedi/{namespace}/{registry_name}/reinstate-registry | Reinstate registry
[**restore_registry**](StateManagementApi.md#restore_registry) | **POST** /dedi/{namespace}/{registry_name}/restore-registry | Restore registry
[**revoke_record**](StateManagementApi.md#revoke_record) | **POST** /dedi/{namespace}/{registry_name}/{record_name}/revoke-record | Revoke record
[**revoke_registry**](StateManagementApi.md#revoke_registry) | **POST** /dedi/{namespace}/{registry_name}/revoke-registry | Revoke registry
[**suspend_record**](StateManagementApi.md#suspend_record) | **POST** /dedi/{namespace}/{registry_name}/{record_name}/suspend-record | Suspend record


# **archive_registry**
> ArchiveRegistry200Response archive_registry(namespace, registry_name)

Archive registry

Archives a registry, making it read-only while preserving existing records.
No new records can be created in archived registries.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.archive_registry200_response import ArchiveRegistry200Response
from dedi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.dedi.global
# See configuration.py for a list of all supported configuration parameters.
configuration = dedi_client.Configuration(
    host = "https://api.dedi.global"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: CookieAuth
configuration.api_key['CookieAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['CookieAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): BearerAuth
configuration = dedi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with dedi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = dedi_client.StateManagementApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    registry_name = 'registry_name_example' # str | Registry name to archive

    try:
        # Archive registry
        api_response = api_instance.archive_registry(namespace, registry_name)
        print("The response of StateManagementApi->archive_registry:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StateManagementApi->archive_registry: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **registry_name** | **str**| Registry name to archive | 

### Return type

[**ArchiveRegistry200Response**](ArchiveRegistry200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Registry archived successfully |  -  |
**404** | Registry not found, already archived, or revoked |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **change_record_state**
> ChangeRecordState200Response change_record_state(namespace, registry_name, record_name, change_record_state_request)

Change record state

Changes the state of a record to a specified value (LIVE, SUSPENDED, REVOKED, EXPIRED).
This is a low-level API for advanced state management.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.change_record_state200_response import ChangeRecordState200Response
from dedi_client.models.change_record_state_request import ChangeRecordStateRequest
from dedi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.dedi.global
# See configuration.py for a list of all supported configuration parameters.
configuration = dedi_client.Configuration(
    host = "https://api.dedi.global"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: CookieAuth
configuration.api_key['CookieAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['CookieAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): BearerAuth
configuration = dedi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with dedi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = dedi_client.StateManagementApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    registry_name = 'registry_name_example' # str | Registry name containing the record
    record_name = 'record_name_example' # str | Record name to change state for
    change_record_state_request = dedi_client.ChangeRecordStateRequest() # ChangeRecordStateRequest | 

    try:
        # Change record state
        api_response = api_instance.change_record_state(namespace, registry_name, record_name, change_record_state_request)
        print("The response of StateManagementApi->change_record_state:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StateManagementApi->change_record_state: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **registry_name** | **str**| Registry name containing the record | 
 **record_name** | **str**| Record name to change state for | 
 **change_record_state_request** | [**ChangeRecordStateRequest**](ChangeRecordStateRequest.md)|  | 

### Return type

[**ChangeRecordState200Response**](ChangeRecordState200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Record state changed successfully |  -  |
**400** | Invalid state or missing parameters |  -  |
**404** | Record not found or state cannot be changed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reinstate_record**
> ReinstateRecord200Response reinstate_record(namespace, registry_name, record_name)

Reinstate record

Reinstates a previously suspended record, making it active and available for queries again.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.reinstate_record200_response import ReinstateRecord200Response
from dedi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.dedi.global
# See configuration.py for a list of all supported configuration parameters.
configuration = dedi_client.Configuration(
    host = "https://api.dedi.global"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: CookieAuth
configuration.api_key['CookieAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['CookieAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): BearerAuth
configuration = dedi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with dedi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = dedi_client.StateManagementApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    registry_name = 'registry_name_example' # str | Registry name containing the record
    record_name = 'record_name_example' # str | Record name to reinstate

    try:
        # Reinstate record
        api_response = api_instance.reinstate_record(namespace, registry_name, record_name)
        print("The response of StateManagementApi->reinstate_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StateManagementApi->reinstate_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **registry_name** | **str**| Registry name containing the record | 
 **record_name** | **str**| Record name to reinstate | 

### Return type

[**ReinstateRecord200Response**](ReinstateRecord200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Record reinstated successfully |  -  |
**404** | Record not found, already active, or cannot be reinstated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reinstate_registry**
> ReinstateRegistry200Response reinstate_registry(namespace, registry_name)

Reinstate registry

Reinstates a previously revoked registry, making it active again for new record creation.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.reinstate_registry200_response import ReinstateRegistry200Response
from dedi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.dedi.global
# See configuration.py for a list of all supported configuration parameters.
configuration = dedi_client.Configuration(
    host = "https://api.dedi.global"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: CookieAuth
configuration.api_key['CookieAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['CookieAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): BearerAuth
configuration = dedi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with dedi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = dedi_client.StateManagementApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    registry_name = 'registry_name_example' # str | Registry name to reinstate

    try:
        # Reinstate registry
        api_response = api_instance.reinstate_registry(namespace, registry_name)
        print("The response of StateManagementApi->reinstate_registry:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StateManagementApi->reinstate_registry: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **registry_name** | **str**| Registry name to reinstate | 

### Return type

[**ReinstateRegistry200Response**](ReinstateRegistry200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Registry reinstated successfully |  -  |
**404** | Registry not found or not in revoked state |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **restore_registry**
> RestoreRegistry200Response restore_registry(namespace, registry_name)

Restore registry

Restores a previously archived registry, making it active again for record creation.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.restore_registry200_response import RestoreRegistry200Response
from dedi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.dedi.global
# See configuration.py for a list of all supported configuration parameters.
configuration = dedi_client.Configuration(
    host = "https://api.dedi.global"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: CookieAuth
configuration.api_key['CookieAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['CookieAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): BearerAuth
configuration = dedi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with dedi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = dedi_client.StateManagementApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    registry_name = 'registry_name_example' # str | Registry name to restore

    try:
        # Restore registry
        api_response = api_instance.restore_registry(namespace, registry_name)
        print("The response of StateManagementApi->restore_registry:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StateManagementApi->restore_registry: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **registry_name** | **str**| Registry name to restore | 

### Return type

[**RestoreRegistry200Response**](RestoreRegistry200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Registry restored successfully |  -  |
**404** | Registry not found or not in archived state |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **revoke_record**
> RevokeRecord200Response revoke_record(namespace, registry_name, record_name)

Revoke record

Permanently revokes a record, making it invalid and preventing any future use.
This action is irreversible.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.revoke_record200_response import RevokeRecord200Response
from dedi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.dedi.global
# See configuration.py for a list of all supported configuration parameters.
configuration = dedi_client.Configuration(
    host = "https://api.dedi.global"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: CookieAuth
configuration.api_key['CookieAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['CookieAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): BearerAuth
configuration = dedi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with dedi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = dedi_client.StateManagementApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    registry_name = 'registry_name_example' # str | Registry name containing the record
    record_name = 'record_name_example' # str | Record name to revoke

    try:
        # Revoke record
        api_response = api_instance.revoke_record(namespace, registry_name, record_name)
        print("The response of StateManagementApi->revoke_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StateManagementApi->revoke_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **registry_name** | **str**| Registry name containing the record | 
 **record_name** | **str**| Record name to revoke | 

### Return type

[**RevokeRecord200Response**](RevokeRecord200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Record revoked successfully |  -  |
**404** | Record not found or already expired |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **revoke_registry**
> RevokeRegistry200Response revoke_registry(namespace, registry_name)

Revoke registry

Permanently revokes a registry, making it invalid and preventing new record creation.
This action is irreversible.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.revoke_registry200_response import RevokeRegistry200Response
from dedi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.dedi.global
# See configuration.py for a list of all supported configuration parameters.
configuration = dedi_client.Configuration(
    host = "https://api.dedi.global"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: CookieAuth
configuration.api_key['CookieAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['CookieAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): BearerAuth
configuration = dedi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with dedi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = dedi_client.StateManagementApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    registry_name = 'registry_name_example' # str | Registry name to revoke

    try:
        # Revoke registry
        api_response = api_instance.revoke_registry(namespace, registry_name)
        print("The response of StateManagementApi->revoke_registry:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StateManagementApi->revoke_registry: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **registry_name** | **str**| Registry name to revoke | 

### Return type

[**RevokeRegistry200Response**](RevokeRegistry200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Registry revoked successfully |  -  |
**404** | Registry not found |  -  |
**403** | Insufficient permissions |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **suspend_record**
> SuspendRecord200Response suspend_record(namespace, registry_name, record_name)

Suspend record

Temporarily suspends a record, making it inactive while preserving its data.
Suspended records can be reinstated.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.suspend_record200_response import SuspendRecord200Response
from dedi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.dedi.global
# See configuration.py for a list of all supported configuration parameters.
configuration = dedi_client.Configuration(
    host = "https://api.dedi.global"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: CookieAuth
configuration.api_key['CookieAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['CookieAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): BearerAuth
configuration = dedi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with dedi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = dedi_client.StateManagementApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    registry_name = 'registry_name_example' # str | Registry name containing the record
    record_name = 'record_name_example' # str | Record name to suspend

    try:
        # Suspend record
        api_response = api_instance.suspend_record(namespace, registry_name, record_name)
        print("The response of StateManagementApi->suspend_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StateManagementApi->suspend_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **registry_name** | **str**| Registry name containing the record | 
 **record_name** | **str**| Record name to suspend | 

### Return type

[**SuspendRecord200Response**](SuspendRecord200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Record suspended successfully |  -  |
**404** | Record not found or cannot be suspended |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

