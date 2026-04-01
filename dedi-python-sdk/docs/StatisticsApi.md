# dedi_client.StatisticsApi

All URIs are relative to *https://api.dedi.global*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_platform_statistics**](StatisticsApi.md#get_platform_statistics) | **GET** /dedi/stats | Get platform statistics


# **get_platform_statistics**
> GetPlatformStatistics200Response get_platform_statistics()

Get platform statistics

Retrieves comprehensive real-time statistics for the entire DeDi platform,
providing insights into platform usage and growth.

**Statistics Include:**
- Total registered user accounts
- Total namespaces across all users
- Total registries across all namespaces
- Total records across all registries

**Public Endpoint** - No authentication required.


### Example


```python
import dedi_client
from dedi_client.models.get_platform_statistics200_response import GetPlatformStatistics200Response
from dedi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.dedi.global
# See configuration.py for a list of all supported configuration parameters.
configuration = dedi_client.Configuration(
    host = "https://api.dedi.global"
)


# Enter a context with an instance of the API client
with dedi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = dedi_client.StatisticsApi(api_client)

    try:
        # Get platform statistics
        api_response = api_instance.get_platform_statistics()
        print("The response of StatisticsApi->get_platform_statistics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StatisticsApi->get_platform_statistics: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**GetPlatformStatistics200Response**](GetPlatformStatistics200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Platform statistics retrieved successfully |  -  |
**500** | Database connection error or internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

