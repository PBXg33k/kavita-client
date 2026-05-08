# Pbxg33k\KavitaClient\ScrobblingApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiScrobblingAddHoldPost**](ScrobblingApi.md#apiscrobblingaddholdpost) | **POST** /api/Scrobbling/add-hold | Adds a hold against the Series for user&#x27;s scrobbling
[**apiScrobblingAnilistTokenGet**](ScrobblingApi.md#apiscrobblinganilisttokenget) | **GET** /api/Scrobbling/anilist-token | Get the current user&#x27;s AniList token
[**apiScrobblingBulkRemoveEventsPost**](ScrobblingApi.md#apiscrobblingbulkremoveeventspost) | **POST** /api/Scrobbling/bulk-remove-events | Delete the given scrobble events if they belong to that user
[**apiScrobblingClearErrorsPost**](ScrobblingApi.md#apiscrobblingclearerrorspost) | **POST** /api/Scrobbling/clear-errors | Clears the scrobbling errors table
[**apiScrobblingGenerateScrobbleEventsPost**](ScrobblingApi.md#apiscrobblinggeneratescrobbleeventspost) | **POST** /api/Scrobbling/generate-scrobble-events | When a user request to generate scrobble events from history. Should only be ran once per user.
[**apiScrobblingHasHoldGet**](ScrobblingApi.md#apiscrobblinghasholdget) | **GET** /api/Scrobbling/has-hold | If there is an active hold on the series
[**apiScrobblingHasRanScrobbleGenGet**](ScrobblingApi.md#apiscrobblinghasranscrobblegenget) | **GET** /api/Scrobbling/has-ran-scrobble-gen | Has the logged in user ran scrobble generation
[**apiScrobblingHoldsGet**](ScrobblingApi.md#apiscrobblingholdsget) | **GET** /api/Scrobbling/holds | Returns all scrobble holds for the current user
[**apiScrobblingLibraryAllowsScrobblingGet**](ScrobblingApi.md#apiscrobblinglibraryallowsscrobblingget) | **GET** /api/Scrobbling/library-allows-scrobbling | Does the library the series is in allow scrobbling?
[**apiScrobblingMalTokenGet**](ScrobblingApi.md#apiscrobblingmaltokenget) | **GET** /api/Scrobbling/mal-token | Get the current user&#x27;s MAL token and username
[**apiScrobblingRemoveHoldDelete**](ScrobblingApi.md#apiscrobblingremoveholddelete) | **DELETE** /api/Scrobbling/remove-hold | Remove a hold against the Series for user&#x27;s scrobbling
[**apiScrobblingScrobbleErrorsGet**](ScrobblingApi.md#apiscrobblingscrobbleerrorsget) | **GET** /api/Scrobbling/scrobble-errors | Returns all scrobbling errors for the instance
[**apiScrobblingScrobbleEventsPost**](ScrobblingApi.md#apiscrobblingscrobbleeventspost) | **POST** /api/Scrobbling/scrobble-events | Returns the scrobbling history for the user
[**apiScrobblingTokenExpiredGet**](ScrobblingApi.md#apiscrobblingtokenexpiredget) | **GET** /api/Scrobbling/token-expired | Checks if the current Scrobbling token for the given Provider has expired for the current user
[**apiScrobblingUpdateAnilistTokenPost**](ScrobblingApi.md#apiscrobblingupdateanilisttokenpost) | **POST** /api/Scrobbling/update-anilist-token | Update the current user&#x27;s AniList token
[**apiScrobblingUpdateMalTokenPost**](ScrobblingApi.md#apiscrobblingupdatemaltokenpost) | **POST** /api/Scrobbling/update-mal-token | Update the current user&#x27;s MAL token (Client ID) and Username

# **apiScrobblingAddHoldPost**
> apiScrobblingAddHoldPost($series_id)

Adds a hold against the Series for user's scrobbling

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ScrobblingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $apiInstance->apiScrobblingAddHoldPost($series_id);
} catch (Exception $e) {
    echo 'Exception when calling ScrobblingApi->apiScrobblingAddHoldPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiScrobblingAnilistTokenGet**
> string apiScrobblingAnilistTokenGet()

Get the current user's AniList token

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ScrobblingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiScrobblingAnilistTokenGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScrobblingApi->apiScrobblingAnilistTokenGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

**string**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiScrobblingBulkRemoveEventsPost**
> apiScrobblingBulkRemoveEventsPost($body)

Delete the given scrobble events if they belong to that user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ScrobblingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = array(56); // int[] | 

try {
    $apiInstance->apiScrobblingBulkRemoveEventsPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ScrobblingApi->apiScrobblingBulkRemoveEventsPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**int[]**](../Model/int.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiScrobblingClearErrorsPost**
> apiScrobblingClearErrorsPost()

Clears the scrobbling errors table

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ScrobblingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $apiInstance->apiScrobblingClearErrorsPost();
} catch (Exception $e) {
    echo 'Exception when calling ScrobblingApi->apiScrobblingClearErrorsPost: ', $e->getMessage(), PHP_EOL;
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

# **apiScrobblingGenerateScrobbleEventsPost**
> apiScrobblingGenerateScrobbleEventsPost()

When a user request to generate scrobble events from history. Should only be ran once per user.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ScrobblingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $apiInstance->apiScrobblingGenerateScrobbleEventsPost();
} catch (Exception $e) {
    echo 'Exception when calling ScrobblingApi->apiScrobblingGenerateScrobbleEventsPost: ', $e->getMessage(), PHP_EOL;
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

# **apiScrobblingHasHoldGet**
> bool apiScrobblingHasHoldGet($series_id)

If there is an active hold on the series

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ScrobblingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $result = $apiInstance->apiScrobblingHasHoldGet($series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScrobblingApi->apiScrobblingHasHoldGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]

### Return type

**bool**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiScrobblingHasRanScrobbleGenGet**
> bool apiScrobblingHasRanScrobbleGenGet()

Has the logged in user ran scrobble generation

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ScrobblingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiScrobblingHasRanScrobbleGenGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScrobblingApi->apiScrobblingHasRanScrobbleGenGet: ', $e->getMessage(), PHP_EOL;
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

# **apiScrobblingHoldsGet**
> \Pbxg33k\KavitaClient\Model\ScrobbleHoldDto[] apiScrobblingHoldsGet()

Returns all scrobble holds for the current user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ScrobblingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiScrobblingHoldsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScrobblingApi->apiScrobblingHoldsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\ScrobbleHoldDto[]**](../Model/ScrobbleHoldDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiScrobblingLibraryAllowsScrobblingGet**
> bool apiScrobblingLibraryAllowsScrobblingGet($series_id)

Does the library the series is in allow scrobbling?

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ScrobblingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $result = $apiInstance->apiScrobblingLibraryAllowsScrobblingGet($series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScrobblingApi->apiScrobblingLibraryAllowsScrobblingGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]

### Return type

**bool**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiScrobblingMalTokenGet**
> \Pbxg33k\KavitaClient\Model\MalUserInfoDto apiScrobblingMalTokenGet()

Get the current user's MAL token and username

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ScrobblingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiScrobblingMalTokenGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScrobblingApi->apiScrobblingMalTokenGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\MalUserInfoDto**](../Model/MalUserInfoDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiScrobblingRemoveHoldDelete**
> apiScrobblingRemoveHoldDelete($series_id)

Remove a hold against the Series for user's scrobbling

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ScrobblingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $apiInstance->apiScrobblingRemoveHoldDelete($series_id);
} catch (Exception $e) {
    echo 'Exception when calling ScrobblingApi->apiScrobblingRemoveHoldDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiScrobblingScrobbleErrorsGet**
> \Pbxg33k\KavitaClient\Model\ScrobbleErrorDto[] apiScrobblingScrobbleErrorsGet()

Returns all scrobbling errors for the instance

Requires admin

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ScrobblingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiScrobblingScrobbleErrorsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScrobblingApi->apiScrobblingScrobbleErrorsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\ScrobbleErrorDto[]**](../Model/ScrobbleErrorDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiScrobblingScrobbleEventsPost**
> \Pbxg33k\KavitaClient\Model\ScrobbleEventDto[] apiScrobblingScrobbleEventsPost($body, $page_number, $page_size)

Returns the scrobbling history for the user

User must have a valid license

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ScrobblingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\ScrobbleEventFilter(); // \Pbxg33k\KavitaClient\Model\ScrobbleEventFilter | 
$page_number = 56; // int | 
$page_size = 56; // int | 

try {
    $result = $apiInstance->apiScrobblingScrobbleEventsPost($body, $page_number, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScrobblingApi->apiScrobblingScrobbleEventsPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\ScrobbleEventFilter**](../Model/ScrobbleEventFilter.md)|  | [optional]
 **page_number** | **int**|  | [optional]
 **page_size** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ScrobbleEventDto[]**](../Model/ScrobbleEventDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiScrobblingTokenExpiredGet**
> bool apiScrobblingTokenExpiredGet($provider)

Checks if the current Scrobbling token for the given Provider has expired for the current user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ScrobblingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$provider = new \Pbxg33k\KavitaClient\Model\ScrobbleProvider(); // \Pbxg33k\KavitaClient\Model\ScrobbleProvider | 

try {
    $result = $apiInstance->apiScrobblingTokenExpiredGet($provider);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScrobblingApi->apiScrobblingTokenExpiredGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **provider** | [**\Pbxg33k\KavitaClient\Model\ScrobbleProvider**](../Model/.md)|  | [optional]

### Return type

**bool**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiScrobblingUpdateAnilistTokenPost**
> bool apiScrobblingUpdateAnilistTokenPost($body)

Update the current user's AniList token

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ScrobblingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\AniListUpdateDto(); // \Pbxg33k\KavitaClient\Model\AniListUpdateDto | 

try {
    $result = $apiInstance->apiScrobblingUpdateAnilistTokenPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScrobblingApi->apiScrobblingUpdateAnilistTokenPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\AniListUpdateDto**](../Model/AniListUpdateDto.md)|  | [optional]

### Return type

**bool**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiScrobblingUpdateMalTokenPost**
> bool apiScrobblingUpdateMalTokenPost($body)

Update the current user's MAL token (Client ID) and Username

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ScrobblingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\MalUserInfoDto(); // \Pbxg33k\KavitaClient\Model\MalUserInfoDto | 

try {
    $result = $apiInstance->apiScrobblingUpdateMalTokenPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScrobblingApi->apiScrobblingUpdateMalTokenPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\MalUserInfoDto**](../Model/MalUserInfoDto.md)|  | [optional]

### Return type

**bool**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

