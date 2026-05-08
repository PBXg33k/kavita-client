# Pbxg33k\KavitaClient\PluginApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiPluginAuthenticatePost**](PluginApi.md#apipluginauthenticatepost) | **POST** /api/Plugin/authenticate | Authenticate with the Server given an auth key. This will log you in by returning the user object and the JWT token.
[**apiPluginAuthkeyExpiresGet**](PluginApi.md#apipluginauthkeyexpiresget) | **GET** /api/Plugin/authkey-expires | Returns the expiration (UTC) of the authenticated Auth key (or null if none set)
[**apiPluginParseBulkPost**](PluginApi.md#apipluginparsebulkpost) | **POST** /api/Plugin/parse-bulk | 
[**apiPluginParseGet**](PluginApi.md#apipluginparseget) | **GET** /api/Plugin/parse | Parse a string and return Parsed information from it. Does not support any directory fallback parsing
[**apiPluginVersionGet**](PluginApi.md#apipluginversionget) | **GET** /api/Plugin/version | Returns the version of the Kavita install

# **apiPluginAuthenticatePost**
> \Pbxg33k\KavitaClient\Model\UserDto apiPluginAuthenticatePost($api_key, $plugin_name)

Authenticate with the Server given an auth key. This will log you in by returning the user object and the JWT token.

This API is not fully built out and may require more information in later releases

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\PluginApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | Auth key which will be used to authenticate and return a valid user token back
$plugin_name = "plugin_name_example"; // string | Name of the Plugin

try {
    $result = $apiInstance->apiPluginAuthenticatePost($api_key, $plugin_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PluginApi->apiPluginAuthenticatePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**| Auth key which will be used to authenticate and return a valid user token back |
 **plugin_name** | **string**| Name of the Plugin |

### Return type

[**\Pbxg33k\KavitaClient\Model\UserDto**](../Model/UserDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiPluginAuthkeyExpiresGet**
> \Pbxg33k\KavitaClient\Model\AuthKeyExpiresAtDto apiPluginAuthkeyExpiresGet()

Returns the expiration (UTC) of the authenticated Auth key (or null if none set)

Will always return null if the Auth Key does not belong to this account

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\PluginApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiPluginAuthkeyExpiresGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PluginApi->apiPluginAuthkeyExpiresGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\AuthKeyExpiresAtDto**](../Model/AuthKeyExpiresAtDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiPluginParseBulkPost**
> \Pbxg33k\KavitaClient\Model\ParseBulkResponseDto apiPluginParseBulkPost($body)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\PluginApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\ParseBulkRequestDto(); // \Pbxg33k\KavitaClient\Model\ParseBulkRequestDto | 

try {
    $result = $apiInstance->apiPluginParseBulkPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PluginApi->apiPluginParseBulkPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\ParseBulkRequestDto**](../Model/ParseBulkRequestDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ParseBulkResponseDto**](../Model/ParseBulkResponseDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiPluginParseGet**
> \Pbxg33k\KavitaClient\Model\ParseResultDto apiPluginParseGet($name, $library_type)

Parse a string and return Parsed information from it. Does not support any directory fallback parsing

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\PluginApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | String to parse
$library_type = new \Pbxg33k\KavitaClient\Model\LibraryType(); // \Pbxg33k\KavitaClient\Model\LibraryType | Determines the set of pattern matching to use

try {
    $result = $apiInstance->apiPluginParseGet($name, $library_type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PluginApi->apiPluginParseGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| String to parse | [optional]
 **library_type** | [**\Pbxg33k\KavitaClient\Model\LibraryType**](../Model/.md)| Determines the set of pattern matching to use | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ParseResultDto**](../Model/ParseResultDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiPluginVersionGet**
> string apiPluginVersionGet($api_key)

Returns the version of the Kavita install

This will log unauthorized requests to Security log

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\PluginApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | Required for authenticating to get result

try {
    $result = $apiInstance->apiPluginVersionGet($api_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PluginApi->apiPluginVersionGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**| Required for authenticating to get result |

### Return type

**string**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

