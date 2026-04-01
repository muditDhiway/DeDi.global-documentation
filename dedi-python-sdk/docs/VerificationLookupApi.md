# dedi_client.VerificationLookupApi

All URIs are relative to *https://api.dedi.global*

Method | HTTP request | Description
------------- | ------------- | -------------
[**verify_namespace_lookup**](VerificationLookupApi.md#verify_namespace_lookup) | **POST** /dedi/verify-namespace-lookup | Verify namespace lookup
[**verify_record_lookup**](VerificationLookupApi.md#verify_record_lookup) | **POST** /dedi/verify-record-lookup | Verify record lookup
[**verify_registry_lookup**](VerificationLookupApi.md#verify_registry_lookup) | **POST** /dedi/verify-registry-lookup | Verify registry lookup


# **verify_namespace_lookup**
> SuccessResponse verify_namespace_lookup(verify_namespace_lookup_request)

Verify namespace lookup

Verify the authenticity and integrity of a namespace lookup result.

**Authentication:** Required (Cookie or API Key)

**Request Body:**
```json
{
  "namespace_lookup_response": { "message": "...", "data": { /* lookup response */ } }
}
```


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.success_response import SuccessResponse
from dedi_client.models.verify_namespace_lookup_request import VerifyNamespaceLookupRequest
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
    api_instance = dedi_client.VerificationLookupApi(api_client)
    verify_namespace_lookup_request = dedi_client.VerifyNamespaceLookupRequest() # VerifyNamespaceLookupRequest | 

    try:
        # Verify namespace lookup
        api_response = api_instance.verify_namespace_lookup(verify_namespace_lookup_request)
        print("The response of VerificationLookupApi->verify_namespace_lookup:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling VerificationLookupApi->verify_namespace_lookup: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **verify_namespace_lookup_request** | [**VerifyNamespaceLookupRequest**](VerifyNamespaceLookupRequest.md)|  | 

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
**200** | Namespace lookup verified successfully |  -  |
**400** | Verification failed or invalid input |  -  |
**401** | Unauthorized |  -  |
**404** | Namespace not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **verify_record_lookup**
> SuccessResponse verify_record_lookup(verify_record_lookup_request)

Verify record lookup

Verify the authenticity and integrity of a record lookup result.

**Authentication:** Required (Cookie or API Key)

**Request Body:**
```json
{
  "record_lookup_response": { "message": "...", "data": { /* lookup response */ } }
}
```


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.success_response import SuccessResponse
from dedi_client.models.verify_record_lookup_request import VerifyRecordLookupRequest
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
    api_instance = dedi_client.VerificationLookupApi(api_client)
    verify_record_lookup_request = dedi_client.VerifyRecordLookupRequest() # VerifyRecordLookupRequest | 

    try:
        # Verify record lookup
        api_response = api_instance.verify_record_lookup(verify_record_lookup_request)
        print("The response of VerificationLookupApi->verify_record_lookup:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling VerificationLookupApi->verify_record_lookup: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **verify_record_lookup_request** | [**VerifyRecordLookupRequest**](VerifyRecordLookupRequest.md)|  | 

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
**200** | Record lookup verified successfully |  -  |
**400** | Verification failed or invalid input |  -  |
**401** | Unauthorized |  -  |
**404** | Record not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **verify_registry_lookup**
> SuccessResponse verify_registry_lookup(verify_registry_lookup_request)

Verify registry lookup

Verify the authenticity and integrity of a registry lookup result.

**Authentication:** Required (Cookie or API Key)

**Request Body:**
```json
{
  "registry_lookup_response": { "message": "...", "data": { /* lookup response */ } }
}
```


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.success_response import SuccessResponse
from dedi_client.models.verify_registry_lookup_request import VerifyRegistryLookupRequest
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
    api_instance = dedi_client.VerificationLookupApi(api_client)
    verify_registry_lookup_request = dedi_client.VerifyRegistryLookupRequest() # VerifyRegistryLookupRequest | 

    try:
        # Verify registry lookup
        api_response = api_instance.verify_registry_lookup(verify_registry_lookup_request)
        print("The response of VerificationLookupApi->verify_registry_lookup:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling VerificationLookupApi->verify_registry_lookup: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **verify_registry_lookup_request** | [**VerifyRegistryLookupRequest**](VerifyRegistryLookupRequest.md)|  | 

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
**200** | Registry lookup verified successfully |  -  |
**400** | Verification failed or invalid input |  -  |
**401** | Unauthorized |  -  |
**404** | Registry not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

