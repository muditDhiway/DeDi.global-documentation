# dedi_client.VersionsApi

All URIs are relative to *https://api.dedi.global*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_namespace_versions**](VersionsApi.md#get_namespace_versions) | **GET** /dedi/versions/{namespace} | Get namespace versions
[**get_record_versions**](VersionsApi.md#get_record_versions) | **GET** /dedi/versions/{namespace}/{registry_name}/{record_name} | Get record versions
[**get_registry_versions**](VersionsApi.md#get_registry_versions) | **GET** /dedi/versions/{namespace}/{registry_name} | Get registry versions


# **get_namespace_versions**
> GetNamespaceVersions200Response get_namespace_versions(namespace)

Get namespace versions

Retrieves all available versions for a specific namespace.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.get_namespace_versions200_response import GetNamespaceVersions200Response
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
    api_instance = dedi_client.VersionsApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name

    try:
        # Get namespace versions
        api_response = api_instance.get_namespace_versions(namespace)
        print("The response of VersionsApi->get_namespace_versions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling VersionsApi->get_namespace_versions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 

### Return type

[**GetNamespaceVersions200Response**](GetNamespaceVersions200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Namespace versions retrieved successfully |  -  |
**404** | Namespace not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_record_versions**
> GetRecordVersions200Response get_record_versions(namespace, registry_name, record_name)

Get record versions

Retrieves all available versions for a specific record.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.get_record_versions200_response import GetRecordVersions200Response
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
    api_instance = dedi_client.VersionsApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    registry_name = 'registry_name_example' # str | Registry name containing the record
    record_name = 'record_name_example' # str | Record name

    try:
        # Get record versions
        api_response = api_instance.get_record_versions(namespace, registry_name, record_name)
        print("The response of VersionsApi->get_record_versions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling VersionsApi->get_record_versions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **registry_name** | **str**| Registry name containing the record | 
 **record_name** | **str**| Record name | 

### Return type

[**GetRecordVersions200Response**](GetRecordVersions200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Record versions retrieved successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_registry_versions**
> GetRegistryVersions200Response get_registry_versions(namespace, registry_name)

Get registry versions

Retrieves all available versions for a specific registry.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.get_registry_versions200_response import GetRegistryVersions200Response
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
    api_instance = dedi_client.VersionsApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    registry_name = 'registry_name_example' # str | Registry name

    try:
        # Get registry versions
        api_response = api_instance.get_registry_versions(namespace, registry_name)
        print("The response of VersionsApi->get_registry_versions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling VersionsApi->get_registry_versions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **registry_name** | **str**| Registry name | 

### Return type

[**GetRegistryVersions200Response**](GetRegistryVersions200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Registry versions retrieved successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

