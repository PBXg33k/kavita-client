# Pbxg33k\KavitaClient\UploadApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiUploadChapterPost**](UploadApi.md#apiuploadchapterpost) | **POST** /api/Upload/chapter | Replaces chapter cover image and locks it with a base64 encoded image. This will update the parent volume&#x27;s cover image.
[**apiUploadCollectionPost**](UploadApi.md#apiuploadcollectionpost) | **POST** /api/Upload/collection | Replaces collection tag cover image and locks it with a base64 encoded image
[**apiUploadLibraryPost**](UploadApi.md#apiuploadlibrarypost) | **POST** /api/Upload/library | Replaces library cover image with a base64 encoded image. If empty string passed, will reset to null.
[**apiUploadPersonPost**](UploadApi.md#apiuploadpersonpost) | **POST** /api/Upload/person | Replaces person tag cover image and locks it with a base64 encoded image
[**apiUploadReadingListPost**](UploadApi.md#apiuploadreadinglistpost) | **POST** /api/Upload/reading-list | Replaces reading list cover image and locks it with a base64 encoded image
[**apiUploadSeriesPost**](UploadApi.md#apiuploadseriespost) | **POST** /api/Upload/series | Replaces series cover image and locks it with a base64 encoded image
[**apiUploadUploadByUrlPost**](UploadApi.md#apiuploaduploadbyurlpost) | **POST** /api/Upload/upload-by-url | This stores a file (image) in temp directory for use in a cover image replacement flow. This is automatically cleaned up.
[**apiUploadUserPost**](UploadApi.md#apiuploaduserpost) | **POST** /api/Upload/user | Replaces user cover image and locks it with a base64 encoded image
[**apiUploadVolumePost**](UploadApi.md#apiuploadvolumepost) | **POST** /api/Upload/volume | Replaces volume cover image and locks it with a base64 encoded image.

# **apiUploadChapterPost**
> apiUploadChapterPost($body)

Replaces chapter cover image and locks it with a base64 encoded image. This will update the parent volume's cover image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\UploadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UploadCoverFileDto(); // \Pbxg33k\KavitaClient\Model\UploadCoverFileDto | 

try {
    $apiInstance->apiUploadChapterPost($body);
} catch (Exception $e) {
    echo 'Exception when calling UploadApi->apiUploadChapterPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UploadCoverFileDto**](../Model/UploadCoverFileDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiUploadCollectionPost**
> apiUploadCollectionPost($body)

Replaces collection tag cover image and locks it with a base64 encoded image

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\UploadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UploadCoverFileDto(); // \Pbxg33k\KavitaClient\Model\UploadCoverFileDto | 

try {
    $apiInstance->apiUploadCollectionPost($body);
} catch (Exception $e) {
    echo 'Exception when calling UploadApi->apiUploadCollectionPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UploadCoverFileDto**](../Model/UploadCoverFileDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiUploadLibraryPost**
> apiUploadLibraryPost($body)

Replaces library cover image with a base64 encoded image. If empty string passed, will reset to null.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\UploadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UploadCoverFileDto(); // \Pbxg33k\KavitaClient\Model\UploadCoverFileDto | 

try {
    $apiInstance->apiUploadLibraryPost($body);
} catch (Exception $e) {
    echo 'Exception when calling UploadApi->apiUploadLibraryPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UploadCoverFileDto**](../Model/UploadCoverFileDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiUploadPersonPost**
> apiUploadPersonPost($body)

Replaces person tag cover image and locks it with a base64 encoded image

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\UploadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UploadCoverFileDto(); // \Pbxg33k\KavitaClient\Model\UploadCoverFileDto | 

try {
    $apiInstance->apiUploadPersonPost($body);
} catch (Exception $e) {
    echo 'Exception when calling UploadApi->apiUploadPersonPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UploadCoverFileDto**](../Model/UploadCoverFileDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiUploadReadingListPost**
> apiUploadReadingListPost($body)

Replaces reading list cover image and locks it with a base64 encoded image

This is the only API that can be called by non-admins, but the authenticated user must have a readinglist permission

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\UploadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UploadCoverFileDto(); // \Pbxg33k\KavitaClient\Model\UploadCoverFileDto | 

try {
    $apiInstance->apiUploadReadingListPost($body);
} catch (Exception $e) {
    echo 'Exception when calling UploadApi->apiUploadReadingListPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UploadCoverFileDto**](../Model/UploadCoverFileDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiUploadSeriesPost**
> apiUploadSeriesPost($body)

Replaces series cover image and locks it with a base64 encoded image

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\UploadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UploadCoverFileDto(); // \Pbxg33k\KavitaClient\Model\UploadCoverFileDto | 

try {
    $apiInstance->apiUploadSeriesPost($body);
} catch (Exception $e) {
    echo 'Exception when calling UploadApi->apiUploadSeriesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UploadCoverFileDto**](../Model/UploadCoverFileDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiUploadUploadByUrlPost**
> string apiUploadUploadByUrlPost($body)

This stores a file (image) in temp directory for use in a cover image replacement flow. This is automatically cleaned up.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\UploadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UploadUrlDto(); // \Pbxg33k\KavitaClient\Model\UploadUrlDto | Escaped url to download from

try {
    $result = $apiInstance->apiUploadUploadByUrlPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UploadApi->apiUploadUploadByUrlPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UploadUrlDto**](../Model/UploadUrlDto.md)| Escaped url to download from | [optional]

### Return type

**string**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiUploadUserPost**
> apiUploadUserPost($body)

Replaces user cover image and locks it with a base64 encoded image

You MUST be the user in question

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\UploadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UploadCoverFileDto(); // \Pbxg33k\KavitaClient\Model\UploadCoverFileDto | 

try {
    $apiInstance->apiUploadUserPost($body);
} catch (Exception $e) {
    echo 'Exception when calling UploadApi->apiUploadUserPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UploadCoverFileDto**](../Model/UploadCoverFileDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiUploadVolumePost**
> apiUploadVolumePost($body)

Replaces volume cover image and locks it with a base64 encoded image.

This will not update the underlying chapter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\UploadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UploadCoverFileDto(); // \Pbxg33k\KavitaClient\Model\UploadCoverFileDto | 

try {
    $apiInstance->apiUploadVolumePost($body);
} catch (Exception $e) {
    echo 'Exception when calling UploadApi->apiUploadVolumePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UploadCoverFileDto**](../Model/UploadCoverFileDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

