# Pbxg33k\KavitaClient\AccountApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiAccountAuthKeyDelete**](AccountApi.md#apiaccountauthkeydelete) | **DELETE** /api/Account/auth-key | Delete the Auth Key
[**apiAccountAuthKeysGet**](AccountApi.md#apiaccountauthkeysget) | **GET** /api/Account/auth-keys | Returns all Auth Keys with the account
[**apiAccountClearOidcLinkPost**](AccountApi.md#apiaccountclearoidclinkpost) | **POST** /api/Account/clear-oidc-link | Remove the OIDC link for the authenticated user. This action will also remove the authentication cookie. The caller should take note and redirect to login if no other authentication is currently present (I.e. JWT)
[**apiAccountConfirmEmailPost**](AccountApi.md#apiaccountconfirmemailpost) | **POST** /api/Account/confirm-email | Last step in authentication flow, confirms the email token for email
[**apiAccountConfirmEmailUpdatePost**](AccountApi.md#apiaccountconfirmemailupdatepost) | **POST** /api/Account/confirm-email-update | Final step in email update change. Given a confirmation token and the email, this will finish the email change.
[**apiAccountConfirmMigrationEmailPost**](AccountApi.md#apiaccountconfirmmigrationemailpost) | **POST** /api/Account/confirm-migration-email | 
[**apiAccountConfirmPasswordResetPost**](AccountApi.md#apiaccountconfirmpasswordresetpost) | **POST** /api/Account/confirm-password-reset | 
[**apiAccountCreateAuthKeyPost**](AccountApi.md#apiaccountcreateauthkeypost) | **POST** /api/Account/create-auth-key | Creates a new Auth Key for a user.
[**apiAccountEmailConfirmedGet**](AccountApi.md#apiaccountemailconfirmedget) | **GET** /api/Account/email-confirmed | 
[**apiAccountForgotPasswordPost**](AccountApi.md#apiaccountforgotpasswordpost) | **POST** /api/Account/forgot-password | Will send user a link to update their password to their email or prompt them if not accessible
[**apiAccountGet**](AccountApi.md#apiaccountget) | **GET** /api/Account | Returns the current user, as it would from login
[**apiAccountInvitePost**](AccountApi.md#apiaccountinvitepost) | **POST** /api/Account/invite | Invites a user to the server. Will generate a setup link for continuing setup. If email is not setup, a link will be presented to user to continue setup.
[**apiAccountInviteUrlGet**](AccountApi.md#apiaccountinviteurlget) | **GET** /api/Account/invite-url | Requests the Invite Url for the AppUserId. Will return error if user is already validated.
[**apiAccountIsEmailValidGet**](AccountApi.md#apiaccountisemailvalidget) | **GET** /api/Account/is-email-valid | Is the user&#x27;s current email valid or not
[**apiAccountLoginPost**](AccountApi.md#apiaccountloginpost) | **POST** /api/Account/login | Perform a login. Will send JWT Token of the logged in user back.
[**apiAccountOidcAuthenticatedGet**](AccountApi.md#apiaccountoidcauthenticatedget) | **GET** /api/Account/oidc-authenticated | Returns true if OIDC authentication cookies are present and the Kavita.Server.Extensions.IdentityServiceExtensions.OpenIdConnect scheme has been registered
[**apiAccountOpdsUrlGet**](AccountApi.md#apiaccountopdsurlget) | **GET** /api/Account/opds-url | Returns the OPDS url for this user
[**apiAccountRefreshAccountGet**](AccountApi.md#apiaccountrefreshaccountget) | **GET** /api/Account/refresh-account | Returns an up-to-date user account
[**apiAccountRefreshTokenPost**](AccountApi.md#apiaccountrefreshtokenpost) | **POST** /api/Account/refresh-token | Refreshes the user&#x27;s JWT token
[**apiAccountRegisterPost**](AccountApi.md#apiaccountregisterpost) | **POST** /api/Account/register | Register the first user (admin) on the server. Will not do anything if an admin is already confirmed
[**apiAccountResendConfirmationEmailPost**](AccountApi.md#apiaccountresendconfirmationemailpost) | **POST** /api/Account/resend-confirmation-email | Resend an invite to a user already invited
[**apiAccountResetPasswordPost**](AccountApi.md#apiaccountresetpasswordpost) | **POST** /api/Account/reset-password | Update a user&#x27;s password
[**apiAccountRotateAuthKeyPost**](AccountApi.md#apiaccountrotateauthkeypost) | **POST** /api/Account/rotate-auth-key | Rotate the Auth Key
[**apiAccountUpdateAgeRestrictionPost**](AccountApi.md#apiaccountupdateagerestrictionpost) | **POST** /api/Account/update/age-restriction | Change the Age Rating restriction for the user
[**apiAccountUpdateEmailPost**](AccountApi.md#apiaccountupdateemailpost) | **POST** /api/Account/update/email | Initiates the flow to update a user&#x27;s email address.              If email is not setup, then the email address is not changed in this API. A confirmation link is sent/dumped which will validate the email. It must be confirmed for the email to update.
[**apiAccountUpdatePost**](AccountApi.md#apiaccountupdatepost) | **POST** /api/Account/update | Update the user account. This can only affect Username, Email (will require confirming), Roles, and Library access.
[**apiAccountUpdateUsernamePost**](AccountApi.md#apiaccountupdateusernamepost) | **POST** /api/Account/update/username | Initiates the flow to update a user&#x27;s username.

# **apiAccountAuthKeyDelete**
> apiAccountAuthKeyDelete($auth_key_id)

Delete the Auth Key

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$auth_key_id = 56; // int | 

try {
    $apiInstance->apiAccountAuthKeyDelete($auth_key_id);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountAuthKeyDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **auth_key_id** | **int**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountAuthKeysGet**
> \Pbxg33k\KavitaClient\Model\AuthKeyDto[] apiAccountAuthKeysGet()

Returns all Auth Keys with the account

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiAccountAuthKeysGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountAuthKeysGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\AuthKeyDto[]**](../Model/AuthKeyDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountClearOidcLinkPost**
> apiAccountClearOidcLinkPost()

Remove the OIDC link for the authenticated user. This action will also remove the authentication cookie. The caller should take note and redirect to login if no other authentication is currently present (I.e. JWT)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $apiInstance->apiAccountClearOidcLinkPost();
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountClearOidcLinkPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountConfirmEmailPost**
> \Pbxg33k\KavitaClient\Model\UserDto apiAccountConfirmEmailPost($body)

Last step in authentication flow, confirms the email token for email

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\ConfirmEmailDto(); // \Pbxg33k\KavitaClient\Model\ConfirmEmailDto | 

try {
    $result = $apiInstance->apiAccountConfirmEmailPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountConfirmEmailPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\ConfirmEmailDto**](../Model/ConfirmEmailDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\UserDto**](../Model/UserDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountConfirmEmailUpdatePost**
> apiAccountConfirmEmailUpdatePost($body)

Final step in email update change. Given a confirmation token and the email, this will finish the email change.

This will force connected clients to re-authenticate

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\ConfirmEmailUpdateDto(); // \Pbxg33k\KavitaClient\Model\ConfirmEmailUpdateDto | 

try {
    $apiInstance->apiAccountConfirmEmailUpdatePost($body);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountConfirmEmailUpdatePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\ConfirmEmailUpdateDto**](../Model/ConfirmEmailUpdateDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountConfirmMigrationEmailPost**
> \Pbxg33k\KavitaClient\Model\UserDto apiAccountConfirmMigrationEmailPost($body)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\ConfirmMigrationEmailDto(); // \Pbxg33k\KavitaClient\Model\ConfirmMigrationEmailDto | 

try {
    $result = $apiInstance->apiAccountConfirmMigrationEmailPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountConfirmMigrationEmailPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\ConfirmMigrationEmailDto**](../Model/ConfirmMigrationEmailDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\UserDto**](../Model/UserDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountConfirmPasswordResetPost**
> string apiAccountConfirmPasswordResetPost($body)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\ConfirmPasswordResetDto(); // \Pbxg33k\KavitaClient\Model\ConfirmPasswordResetDto | 

try {
    $result = $apiInstance->apiAccountConfirmPasswordResetPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountConfirmPasswordResetPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\ConfirmPasswordResetDto**](../Model/ConfirmPasswordResetDto.md)|  | [optional]

### Return type

**string**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountCreateAuthKeyPost**
> \Pbxg33k\KavitaClient\Model\AuthKeyDto apiAccountCreateAuthKeyPost($body)

Creates a new Auth Key for a user.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\RotateAuthKeyRequestDto(); // \Pbxg33k\KavitaClient\Model\RotateAuthKeyRequestDto | 

try {
    $result = $apiInstance->apiAccountCreateAuthKeyPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountCreateAuthKeyPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\RotateAuthKeyRequestDto**](../Model/RotateAuthKeyRequestDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\AuthKeyDto**](../Model/AuthKeyDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountEmailConfirmedGet**
> bool apiAccountEmailConfirmedGet()



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiAccountEmailConfirmedGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountEmailConfirmedGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

**bool**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountForgotPasswordPost**
> string apiAccountForgotPasswordPost($email)

Will send user a link to update their password to their email or prompt them if not accessible

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$email = "email_example"; // string | 

try {
    $result = $apiInstance->apiAccountForgotPasswordPost($email);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountForgotPasswordPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email** | **string**|  | [optional]

### Return type

**string**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountGet**
> \Pbxg33k\KavitaClient\Model\UserDto apiAccountGet()

Returns the current user, as it would from login

Does not return tokens for the user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiAccountGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\UserDto**](../Model/UserDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountInvitePost**
> string apiAccountInvitePost($body)

Invites a user to the server. Will generate a setup link for continuing setup. If email is not setup, a link will be presented to user to continue setup.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\InviteUserDto(); // \Pbxg33k\KavitaClient\Model\InviteUserDto | 

try {
    $result = $apiInstance->apiAccountInvitePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountInvitePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\InviteUserDto**](../Model/InviteUserDto.md)|  | [optional]

### Return type

**string**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountInviteUrlGet**
> string apiAccountInviteUrlGet($user_id, $with_base_url)

Requests the Invite Url for the AppUserId. Will return error if user is already validated.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 56; // int | 
$with_base_url = true; // bool | Include the \"https://ip:port/\" in the generated link

try {
    $result = $apiInstance->apiAccountInviteUrlGet($user_id, $with_base_url);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountInviteUrlGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **int**|  | [optional]
 **with_base_url** | **bool**| Include the \&quot;https://ip:port/\&quot; in the generated link | [optional]

### Return type

**string**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountIsEmailValidGet**
> bool apiAccountIsEmailValidGet()

Is the user's current email valid or not

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiAccountIsEmailValidGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountIsEmailValidGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

**bool**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountLoginPost**
> \Pbxg33k\KavitaClient\Model\UserDto apiAccountLoginPost($body)

Perform a login. Will send JWT Token of the logged in user back.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\LoginDto(); // \Pbxg33k\KavitaClient\Model\LoginDto | 

try {
    $result = $apiInstance->apiAccountLoginPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountLoginPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\LoginDto**](../Model/LoginDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\UserDto**](../Model/UserDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountOidcAuthenticatedGet**
> bool apiAccountOidcAuthenticatedGet()

Returns true if OIDC authentication cookies are present and the Kavita.Server.Extensions.IdentityServiceExtensions.OpenIdConnect scheme has been registered

Makes no guarantee about their validity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiAccountOidcAuthenticatedGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountOidcAuthenticatedGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

**bool**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountOpdsUrlGet**
> string apiAccountOpdsUrlGet($auth_key_name)

Returns the OPDS url for this user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$auth_key_name = "auth_key_name_example"; // string | 

try {
    $result = $apiInstance->apiAccountOpdsUrlGet($auth_key_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountOpdsUrlGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **auth_key_name** | **string**|  | [optional]

### Return type

**string**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountRefreshAccountGet**
> \Pbxg33k\KavitaClient\Model\UserDto apiAccountRefreshAccountGet()

Returns an up-to-date user account

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiAccountRefreshAccountGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountRefreshAccountGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\UserDto**](../Model/UserDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountRefreshTokenPost**
> \Pbxg33k\KavitaClient\Model\TokenRequestDto apiAccountRefreshTokenPost($body)

Refreshes the user's JWT token

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\TokenRequestDto(); // \Pbxg33k\KavitaClient\Model\TokenRequestDto | 

try {
    $result = $apiInstance->apiAccountRefreshTokenPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountRefreshTokenPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\TokenRequestDto**](../Model/TokenRequestDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\TokenRequestDto**](../Model/TokenRequestDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountRegisterPost**
> \Pbxg33k\KavitaClient\Model\UserDto apiAccountRegisterPost($body)

Register the first user (admin) on the server. Will not do anything if an admin is already confirmed

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\RegisterDto(); // \Pbxg33k\KavitaClient\Model\RegisterDto | 

try {
    $result = $apiInstance->apiAccountRegisterPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountRegisterPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\RegisterDto**](../Model/RegisterDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\UserDto**](../Model/UserDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountResendConfirmationEmailPost**
> \Pbxg33k\KavitaClient\Model\InviteUserResponse apiAccountResendConfirmationEmailPost($user_id)

Resend an invite to a user already invited

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 56; // int | 

try {
    $result = $apiInstance->apiAccountResendConfirmationEmailPost($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountResendConfirmationEmailPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\InviteUserResponse**](../Model/InviteUserResponse.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountResetPasswordPost**
> apiAccountResetPasswordPost($body)

Update a user's password

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\ResetPasswordDto(); // \Pbxg33k\KavitaClient\Model\ResetPasswordDto | 

try {
    $apiInstance->apiAccountResetPasswordPost($body);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountResetPasswordPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\ResetPasswordDto**](../Model/ResetPasswordDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountRotateAuthKeyPost**
> \Pbxg33k\KavitaClient\Model\AuthKeyDto apiAccountRotateAuthKeyPost($body, $auth_key_id)

Rotate the Auth Key

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\RotateAuthKeyRequestDto(); // \Pbxg33k\KavitaClient\Model\RotateAuthKeyRequestDto | 
$auth_key_id = 56; // int | 

try {
    $result = $apiInstance->apiAccountRotateAuthKeyPost($body, $auth_key_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountRotateAuthKeyPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\RotateAuthKeyRequestDto**](../Model/RotateAuthKeyRequestDto.md)|  | [optional]
 **auth_key_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\AuthKeyDto**](../Model/AuthKeyDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountUpdateAgeRestrictionPost**
> apiAccountUpdateAgeRestrictionPost($body)

Change the Age Rating restriction for the user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateAgeRestrictionDto(); // \Pbxg33k\KavitaClient\Model\UpdateAgeRestrictionDto | 

try {
    $apiInstance->apiAccountUpdateAgeRestrictionPost($body);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountUpdateAgeRestrictionPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateAgeRestrictionDto**](../Model/UpdateAgeRestrictionDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountUpdateEmailPost**
> \Pbxg33k\KavitaClient\Model\InviteUserResponse apiAccountUpdateEmailPost($body)

Initiates the flow to update a user's email address.              If email is not setup, then the email address is not changed in this API. A confirmation link is sent/dumped which will validate the email. It must be confirmed for the email to update.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateEmailDto(); // \Pbxg33k\KavitaClient\Model\UpdateEmailDto | 

try {
    $result = $apiInstance->apiAccountUpdateEmailPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountUpdateEmailPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateEmailDto**](../Model/UpdateEmailDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\InviteUserResponse**](../Model/InviteUserResponse.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountUpdatePost**
> apiAccountUpdatePost($body)

Update the user account. This can only affect Username, Email (will require confirming), Roles, and Library access.

Users who's Kavita.Models.Entities.User.AppUser.IdentityProvider is not Kavita.Models.Entities.Enums.IdentityProvider.Kavita cannot be edited if Kavita.Models.DTOs.Settings.OidcConfigDto.SyncUserSettings is true

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateUserDto(); // \Pbxg33k\KavitaClient\Model\UpdateUserDto | 

try {
    $apiInstance->apiAccountUpdatePost($body);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountUpdatePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateUserDto**](../Model/UpdateUserDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAccountUpdateUsernamePost**
> \Pbxg33k\KavitaClient\Model\InviteUserResponse apiAccountUpdateUsernamePost($body)

Initiates the flow to update a user's username.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateUsernameRequestDto(); // \Pbxg33k\KavitaClient\Model\UpdateUsernameRequestDto | 

try {
    $result = $apiInstance->apiAccountUpdateUsernamePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountUpdateUsernamePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateUsernameRequestDto**](../Model/UpdateUsernameRequestDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\InviteUserResponse**](../Model/InviteUserResponse.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

