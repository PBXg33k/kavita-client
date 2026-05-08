# Pbxg33k\KavitaClient\TachiyomiApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiTachiyomiLatestChapterGet**](TachiyomiApi.md#apitachiyomilatestchapterget) | **GET** /api/Tachiyomi/latest-chapter | Given the series Id, this should return the latest chapter that has been fully read.
[**apiTachiyomiMarkChapterUntilAsReadPost**](TachiyomiApi.md#apitachiyomimarkchapteruntilasreadpost) | **POST** /api/Tachiyomi/mark-chapter-until-as-read | Marks every chapter that is sorted below the passed number as Read. This will not mark any specials as read.

# **apiTachiyomiLatestChapterGet**
> \Pbxg33k\KavitaClient\Model\TachiyomiChapterDto apiTachiyomiLatestChapterGet($series_id)

Given the series Id, this should return the latest chapter that has been fully read.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\TachiyomiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $result = $apiInstance->apiTachiyomiLatestChapterGet($series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TachiyomiApi->apiTachiyomiLatestChapterGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\TachiyomiChapterDto**](../Model/TachiyomiChapterDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiTachiyomiMarkChapterUntilAsReadPost**
> bool apiTachiyomiMarkChapterUntilAsReadPost($series_id, $chapter_number, $generate_reading_sessions)

Marks every chapter that is sorted below the passed number as Read. This will not mark any specials as read.

This is built for Tachiyomi and is not expected to be called by any other place

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\TachiyomiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 
$chapter_number = 3.4; // float | 
$generate_reading_sessions = true; // bool | 

try {
    $result = $apiInstance->apiTachiyomiMarkChapterUntilAsReadPost($series_id, $chapter_number, $generate_reading_sessions);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TachiyomiApi->apiTachiyomiMarkChapterUntilAsReadPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]
 **chapter_number** | **float**|  | [optional]
 **generate_reading_sessions** | **bool**|  | [optional] [default to true]

### Return type

**bool**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

