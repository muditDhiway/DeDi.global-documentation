# dedi_client.DomainVerificationApi

All URIs are relative to *https://api.dedi.global*

Method | HTTP request | Description
------------- | ------------- | -------------
[**check_domain_verification**](DomainVerificationApi.md#check_domain_verification) | **GET** /dedi/check-verification/{namespace} | Check domain verification status
[**generate_txt_record**](DomainVerificationApi.md#generate_txt_record) | **GET** /dedi/generate-txt/{namespace} | Generate TXT record
[**remove_namespace_verification**](DomainVerificationApi.md#remove_namespace_verification) | **POST** /dedi/{namespace}/remove-namespace-verification | Remove namespace domain verification
[**verify_domain**](DomainVerificationApi.md#verify_domain) | **POST** /dedi/verify-domain | Verify domain ownership


# **check_domain_verification**
> CheckDomainVerification200Response check_domain_verification(namespace)

Check domain verification status

Checks the current domain verification status for a namespace.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.check_domain_verification200_response import CheckDomainVerification200Response
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
    api_instance = dedi_client.DomainVerificationApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name

    try:
        # Check domain verification status
        api_response = api_instance.check_domain_verification(namespace)
        print("The response of DomainVerificationApi->check_domain_verification:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainVerificationApi->check_domain_verification: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 

### Return type

[**CheckDomainVerification200Response**](CheckDomainVerification200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Verification status retrieved |  -  |
**404** | Namespace not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **generate_txt_record**
> GenerateTxtRecord200Response generate_txt_record(namespace)

Generate TXT record

Generates a DNS TXT record for domain verification.
Used to verify ownership of a domain for namespace binding.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.generate_txt_record200_response import GenerateTxtRecord200Response
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
    api_instance = dedi_client.DomainVerificationApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name

    try:
        # Generate TXT record
        api_response = api_instance.generate_txt_record(namespace)
        print("The response of DomainVerificationApi->generate_txt_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainVerificationApi->generate_txt_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 

### Return type

[**GenerateTxtRecord200Response**](GenerateTxtRecord200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | TXT record generated |  -  |
**400** | Bad request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_namespace_verification**
> RemoveNamespaceVerification200Response remove_namespace_verification(namespace)

Remove namespace domain verification

Removes domain verification from a namespace, reverting it to unverified status.
This operation removes the domain association and resets verification status.

**Authentication:** Required (Cookie or API Key)

**Prerequisites:**
- Namespace must exist and be currently verified
- Domain must be associated with the namespace

**Process:**
1. Validates namespace exists (by ID or domain)
2. Confirms namespace is currently verified  
3. Removes the domain verification record from database
4. Resets namespace verification status to false
5. Clears the domain association from namespace

**Important Notes:**
- This action is irreversible - verification must be performed again to re-verify
- Removing verification does not delete the namespace itself
- The namespace can be re-verified with the same or different domain after removal
- This reduces the trust level of the namespace


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.remove_namespace_verification200_response import RemoveNamespaceVerification200Response
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
    api_instance = dedi_client.DomainVerificationApi(api_client)
    namespace = 'techcorp.com' # str | Namespace ID or verified domain name to remove verification from

    try:
        # Remove namespace domain verification
        api_response = api_instance.remove_namespace_verification(namespace)
        print("The response of DomainVerificationApi->remove_namespace_verification:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainVerificationApi->remove_namespace_verification: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or verified domain name to remove verification from | 

### Return type

[**RemoveNamespaceVerification200Response**](RemoveNamespaceVerification200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Namespace verification removed successfully |  -  |
**400** | Bad request - namespace parameter required |  -  |
**404** | Namespace not found, namespace not verified, or domain not found |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **verify_domain**
> SuccessResponse verify_domain(verify_domain_request)

Verify domain ownership

Verifies domain ownership by checking the DNS TXT record.
Must be called after adding the TXT record to domain DNS.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.success_response import SuccessResponse
from dedi_client.models.verify_domain_request import VerifyDomainRequest
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
    api_instance = dedi_client.DomainVerificationApi(api_client)
    verify_domain_request = dedi_client.VerifyDomainRequest() # VerifyDomainRequest | 

    try:
        # Verify domain ownership
        api_response = api_instance.verify_domain(verify_domain_request)
        print("The response of DomainVerificationApi->verify_domain:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainVerificationApi->verify_domain: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **verify_domain_request** | [**VerifyDomainRequest**](VerifyDomainRequest.md)|  | 

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
**200** | Domain verified successfully |  -  |
**400** | Verification failed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

