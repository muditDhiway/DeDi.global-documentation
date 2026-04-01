# dedi_client.QueryApi

All URIs are relative to *https://api.dedi.global*

Method | HTTP request | Description
------------- | ------------- | -------------
[**query_namespace_registries**](QueryApi.md#query_namespace_registries) | **GET** /dedi/query/{namespace} | Query namespace registries
[**query_registry_records**](QueryApi.md#query_registry_records) | **GET** /dedi/query/{namespace}/{registry_name} | Query registry records


# **query_namespace_registries**
> QueryNamespaceRegistries200Response query_namespace_registries(namespace, var_from=var_from, to=to, state=state, name=name, sort=sort, page=page, page_size=page_size, as_on=as_on)

Query namespace registries

Queries all registries within a namespace with filtering and pagination support.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.query_namespace_registries200_response import QueryNamespaceRegistries200Response
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
    api_instance = dedi_client.QueryApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    var_from = '2013-10-20' # date | Filter registries updated from date (YYYY-MM-DD) (optional)
    to = '2013-10-20' # date | Filter registries updated to date (YYYY-MM-DD) (optional)
    state = 'state_example' # str | Filter by registry state (optional)
    name = 'name_example' # str | Search by registry name (minimum 3 characters) (optional)
    sort = 'sort_example' # str | Sort results (optional)
    page = 56 # int | Page number for pagination (optional)
    page_size = 56 # int | Items per page (optional)
    as_on = '2013-10-20' # date | Historical query date (YYYY-MM-DD) (optional)

    try:
        # Query namespace registries
        api_response = api_instance.query_namespace_registries(namespace, var_from=var_from, to=to, state=state, name=name, sort=sort, page=page, page_size=page_size, as_on=as_on)
        print("The response of QueryApi->query_namespace_registries:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling QueryApi->query_namespace_registries: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **var_from** | **date**| Filter registries updated from date (YYYY-MM-DD) | [optional] 
 **to** | **date**| Filter registries updated to date (YYYY-MM-DD) | [optional] 
 **state** | **str**| Filter by registry state | [optional] 
 **name** | **str**| Search by registry name (minimum 3 characters) | [optional] 
 **sort** | **str**| Sort results | [optional] 
 **page** | **int**| Page number for pagination | [optional] 
 **page_size** | **int**| Items per page | [optional] 
 **as_on** | **date**| Historical query date (YYYY-MM-DD) | [optional] 

### Return type

[**QueryNamespaceRegistries200Response**](QueryNamespaceRegistries200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Registries retrieved successfully |  -  |
**404** | Namespace not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **query_registry_records**
> QueryRegistryRecords200Response query_registry_records(namespace, registry_name, var_from=var_from, to=to, state=state, name=name, sort=sort, page=page, page_size=page_size, as_on=as_on)

Query registry records

Queries all records within a registry with filtering and pagination support.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.query_registry_records200_response import QueryRegistryRecords200Response
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
    api_instance = dedi_client.QueryApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    registry_name = 'registry_name_example' # str | Registry name to query
    var_from = '2013-10-20' # date | Filter records updated from date (YYYY-MM-DD) (optional)
    to = '2013-10-20' # date | Filter records updated to date (YYYY-MM-DD) (optional)
    state = 'state_example' # str | Filter by record state (optional)
    name = 'name_example' # str | Search by record name (minimum 3 characters) (optional)
    sort = 'sort_example' # str | Sort results (optional)
    page = 56 # int | Page number for pagination (optional)
    page_size = 56 # int | Items per page (optional)
    as_on = '2013-10-20' # date | Historical query date (YYYY-MM-DD) (optional)

    try:
        # Query registry records
        api_response = api_instance.query_registry_records(namespace, registry_name, var_from=var_from, to=to, state=state, name=name, sort=sort, page=page, page_size=page_size, as_on=as_on)
        print("The response of QueryApi->query_registry_records:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling QueryApi->query_registry_records: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **registry_name** | **str**| Registry name to query | 
 **var_from** | **date**| Filter records updated from date (YYYY-MM-DD) | [optional] 
 **to** | **date**| Filter records updated to date (YYYY-MM-DD) | [optional] 
 **state** | **str**| Filter by record state | [optional] 
 **name** | **str**| Search by record name (minimum 3 characters) | [optional] 
 **sort** | **str**| Sort results | [optional] 
 **page** | **int**| Page number for pagination | [optional] 
 **page_size** | **int**| Items per page | [optional] 
 **as_on** | **date**| Historical query date (YYYY-MM-DD) | [optional] 

### Return type

[**QueryRegistryRecords200Response**](QueryRegistryRecords200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Records retrieved successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

