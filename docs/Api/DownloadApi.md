# Pbxg33k\KavitaClient\DownloadApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiDownloadBookmarksPost**](DownloadApi.md#apidownloadbookmarkspost) | **POST** /api/Download/bookmarks | Downloads all bookmarks in a zip for
[**apiDownloadBulkChapterSizePost**](DownloadApi.md#apidownloadbulkchaptersizepost) | **POST** /api/Download/bulk-chapter-size | For a set of chapters, return the size in bytes
[**apiDownloadBulkReadinglistSizePost**](DownloadApi.md#apidownloadbulkreadinglistsizepost) | **POST** /api/Download/bulk-readinglist-size | Returns the mapping of readinglist -&gt; size
[**apiDownloadBulkSeriesSizePost**](DownloadApi.md#apidownloadbulkseriessizepost) | **POST** /api/Download/bulk-series-size | For a set of series, return the size in bytes
[**apiDownloadBulkVolumeSizePost**](DownloadApi.md#apidownloadbulkvolumesizepost) | **POST** /api/Download/bulk-volume-size | For a set of volumes, return the size in bytes
[**apiDownloadChapterGet**](DownloadApi.md#apidownloadchapterget) | **GET** /api/Download/chapter | Returns the zip for a single chapter. If the chapter contains multiple files, they will be zipped.
[**apiDownloadChapterSizeGet**](DownloadApi.md#apidownloadchaptersizeget) | **GET** /api/Download/chapter-size | For a given chapter, return the size in bytes
[**apiDownloadReadinglistSizeGet**](DownloadApi.md#apidownloadreadinglistsizeget) | **GET** /api/Download/readinglist-size | Returns the filesize for all items of a reading list that the requesting user has access to
[**apiDownloadSeriesGet**](DownloadApi.md#apidownloadseriesget) | **GET** /api/Download/series | 
[**apiDownloadSeriesSizeGet**](DownloadApi.md#apidownloadseriessizeget) | **GET** /api/Download/series-size | For a series, return the size in bytes
[**apiDownloadVolumeGet**](DownloadApi.md#apidownloadvolumeget) | **GET** /api/Download/volume | Downloads all chapters within a volume. If the chapters are multiple zips, they will all be zipped up.
[**apiDownloadVolumeSizeGet**](DownloadApi.md#apidownloadvolumesizeget) | **GET** /api/Download/volume-size | For a given volume, return the size in bytes

# **apiDownloadBookmarksPost**
> apiDownloadBookmarksPost($body)

Downloads all bookmarks in a zip for

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DownloadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\DownloadBookmarkDto(); // \Pbxg33k\KavitaClient\Model\DownloadBookmarkDto | 

try {
    $apiInstance->apiDownloadBookmarksPost($body);
} catch (Exception $e) {
    echo 'Exception when calling DownloadApi->apiDownloadBookmarksPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\DownloadBookmarkDto**](../Model/DownloadBookmarkDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiDownloadBulkChapterSizePost**
> map[string,int] apiDownloadBulkChapterSizePost($body)

For a set of chapters, return the size in bytes

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DownloadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\BulkChapterSizeRequest(); // \Pbxg33k\KavitaClient\Model\BulkChapterSizeRequest | 

try {
    $result = $apiInstance->apiDownloadBulkChapterSizePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DownloadApi->apiDownloadBulkChapterSizePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\BulkChapterSizeRequest**](../Model/BulkChapterSizeRequest.md)|  | [optional]

### Return type

**map[string,int]**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiDownloadBulkReadinglistSizePost**
> map[string,int] apiDownloadBulkReadinglistSizePost($body)

Returns the mapping of readinglist -> size

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DownloadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\BulkReadingListSizeRequest(); // \Pbxg33k\KavitaClient\Model\BulkReadingListSizeRequest | 

try {
    $result = $apiInstance->apiDownloadBulkReadinglistSizePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DownloadApi->apiDownloadBulkReadinglistSizePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\BulkReadingListSizeRequest**](../Model/BulkReadingListSizeRequest.md)|  | [optional]

### Return type

**map[string,int]**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiDownloadBulkSeriesSizePost**
> map[string,int] apiDownloadBulkSeriesSizePost($body)

For a set of series, return the size in bytes

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DownloadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\BulkSeriesSizeRequest(); // \Pbxg33k\KavitaClient\Model\BulkSeriesSizeRequest | 

try {
    $result = $apiInstance->apiDownloadBulkSeriesSizePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DownloadApi->apiDownloadBulkSeriesSizePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\BulkSeriesSizeRequest**](../Model/BulkSeriesSizeRequest.md)|  | [optional]

### Return type

**map[string,int]**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiDownloadBulkVolumeSizePost**
> map[string,int] apiDownloadBulkVolumeSizePost($body)

For a set of volumes, return the size in bytes

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DownloadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\BulkVolumeSizeRequest(); // \Pbxg33k\KavitaClient\Model\BulkVolumeSizeRequest | 

try {
    $result = $apiInstance->apiDownloadBulkVolumeSizePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DownloadApi->apiDownloadBulkVolumeSizePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\BulkVolumeSizeRequest**](../Model/BulkVolumeSizeRequest.md)|  | [optional]

### Return type

**map[string,int]**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiDownloadChapterGet**
> apiDownloadChapterGet($chapter_id, $correlation_id)

Returns the zip for a single chapter. If the chapter contains multiple files, they will be zipped.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DownloadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 
$correlation_id = "correlation_id_example"; // string | 

try {
    $apiInstance->apiDownloadChapterGet($chapter_id, $correlation_id);
} catch (Exception $e) {
    echo 'Exception when calling DownloadApi->apiDownloadChapterGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  | [optional]
 **correlation_id** | **string**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiDownloadChapterSizeGet**
> int apiDownloadChapterSizeGet($chapter_id)

For a given chapter, return the size in bytes

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DownloadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 

try {
    $result = $apiInstance->apiDownloadChapterSizeGet($chapter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DownloadApi->apiDownloadChapterSizeGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  | [optional]

### Return type

**int**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiDownloadReadinglistSizeGet**
> int apiDownloadReadinglistSizeGet($reading_list_id)

Returns the filesize for all items of a reading list that the requesting user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DownloadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reading_list_id = 56; // int | 

try {
    $result = $apiInstance->apiDownloadReadinglistSizeGet($reading_list_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DownloadApi->apiDownloadReadinglistSizeGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **reading_list_id** | **int**|  | [optional]

### Return type

**int**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiDownloadSeriesGet**
> apiDownloadSeriesGet($series_id, $correlation_id)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DownloadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 
$correlation_id = "correlation_id_example"; // string | 

try {
    $apiInstance->apiDownloadSeriesGet($series_id, $correlation_id);
} catch (Exception $e) {
    echo 'Exception when calling DownloadApi->apiDownloadSeriesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]
 **correlation_id** | **string**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiDownloadSeriesSizeGet**
> int apiDownloadSeriesSizeGet($series_id)

For a series, return the size in bytes

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DownloadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $result = $apiInstance->apiDownloadSeriesSizeGet($series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DownloadApi->apiDownloadSeriesSizeGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]

### Return type

**int**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiDownloadVolumeGet**
> apiDownloadVolumeGet($volume_id, $correlation_id)

Downloads all chapters within a volume. If the chapters are multiple zips, they will all be zipped up.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DownloadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$volume_id = 56; // int | 
$correlation_id = "correlation_id_example"; // string | Only for UI

try {
    $apiInstance->apiDownloadVolumeGet($volume_id, $correlation_id);
} catch (Exception $e) {
    echo 'Exception when calling DownloadApi->apiDownloadVolumeGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **volume_id** | **int**|  | [optional]
 **correlation_id** | **string**| Only for UI | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiDownloadVolumeSizeGet**
> int apiDownloadVolumeSizeGet($volume_id)

For a given volume, return the size in bytes

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DownloadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$volume_id = 56; // int | 

try {
    $result = $apiInstance->apiDownloadVolumeSizeGet($volume_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DownloadApi->apiDownloadVolumeSizeGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **volume_id** | **int**|  | [optional]

### Return type

**int**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

