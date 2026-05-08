# Pbxg33k\KavitaClient\SearchApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiSearchChaptersBySeriesGet**](SearchApi.md#apisearchchaptersbyseriesget) | **GET** /api/Search/chapters-by-series | Returns all chapters for a given series with localized titles. Used for CBL chapter-level matching.
[**apiSearchSearchGet**](SearchApi.md#apisearchsearchget) | **GET** /api/Search/search | Searches against different entities in the system against a query string
[**apiSearchSeriesForChapterGet**](SearchApi.md#apisearchseriesforchapterget) | **GET** /api/Search/series-for-chapter | Returns the series for the Chapter id. If the user does not have access (shouldn&#x27;t happen by the UI), then null is returned
[**apiSearchSeriesForMangafileGet**](SearchApi.md#apisearchseriesformangafileget) | **GET** /api/Search/series-for-mangafile | Returns the series for the MangaFile id. If the user does not have access (shouldn&#x27;t happen by the UI), then null is returned

# **apiSearchChaptersBySeriesGet**
> \Pbxg33k\KavitaClient\Model\ChapterDto[] apiSearchChaptersBySeriesGet($series_id)

Returns all chapters for a given series with localized titles. Used for CBL chapter-level matching.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SearchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $result = $apiInstance->apiSearchChaptersBySeriesGet($series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SearchApi->apiSearchChaptersBySeriesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ChapterDto[]**](../Model/ChapterDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSearchSearchGet**
> \Pbxg33k\KavitaClient\Model\SearchResultGroupDto apiSearchSearchGet($query_string, $include_chapter_and_files)

Searches against different entities in the system against a query string

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SearchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query_string = "query_string_example"; // string | 
$include_chapter_and_files = true; // bool | Include Chapter and Filenames in the entities. This can slow down the search on larger systems

try {
    $result = $apiInstance->apiSearchSearchGet($query_string, $include_chapter_and_files);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SearchApi->apiSearchSearchGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query_string** | **string**|  | [optional]
 **include_chapter_and_files** | **bool**| Include Chapter and Filenames in the entities. This can slow down the search on larger systems | [optional] [default to true]

### Return type

[**\Pbxg33k\KavitaClient\Model\SearchResultGroupDto**](../Model/SearchResultGroupDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSearchSeriesForChapterGet**
> \Pbxg33k\KavitaClient\Model\SeriesDto apiSearchSeriesForChapterGet($chapter_id)

Returns the series for the Chapter id. If the user does not have access (shouldn't happen by the UI), then null is returned

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SearchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 

try {
    $result = $apiInstance->apiSearchSeriesForChapterGet($chapter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SearchApi->apiSearchSeriesForChapterGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\SeriesDto**](../Model/SeriesDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSearchSeriesForMangafileGet**
> \Pbxg33k\KavitaClient\Model\SeriesDto apiSearchSeriesForMangafileGet($manga_file_id)

Returns the series for the MangaFile id. If the user does not have access (shouldn't happen by the UI), then null is returned

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SearchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$manga_file_id = 56; // int | 

try {
    $result = $apiInstance->apiSearchSeriesForMangafileGet($manga_file_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SearchApi->apiSearchSeriesForMangafileGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **manga_file_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\SeriesDto**](../Model/SeriesDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

