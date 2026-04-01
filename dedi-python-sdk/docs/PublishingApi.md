# dedi_client.PublishingApi

All URIs are relative to *https://api.dedi.global*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bulk_upload_records**](PublishingApi.md#bulk_upload_records) | **POST** /dedi/{namespace}/{registry_name}/bulk-upload | Bulk upload records
[**create_namespace**](PublishingApi.md#create_namespace) | **POST** /dedi/create-namespace | Create a new namespace
[**create_registry**](PublishingApi.md#create_registry) | **POST** /dedi/{namespace}/create-registry | Create a new registry
[**export_records_as_csv**](PublishingApi.md#export_records_as_csv) | **GET** /dedi/{namespace}/{registry_name}/export-records-as-csv | Export records as CSV
[**get_job_status**](PublishingApi.md#get_job_status) | **GET** /dedi/jobs/{job_id} | Get job status
[**get_user_jobs**](PublishingApi.md#get_user_jobs) | **GET** /dedi/jobs | Get user jobs
[**publish_record**](PublishingApi.md#publish_record) | **POST** /dedi/{namespace}/{registry_name}/publish-record | Publish record
[**save_record_as_draft**](PublishingApi.md#save_record_as_draft) | **POST** /dedi/{namespace}/{registry_name}/save-draft | Save record as draft


# **bulk_upload_records**
> BulkUploadRecords202Response bulk_upload_records(namespace, registry_name, file)

Bulk upload records

Uploads multiple records in a single operation. Returns a job ID for tracking progress.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.bulk_upload_records202_response import BulkUploadRecords202Response
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
    api_instance = dedi_client.PublishingApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    registry_name = 'registry_name_example' # str | Registry name
    file = None # bytes | CSV file containing record data

    try:
        # Bulk upload records
        api_response = api_instance.bulk_upload_records(namespace, registry_name, file)
        print("The response of PublishingApi->bulk_upload_records:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PublishingApi->bulk_upload_records: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **registry_name** | **str**| Registry name | 
 **file** | **bytes**| CSV file containing record data | 

### Return type

[**BulkUploadRecords202Response**](BulkUploadRecords202Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Bulk upload job started |  -  |
**400** | Bad request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_namespace**
> CreateNamespace201Response create_namespace(create_namespace_request)

Create a new namespace

Creates a new namespace to organize and group related registries.
Namespaces provide top-level organization for data segregation.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.create_namespace201_response import CreateNamespace201Response
from dedi_client.models.create_namespace_request import CreateNamespaceRequest
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
    api_instance = dedi_client.PublishingApi(api_client)
    create_namespace_request = dedi_client.CreateNamespaceRequest() # CreateNamespaceRequest | 

    try:
        # Create a new namespace
        api_response = api_instance.create_namespace(create_namespace_request)
        print("The response of PublishingApi->create_namespace:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PublishingApi->create_namespace: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_namespace_request** | [**CreateNamespaceRequest**](CreateNamespaceRequest.md)|  | 

### Return type

[**CreateNamespace201Response**](CreateNamespace201Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Namespace created successfully |  -  |
**400** | Bad request - invalid parameters |  -  |
**401** | Unauthorized |  -  |
**409** | Conflict - namespace name already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_registry**
> CreateRegistry201Response create_registry(namespace, create_registry_request)

Create a new registry

Creates a new registry within a namespace with a defined schema for records.
Registries define the structure and validation rules for records.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.create_registry201_response import CreateRegistry201Response
from dedi_client.models.create_registry_request import CreateRegistryRequest
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
    api_instance = dedi_client.PublishingApi(api_client)
    namespace = 'my-company' # str | Namespace ID or domain name
    create_registry_request = dedi_client.CreateRegistryRequest() # CreateRegistryRequest | 

    try:
        # Create a new registry
        api_response = api_instance.create_registry(namespace, create_registry_request)
        print("The response of PublishingApi->create_registry:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PublishingApi->create_registry: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **create_registry_request** | [**CreateRegistryRequest**](CreateRegistryRequest.md)|  | 

### Return type

[**CreateRegistry201Response**](CreateRegistry201Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Registry created successfully |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |
**403** | Forbidden - insufficient permissions |  -  |
**404** | Namespace not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **export_records_as_csv**
> bytes export_records_as_csv(namespace, registry_name)

Export records as CSV

Export all records from a registry as a CSV file for analysis, backup, or migration purposes.

**CSV Format:**
- Headers match registry schema fields
- One row per record
- Includes record metadata (ID, timestamps, state)
- Nested objects flattened with dot notation

**Performance:**
- Optimized for large datasets
- Streaming response for memory efficiency
- Suitable for registries with thousands of records

**Access Control:**
- Requires registry read permissions
- User must be authorized for the registry


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
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
    api_instance = dedi_client.PublishingApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain
    registry_name = 'registry_name_example' # str | Registry name to export records from

    try:
        # Export records as CSV
        api_response = api_instance.export_records_as_csv(namespace, registry_name)
        print("The response of PublishingApi->export_records_as_csv:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PublishingApi->export_records_as_csv: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain | 
 **registry_name** | **str**| Registry name to export records from | 

### Return type

**bytes**

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/csv, application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | CSV file with registry records |  -  |
**401** | Unauthorized |  -  |
**403** | Insufficient permissions |  -  |
**404** | Namespace or registry not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_job_status**
> GetJobStatus200Response get_job_status(job_id)

Get job status

Retrieves the status and progress of a bulk upload job

### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.get_job_status200_response import GetJobStatus200Response
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
    api_instance = dedi_client.PublishingApi(api_client)
    job_id = 'job_id_example' # str | Job ID from bulk upload

    try:
        # Get job status
        api_response = api_instance.get_job_status(job_id)
        print("The response of PublishingApi->get_job_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PublishingApi->get_job_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **job_id** | **str**| Job ID from bulk upload | 

### Return type

[**GetJobStatus200Response**](GetJobStatus200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Job status retrieved |  -  |
**404** | Job not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_user_jobs**
> GetUserJobs200Response get_user_jobs()

Get user jobs

Retrieves all jobs for the authenticated user

### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.get_user_jobs200_response import GetUserJobs200Response
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
    api_instance = dedi_client.PublishingApi(api_client)

    try:
        # Get user jobs
        api_response = api_instance.get_user_jobs()
        print("The response of PublishingApi->get_user_jobs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PublishingApi->get_user_jobs: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**GetUserJobs200Response**](GetUserJobs200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | User jobs retrieved |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **publish_record**
> PublishRecord201Response publish_record(namespace, registry_name, publish_record_request)

Publish record

Publishes a record directly or promotes a draft to live state.
Published records become available for lookup and queries.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.publish_record201_response import PublishRecord201Response
from dedi_client.models.publish_record_request import PublishRecordRequest
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
    api_instance = dedi_client.PublishingApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    registry_name = 'registry_name_example' # str | Registry name
    publish_record_request = dedi_client.PublishRecordRequest() # PublishRecordRequest | 

    try:
        # Publish record
        api_response = api_instance.publish_record(namespace, registry_name, publish_record_request)
        print("The response of PublishingApi->publish_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PublishingApi->publish_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **registry_name** | **str**| Registry name | 
 **publish_record_request** | [**PublishRecordRequest**](PublishRecordRequest.md)|  | 

### Return type

[**PublishRecord201Response**](PublishRecord201Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Record published successfully |  -  |
**400** | Bad request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **save_record_as_draft**
> SaveRecordAsDraft201Response save_record_as_draft(namespace, registry_name, save_record_as_draft_request, publish=publish)

Save record as draft

Saves a record as a draft without publishing. Drafts can be edited and later published.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.save_record_as_draft201_response import SaveRecordAsDraft201Response
from dedi_client.models.save_record_as_draft_request import SaveRecordAsDraftRequest
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
    api_instance = dedi_client.PublishingApi(api_client)
    namespace = 'namespace_example' # str | Namespace ID or domain name
    registry_name = 'registry_name_example' # str | Registry name
    save_record_as_draft_request = dedi_client.SaveRecordAsDraftRequest() # SaveRecordAsDraftRequest | 
    publish = true # bool | Set to true to save and publish immediately (optional)

    try:
        # Save record as draft
        api_response = api_instance.save_record_as_draft(namespace, registry_name, save_record_as_draft_request, publish=publish)
        print("The response of PublishingApi->save_record_as_draft:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PublishingApi->save_record_as_draft: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **namespace** | **str**| Namespace ID or domain name | 
 **registry_name** | **str**| Registry name | 
 **save_record_as_draft_request** | [**SaveRecordAsDraftRequest**](SaveRecordAsDraftRequest.md)|  | 
 **publish** | **bool**| Set to true to save and publish immediately | [optional] 

### Return type

[**SaveRecordAsDraft201Response**](SaveRecordAsDraft201Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Draft saved successfully |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |
**404** | Namespace or registry not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

