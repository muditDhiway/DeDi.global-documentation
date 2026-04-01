# dedi_client.AccessApi

All URIs are relative to *https://api.dedi.global*

Method | HTTP request | Description
------------- | ------------- | -------------
[**lookup_namespace**](AccessApi.md#lookup_namespace) | **GET** /dedi/lookup/{namespace} | Namespace lookup
[**lookup_record**](AccessApi.md#lookup_record) | **GET** /dedi/lookup/{namespace}/{registry_name}/{record_name} | Record lookup
[**lookup_registry**](AccessApi.md#lookup_registry) | **GET** /dedi/lookup/{namespace}/{registry_name} | Registry lookup


# **lookup_namespace**
> LookupNamespace200Response lookup_namespace(namespace, version_id=version_id, as_on=as_on)

Namespace lookup

Retrieves detailed information about a specific namespace including metadata and configuration.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.lookup_namespace200_response import LookupNamespace200Response
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
    api_instance = dedi_client.AccessApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    version_id = 'version_id_example' # str | Specific version to retrieve (optional)
    as_on = '2013-10-20' # date | Historical lookup date (YYYY-MM-DD) (optional)

    try:
        # Namespace lookup
        api_response = api_instance.lookup_namespace(namespace, version_id=version_id, as_on=as_on)
        print("The response of AccessApi->lookup_namespace:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccessApi->lookup_namespace: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **version_id** | **str**| Specific version to retrieve | [optional] 
 **as_on** | **date**| Historical lookup date (YYYY-MM-DD) | [optional] 

### Return type

[**LookupNamespace200Response**](LookupNamespace200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Namespace retrieved successfully |  -  |
**404** | Namespace not found |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **lookup_record**
> LookupRecord200Response lookup_record(namespace, registry_name, record_name, version_id=version_id, as_on=as_on)

Record lookup

Retrieves detailed information about a specific record including data and metadata.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.lookup_record200_response import LookupRecord200Response
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
    api_instance = dedi_client.AccessApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    registry_name = 'registry_name_example' # str | Registry name containing the record
    record_name = 'record_name_example' # str | Record name to lookup
    version_id = 'version_id_example' # str | Specific version to retrieve (optional)
    as_on = '2013-10-20' # date | Historical lookup date (YYYY-MM-DD) (optional)

    try:
        # Record lookup
        api_response = api_instance.lookup_record(namespace, registry_name, record_name, version_id=version_id, as_on=as_on)
        print("The response of AccessApi->lookup_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccessApi->lookup_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **registry_name** | **str**| Registry name containing the record | 
 **record_name** | **str**| Record name to lookup | 
 **version_id** | **str**| Specific version to retrieve | [optional] 
 **as_on** | **date**| Historical lookup date (YYYY-MM-DD) | [optional] 

### Return type

[**LookupRecord200Response**](LookupRecord200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Record retrieved successfully |  -  |
**404** | Record not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **lookup_registry**
> LookupRegistry200Response lookup_registry(namespace, registry_name, version_id=version_id, as_on=as_on)

Registry lookup

Retrieves detailed information about a specific registry including schema and configuration.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.lookup_registry200_response import LookupRegistry200Response
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
    api_instance = dedi_client.AccessApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    registry_name = 'registry_name_example' # str | Registry name
    version_id = 'version_id_example' # str | Specific version to retrieve (optional)
    as_on = '2013-10-20' # date | Historical lookup date (YYYY-MM-DD) (optional)

    try:
        # Registry lookup
        api_response = api_instance.lookup_registry(namespace, registry_name, version_id=version_id, as_on=as_on)
        print("The response of AccessApi->lookup_registry:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccessApi->lookup_registry: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **registry_name** | **str**| Registry name | 
 **version_id** | **str**| Specific version to retrieve | [optional] 
 **as_on** | **date**| Historical lookup date (YYYY-MM-DD) | [optional] 

### Return type

[**LookupRegistry200Response**](LookupRegistry200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Registry retrieved successfully |  -  |
**404** | Registry not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

