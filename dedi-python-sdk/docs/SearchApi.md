# dedi_client.SearchApi

All URIs are relative to *https://api.dedi.global*

Method | HTTP request | Description
------------- | ------------- | -------------
[**search_records**](SearchApi.md#search_records) | **GET** /dedi/search/{namespace} | Advanced record search


# **search_records**
> SearchRecords200Response search_records(namespace, registry_name=registry_name, record_name=record_name, email=email, public_key=public_key, detail_address=detail_address, profile_name=profile_name)

Advanced record search

Powerful search functionality across all records in a namespace with support for nested field searching and flexible filtering.

**Search Capabilities:**
- Registry filtering by name
- Record name search with partial matching
- Direct field search in record details
- Nested field search using dot notation
- Multiple criteria combination
- Case-insensitive partial matching

**Field Search Examples:**
- Basic fields: `email`, `publicKey`, `phone`, `name`
- Nested fields: `detail.address`, `profile.name`, `contact.email`
- Deep nesting: `data.user.profile.settings.theme`


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.search_records200_response import SearchRecords200Response
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
    api_instance = dedi_client.SearchApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name to search within
    registry_name = 'registry_name_example' # str | Filter by registry name (partial match) (optional)
    record_name = 'record_name_example' # str | Search by record name (partial match) (optional)
    email = 'email_example' # str | Search by email field in record details (optional)
    public_key = 'public_key_example' # str | Search by publicKey field in record details (optional)
    detail_address = 'detail_address_example' # str | Example - Search nested field using dot notation (optional)
    profile_name = 'profile_name_example' # str | Example - Search deeply nested field (optional)

    try:
        # Advanced record search
        api_response = api_instance.search_records(namespace, registry_name=registry_name, record_name=record_name, email=email, public_key=public_key, detail_address=detail_address, profile_name=profile_name)
        print("The response of SearchApi->search_records:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SearchApi->search_records: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name to search within | 
 **registry_name** | **str**| Filter by registry name (partial match) | [optional] 
 **record_name** | **str**| Search by record name (partial match) | [optional] 
 **email** | **str**| Search by email field in record details | [optional] 
 **public_key** | **str**| Search by publicKey field in record details | [optional] 
 **detail_address** | **str**| Example - Search nested field using dot notation | [optional] 
 **profile_name** | **str**| Example - Search deeply nested field | [optional] 

### Return type

[**SearchRecords200Response**](SearchRecords200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Search results retrieved successfully |  -  |
**400** | Missing namespace parameter |  -  |
**401** | Unauthorized - invalid or missing token |  -  |
**404** | Namespace not found |  -  |
**500** | Query failed or database error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

