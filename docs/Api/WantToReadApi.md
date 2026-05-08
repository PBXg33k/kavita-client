# Pbxg33k\KavitaClient\WantToReadApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiWantToReadAddSeriesPost**](WantToReadApi.md#apiwanttoreadaddseriespost) | **POST** /api/want-to-read/add-series | Given a list of Series Ids, add them to the current logged in user&#x27;s Want To Read list
[**apiWantToReadGet**](WantToReadApi.md#apiwanttoreadget) | **GET** /api/want-to-read | 
[**apiWantToReadRemoveSeriesPost**](WantToReadApi.md#apiwanttoreadremoveseriespost) | **POST** /api/want-to-read/remove-series | Given a list of Series Ids, remove them from the current logged in user&#x27;s Want To Read list
[**apiWantToReadV2Post**](WantToReadApi.md#apiwanttoreadv2post) | **POST** /api/want-to-read/v2 | Return all Series that are in the current logged in user&#x27;s Want to Read list, filtered

# **apiWantToReadAddSeriesPost**
> apiWantToReadAddSeriesPost($body)

Given a list of Series Ids, add them to the current logged in user's Want To Read list

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\WantToReadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateWantToReadDto(); // \Pbxg33k\KavitaClient\Model\UpdateWantToReadDto | 

try {
    $apiInstance->apiWantToReadAddSeriesPost($body);
} catch (Exception $e) {
    echo 'Exception when calling WantToReadApi->apiWantToReadAddSeriesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateWantToReadDto**](../Model/UpdateWantToReadDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiWantToReadGet**
> bool apiWantToReadGet($series_id)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\WantToReadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $result = $apiInstance->apiWantToReadGet($series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WantToReadApi->apiWantToReadGet: ', $e->getMessage(), PHP_EOL;
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

# **apiWantToReadRemoveSeriesPost**
> apiWantToReadRemoveSeriesPost($body)

Given a list of Series Ids, remove them from the current logged in user's Want To Read list

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\WantToReadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateWantToReadDto(); // \Pbxg33k\KavitaClient\Model\UpdateWantToReadDto | 

try {
    $apiInstance->apiWantToReadRemoveSeriesPost($body);
} catch (Exception $e) {
    echo 'Exception when calling WantToReadApi->apiWantToReadRemoveSeriesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateWantToReadDto**](../Model/UpdateWantToReadDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiWantToReadV2Post**
> \Pbxg33k\KavitaClient\Model\SeriesDto[] apiWantToReadV2Post($body, $page_number, $page_size, $user_id)

Return all Series that are in the current logged in user's Want to Read list, filtered

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\WantToReadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\SeriesFilterV2Dto(); // \Pbxg33k\KavitaClient\Model\SeriesFilterV2Dto | 
$page_number = 56; // int | 
$page_size = 56; // int | 
$user_id = 56; // int | Optional user id to request the OnDeck for someone else. They must have profile sharing enabled when doing so

try {
    $result = $apiInstance->apiWantToReadV2Post($body, $page_number, $page_size, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WantToReadApi->apiWantToReadV2Post: ', $e->getMessage(), PHP_EOL;
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

### Return type

[**\Pbxg33k\KavitaClient\Model\SeriesDto[]**](../Model/SeriesDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

