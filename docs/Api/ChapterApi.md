# Pbxg33k\KavitaClient\ChapterApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiChapterChapterDetailPlusGet**](ChapterApi.md#apichapterchapterdetailplusget) | **GET** /api/Chapter/chapter-detail-plus | Returns Ratings and Reviews for an individual Chapter
[**apiChapterDelete**](ChapterApi.md#apichapterdelete) | **DELETE** /api/Chapter | Removes a Chapter
[**apiChapterDeleteMultiplePost**](ChapterApi.md#apichapterdeletemultiplepost) | **POST** /api/Chapter/delete-multiple | Deletes multiple chapters and any volumes with no leftover chapters
[**apiChapterGet**](ChapterApi.md#apichapterget) | **GET** /api/Chapter | Gets a single chapter
[**apiChapterUpdatePost**](ChapterApi.md#apichapterupdatepost) | **POST** /api/Chapter/update | Update chapter metadata

# **apiChapterChapterDetailPlusGet**
> \Pbxg33k\KavitaClient\Model\ChapterDetailPlusDto apiChapterChapterDetailPlusGet($chapter_id)

Returns Ratings and Reviews for an individual Chapter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ChapterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 

try {
    $result = $apiInstance->apiChapterChapterDetailPlusGet($chapter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChapterApi->apiChapterChapterDetailPlusGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ChapterDetailPlusDto**](../Model/ChapterDetailPlusDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiChapterDelete**
> bool apiChapterDelete($chapter_id)

Removes a Chapter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ChapterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 

try {
    $result = $apiInstance->apiChapterDelete($chapter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChapterApi->apiChapterDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  | [optional]

### Return type

**bool**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiChapterDeleteMultiplePost**
> bool apiChapterDeleteMultiplePost($body, $series_id)

Deletes multiple chapters and any volumes with no leftover chapters

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ChapterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\DeleteChaptersDto(); // \Pbxg33k\KavitaClient\Model\DeleteChaptersDto | The IDs of the chapters to be deleted
$series_id = 56; // int | The ID of the series

try {
    $result = $apiInstance->apiChapterDeleteMultiplePost($body, $series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChapterApi->apiChapterDeleteMultiplePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\DeleteChaptersDto**](../Model/DeleteChaptersDto.md)| The IDs of the chapters to be deleted | [optional]
 **series_id** | **int**| The ID of the series | [optional]

### Return type

**bool**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiChapterGet**
> \Pbxg33k\KavitaClient\Model\ChapterDto apiChapterGet($chapter_id)

Gets a single chapter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ChapterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 

try {
    $result = $apiInstance->apiChapterGet($chapter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChapterApi->apiChapterGet: ', $e->getMessage(), PHP_EOL;
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

# **apiChapterUpdatePost**
> apiChapterUpdatePost($body)

Update chapter metadata

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ChapterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateChapterDto(); // \Pbxg33k\KavitaClient\Model\UpdateChapterDto | 

try {
    $apiInstance->apiChapterUpdatePost($body);
} catch (Exception $e) {
    echo 'Exception when calling ChapterApi->apiChapterUpdatePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateChapterDto**](../Model/UpdateChapterDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

