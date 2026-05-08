# Pbxg33k\KavitaClient\StatsApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiStatsAvgTimeByHourGet**](StatsApi.md#apistatsavgtimebyhourget) | **GET** /api/Stats/avg-time-by-hour | Returns the avg time read by hour in the given filter
[**apiStatsDayBreakdownGet**](StatsApi.md#apistatsdaybreakdownget) | **GET** /api/Stats/day-breakdown | 
[**apiStatsDeviceClientTypeGet**](StatsApi.md#apistatsdeviceclienttypeget) | **GET** /api/Stats/device/client-type | Returns client type breakdown for the current month
[**apiStatsDeviceDeviceTypeGet**](StatsApi.md#apistatsdevicedevicetypeget) | **GET** /api/Stats/device/device-type | Desktop vs Mobile spread over this month
[**apiStatsFavoriteAuthorsGet**](StatsApi.md#apistatsfavoriteauthorsget) | **GET** /api/Stats/favorite-authors | 
[**apiStatsFilesAddedOverTimeGet**](StatsApi.md#apistatsfilesaddedovertimeget) | **GET** /api/Stats/files-added-over-time | 
[**apiStatsGenreBreakdownGet**](StatsApi.md#apistatsgenrebreakdownget) | **GET** /api/Stats/genre-breakdown | Returns the top 10 genres that the user likes reading
[**apiStatsMostActiveUsersGet**](StatsApi.md#apistatsmostactiveusersget) | **GET** /api/Stats/most-active-users | Top 5 most active readers for the given timeframe
[**apiStatsPageSpreadGet**](StatsApi.md#apistatspagespreadget) | **GET** /api/Stats/page-spread | 
[**apiStatsPagesPerYearGet**](StatsApi.md#apistatspagesperyearget) | **GET** /api/Stats/pages-per-year | Returns a count of pages read per year for a given userId.
[**apiStatsPopularDecadesGet**](StatsApi.md#apistatspopulardecadesget) | **GET** /api/Stats/popular-decades | 
[**apiStatsPopularGenresGet**](StatsApi.md#apistatspopulargenresget) | **GET** /api/Stats/popular-genres | 
[**apiStatsPopularLibrariesGet**](StatsApi.md#apistatspopularlibrariesget) | **GET** /api/Stats/popular-libraries | 
[**apiStatsPopularPeopleGet**](StatsApi.md#apistatspopularpeopleget) | **GET** /api/Stats/popular-people | 
[**apiStatsPopularReadingListGet**](StatsApi.md#apistatspopularreadinglistget) | **GET** /api/Stats/popular-reading-list | Gets the top 5 most popular reading lists. Counts a reading list as active if a user has read at least some
[**apiStatsPopularSeriesGet**](StatsApi.md#apistatspopularseriesget) | **GET** /api/Stats/popular-series | 
[**apiStatsPopularTagsGet**](StatsApi.md#apistatspopulartagsget) | **GET** /api/Stats/popular-tags | 
[**apiStatsReadingActivityGet**](StatsApi.md#apistatsreadingactivityget) | **GET** /api/Stats/reading-activity | 
[**apiStatsReadingCountsGet**](StatsApi.md#apistatsreadingcountsget) | **GET** /api/Stats/reading-counts | Returns reading history events for a give or all users, broken up by day, and format
[**apiStatsReadingHistoryGet**](StatsApi.md#apistatsreadinghistoryget) | **GET** /api/Stats/reading-history | Return a user&#x27;s reading session history
[**apiStatsReadingHistorySeriesSeriesIdGet**](StatsApi.md#apistatsreadinghistoryseriesseriesidget) | **GET** /api/Stats/reading-history/series/{seriesId} | Return the authenticated users reading session history for a given series
[**apiStatsReadingPaceGet**](StatsApi.md#apistatsreadingpaceget) | **GET** /api/Stats/reading-pace | 
[**apiStatsReadsByMonthGet**](StatsApi.md#apistatsreadsbymonthget) | **GET** /api/Stats/reads-by-month | 
[**apiStatsServerCountMangaFormatGet**](StatsApi.md#apistatsservercountmangaformatget) | **GET** /api/Stats/server/count/manga-format | 
[**apiStatsServerCountPublicationStatusGet**](StatsApi.md#apistatsservercountpublicationstatusget) | **GET** /api/Stats/server/count/publication-status | 
[**apiStatsServerFileBreakdownGet**](StatsApi.md#apistatsserverfilebreakdownget) | **GET** /api/Stats/server/file-breakdown | A breakdown of different files, their size, and format
[**apiStatsServerFileExtensionGet**](StatsApi.md#apistatsserverfileextensionget) | **GET** /api/Stats/server/file-extension | Generates a csv of all file paths for a given extension
[**apiStatsServerStatsGet**](StatsApi.md#apistatsserverstatsget) | **GET** /api/Stats/server/stats | 
[**apiStatsTagBreakdownGet**](StatsApi.md#apistatstagbreakdownget) | **GET** /api/Stats/tag-breakdown | Returns top 10 tags that user likes reading
[**apiStatsTotalReadsGet**](StatsApi.md#apistatstotalreadsget) | **GET** /api/Stats/total-reads | Returns the total amount reads in the given filter
[**apiStatsUserReadGet**](StatsApi.md#apistatsuserreadget) | **GET** /api/Stats/user-read | 
[**apiStatsUserStatsGet**](StatsApi.md#apistatsuserstatsget) | **GET** /api/Stats/user-stats | 
[**apiStatsWordSpreadGet**](StatsApi.md#apistatswordspreadget) | **GET** /api/Stats/word-spread | 
[**apiStatsWordsPerYearGet**](StatsApi.md#apistatswordsperyearget) | **GET** /api/Stats/words-per-year | Returns a count of words read per year for a given userId.

# **apiStatsAvgTimeByHourGet**
> \Pbxg33k\KavitaClient\Model\ReadTimeByHourDto apiStatsAvgTimeByHourGet($start_date, $time_zone_id, $end_date, $libraries, $user_id)

Returns the avg time read by hour in the given filter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$start_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$time_zone_id = "time_zone_id_example"; // string | 
$end_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$libraries = array(56); // int[] | 
$user_id = 56; // int | 

try {
    $result = $apiInstance->apiStatsAvgTimeByHourGet($start_date, $time_zone_id, $end_date, $libraries, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsAvgTimeByHourGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start_date** | **\DateTime**|  | [optional]
 **time_zone_id** | **string**|  | [optional]
 **end_date** | **\DateTime**|  | [optional]
 **libraries** | [**int[]**](../Model/int.md)|  | [optional]
 **user_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ReadTimeByHourDto**](../Model/ReadTimeByHourDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsDayBreakdownGet**
> \Pbxg33k\KavitaClient\Model\DayOfWeekStatCount[] apiStatsDayBreakdownGet($user_id)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 0; // int | 

try {
    $result = $apiInstance->apiStatsDayBreakdownGet($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsDayBreakdownGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **int**|  | [optional] [default to 0]

### Return type

[**\Pbxg33k\KavitaClient\Model\DayOfWeekStatCount[]**](../Model/DayOfWeekStatCount.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsDeviceClientTypeGet**
> \Pbxg33k\KavitaClient\Model\DeviceClientBreakdownDto apiStatsDeviceClientTypeGet()

Returns client type breakdown for the current month

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiStatsDeviceClientTypeGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsDeviceClientTypeGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\DeviceClientBreakdownDto**](../Model/DeviceClientBreakdownDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsDeviceDeviceTypeGet**
> \Pbxg33k\KavitaClient\Model\StringStatCount apiStatsDeviceDeviceTypeGet()

Desktop vs Mobile spread over this month

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiStatsDeviceDeviceTypeGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsDeviceDeviceTypeGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\StringStatCount**](../Model/StringStatCount.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsFavoriteAuthorsGet**
> \Pbxg33k\KavitaClient\Model\MostReadAuthorsDto apiStatsFavoriteAuthorsGet($start_date, $time_zone_id, $end_date, $libraries, $user_id)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$start_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$time_zone_id = "time_zone_id_example"; // string | 
$end_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$libraries = array(56); // int[] | 
$user_id = 56; // int | 

try {
    $result = $apiInstance->apiStatsFavoriteAuthorsGet($start_date, $time_zone_id, $end_date, $libraries, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsFavoriteAuthorsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start_date** | **\DateTime**|  | [optional]
 **time_zone_id** | **string**|  | [optional]
 **end_date** | **\DateTime**|  | [optional]
 **libraries** | [**int[]**](../Model/int.md)|  | [optional]
 **user_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\MostReadAuthorsDto**](../Model/MostReadAuthorsDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsFilesAddedOverTimeGet**
> \Pbxg33k\KavitaClient\Model\DateTimeStatCountWithFormat[] apiStatsFilesAddedOverTimeGet()



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiStatsFilesAddedOverTimeGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsFilesAddedOverTimeGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\DateTimeStatCountWithFormat[]**](../Model/DateTimeStatCountWithFormat.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsGenreBreakdownGet**
> \Pbxg33k\KavitaClient\Model\StringBreakDownDto apiStatsGenreBreakdownGet($start_date, $time_zone_id, $end_date, $libraries, $user_id)

Returns the top 10 genres that the user likes reading

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$start_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$time_zone_id = "time_zone_id_example"; // string | 
$end_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$libraries = array(56); // int[] | 
$user_id = 56; // int | 

try {
    $result = $apiInstance->apiStatsGenreBreakdownGet($start_date, $time_zone_id, $end_date, $libraries, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsGenreBreakdownGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start_date** | **\DateTime**|  | [optional]
 **time_zone_id** | **string**|  | [optional]
 **end_date** | **\DateTime**|  | [optional]
 **libraries** | [**int[]**](../Model/int.md)|  | [optional]
 **user_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\StringBreakDownDto**](../Model/StringBreakDownDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsMostActiveUsersGet**
> \Pbxg33k\KavitaClient\Model\TopReadDto[] apiStatsMostActiveUsersGet($start_date, $time_zone_id, $end_date, $libraries)

Top 5 most active readers for the given timeframe

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$start_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$time_zone_id = "time_zone_id_example"; // string | 
$end_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$libraries = array(56); // int[] | 

try {
    $result = $apiInstance->apiStatsMostActiveUsersGet($start_date, $time_zone_id, $end_date, $libraries);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsMostActiveUsersGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start_date** | **\DateTime**|  | [optional]
 **time_zone_id** | **string**|  | [optional]
 **end_date** | **\DateTime**|  | [optional]
 **libraries** | [**int[]**](../Model/int.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\TopReadDto[]**](../Model/TopReadDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsPageSpreadGet**
> \Pbxg33k\KavitaClient\Model\SpreadStatsDto apiStatsPageSpreadGet($start_date, $time_zone_id, $end_date, $libraries, $user_id)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$start_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$time_zone_id = "time_zone_id_example"; // string | 
$end_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$libraries = array(56); // int[] | 
$user_id = 56; // int | 

try {
    $result = $apiInstance->apiStatsPageSpreadGet($start_date, $time_zone_id, $end_date, $libraries, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsPageSpreadGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start_date** | **\DateTime**|  | [optional]
 **time_zone_id** | **string**|  | [optional]
 **end_date** | **\DateTime**|  | [optional]
 **libraries** | [**int[]**](../Model/int.md)|  | [optional]
 **user_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\SpreadStatsDto**](../Model/SpreadStatsDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsPagesPerYearGet**
> \Pbxg33k\KavitaClient\Model\Int32StatCount[] apiStatsPagesPerYearGet($user_id)

Returns a count of pages read per year for a given userId.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 56; // int | 

try {
    $result = $apiInstance->apiStatsPagesPerYearGet($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsPagesPerYearGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\Int32StatCount[]**](../Model/Int32StatCount.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsPopularDecadesGet**
> \Pbxg33k\KavitaClient\Model\StatBucketDto[] apiStatsPopularDecadesGet()



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiStatsPopularDecadesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsPopularDecadesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\StatBucketDto[]**](../Model/StatBucketDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsPopularGenresGet**
> \Pbxg33k\KavitaClient\Model\GenreTagDtoStatCount[] apiStatsPopularGenresGet()



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiStatsPopularGenresGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsPopularGenresGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\GenreTagDtoStatCount[]**](../Model/GenreTagDtoStatCount.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsPopularLibrariesGet**
> \Pbxg33k\KavitaClient\Model\LibraryDtoStatCount[] apiStatsPopularLibrariesGet()



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiStatsPopularLibrariesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsPopularLibrariesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\LibraryDtoStatCount[]**](../Model/LibraryDtoStatCount.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsPopularPeopleGet**
> \Pbxg33k\KavitaClient\Model\PersonDtoStatCount[] apiStatsPopularPeopleGet($role)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$role = new \Pbxg33k\KavitaClient\Model\PersonRole(); // \Pbxg33k\KavitaClient\Model\PersonRole | Members: - `3` — Writer - `4` — Penciller - `5` — Inker - `6` — Colorist - `7` — Letterer - `8` — CoverArtist - `9` — Editor - `10` — Publisher - `11` — Character - `12` — Translator - `13` — Imprint - `14` — Team - `15` — Location

try {
    $result = $apiInstance->apiStatsPopularPeopleGet($role);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsPopularPeopleGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **role** | [**\Pbxg33k\KavitaClient\Model\PersonRole**](../Model/.md)| Members: - &#x60;3&#x60; — Writer - &#x60;4&#x60; — Penciller - &#x60;5&#x60; — Inker - &#x60;6&#x60; — Colorist - &#x60;7&#x60; — Letterer - &#x60;8&#x60; — CoverArtist - &#x60;9&#x60; — Editor - &#x60;10&#x60; — Publisher - &#x60;11&#x60; — Character - &#x60;12&#x60; — Translator - &#x60;13&#x60; — Imprint - &#x60;14&#x60; — Team - &#x60;15&#x60; — Location | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\PersonDtoStatCount[]**](../Model/PersonDtoStatCount.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsPopularReadingListGet**
> \Pbxg33k\KavitaClient\Model\SeriesDtoStatCount[] apiStatsPopularReadingListGet()

Gets the top 5 most popular reading lists. Counts a reading list as active if a user has read at least some

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiStatsPopularReadingListGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsPopularReadingListGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\SeriesDtoStatCount[]**](../Model/SeriesDtoStatCount.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsPopularSeriesGet**
> \Pbxg33k\KavitaClient\Model\SeriesDtoStatCount[] apiStatsPopularSeriesGet()



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiStatsPopularSeriesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsPopularSeriesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\SeriesDtoStatCount[]**](../Model/SeriesDtoStatCount.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsPopularTagsGet**
> \Pbxg33k\KavitaClient\Model\TagDtoStatCount[] apiStatsPopularTagsGet()



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiStatsPopularTagsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsPopularTagsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\TagDtoStatCount[]**](../Model/TagDtoStatCount.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsReadingActivityGet**
> map[string,\Pbxg33k\KavitaClient\Model\ReadingActivityGraphEntryDto] apiStatsReadingActivityGet($start_date, $time_zone_id, $end_date, $libraries, $user_id, $year)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$start_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$time_zone_id = "time_zone_id_example"; // string | 
$end_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$libraries = array(56); // int[] | 
$user_id = 56; // int | 
$year = 56; // int | 

try {
    $result = $apiInstance->apiStatsReadingActivityGet($start_date, $time_zone_id, $end_date, $libraries, $user_id, $year);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsReadingActivityGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start_date** | **\DateTime**|  | [optional]
 **time_zone_id** | **string**|  | [optional]
 **end_date** | **\DateTime**|  | [optional]
 **libraries** | [**int[]**](../Model/int.md)|  | [optional]
 **user_id** | **int**|  | [optional]
 **year** | **int**|  | [optional]

### Return type

[**map[string,\Pbxg33k\KavitaClient\Model\ReadingActivityGraphEntryDto]**](../Model/ReadingActivityGraphEntryDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsReadingCountsGet**
> \Pbxg33k\KavitaClient\Model\DateTimeStatCountWithFormat[] apiStatsReadingCountsGet($start_date, $time_zone_id, $end_date, $libraries, $user_id)

Returns reading history events for a give or all users, broken up by day, and format

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$start_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$time_zone_id = "time_zone_id_example"; // string | 
$end_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$libraries = array(56); // int[] | 
$user_id = 56; // int | If 0, defaults to all users, else just userId

try {
    $result = $apiInstance->apiStatsReadingCountsGet($start_date, $time_zone_id, $end_date, $libraries, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsReadingCountsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start_date** | **\DateTime**|  | [optional]
 **time_zone_id** | **string**|  | [optional]
 **end_date** | **\DateTime**|  | [optional]
 **libraries** | [**int[]**](../Model/int.md)|  | [optional]
 **user_id** | **int**| If 0, defaults to all users, else just userId | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\DateTimeStatCountWithFormat[]**](../Model/DateTimeStatCountWithFormat.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsReadingHistoryGet**
> \Pbxg33k\KavitaClient\Model\ReadingHistoryItemDto[] apiStatsReadingHistoryGet($start_date, $time_zone_id, $end_date, $libraries, $page_number, $page_size)

Return a user's reading session history

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$start_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$time_zone_id = "time_zone_id_example"; // string | 
$end_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$libraries = array(56); // int[] | 
$page_number = 56; // int | 
$page_size = 56; // int | 

try {
    $result = $apiInstance->apiStatsReadingHistoryGet($start_date, $time_zone_id, $end_date, $libraries, $page_number, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsReadingHistoryGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start_date** | **\DateTime**|  | [optional]
 **time_zone_id** | **string**|  | [optional]
 **end_date** | **\DateTime**|  | [optional]
 **libraries** | [**int[]**](../Model/int.md)|  | [optional]
 **page_number** | **int**|  | [optional]
 **page_size** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ReadingHistoryItemDto[]**](../Model/ReadingHistoryItemDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsReadingHistorySeriesSeriesIdGet**
> \Pbxg33k\KavitaClient\Model\ReadingHistoryItemDto[] apiStatsReadingHistorySeriesSeriesIdGet($series_id, $tz_id, $page_number, $page_size)

Return the authenticated users reading session history for a given series

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 
$tz_id = "tz_id_example"; // string | 
$page_number = 56; // int | 
$page_size = 56; // int | 

try {
    $result = $apiInstance->apiStatsReadingHistorySeriesSeriesIdGet($series_id, $tz_id, $page_number, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsReadingHistorySeriesSeriesIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  |
 **tz_id** | **string**|  | [optional]
 **page_number** | **int**|  | [optional]
 **page_size** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ReadingHistoryItemDto[]**](../Model/ReadingHistoryItemDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsReadingPaceGet**
> \Pbxg33k\KavitaClient\Model\ReadingPaceDto apiStatsReadingPaceGet($start_date, $time_zone_id, $end_date, $libraries, $user_id, $year, $books_only)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$start_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$time_zone_id = "time_zone_id_example"; // string | 
$end_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$libraries = array(56); // int[] | 
$user_id = 56; // int | 
$year = 56; // int | 
$books_only = true; // bool | This API only returns for Books (epub/pdf) and Comics (Image/Archive) regardless of Library type

try {
    $result = $apiInstance->apiStatsReadingPaceGet($start_date, $time_zone_id, $end_date, $libraries, $user_id, $year, $books_only);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsReadingPaceGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start_date** | **\DateTime**|  | [optional]
 **time_zone_id** | **string**|  | [optional]
 **end_date** | **\DateTime**|  | [optional]
 **libraries** | [**int[]**](../Model/int.md)|  | [optional]
 **user_id** | **int**|  | [optional]
 **year** | **int**|  | [optional]
 **books_only** | **bool**| This API only returns for Books (epub/pdf) and Comics (Image/Archive) regardless of Library type | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ReadingPaceDto**](../Model/ReadingPaceDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsReadsByMonthGet**
> \Pbxg33k\KavitaClient\Model\YearMonthGroupingDtoStatCount[] apiStatsReadsByMonthGet($start_date, $time_zone_id, $end_date, $libraries, $user_id)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$start_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$time_zone_id = "time_zone_id_example"; // string | 
$end_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$libraries = array(56); // int[] | 
$user_id = 56; // int | 

try {
    $result = $apiInstance->apiStatsReadsByMonthGet($start_date, $time_zone_id, $end_date, $libraries, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsReadsByMonthGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start_date** | **\DateTime**|  | [optional]
 **time_zone_id** | **string**|  | [optional]
 **end_date** | **\DateTime**|  | [optional]
 **libraries** | [**int[]**](../Model/int.md)|  | [optional]
 **user_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\YearMonthGroupingDtoStatCount[]**](../Model/YearMonthGroupingDtoStatCount.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsServerCountMangaFormatGet**
> \Pbxg33k\KavitaClient\Model\MangaFormatStatCount[] apiStatsServerCountMangaFormatGet()



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiStatsServerCountMangaFormatGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsServerCountMangaFormatGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\MangaFormatStatCount[]**](../Model/MangaFormatStatCount.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsServerCountPublicationStatusGet**
> \Pbxg33k\KavitaClient\Model\PublicationStatusStatCount[] apiStatsServerCountPublicationStatusGet()



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiStatsServerCountPublicationStatusGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsServerCountPublicationStatusGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\PublicationStatusStatCount[]**](../Model/PublicationStatusStatCount.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsServerFileBreakdownGet**
> \Pbxg33k\KavitaClient\Model\FileExtensionBreakdownDto[] apiStatsServerFileBreakdownGet()

A breakdown of different files, their size, and format

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiStatsServerFileBreakdownGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsServerFileBreakdownGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\FileExtensionBreakdownDto[]**](../Model/FileExtensionBreakdownDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsServerFileExtensionGet**
> apiStatsServerFileExtensionGet($file_extension)

Generates a csv of all file paths for a given extension

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file_extension = "file_extension_example"; // string | 

try {
    $apiInstance->apiStatsServerFileExtensionGet($file_extension);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsServerFileExtensionGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file_extension** | **string**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsServerStatsGet**
> \Pbxg33k\KavitaClient\Model\ServerStatisticsDto apiStatsServerStatsGet()



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiStatsServerStatsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsServerStatsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\ServerStatisticsDto**](../Model/ServerStatisticsDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsTagBreakdownGet**
> \Pbxg33k\KavitaClient\Model\StringBreakDownDto apiStatsTagBreakdownGet($start_date, $time_zone_id, $end_date, $libraries, $user_id)

Returns top 10 tags that user likes reading

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$start_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$time_zone_id = "time_zone_id_example"; // string | 
$end_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$libraries = array(56); // int[] | 
$user_id = 56; // int | 

try {
    $result = $apiInstance->apiStatsTagBreakdownGet($start_date, $time_zone_id, $end_date, $libraries, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsTagBreakdownGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start_date** | **\DateTime**|  | [optional]
 **time_zone_id** | **string**|  | [optional]
 **end_date** | **\DateTime**|  | [optional]
 **libraries** | [**int[]**](../Model/int.md)|  | [optional]
 **user_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\StringBreakDownDto**](../Model/StringBreakDownDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsTotalReadsGet**
> int apiStatsTotalReadsGet($user_id)

Returns the total amount reads in the given filter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 56; // int | 

try {
    $result = $apiInstance->apiStatsTotalReadsGet($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsTotalReadsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **int**|  | [optional]

### Return type

**int**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsUserReadGet**
> \Pbxg33k\KavitaClient\Model\UserReadStatistics apiStatsUserReadGet($user_id)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 56; // int | 

try {
    $result = $apiInstance->apiStatsUserReadGet($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsUserReadGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\UserReadStatistics**](../Model/UserReadStatistics.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsUserStatsGet**
> \Pbxg33k\KavitaClient\Model\ProfileStatBarDto apiStatsUserStatsGet($start_date, $time_zone_id, $end_date, $libraries, $user_id)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$start_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$time_zone_id = "time_zone_id_example"; // string | 
$end_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$libraries = array(56); // int[] | 
$user_id = 56; // int | 

try {
    $result = $apiInstance->apiStatsUserStatsGet($start_date, $time_zone_id, $end_date, $libraries, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsUserStatsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start_date** | **\DateTime**|  | [optional]
 **time_zone_id** | **string**|  | [optional]
 **end_date** | **\DateTime**|  | [optional]
 **libraries** | [**int[]**](../Model/int.md)|  | [optional]
 **user_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ProfileStatBarDto**](../Model/ProfileStatBarDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsWordSpreadGet**
> \Pbxg33k\KavitaClient\Model\SpreadStatsDto apiStatsWordSpreadGet($start_date, $time_zone_id, $end_date, $libraries, $user_id)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$start_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$time_zone_id = "time_zone_id_example"; // string | 
$end_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$libraries = array(56); // int[] | 
$user_id = 56; // int | 

try {
    $result = $apiInstance->apiStatsWordSpreadGet($start_date, $time_zone_id, $end_date, $libraries, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsWordSpreadGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start_date** | **\DateTime**|  | [optional]
 **time_zone_id** | **string**|  | [optional]
 **end_date** | **\DateTime**|  | [optional]
 **libraries** | [**int[]**](../Model/int.md)|  | [optional]
 **user_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\SpreadStatsDto**](../Model/SpreadStatsDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStatsWordsPerYearGet**
> \Pbxg33k\KavitaClient\Model\Int32StatCount[] apiStatsWordsPerYearGet($user_id)

Returns a count of words read per year for a given userId.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 56; // int | 

try {
    $result = $apiInstance->apiStatsWordsPerYearGet($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->apiStatsWordsPerYearGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\Int32StatCount[]**](../Model/Int32StatCount.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

