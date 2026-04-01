# dedi_client.DelegationApi

All URIs are relative to *https://api.dedi.global*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_registry_delegate**](DelegationApi.md#add_registry_delegate) | **POST** /dedi/{namespace}/{registry_name}/add-delegate | Add registry delegate
[**remove_registry_delegate**](DelegationApi.md#remove_registry_delegate) | **POST** /dedi/{namespace}/{registry_name}/remove-delegate | Remove registry delegate


# **add_registry_delegate**
> SuccessResponse add_registry_delegate(namespace, registry_name, add_registry_delegate_request)

Add registry delegate

Adds a delegate user who can manage records in the registry.
Delegates have permissions to create, update, and manage records.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.add_registry_delegate_request import AddRegistryDelegateRequest
from dedi_client.models.success_response import SuccessResponse
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
    api_instance = dedi_client.DelegationApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    registry_name = 'registry_name_example' # str | Registry name
    add_registry_delegate_request = dedi_client.AddRegistryDelegateRequest() # AddRegistryDelegateRequest | 

    try:
        # Add registry delegate
        api_response = api_instance.add_registry_delegate(namespace, registry_name, add_registry_delegate_request)
        print("The response of DelegationApi->add_registry_delegate:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DelegationApi->add_registry_delegate: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **registry_name** | **str**| Registry name | 
 **add_registry_delegate_request** | [**AddRegistryDelegateRequest**](AddRegistryDelegateRequest.md)|  | 

### Return type

[**SuccessResponse**](SuccessResponse.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Delegate added successfully |  -  |
**400** | Bad request |  -  |
**403** | Insufficient permissions |  -  |
**404** | Registry or user not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_registry_delegate**
> SuccessResponse remove_registry_delegate(namespace, registry_name, remove_registry_delegate_request)

Remove registry delegate

Removes a delegate user from the registry, revoking their permissions to manage records.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.remove_registry_delegate_request import RemoveRegistryDelegateRequest
from dedi_client.models.success_response import SuccessResponse
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
    api_instance = dedi_client.DelegationApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    registry_name = 'registry_name_example' # str | Registry name
    remove_registry_delegate_request = dedi_client.RemoveRegistryDelegateRequest() # RemoveRegistryDelegateRequest | 

    try:
        # Remove registry delegate
        api_response = api_instance.remove_registry_delegate(namespace, registry_name, remove_registry_delegate_request)
        print("The response of DelegationApi->remove_registry_delegate:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DelegationApi->remove_registry_delegate: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **registry_name** | **str**| Registry name | 
 **remove_registry_delegate_request** | [**RemoveRegistryDelegateRequest**](RemoveRegistryDelegateRequest.md)|  | 

### Return type

[**SuccessResponse**](SuccessResponse.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Delegate removed successfully |  -  |
**400** | Bad request |  -  |
**403** | Insufficient permissions |  -  |
**404** | Registry, delegate, or user not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

