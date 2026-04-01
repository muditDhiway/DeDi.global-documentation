# dedi_client.UpdatesApi

All URIs are relative to *https://api.dedi.global*

Method | HTTP request | Description
------------- | ------------- | -------------
[**update_namespace**](UpdatesApi.md#update_namespace) | **POST** /dedi/{namespace}/update-namespace | Update namespace
[**update_record**](UpdatesApi.md#update_record) | **POST** /dedi/{namespace}/{registry_name}/{record_name}/update-record | Update record
[**update_registry**](UpdatesApi.md#update_registry) | **POST** /dedi/{namespace}/{registry_name}/update-registry | Update registry


# **update_namespace**
> SuccessResponse update_namespace(namespace, update_namespace_request)

Update namespace

Updates namespace information such as description and metadata.
The namespace name cannot be changed after creation.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.success_response import SuccessResponse
from dedi_client.models.update_namespace_request import UpdateNamespaceRequest
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
    api_instance = dedi_client.UpdatesApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    update_namespace_request = dedi_client.UpdateNamespaceRequest() # UpdateNamespaceRequest | 

    try:
        # Update namespace
        api_response = api_instance.update_namespace(namespace, update_namespace_request)
        print("The response of UpdatesApi->update_namespace:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UpdatesApi->update_namespace: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **update_namespace_request** | [**UpdateNamespaceRequest**](UpdateNamespaceRequest.md)|  | 

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
**200** | Namespace updated successfully |  -  |
**400** | Bad request |  -  |
**403** | Insufficient permissions |  -  |
**404** | Namespace not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_record**
> SuccessResponse update_record(namespace, registry_name, record_name, update_record_request)

Update record

Updates record information including description, details, and metadata.
Creates a new version of the record while preserving history.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.success_response import SuccessResponse
from dedi_client.models.update_record_request import UpdateRecordRequest
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
    api_instance = dedi_client.UpdatesApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    registry_name = 'registry_name_example' # str | Registry name
    record_name = 'record_name_example' # str | Record name
    update_record_request = dedi_client.UpdateRecordRequest() # UpdateRecordRequest | 

    try:
        # Update record
        api_response = api_instance.update_record(namespace, registry_name, record_name, update_record_request)
        print("The response of UpdatesApi->update_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UpdatesApi->update_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **registry_name** | **str**| Registry name | 
 **record_name** | **str**| Record name | 
 **update_record_request** | [**UpdateRecordRequest**](UpdateRecordRequest.md)|  | 

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
**200** | Record updated successfully |  -  |
**400** | Bad request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_registry**
> SuccessResponse update_registry(namespace, registry_name, update_registry_request)

Update registry

Updates registry information including description, schema, and metadata.
Schema updates must be backward compatible.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.success_response import SuccessResponse
from dedi_client.models.update_registry_request import UpdateRegistryRequest
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
    api_instance = dedi_client.UpdatesApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    registry_name = 'registry_name_example' # str | Registry name
    update_registry_request = dedi_client.UpdateRegistryRequest() # UpdateRegistryRequest | 

    try:
        # Update registry
        api_response = api_instance.update_registry(namespace, registry_name, update_registry_request)
        print("The response of UpdatesApi->update_registry:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UpdatesApi->update_registry: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **registry_name** | **str**| Registry name | 
 **update_registry_request** | [**UpdateRegistryRequest**](UpdateRegistryRequest.md)|  | 

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
**200** | Registry updated successfully |  -  |
**400** | Bad request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

