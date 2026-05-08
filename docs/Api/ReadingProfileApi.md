# Pbxg33k\KavitaClient\ReadingProfileApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiReadingProfileAllGet**](ReadingProfileApi.md#apireadingprofileallget) | **GET** /api/reading-profile/all | Gets all non-implicit reading profiles for a user
[**apiReadingProfileBulkPost**](ReadingProfileApi.md#apireadingprofilebulkpost) | **POST** /api/reading-profile/bulk | Assigns the reading profile to all passes series, and deletes their implicit profiles
[**apiReadingProfileCreatePost**](ReadingProfileApi.md#apireadingprofilecreatepost) | **POST** /api/reading-profile/create | Creates a new reading profile for the current user
[**apiReadingProfileDelete**](ReadingProfileApi.md#apireadingprofiledelete) | **DELETE** /api/reading-profile | Deletes the given profile, requires the profile to belong to the logged-in user
[**apiReadingProfileLibraryGet**](ReadingProfileApi.md#apireadingprofilelibraryget) | **GET** /api/reading-profile/library | Returns all the Reading rofiles bound to the library
[**apiReadingProfileLibraryIdSeriesIdGet**](ReadingProfileApi.md#apireadingprofilelibraryidseriesidget) | **GET** /api/reading-profile/{libraryId}/{seriesId} | Returns the ReadingProfile that should be applied to the given series, walks up the tree. Series -&gt; Library -&gt; Default
[**apiReadingProfileLibraryLibraryIdDelete**](ReadingProfileApi.md#apireadingprofilelibrarylibraryiddelete) | **DELETE** /api/reading-profile/library/{libraryId} | Clears the reading profile for the given library for the currently logged-in user
[**apiReadingProfileLibraryLibraryIdPost**](ReadingProfileApi.md#apireadingprofilelibrarylibraryidpost) | **POST** /api/reading-profile/library/{libraryId} | Sets the reading profile for a given library, removes the old one
[**apiReadingProfilePost**](ReadingProfileApi.md#apireadingprofilepost) | **POST** /api/reading-profile | Updates the given reading profile, must belong to the current user
[**apiReadingProfilePromotePost**](ReadingProfileApi.md#apireadingprofilepromotepost) | **POST** /api/reading-profile/promote | Promotes the implicit profile to a user profile. Removes the series from other profiles
[**apiReadingProfileSeriesGet**](ReadingProfileApi.md#apireadingprofileseriesget) | **GET** /api/reading-profile/series | Returns all Reading Profiles bound to a series
[**apiReadingProfileSeriesPost**](ReadingProfileApi.md#apireadingprofileseriespost) | **POST** /api/reading-profile/series | Update the implicit reading profile for a series, creates one if none exists
[**apiReadingProfileSeriesSeriesIdDelete**](ReadingProfileApi.md#apireadingprofileseriesseriesiddelete) | **DELETE** /api/reading-profile/series/{seriesId} | Clears the reading profile for the given series for the currently logged-in user
[**apiReadingProfileSeriesSeriesIdPost**](ReadingProfileApi.md#apireadingprofileseriesseriesidpost) | **POST** /api/reading-profile/series/{seriesId} | Sets the reading profile for a given series, removes the old one
[**apiReadingProfileSetDevicesPost**](ReadingProfileApi.md#apireadingprofilesetdevicespost) | **POST** /api/reading-profile/set-devices | Set the assigned devices for a reading profile
[**apiReadingProfileUpdateParentPost**](ReadingProfileApi.md#apireadingprofileupdateparentpost) | **POST** /api/reading-profile/update-parent | Updates the non-implicit reading profile for the given series, and removes implicit profiles

# **apiReadingProfileAllGet**
> \Pbxg33k\KavitaClient\Model\UserReadingProfileDto[] apiReadingProfileAllGet()

Gets all non-implicit reading profiles for a user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiReadingProfileAllGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingProfileApi->apiReadingProfileAllGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\UserReadingProfileDto[]**](../Model/UserReadingProfileDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingProfileBulkPost**
> apiReadingProfileBulkPost($body)

Assigns the reading profile to all passes series, and deletes their implicit profiles

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\BulkSetSeriesProfiles(); // \Pbxg33k\KavitaClient\Model\BulkSetSeriesProfiles | 

try {
    $apiInstance->apiReadingProfileBulkPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReadingProfileApi->apiReadingProfileBulkPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\BulkSetSeriesProfiles**](../Model/BulkSetSeriesProfiles.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingProfileCreatePost**
> \Pbxg33k\KavitaClient\Model\UserReadingProfileDto apiReadingProfileCreatePost($body)

Creates a new reading profile for the current user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UserReadingProfileDto(); // \Pbxg33k\KavitaClient\Model\UserReadingProfileDto | 

try {
    $result = $apiInstance->apiReadingProfileCreatePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingProfileApi->apiReadingProfileCreatePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UserReadingProfileDto**](../Model/UserReadingProfileDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\UserReadingProfileDto**](../Model/UserReadingProfileDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingProfileDelete**
> apiReadingProfileDelete($profile_id)

Deletes the given profile, requires the profile to belong to the logged-in user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$profile_id = 56; // int | 

try {
    $apiInstance->apiReadingProfileDelete($profile_id);
} catch (Exception $e) {
    echo 'Exception when calling ReadingProfileApi->apiReadingProfileDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **profile_id** | **int**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingProfileLibraryGet**
> \Pbxg33k\KavitaClient\Model\UserReadingProfileDto[] apiReadingProfileLibraryGet($library_id)

Returns all the Reading rofiles bound to the library

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$library_id = 56; // int | 

try {
    $result = $apiInstance->apiReadingProfileLibraryGet($library_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingProfileApi->apiReadingProfileLibraryGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **library_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\UserReadingProfileDto[]**](../Model/UserReadingProfileDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingProfileLibraryIdSeriesIdGet**
> \Pbxg33k\KavitaClient\Model\UserReadingProfileDto apiReadingProfileLibraryIdSeriesIdGet($library_id, $series_id, $skip_implicit, $device_id)

Returns the ReadingProfile that should be applied to the given series, walks up the tree. Series -> Library -> Default

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$library_id = 56; // int | 
$series_id = 56; // int | 
$skip_implicit = true; // bool | 
$device_id = 56; // int | Defaults to currently active device

try {
    $result = $apiInstance->apiReadingProfileLibraryIdSeriesIdGet($library_id, $series_id, $skip_implicit, $device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingProfileApi->apiReadingProfileLibraryIdSeriesIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **library_id** | **int**|  |
 **series_id** | **int**|  |
 **skip_implicit** | **bool**|  | [optional]
 **device_id** | **int**| Defaults to currently active device | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\UserReadingProfileDto**](../Model/UserReadingProfileDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingProfileLibraryLibraryIdDelete**
> apiReadingProfileLibraryLibraryIdDelete($library_id)

Clears the reading profile for the given library for the currently logged-in user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$library_id = 56; // int | 

try {
    $apiInstance->apiReadingProfileLibraryLibraryIdDelete($library_id);
} catch (Exception $e) {
    echo 'Exception when calling ReadingProfileApi->apiReadingProfileLibraryLibraryIdDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **library_id** | **int**|  |

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingProfileLibraryLibraryIdPost**
> apiReadingProfileLibraryLibraryIdPost($library_id, $body)

Sets the reading profile for a given library, removes the old one

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$library_id = 56; // int | 
$body = array(56); // int[] | 

try {
    $apiInstance->apiReadingProfileLibraryLibraryIdPost($library_id, $body);
} catch (Exception $e) {
    echo 'Exception when calling ReadingProfileApi->apiReadingProfileLibraryLibraryIdPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **library_id** | **int**|  |
 **body** | [**int[]**](../Model/int.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingProfilePost**
> \Pbxg33k\KavitaClient\Model\UserReadingProfileDto apiReadingProfilePost($body)

Updates the given reading profile, must belong to the current user

This does not update connected series and libraries.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UserReadingProfileDto(); // \Pbxg33k\KavitaClient\Model\UserReadingProfileDto | 

try {
    $result = $apiInstance->apiReadingProfilePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingProfileApi->apiReadingProfilePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UserReadingProfileDto**](../Model/UserReadingProfileDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\UserReadingProfileDto**](../Model/UserReadingProfileDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingProfilePromotePost**
> \Pbxg33k\KavitaClient\Model\UserReadingProfileDto apiReadingProfilePromotePost($profile_id, $device_id)

Promotes the implicit profile to a user profile. Removes the series from other profiles

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$profile_id = 56; // int | 
$device_id = 56; // int | Defaults to the currently active device

try {
    $result = $apiInstance->apiReadingProfilePromotePost($profile_id, $device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingProfileApi->apiReadingProfilePromotePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **profile_id** | **int**|  | [optional]
 **device_id** | **int**| Defaults to the currently active device | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\UserReadingProfileDto**](../Model/UserReadingProfileDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingProfileSeriesGet**
> \Pbxg33k\KavitaClient\Model\UserReadingProfileDto[] apiReadingProfileSeriesGet($series_id)

Returns all Reading Profiles bound to a series

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $result = $apiInstance->apiReadingProfileSeriesGet($series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingProfileApi->apiReadingProfileSeriesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\UserReadingProfileDto[]**](../Model/UserReadingProfileDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingProfileSeriesPost**
> \Pbxg33k\KavitaClient\Model\UserReadingProfileDto apiReadingProfileSeriesPost($body, $library_id, $series_id, $device_id)

Update the implicit reading profile for a series, creates one if none exists

Any modification to the reader settings during reading will create an implicit profile. Use \"update-parent\" to save to the bound series profile.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UserReadingProfileDto(); // \Pbxg33k\KavitaClient\Model\UserReadingProfileDto | 
$library_id = 56; // int | 
$series_id = 56; // int | 
$device_id = 56; // int | Defaults to the currently active device

try {
    $result = $apiInstance->apiReadingProfileSeriesPost($body, $library_id, $series_id, $device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingProfileApi->apiReadingProfileSeriesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UserReadingProfileDto**](../Model/UserReadingProfileDto.md)|  | [optional]
 **library_id** | **int**|  | [optional]
 **series_id** | **int**|  | [optional]
 **device_id** | **int**| Defaults to the currently active device | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\UserReadingProfileDto**](../Model/UserReadingProfileDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingProfileSeriesSeriesIdDelete**
> apiReadingProfileSeriesSeriesIdDelete($series_id)

Clears the reading profile for the given series for the currently logged-in user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $apiInstance->apiReadingProfileSeriesSeriesIdDelete($series_id);
} catch (Exception $e) {
    echo 'Exception when calling ReadingProfileApi->apiReadingProfileSeriesSeriesIdDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  |

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingProfileSeriesSeriesIdPost**
> apiReadingProfileSeriesSeriesIdPost($series_id, $body)

Sets the reading profile for a given series, removes the old one

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 
$body = array(56); // int[] | 

try {
    $apiInstance->apiReadingProfileSeriesSeriesIdPost($series_id, $body);
} catch (Exception $e) {
    echo 'Exception when calling ReadingProfileApi->apiReadingProfileSeriesSeriesIdPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  |
 **body** | [**int[]**](../Model/int.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingProfileSetDevicesPost**
> apiReadingProfileSetDevicesPost($body, $profile_id)

Set the assigned devices for a reading profile

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = array(56); // int[] | 
$profile_id = 56; // int | 

try {
    $apiInstance->apiReadingProfileSetDevicesPost($body, $profile_id);
} catch (Exception $e) {
    echo 'Exception when calling ReadingProfileApi->apiReadingProfileSetDevicesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**int[]**](../Model/int.md)|  | [optional]
 **profile_id** | **int**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingProfileUpdateParentPost**
> \Pbxg33k\KavitaClient\Model\UserReadingProfileDto apiReadingProfileUpdateParentPost($body, $library_id, $series_id, $device_id)

Updates the non-implicit reading profile for the given series, and removes implicit profiles

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UserReadingProfileDto(); // \Pbxg33k\KavitaClient\Model\UserReadingProfileDto | 
$library_id = 56; // int | 
$series_id = 56; // int | 
$device_id = 56; // int | Defaults to currently active device

try {
    $result = $apiInstance->apiReadingProfileUpdateParentPost($body, $library_id, $series_id, $device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingProfileApi->apiReadingProfileUpdateParentPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UserReadingProfileDto**](../Model/UserReadingProfileDto.md)|  | [optional]
 **library_id** | **int**|  | [optional]
 **series_id** | **int**|  | [optional]
 **device_id** | **int**| Defaults to currently active device | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\UserReadingProfileDto**](../Model/UserReadingProfileDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

