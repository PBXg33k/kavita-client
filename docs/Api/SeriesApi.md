# Pbxg33k\KavitaClient\SeriesApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiSeriesAgeRatingGet**](SeriesApi.md#apiseriesageratingget) | **GET** /api/Series/age-rating | Get the age rating for the Kavita.Models.Entities.Enums.AgeRating enum value
[**apiSeriesAllRelatedGet**](SeriesApi.md#apiseriesallrelatedget) | **GET** /api/Series/all-related | Returns all related series against the passed series Id
[**apiSeriesAllV2Post**](SeriesApi.md#apiseriesallv2post) | **POST** /api/Series/all-v2 | Returns all series for the library
[**apiSeriesAnalyzePost**](SeriesApi.md#apiseriesanalyzepost) | **POST** /api/Series/analyze | Run a file analysis on the series.
[**apiSeriesChapterGet**](SeriesApi.md#apiserieschapterget) | **GET** /api/Series/chapter | Returns a single Chapter with progress information
[**apiSeriesCurrentlyReadingGet**](SeriesApi.md#apiseriescurrentlyreadingget) | **GET** /api/Series/currently-reading | Get series a user is currently reading, requires the user to share their profile
[**apiSeriesDeleteMultiplePost**](SeriesApi.md#apiseriesdeletemultiplepost) | **POST** /api/Series/delete-multiple | Deletes multiple series from Kavita at once
[**apiSeriesDontMatchPost**](SeriesApi.md#apiseriesdontmatchpost) | **POST** /api/Series/dont-match | When true, will not perform a match and will prevent Kavita from attempting to match/scrobble against this series
[**apiSeriesExternalSeriesDetailGet**](SeriesApi.md#apiseriesexternalseriesdetailget) | **GET** /api/Series/external-series-detail | 
[**apiSeriesMatchPost**](SeriesApi.md#apiseriesmatchpost) | **POST** /api/Series/match | Sends a request to Kavita+ API for all potential matches, sorted by relevance
[**apiSeriesMetadataGet**](SeriesApi.md#apiseriesmetadataget) | **GET** /api/Series/metadata | Returns metadata for a given series
[**apiSeriesMetadataPost**](SeriesApi.md#apiseriesmetadatapost) | **POST** /api/Series/metadata | Update series metadata
[**apiSeriesNextExpectedGet**](SeriesApi.md#apiseriesnextexpectedget) | **GET** /api/Series/next-expected | Based on the delta times between when chapters are added, for series that are not Completed/Cancelled/Hiatus, forecast the next date when it will be available.
[**apiSeriesOnDeckPost**](SeriesApi.md#apiseriesondeckpost) | **POST** /api/Series/on-deck | Fetches series that are on deck aka have progress on them.
[**apiSeriesRecentlyAddedV2Post**](SeriesApi.md#apiseriesrecentlyaddedv2post) | **POST** /api/Series/recently-added-v2 | Gets all recently added series
[**apiSeriesRecentlyUpdatedSeriesPost**](SeriesApi.md#apiseriesrecentlyupdatedseriespost) | **POST** /api/Series/recently-updated-series | Returns series that were recently updated, like adding or removing a chapter
[**apiSeriesRefreshMetadataPost**](SeriesApi.md#apiseriesrefreshmetadatapost) | **POST** /api/Series/refresh-metadata | Runs a Cover Image Generation task
[**apiSeriesRelatedGet**](SeriesApi.md#apiseriesrelatedget) | **GET** /api/Series/related | Fetches the related series for a given series
[**apiSeriesRemoveFromOnDeckPost**](SeriesApi.md#apiseriesremovefromondeckpost) | **POST** /api/Series/remove-from-on-deck | Removes a series from displaying on deck until the next read event on that series
[**apiSeriesScanPost**](SeriesApi.md#apiseriesscanpost) | **POST** /api/Series/scan | Scan a series and force each file to be updated. This should be invoked via the User, hence why we force.
[**apiSeriesSeriesByCollectionGet**](SeriesApi.md#apiseriesseriesbycollectionget) | **GET** /api/Series/series-by-collection | Returns all Series grouped by the passed Collection Id with Pagination.
[**apiSeriesSeriesByIdsPost**](SeriesApi.md#apiseriesseriesbyidspost) | **POST** /api/Series/series-by-ids | Fetches Series for a set of Ids. This will check User for permission access and filter out any Ids that don&#x27;t exist or the user does not have access to.
[**apiSeriesSeriesDetailGet**](SeriesApi.md#apiseriesseriesdetailget) | **GET** /api/Series/series-detail | Get a special DTO for Series Detail page.
[**apiSeriesSeriesIdDelete**](SeriesApi.md#apiseriesseriesiddelete) | **DELETE** /api/Series/{seriesId} | Deletes a series from Kavita
[**apiSeriesSeriesIdGet**](SeriesApi.md#apiseriesseriesidget) | **GET** /api/Series/{seriesId} | Fetches a Series for a given Id
[**apiSeriesSeriesWithAnnotationsGet**](SeriesApi.md#apiseriesserieswithannotationsget) | **GET** /api/Series/series-with-annotations | Returns all Series that a user has access to
[**apiSeriesUpdateMatchPost**](SeriesApi.md#apiseriesupdatematchpost) | **POST** /api/Series/update-match | This will perform the fix match
[**apiSeriesUpdatePost**](SeriesApi.md#apiseriesupdatepost) | **POST** /api/Series/update | Updates the Series
[**apiSeriesUpdateRelatedPost**](SeriesApi.md#apiseriesupdaterelatedpost) | **POST** /api/Series/update-related | Update the relations attached to the Series. Does not generate associated Sequel/Prequel pairs on target series.
[**apiSeriesV2Post**](SeriesApi.md#apiseriesv2post) | **POST** /api/Series/v2 | Gets series with the applied Filter
[**apiSeriesVolumeGet**](SeriesApi.md#apiseriesvolumeget) | **GET** /api/Series/volume | Returns a single Volume with progress information and Chapters
[**apiSeriesVolumesGet**](SeriesApi.md#apiseriesvolumesget) | **GET** /api/Series/volumes | Returns All volumes for a series with progress information and Chapters

# **apiSeriesAgeRatingGet**
> string apiSeriesAgeRatingGet($age_rating)

Get the age rating for the Kavita.Models.Entities.Enums.AgeRating enum value

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$age_rating = 56; // int | 

try {
    $result = $apiInstance->apiSeriesAgeRatingGet($age_rating);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesAgeRatingGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **age_rating** | **int**|  | [optional]

### Return type

**string**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesAllRelatedGet**
> \Pbxg33k\KavitaClient\Model\RelatedSeriesDto apiSeriesAllRelatedGet($series_id)

Returns all related series against the passed series Id

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $result = $apiInstance->apiSeriesAllRelatedGet($series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesAllRelatedGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\RelatedSeriesDto**](../Model/RelatedSeriesDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesAllV2Post**
> \Pbxg33k\KavitaClient\Model\SeriesDto[] apiSeriesAllV2Post($body, $page_number, $page_size, $user_id, $context)

Returns all series for the library

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\SeriesFilterV2Dto(); // \Pbxg33k\KavitaClient\Model\SeriesFilterV2Dto | 
$page_number = 56; // int | 
$page_size = 56; // int | 
$user_id = 56; // int | Optional user id to request the OnDeck for someone else. They must have profile sharing enabled when doing so
$context = new \Pbxg33k\KavitaClient\Model\QueryContext(); // \Pbxg33k\KavitaClient\Model\QueryContext | 

try {
    $result = $apiInstance->apiSeriesAllV2Post($body, $page_number, $page_size, $user_id, $context);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesAllV2Post: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\SeriesFilterV2Dto**](../Model/SeriesFilterV2Dto.md)|  | [optional]
 **page_number** | **int**|  | [optional]
 **page_size** | **int**|  | [optional]
 **user_id** | **int**| Optional user id to request the OnDeck for someone else. They must have profile sharing enabled when doing so | [optional]
 **context** | [**\Pbxg33k\KavitaClient\Model\QueryContext**](../Model/.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\SeriesDto[]**](../Model/SeriesDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesAnalyzePost**
> apiSeriesAnalyzePost($body)

Run a file analysis on the series.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\RefreshSeriesDto(); // \Pbxg33k\KavitaClient\Model\RefreshSeriesDto | 

try {
    $apiInstance->apiSeriesAnalyzePost($body);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesAnalyzePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\RefreshSeriesDto**](../Model/RefreshSeriesDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesChapterGet**
> \Pbxg33k\KavitaClient\Model\ChapterDto apiSeriesChapterGet($chapter_id)

Returns a single Chapter with progress information

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 

try {
    $result = $apiInstance->apiSeriesChapterGet($chapter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesChapterGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ChapterDto**](../Model/ChapterDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesCurrentlyReadingGet**
> \Pbxg33k\KavitaClient\Model\SeriesDto[] apiSeriesCurrentlyReadingGet($page_number, $page_size, $user_id)

Get series a user is currently reading, requires the user to share their profile

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page_number = 56; // int | 
$page_size = 56; // int | 
$user_id = 56; // int | 

try {
    $result = $apiInstance->apiSeriesCurrentlyReadingGet($page_number, $page_size, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesCurrentlyReadingGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page_number** | **int**|  | [optional]
 **page_size** | **int**|  | [optional]
 **user_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\SeriesDto[]**](../Model/SeriesDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesDeleteMultiplePost**
> apiSeriesDeleteMultiplePost($body)

Deletes multiple series from Kavita at once

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\DeleteSeriesDto(); // \Pbxg33k\KavitaClient\Model\DeleteSeriesDto | 

try {
    $apiInstance->apiSeriesDeleteMultiplePost($body);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesDeleteMultiplePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\DeleteSeriesDto**](../Model/DeleteSeriesDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesDontMatchPost**
> apiSeriesDontMatchPost($series_id, $dont_match)

When true, will not perform a match and will prevent Kavita from attempting to match/scrobble against this series

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 
$dont_match = true; // bool | 

try {
    $apiInstance->apiSeriesDontMatchPost($series_id, $dont_match);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesDontMatchPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]
 **dont_match** | **bool**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesExternalSeriesDetailGet**
> \Pbxg33k\KavitaClient\Model\ExternalSeriesDto apiSeriesExternalSeriesDetailGet($ani_list_id, $mal_id, $series_id)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ani_list_id = 56; // int | 
$mal_id = 789; // int | 
$series_id = 56; // int | 

try {
    $result = $apiInstance->apiSeriesExternalSeriesDetailGet($ani_list_id, $mal_id, $series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesExternalSeriesDetailGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ani_list_id** | **int**|  | [optional]
 **mal_id** | **int**|  | [optional]
 **series_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ExternalSeriesDto**](../Model/ExternalSeriesDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesMatchPost**
> \Pbxg33k\KavitaClient\Model\ExternalSeriesMatchDto[] apiSeriesMatchPost($body)

Sends a request to Kavita+ API for all potential matches, sorted by relevance

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\MatchSeriesDto(); // \Pbxg33k\KavitaClient\Model\MatchSeriesDto | 

try {
    $result = $apiInstance->apiSeriesMatchPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesMatchPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\MatchSeriesDto**](../Model/MatchSeriesDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ExternalSeriesMatchDto[]**](../Model/ExternalSeriesMatchDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesMetadataGet**
> \Pbxg33k\KavitaClient\Model\SeriesMetadataDto apiSeriesMetadataGet($series_id)

Returns metadata for a given series

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $result = $apiInstance->apiSeriesMetadataGet($series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesMetadataGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\SeriesMetadataDto**](../Model/SeriesMetadataDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesMetadataPost**
> apiSeriesMetadataPost($body)

Update series metadata

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateSeriesMetadataDto(); // \Pbxg33k\KavitaClient\Model\UpdateSeriesMetadataDto | 

try {
    $apiInstance->apiSeriesMetadataPost($body);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesMetadataPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateSeriesMetadataDto**](../Model/UpdateSeriesMetadataDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesNextExpectedGet**
> \Pbxg33k\KavitaClient\Model\NextExpectedChapterDto apiSeriesNextExpectedGet($series_id)

Based on the delta times between when chapters are added, for series that are not Completed/Cancelled/Hiatus, forecast the next date when it will be available.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $result = $apiInstance->apiSeriesNextExpectedGet($series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesNextExpectedGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\NextExpectedChapterDto**](../Model/NextExpectedChapterDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesOnDeckPost**
> \Pbxg33k\KavitaClient\Model\SeriesDto[] apiSeriesOnDeckPost($page_number, $page_size, $library_id)

Fetches series that are on deck aka have progress on them.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page_number = 56; // int | 
$page_size = 56; // int | 
$library_id = 0; // int | Default of 0 meaning all libraries

try {
    $result = $apiInstance->apiSeriesOnDeckPost($page_number, $page_size, $library_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesOnDeckPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page_number** | **int**|  | [optional]
 **page_size** | **int**|  | [optional]
 **library_id** | **int**| Default of 0 meaning all libraries | [optional] [default to 0]

### Return type

[**\Pbxg33k\KavitaClient\Model\SeriesDto[]**](../Model/SeriesDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesRecentlyAddedV2Post**
> \Pbxg33k\KavitaClient\Model\SeriesDto[] apiSeriesRecentlyAddedV2Post($body, $page_number, $page_size)

Gets all recently added series

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\SeriesFilterV2Dto(); // \Pbxg33k\KavitaClient\Model\SeriesFilterV2Dto | 
$page_number = 56; // int | 
$page_size = 56; // int | 

try {
    $result = $apiInstance->apiSeriesRecentlyAddedV2Post($body, $page_number, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesRecentlyAddedV2Post: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\SeriesFilterV2Dto**](../Model/SeriesFilterV2Dto.md)|  | [optional]
 **page_number** | **int**|  | [optional]
 **page_size** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\SeriesDto[]**](../Model/SeriesDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesRecentlyUpdatedSeriesPost**
> \Pbxg33k\KavitaClient\Model\GroupedSeriesDto[] apiSeriesRecentlyUpdatedSeriesPost($page_number, $page_size)

Returns series that were recently updated, like adding or removing a chapter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page_number = 56; // int | 
$page_size = 56; // int | 

try {
    $result = $apiInstance->apiSeriesRecentlyUpdatedSeriesPost($page_number, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesRecentlyUpdatedSeriesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page_number** | **int**|  | [optional]
 **page_size** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\GroupedSeriesDto[]**](../Model/GroupedSeriesDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesRefreshMetadataPost**
> apiSeriesRefreshMetadataPost($body)

Runs a Cover Image Generation task

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\RefreshSeriesDto(); // \Pbxg33k\KavitaClient\Model\RefreshSeriesDto | 

try {
    $apiInstance->apiSeriesRefreshMetadataPost($body);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesRefreshMetadataPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\RefreshSeriesDto**](../Model/RefreshSeriesDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesRelatedGet**
> \Pbxg33k\KavitaClient\Model\SeriesDto[] apiSeriesRelatedGet($series_id, $relation)

Fetches the related series for a given series

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 
$relation = new \Pbxg33k\KavitaClient\Model\RelationKind(); // \Pbxg33k\KavitaClient\Model\RelationKind | Type of Relationship to pull back

try {
    $result = $apiInstance->apiSeriesRelatedGet($series_id, $relation);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesRelatedGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]
 **relation** | [**\Pbxg33k\KavitaClient\Model\RelationKind**](../Model/.md)| Type of Relationship to pull back | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\SeriesDto[]**](../Model/SeriesDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesRemoveFromOnDeckPost**
> apiSeriesRemoveFromOnDeckPost($series_id)

Removes a series from displaying on deck until the next read event on that series

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $apiInstance->apiSeriesRemoveFromOnDeckPost($series_id);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesRemoveFromOnDeckPost: ', $e->getMessage(), PHP_EOL;
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

# **apiSeriesScanPost**
> apiSeriesScanPost($body)

Scan a series and force each file to be updated. This should be invoked via the User, hence why we force.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\RefreshSeriesDto(); // \Pbxg33k\KavitaClient\Model\RefreshSeriesDto | 

try {
    $apiInstance->apiSeriesScanPost($body);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesScanPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\RefreshSeriesDto**](../Model/RefreshSeriesDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesSeriesByCollectionGet**
> \Pbxg33k\KavitaClient\Model\SeriesDto[] apiSeriesSeriesByCollectionGet($collection_id, $page_number, $page_size)

Returns all Series grouped by the passed Collection Id with Pagination.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$collection_id = 56; // int | Collection Id to pull series from
$page_number = 56; // int | 
$page_size = 56; // int | 

try {
    $result = $apiInstance->apiSeriesSeriesByCollectionGet($collection_id, $page_number, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesSeriesByCollectionGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **collection_id** | **int**| Collection Id to pull series from | [optional]
 **page_number** | **int**|  | [optional]
 **page_size** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\SeriesDto[]**](../Model/SeriesDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesSeriesByIdsPost**
> \Pbxg33k\KavitaClient\Model\SeriesDto[] apiSeriesSeriesByIdsPost($body)

Fetches Series for a set of Ids. This will check User for permission access and filter out any Ids that don't exist or the user does not have access to.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\SeriesByIdsDto(); // \Pbxg33k\KavitaClient\Model\SeriesByIdsDto | 

try {
    $result = $apiInstance->apiSeriesSeriesByIdsPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesSeriesByIdsPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\SeriesByIdsDto**](../Model/SeriesByIdsDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\SeriesDto[]**](../Model/SeriesDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesSeriesDetailGet**
> \Pbxg33k\KavitaClient\Model\SeriesDetailDto apiSeriesSeriesDetailGet($series_id)

Get a special DTO for Series Detail page.

Do not rely on this API externally. May change without hesitation.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $result = $apiInstance->apiSeriesSeriesDetailGet($series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesSeriesDetailGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\SeriesDetailDto**](../Model/SeriesDetailDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesSeriesIdDelete**
> bool apiSeriesSeriesIdDelete($series_id)

Deletes a series from Kavita

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $result = $apiInstance->apiSeriesSeriesIdDelete($series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesSeriesIdDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  |

### Return type

**bool**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesSeriesIdGet**
> \Pbxg33k\KavitaClient\Model\SeriesDto apiSeriesSeriesIdGet($series_id)

Fetches a Series for a given Id

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | Series Id to fetch details for

try {
    $result = $apiInstance->apiSeriesSeriesIdGet($series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesSeriesIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**| Series Id to fetch details for |

### Return type

[**\Pbxg33k\KavitaClient\Model\SeriesDto**](../Model/SeriesDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesSeriesWithAnnotationsGet**
> \Pbxg33k\KavitaClient\Model\SeriesDto[] apiSeriesSeriesWithAnnotationsGet()

Returns all Series that a user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiSeriesSeriesWithAnnotationsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesSeriesWithAnnotationsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\SeriesDto[]**](../Model/SeriesDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesUpdateMatchPost**
> apiSeriesUpdateMatchPost($series_id, $ani_list_id, $mal_id, $cbr_id)

This will perform the fix match

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 
$ani_list_id = 56; // int | 
$mal_id = 789; // int | 
$cbr_id = 56; // int | 

try {
    $apiInstance->apiSeriesUpdateMatchPost($series_id, $ani_list_id, $mal_id, $cbr_id);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesUpdateMatchPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]
 **ani_list_id** | **int**|  | [optional]
 **mal_id** | **int**|  | [optional]
 **cbr_id** | **int**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesUpdatePost**
> \Pbxg33k\KavitaClient\Model\SeriesDto apiSeriesUpdatePost($body)

Updates the Series

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateSeriesDto(); // \Pbxg33k\KavitaClient\Model\UpdateSeriesDto | 

try {
    $result = $apiInstance->apiSeriesUpdatePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesUpdatePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateSeriesDto**](../Model/UpdateSeriesDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\SeriesDto**](../Model/SeriesDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesUpdateRelatedPost**
> apiSeriesUpdateRelatedPost($body)

Update the relations attached to the Series. Does not generate associated Sequel/Prequel pairs on target series.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateRelatedSeriesDto(); // \Pbxg33k\KavitaClient\Model\UpdateRelatedSeriesDto | 

try {
    $apiInstance->apiSeriesUpdateRelatedPost($body);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesUpdateRelatedPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateRelatedSeriesDto**](../Model/UpdateRelatedSeriesDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesV2Post**
> \Pbxg33k\KavitaClient\Model\SeriesDto[] apiSeriesV2Post($body, $page_number, $page_size)

Gets series with the applied Filter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\SeriesFilterV2Dto(); // \Pbxg33k\KavitaClient\Model\SeriesFilterV2Dto | 
$page_number = 56; // int | 
$page_size = 56; // int | 

try {
    $result = $apiInstance->apiSeriesV2Post($body, $page_number, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesV2Post: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\SeriesFilterV2Dto**](../Model/SeriesFilterV2Dto.md)|  | [optional]
 **page_number** | **int**|  | [optional]
 **page_size** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\SeriesDto[]**](../Model/SeriesDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesVolumeGet**
> \Pbxg33k\KavitaClient\Model\VolumeDto apiSeriesVolumeGet($volume_id)

Returns a single Volume with progress information and Chapters

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$volume_id = 56; // int | 

try {
    $result = $apiInstance->apiSeriesVolumeGet($volume_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesVolumeGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **volume_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\VolumeDto**](../Model/VolumeDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiSeriesVolumesGet**
> \Pbxg33k\KavitaClient\Model\VolumeDto[] apiSeriesVolumesGet($series_id)

Returns All volumes for a series with progress information and Chapters

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\SeriesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $result = $apiInstance->apiSeriesVolumesGet($series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SeriesApi->apiSeriesVolumesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\VolumeDto[]**](../Model/VolumeDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

