# Pbxg33k\KavitaClient\ReviewApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiReviewAllGet**](ReviewApi.md#apireviewallget) | **GET** /api/Review/all | Returns all reviews for the user. If you are authenticated as the user, will always return data, regardless of ShareReviews setting
[**apiReviewChapterDelete**](ReviewApi.md#apireviewchapterdelete) | **DELETE** /api/Review/chapter | Deletes the user&#x27;s review for the given chapter
[**apiReviewChapterPost**](ReviewApi.md#apireviewchapterpost) | **POST** /api/Review/chapter | Update the user&#x27;s review for a given chapter
[**apiReviewSeriesDelete**](ReviewApi.md#apireviewseriesdelete) | **DELETE** /api/Review/series | Deletes the user&#x27;s review for the given series
[**apiReviewSeriesPost**](ReviewApi.md#apireviewseriespost) | **POST** /api/Review/series | Updates the user&#x27;s review for a given series

# **apiReviewAllGet**
> \Pbxg33k\KavitaClient\Model\UserReviewExtendedDto[] apiReviewAllGet($user_id, $rating, $filter_query)

Returns all reviews for the user. If you are authenticated as the user, will always return data, regardless of ShareReviews setting

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReviewApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 56; // int | User to load, if your own, will bypass RBS and ShareReviews restrictions
$rating = 3.4; // float | Null to ignore filtering. >= rating
$filter_query = "filter_query_example"; // string | Null to ignore filtering on Series name

try {
    $result = $apiInstance->apiReviewAllGet($user_id, $rating, $filter_query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReviewApi->apiReviewAllGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **int**| User to load, if your own, will bypass RBS and ShareReviews restrictions | [optional]
 **rating** | **float**| Null to ignore filtering. &gt;&#x3D; rating | [optional]
 **filter_query** | **string**| Null to ignore filtering on Series name | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\UserReviewExtendedDto[]**](../Model/UserReviewExtendedDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReviewChapterDelete**
> apiReviewChapterDelete($chapter_id)

Deletes the user's review for the given chapter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReviewApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 

try {
    $apiInstance->apiReviewChapterDelete($chapter_id);
} catch (Exception $e) {
    echo 'Exception when calling ReviewApi->apiReviewChapterDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReviewChapterPost**
> \Pbxg33k\KavitaClient\Model\UserReviewDto apiReviewChapterPost($body)

Update the user's review for a given chapter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReviewApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateUserReviewDto(); // \Pbxg33k\KavitaClient\Model\UpdateUserReviewDto | chapterId must be set

try {
    $result = $apiInstance->apiReviewChapterPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReviewApi->apiReviewChapterPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateUserReviewDto**](../Model/UpdateUserReviewDto.md)| chapterId must be set | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\UserReviewDto**](../Model/UserReviewDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReviewSeriesDelete**
> apiReviewSeriesDelete($series_id)

Deletes the user's review for the given series

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReviewApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $apiInstance->apiReviewSeriesDelete($series_id);
} catch (Exception $e) {
    echo 'Exception when calling ReviewApi->apiReviewSeriesDelete: ', $e->getMessage(), PHP_EOL;
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

# **apiReviewSeriesPost**
> \Pbxg33k\KavitaClient\Model\UserReviewDto apiReviewSeriesPost($body)

Updates the user's review for a given series

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReviewApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateUserReviewDto(); // \Pbxg33k\KavitaClient\Model\UpdateUserReviewDto | 

try {
    $result = $apiInstance->apiReviewSeriesPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReviewApi->apiReviewSeriesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateUserReviewDto**](../Model/UpdateUserReviewDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\UserReviewDto**](../Model/UserReviewDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

