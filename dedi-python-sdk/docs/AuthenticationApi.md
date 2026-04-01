# dedi_client.AuthenticationApi

All URIs are relative to *https://api.dedi.global*

Method | HTTP request | Description
------------- | ------------- | -------------
[**confirm_password_reset**](AuthenticationApi.md#confirm_password_reset) | **POST** /dedi/reset-password/confirm | Confirm password reset
[**forgot_password**](AuthenticationApi.md#forgot_password) | **POST** /dedi/forgot-password | Forgot password
[**get_api_key**](AuthenticationApi.md#get_api_key) | **GET** /dedi/get-api-key | Generate API key
[**get_current_user**](AuthenticationApi.md#get_current_user) | **GET** /dedi/auth/me | Get current authenticated user
[**logout**](AuthenticationApi.md#logout) | **POST** /dedi/logout | Logout user
[**refresh_token**](AuthenticationApi.md#refresh_token) | **POST** /dedi/token/refresh | Refresh authentication token
[**register_login**](AuthenticationApi.md#register_login) | **POST** /dedi/register | Register or login user
[**resend_magic_link**](AuthenticationApi.md#resend_magic_link) | **POST** /dedi/resend-magic-link | Resend magic link
[**reset_password**](AuthenticationApi.md#reset_password) | **POST** /dedi/reset-password | Reset password (authenticated user)
[**verify_email**](AuthenticationApi.md#verify_email) | **GET** /dedi/verify-email | Verify email with magic link token


# **confirm_password_reset**
> SuccessResponse confirm_password_reset(confirm_password_reset_request)

Confirm password reset

Confirm password reset using the token received via email.

**Password Requirements:**
- Minimum 6 characters
- Must include at least one special character (@$!%*?&)

**Security:** Reset tokens expire after 15 minutes by default


### Example


```python
import dedi_client
from dedi_client.models.confirm_password_reset_request import ConfirmPasswordResetRequest
from dedi_client.models.success_response import SuccessResponse
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
    api_instance = dedi_client.AuthenticationApi(api_client)
    confirm_password_reset_request = dedi_client.ConfirmPasswordResetRequest() # ConfirmPasswordResetRequest | 

    try:
        # Confirm password reset
        api_response = api_instance.confirm_password_reset(confirm_password_reset_request)
        print("The response of AuthenticationApi->confirm_password_reset:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->confirm_password_reset: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **confirm_password_reset_request** | [**ConfirmPasswordResetRequest**](ConfirmPasswordResetRequest.md)|  | 

### Return type

[**SuccessResponse**](SuccessResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Password reset confirmed successfully |  -  |
**400** | Invalid or expired token, or invalid password |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **forgot_password**
> SuccessResponse forgot_password(forgot_password_request)

Forgot password

Send a password reset link to the user's email address.

**Process:**
1. Submit email address
2. Check email for reset link
3. Use reset link to access password reset form
4. Set new password via reset-password/confirm endpoint


### Example


```python
import dedi_client
from dedi_client.models.forgot_password_request import ForgotPasswordRequest
from dedi_client.models.success_response import SuccessResponse
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
    api_instance = dedi_client.AuthenticationApi(api_client)
    forgot_password_request = dedi_client.ForgotPasswordRequest() # ForgotPasswordRequest | 

    try:
        # Forgot password
        api_response = api_instance.forgot_password(forgot_password_request)
        print("The response of AuthenticationApi->forgot_password:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->forgot_password: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **forgot_password_request** | [**ForgotPasswordRequest**](ForgotPasswordRequest.md)|  | 

### Return type

[**SuccessResponse**](SuccessResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Reset link sent to email |  -  |
**400** | Invalid email format |  -  |
**404** | Email not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_api_key**
> GetApiKey200Response get_api_key()

Generate API key

Generates a new API key for authenticated user for programmatic access

### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.get_api_key200_response import GetApiKey200Response
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
    api_instance = dedi_client.AuthenticationApi(api_client)

    try:
        # Generate API key
        api_response = api_instance.get_api_key()
        print("The response of AuthenticationApi->get_api_key:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->get_api_key: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**GetApiKey200Response**](GetApiKey200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | API key generated successfully |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_current_user**
> GetCurrentUser200Response get_current_user()

Get current authenticated user

Retrieves information about the currently authenticated user

### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.get_current_user200_response import GetCurrentUser200Response
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
    api_instance = dedi_client.AuthenticationApi(api_client)

    try:
        # Get current authenticated user
        api_response = api_instance.get_current_user()
        print("The response of AuthenticationApi->get_current_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->get_current_user: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**GetCurrentUser200Response**](GetCurrentUser200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | User information retrieved successfully |  -  |
**401** | Unauthorized - invalid or missing token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **logout**
> SuccessResponse logout()

Logout user

Invalidates the current session and authentication tokens

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
    api_instance = dedi_client.AuthenticationApi(api_client)

    try:
        # Logout user
        api_response = api_instance.logout()
        print("The response of AuthenticationApi->logout:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->logout: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

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
**200** | Logged out successfully |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **refresh_token**
> RefreshToken200Response refresh_token(refresh_token_request)

Refresh authentication token

Refreshes the authentication token using a valid refresh token

### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.refresh_token200_response import RefreshToken200Response
from dedi_client.models.refresh_token_request import RefreshTokenRequest
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
    api_instance = dedi_client.AuthenticationApi(api_client)
    refresh_token_request = dedi_client.RefreshTokenRequest() # RefreshTokenRequest | 

    try:
        # Refresh authentication token
        api_response = api_instance.refresh_token(refresh_token_request)
        print("The response of AuthenticationApi->refresh_token:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->refresh_token: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **refresh_token_request** | [**RefreshTokenRequest**](RefreshTokenRequest.md)|  | 

### Return type

[**RefreshToken200Response**](RefreshToken200Response.md)

### Authorization

[CookieAuth](../README.md#CookieAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Token refreshed successfully |  -  |
**401** | Invalid or expired refresh token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **register_login**
> SuccessResponse register_login(register_login_request)

Register or login user

Universal endpoint for user registration and login. Use 'action' parameter to specify operation.
- For registration: email, name, password, and action='register' required
- For login: email, password, and action='login' required

**Password Requirements:**
- Minimum 6 characters
- Must include at least one special character (@$!%*?&)


### Example


```python
import dedi_client
from dedi_client.models.register_login_request import RegisterLoginRequest
from dedi_client.models.success_response import SuccessResponse
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
    api_instance = dedi_client.AuthenticationApi(api_client)
    register_login_request = {"email":"user@example.com","name":"John Doe","action":"register","password":"Test@123"} # RegisterLoginRequest | 

    try:
        # Register or login user
        api_response = api_instance.register_login(register_login_request)
        print("The response of AuthenticationApi->register_login:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->register_login: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **register_login_request** | [**RegisterLoginRequest**](RegisterLoginRequest.md)|  | 

### Return type

[**SuccessResponse**](SuccessResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success - check email for verification link |  -  |
**400** | Bad request - missing or invalid parameters |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **resend_magic_link**
> SuccessResponse resend_magic_link(resend_magic_link_request)

Resend magic link

Resend email verification link for users who didn't receive or lost their verification email.

**Prerequisites:**
- User must already be registered
- Account must exist in the system

**Note:** This endpoint requires the user's existing credentials to prevent abuse


### Example


```python
import dedi_client
from dedi_client.models.resend_magic_link_request import ResendMagicLinkRequest
from dedi_client.models.success_response import SuccessResponse
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
    api_instance = dedi_client.AuthenticationApi(api_client)
    resend_magic_link_request = dedi_client.ResendMagicLinkRequest() # ResendMagicLinkRequest | 

    try:
        # Resend magic link
        api_response = api_instance.resend_magic_link(resend_magic_link_request)
        print("The response of AuthenticationApi->resend_magic_link:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->resend_magic_link: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **resend_magic_link_request** | [**ResendMagicLinkRequest**](ResendMagicLinkRequest.md)|  | 

### Return type

[**SuccessResponse**](SuccessResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Magic link resent successfully |  -  |
**400** | Invalid credentials or account not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reset_password**
> SuccessResponse reset_password(reset_password_request)

Reset password (authenticated user)

Reset password for the currently authenticated user.

**Password Requirements:**
- Minimum 6 characters
- Must include at least one special character (@$!%*?&)


### Example

* Api Key Authentication (CookieAuth):
* Bearer (JWT) Authentication (BearerAuth):

```python
import dedi_client
from dedi_client.models.reset_password_request import ResetPasswordRequest
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
    api_instance = dedi_client.AuthenticationApi(api_client)
    reset_password_request = dedi_client.ResetPasswordRequest() # ResetPasswordRequest | 

    try:
        # Reset password (authenticated user)
        api_response = api_instance.reset_password(reset_password_request)
        print("The response of AuthenticationApi->reset_password:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->reset_password: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **reset_password_request** | [**ResetPasswordRequest**](ResetPasswordRequest.md)|  | 

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
**200** | Password reset successfully |  -  |
**400** | Invalid password or missing parameters |  -  |
**401** | Unauthorized or incorrect old password |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **verify_email**
> VerifyEmail200Response verify_email(token)

Verify email with magic link token

Verifies user email using the token from the magic link sent via email

### Example


```python
import dedi_client
from dedi_client.models.verify_email200_response import VerifyEmail200Response
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
    api_instance = dedi_client.AuthenticationApi(api_client)
    token = 'abc123xyz456' # str | Email verification token from magic link

    try:
        # Verify email with magic link token
        api_response = api_instance.verify_email(token)
        print("The response of AuthenticationApi->verify_email:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->verify_email: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token** | **str**| Email verification token from magic link | 

### Return type

[**VerifyEmail200Response**](VerifyEmail200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Email verified successfully |  -  |
**400** | Invalid or expired token |  -  |
**404** | Token not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

