# Pbxg33k\KavitaClient\OpdsApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiOpdsApiKeyCollectionsCollectionIdGet**](OpdsApi.md#apiopdsapikeycollectionscollectionidget) | **GET** /api/Opds/{apiKey}/collections/{collectionId} | Get Series for a given Collection - Supports Pagination
[**apiOpdsApiKeyCollectionsGet**](OpdsApi.md#apiopdsapikeycollectionsget) | **GET** /api/Opds/{apiKey}/collections | Get all Collections - Supports Pagination
[**apiOpdsApiKeyFaviconGet**](OpdsApi.md#apiopdsapikeyfaviconget) | **GET** /api/Opds/{apiKey}/favicon | 
[**apiOpdsApiKeyGet**](OpdsApi.md#apiopdsapikeyget) | **GET** /api/Opds/{apiKey} | Returns the Catalogue for Kavita&#x27;s OPDS Service
[**apiOpdsApiKeyImageGet**](OpdsApi.md#apiopdsapikeyimageget) | **GET** /api/Opds/{apiKey}/image | This returns a streamed image following OPDS-PS v1.2
[**apiOpdsApiKeyLibrariesGet**](OpdsApi.md#apiopdsapikeylibrariesget) | **GET** /api/Opds/{apiKey}/libraries | Get the User&#x27;s Libraries - No Pagination Support
[**apiOpdsApiKeyLibrariesLibraryIdGet**](OpdsApi.md#apiopdsapikeylibrarieslibraryidget) | **GET** /api/Opds/{apiKey}/libraries/{libraryId} | Returns Series from the Library - Supports Pagination
[**apiOpdsApiKeyOnDeckGet**](OpdsApi.md#apiopdsapikeyondeckget) | **GET** /api/Opds/{apiKey}/on-deck | Get the On Deck (Dashboard) - Supports Pagination
[**apiOpdsApiKeyPost**](OpdsApi.md#apiopdsapikeypost) | **POST** /api/Opds/{apiKey} | Returns the Catalogue for Kavita&#x27;s OPDS Service
[**apiOpdsApiKeyReadingListGet**](OpdsApi.md#apiopdsapikeyreadinglistget) | **GET** /api/Opds/{apiKey}/reading-list | Get a User&#x27;s Reading Lists - Supports Pagination
[**apiOpdsApiKeyReadingListReadingListIdGet**](OpdsApi.md#apiopdsapikeyreadinglistreadinglistidget) | **GET** /api/Opds/{apiKey}/reading-list/{readingListId} | Returns individual items (chapters) from Reading List by ID - Supports Pagination
[**apiOpdsApiKeyRecentlyAddedGet**](OpdsApi.md#apiopdsapikeyrecentlyaddedget) | **GET** /api/Opds/{apiKey}/recently-added | Returns Recently Added (Dashboard Feed) - Supports Pagination
[**apiOpdsApiKeyRecentlyUpdatedGet**](OpdsApi.md#apiopdsapikeyrecentlyupdatedget) | **GET** /api/Opds/{apiKey}/recently-updated | Get the Recently Updated Series (Dashboard) - Pagination available, total pages will not be filled due to underlying implementation
[**apiOpdsApiKeySearchGet**](OpdsApi.md#apiopdsapikeysearchget) | **GET** /api/Opds/{apiKey}/search | 
[**apiOpdsApiKeySeriesGet**](OpdsApi.md#apiopdsapikeyseriesget) | **GET** /api/Opds/{apiKey}/series | OPDS Search endpoint
[**apiOpdsApiKeySeriesSeriesIdGet**](OpdsApi.md#apiopdsapikeyseriesseriesidget) | **GET** /api/Opds/{apiKey}/series/{seriesId} | Returns the items within a Series (Series Detail)
[**apiOpdsApiKeySeriesSeriesIdVolumeVolumeIdChapterChapterIdDownloadFilenameGet**](OpdsApi.md#apiopdsapikeyseriesseriesidvolumevolumeidchapterchapteriddownloadfilenameget) | **GET** /api/Opds/{apiKey}/series/{seriesId}/volume/{volumeId}/chapter/{chapterId}/download/{filename} | Downloads a file (user must have download permission)
[**apiOpdsApiKeySeriesSeriesIdVolumeVolumeIdChapterChapterIdGet**](OpdsApi.md#apiopdsapikeyseriesseriesidvolumevolumeidchapterchapteridget) | **GET** /api/Opds/{apiKey}/series/{seriesId}/volume/{volumeId}/chapter/{chapterId} | Gets items for a given Chapter
[**apiOpdsApiKeySeriesSeriesIdVolumeVolumeIdGet**](OpdsApi.md#apiopdsapikeyseriesseriesidvolumevolumeidget) | **GET** /api/Opds/{apiKey}/series/{seriesId}/volume/{volumeId} | Returns items for a given Volume
[**apiOpdsApiKeySmartFiltersFilterIdGet**](OpdsApi.md#apiopdsapikeysmartfiltersfilteridget) | **GET** /api/Opds/{apiKey}/smart-filters/{filterId} | Get the User&#x27;s Smart Filter - Supports Pagination
[**apiOpdsApiKeySmartFiltersGet**](OpdsApi.md#apiopdsapikeysmartfiltersget) | **GET** /api/Opds/{apiKey}/smart-filters | Get the User&#x27;s Smart Filters (Dashboard Context) - Supports Pagination
[**apiOpdsApiKeyWantToReadGet**](OpdsApi.md#apiopdsapikeywanttoreadget) | **GET** /api/Opds/{apiKey}/want-to-read | Get the User&#x27;s Want to Read list - Supports Pagination

# **apiOpdsApiKeyCollectionsCollectionIdGet**
> apiOpdsApiKeyCollectionsCollectionIdGet($collection_id, $api_key, $page_number)

Get Series for a given Collection - Supports Pagination

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$collection_id = 56; // int | 
$api_key = "api_key_example"; // string | 
$page_number = 1; // int | 

try {
    $apiInstance->apiOpdsApiKeyCollectionsCollectionIdGet($collection_id, $api_key, $page_number);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeyCollectionsCollectionIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **collection_id** | **int**|  |
 **api_key** | **string**|  |
 **page_number** | **int**|  | [optional] [default to 1]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeyCollectionsGet**
> apiOpdsApiKeyCollectionsGet($api_key, $page_number)

Get all Collections - Supports Pagination

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 
$page_number = 1; // int | 

try {
    $apiInstance->apiOpdsApiKeyCollectionsGet($api_key, $page_number);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeyCollectionsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**|  |
 **page_number** | **int**|  | [optional] [default to 1]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeyFaviconGet**
> apiOpdsApiKeyFaviconGet($api_key)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 

try {
    $apiInstance->apiOpdsApiKeyFaviconGet($api_key);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeyFaviconGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**|  |

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeyGet**
> apiOpdsApiKeyGet($api_key)

Returns the Catalogue for Kavita's OPDS Service

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 

try {
    $apiInstance->apiOpdsApiKeyGet($api_key);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeyGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**|  |

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeyImageGet**
> apiOpdsApiKeyImageGet($api_key, $library_id, $series_id, $volume_id, $chapter_id, $page_number, $save_progress)

This returns a streamed image following OPDS-PS v1.2

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 
$library_id = 56; // int | 
$series_id = 56; // int | 
$volume_id = 56; // int | 
$chapter_id = 56; // int | 
$page_number = 56; // int | 
$save_progress = true; // bool | Optional parameter. Can pass false and progress saving will be suppressed

try {
    $apiInstance->apiOpdsApiKeyImageGet($api_key, $library_id, $series_id, $volume_id, $chapter_id, $page_number, $save_progress);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeyImageGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**|  |
 **library_id** | **int**|  | [optional]
 **series_id** | **int**|  | [optional]
 **volume_id** | **int**|  | [optional]
 **chapter_id** | **int**|  | [optional]
 **page_number** | **int**|  | [optional]
 **save_progress** | **bool**| Optional parameter. Can pass false and progress saving will be suppressed | [optional] [default to true]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeyLibrariesGet**
> apiOpdsApiKeyLibrariesGet($api_key, $page_number)

Get the User's Libraries - No Pagination Support

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 
$page_number = 1; // int | 

try {
    $apiInstance->apiOpdsApiKeyLibrariesGet($api_key, $page_number);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeyLibrariesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**|  |
 **page_number** | **int**|  | [optional] [default to 1]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeyLibrariesLibraryIdGet**
> apiOpdsApiKeyLibrariesLibraryIdGet($library_id, $api_key, $page_number)

Returns Series from the Library - Supports Pagination

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$library_id = 56; // int | 
$api_key = "api_key_example"; // string | 
$page_number = 1; // int | 

try {
    $apiInstance->apiOpdsApiKeyLibrariesLibraryIdGet($library_id, $api_key, $page_number);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeyLibrariesLibraryIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **library_id** | **int**|  |
 **api_key** | **string**|  |
 **page_number** | **int**|  | [optional] [default to 1]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeyOnDeckGet**
> apiOpdsApiKeyOnDeckGet($api_key, $page_number)

Get the On Deck (Dashboard) - Supports Pagination

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 
$page_number = 1; // int | 

try {
    $apiInstance->apiOpdsApiKeyOnDeckGet($api_key, $page_number);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeyOnDeckGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**|  |
 **page_number** | **int**|  | [optional] [default to 1]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeyPost**
> apiOpdsApiKeyPost($api_key)

Returns the Catalogue for Kavita's OPDS Service

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 

try {
    $apiInstance->apiOpdsApiKeyPost($api_key);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeyPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**|  |

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeyReadingListGet**
> apiOpdsApiKeyReadingListGet($api_key, $page_number)

Get a User's Reading Lists - Supports Pagination

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 
$page_number = 1; // int | 

try {
    $apiInstance->apiOpdsApiKeyReadingListGet($api_key, $page_number);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeyReadingListGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**|  |
 **page_number** | **int**|  | [optional] [default to 1]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeyReadingListReadingListIdGet**
> apiOpdsApiKeyReadingListReadingListIdGet($reading_list_id, $api_key, $page_number)

Returns individual items (chapters) from Reading List by ID - Supports Pagination

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reading_list_id = 56; // int | 
$api_key = "api_key_example"; // string | 
$page_number = 1; // int | 

try {
    $apiInstance->apiOpdsApiKeyReadingListReadingListIdGet($reading_list_id, $api_key, $page_number);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeyReadingListReadingListIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **reading_list_id** | **int**|  |
 **api_key** | **string**|  |
 **page_number** | **int**|  | [optional] [default to 1]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeyRecentlyAddedGet**
> apiOpdsApiKeyRecentlyAddedGet($api_key, $page_number)

Returns Recently Added (Dashboard Feed) - Supports Pagination

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 
$page_number = 1; // int | 

try {
    $apiInstance->apiOpdsApiKeyRecentlyAddedGet($api_key, $page_number);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeyRecentlyAddedGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**|  |
 **page_number** | **int**|  | [optional] [default to 1]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeyRecentlyUpdatedGet**
> apiOpdsApiKeyRecentlyUpdatedGet($api_key, $page_number)

Get the Recently Updated Series (Dashboard) - Pagination available, total pages will not be filled due to underlying implementation

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 
$page_number = 1; // int | 

try {
    $apiInstance->apiOpdsApiKeyRecentlyUpdatedGet($api_key, $page_number);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeyRecentlyUpdatedGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**|  |
 **page_number** | **int**|  | [optional] [default to 1]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeySearchGet**
> apiOpdsApiKeySearchGet($api_key)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 

try {
    $apiInstance->apiOpdsApiKeySearchGet($api_key);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeySearchGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**|  |

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeySeriesGet**
> apiOpdsApiKeySeriesGet($api_key, $query)

OPDS Search endpoint

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 
$query = "query_example"; // string | 

try {
    $apiInstance->apiOpdsApiKeySeriesGet($api_key, $query);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeySeriesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**|  |
 **query** | **string**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeySeriesSeriesIdGet**
> apiOpdsApiKeySeriesSeriesIdGet($api_key, $series_id)

Returns the items within a Series (Series Detail)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 
$series_id = 56; // int | 

try {
    $apiInstance->apiOpdsApiKeySeriesSeriesIdGet($api_key, $series_id);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeySeriesSeriesIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**|  |
 **series_id** | **int**|  |

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeySeriesSeriesIdVolumeVolumeIdChapterChapterIdDownloadFilenameGet**
> apiOpdsApiKeySeriesSeriesIdVolumeVolumeIdChapterChapterIdDownloadFilenameGet($api_key, $series_id, $volume_id, $chapter_id, $filename)

Downloads a file (user must have download permission)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | User's API Key
$series_id = 56; // int | 
$volume_id = 56; // int | 
$chapter_id = 56; // int | 
$filename = "filename_example"; // string | Not used. Only for Chunky to allow download links

try {
    $apiInstance->apiOpdsApiKeySeriesSeriesIdVolumeVolumeIdChapterChapterIdDownloadFilenameGet($api_key, $series_id, $volume_id, $chapter_id, $filename);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeySeriesSeriesIdVolumeVolumeIdChapterChapterIdDownloadFilenameGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**| User&#x27;s API Key |
 **series_id** | **int**|  |
 **volume_id** | **int**|  |
 **chapter_id** | **int**|  |
 **filename** | **string**| Not used. Only for Chunky to allow download links |

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeySeriesSeriesIdVolumeVolumeIdChapterChapterIdGet**
> apiOpdsApiKeySeriesSeriesIdVolumeVolumeIdChapterChapterIdGet($api_key, $series_id, $volume_id, $chapter_id)

Gets items for a given Chapter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 
$series_id = 56; // int | 
$volume_id = 56; // int | 
$chapter_id = 56; // int | 

try {
    $apiInstance->apiOpdsApiKeySeriesSeriesIdVolumeVolumeIdChapterChapterIdGet($api_key, $series_id, $volume_id, $chapter_id);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeySeriesSeriesIdVolumeVolumeIdChapterChapterIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**|  |
 **series_id** | **int**|  |
 **volume_id** | **int**|  |
 **chapter_id** | **int**|  |

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeySeriesSeriesIdVolumeVolumeIdGet**
> apiOpdsApiKeySeriesSeriesIdVolumeVolumeIdGet($api_key, $series_id, $volume_id)

Returns items for a given Volume

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 
$series_id = 56; // int | 
$volume_id = 56; // int | 

try {
    $apiInstance->apiOpdsApiKeySeriesSeriesIdVolumeVolumeIdGet($api_key, $series_id, $volume_id);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeySeriesSeriesIdVolumeVolumeIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**|  |
 **series_id** | **int**|  |
 **volume_id** | **int**|  |

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeySmartFiltersFilterIdGet**
> apiOpdsApiKeySmartFiltersFilterIdGet($api_key, $filter_id, $page_number)

Get the User's Smart Filter - Supports Pagination

Smart filters have different entity types, this will resolve to the underlying entity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 
$filter_id = 56; // int | 
$page_number = 1; // int | 

try {
    $apiInstance->apiOpdsApiKeySmartFiltersFilterIdGet($api_key, $filter_id, $page_number);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeySmartFiltersFilterIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**|  |
 **filter_id** | **int**|  |
 **page_number** | **int**|  | [optional] [default to 1]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeySmartFiltersGet**
> apiOpdsApiKeySmartFiltersGet($api_key, $page_number)

Get the User's Smart Filters (Dashboard Context) - Supports Pagination

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 
$page_number = 1; // int | 

try {
    $apiInstance->apiOpdsApiKeySmartFiltersGet($api_key, $page_number);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeySmartFiltersGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**|  |
 **page_number** | **int**|  | [optional] [default to 1]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiOpdsApiKeyWantToReadGet**
> apiOpdsApiKeyWantToReadGet($api_key, $page_number)

Get the User's Want to Read list - Supports Pagination

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\OpdsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 
$page_number = 1; // int | 

try {
    $apiInstance->apiOpdsApiKeyWantToReadGet($api_key, $page_number);
} catch (Exception $e) {
    echo 'Exception when calling OpdsApi->apiOpdsApiKeyWantToReadGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**|  |
 **page_number** | **int**|  | [optional] [default to 1]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

