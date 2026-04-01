# dedi_client.WatchNotificationsApi

All URIs are relative to *https://api.dedi.global*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_user_watch_subscriptions**](WatchNotificationsApi.md#get_user_watch_subscriptions) | **GET** /dedi/watch/subscriptions | List user&#39;s watch subscriptions
[**subscribe_to_watch**](WatchNotificationsApi.md#subscribe_to_watch) | **POST** /dedi/watch | Subscribe to watch notifications
[**unsubscribe_from_watch**](WatchNotificationsApi.md#unsubscribe_from_watch) | **DELETE** /dedi/watch/{subscription_id} | Unsubscribe from watch notifications


# **get_user_watch_subscriptions**
> GetUserWatchSubscriptions200Response get_user_watch_subscriptions()

List user's watch subscriptions

Retrieves all active watch subscriptions for the authenticated user.
Includes subscription details and status information.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.get_user_watch_subscriptions200_response import GetUserWatchSubscriptions200Response
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
    api_instance = dedi_client.WatchNotificationsApi(api_client)

    try:
        # List user's watch subscriptions
        api_response = api_instance.get_user_watch_subscriptions()
        print("The response of WatchNotificationsApi->get_user_watch_subscriptions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WatchNotificationsApi->get_user_watch_subscriptions: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**GetUserWatchSubscriptions200Response**](GetUserWatchSubscriptions200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Watch subscriptions retrieved successfully |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **subscribe_to_watch**
> SubscribeToWatch201Response subscribe_to_watch(subscribe_to_watch_request)

Subscribe to watch notifications

Subscribe to receive notifications when changes occur to namespaces, registries, or records.

**Supported Watch Types:**
- `namespace`: Watch all changes within a namespace
- `registry`: Watch all changes within a specific registry
- `record`: Watch changes to a specific record

**Notification Methods:**
- Webhook URL (HTTP POST with change details)
- Real-time events (if supported by client)

**Use Cases:**
- Monitor data changes for compliance
- Trigger automated workflows
- Real-time synchronization
- Audit trail generation


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.subscribe_to_watch201_response import SubscribeToWatch201Response
from dedi_client.models.subscribe_to_watch_request import SubscribeToWatchRequest
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
    api_instance = dedi_client.WatchNotificationsApi(api_client)
    subscribe_to_watch_request = dedi_client.SubscribeToWatchRequest() # SubscribeToWatchRequest | 

    try:
        # Subscribe to watch notifications
        api_response = api_instance.subscribe_to_watch(subscribe_to_watch_request)
        print("The response of WatchNotificationsApi->subscribe_to_watch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WatchNotificationsApi->subscribe_to_watch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **subscribe_to_watch_request** | [**SubscribeToWatchRequest**](SubscribeToWatchRequest.md)|  | 

### Return type

[**SubscribeToWatch201Response**](SubscribeToWatch201Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Watch subscription created successfully |  -  |
**400** | Invalid watch parameters |  -  |
**401** | Unauthorized |  -  |
**404** | Target resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **unsubscribe_from_watch**
> SuccessResponse unsubscribe_from_watch(subscription_id)

Unsubscribe from watch notifications

Unsubscribe from watch notifications by providing the subscription ID.
This will stop all future notifications for the specified watch.


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
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
    api_instance = dedi_client.WatchNotificationsApi(api_client)
    subscription_id = 'sub_67890' # str | Watch subscription ID to remove

    try:
        # Unsubscribe from watch notifications
        api_response = api_instance.unsubscribe_from_watch(subscription_id)
        print("The response of WatchNotificationsApi->unsubscribe_from_watch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WatchNotificationsApi->unsubscribe_from_watch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **subscription_id** | **str**| Watch subscription ID to remove | 

### Return type

[**SuccessResponse**](SuccessResponse.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Watch subscription removed successfully |  -  |
**404** | Subscription not found |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

