# Pbxg33k\KavitaClient\BookApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiBookChapterIdBookInfoGet**](BookApi.md#apibookchapteridbookinfoget) | **GET** /api/Book/{chapterId}/book-info | Retrieves information for the PDF and Epub reader. This will cache the file.
[**apiBookChapterIdBookPageGet**](BookApi.md#apibookchapteridbookpageget) | **GET** /api/Book/{chapterId}/book-page | This returns a single page within the epub book. All html will be rewritten to be scoped within our reader, all css is scoped, etc.
[**apiBookChapterIdBookResourcesGet**](BookApi.md#apibookchapteridbookresourcesget) | **GET** /api/Book/{chapterId}/book-resources | This is an entry point to fetch resources from within an epub chapter/book.
[**apiBookChapterIdChaptersGet**](BookApi.md#apibookchapteridchaptersget) | **GET** /api/Book/{chapterId}/chapters | This will return a list of mappings from ID -&gt; page num. ID will be the xhtml key and page num will be the reading order this is used to rewrite anchors in the book text so that we always load properly in our reader.

# **apiBookChapterIdBookInfoGet**
> \Pbxg33k\KavitaClient\Model\BookInfoDto apiBookChapterIdBookInfoGet($chapter_id)

Retrieves information for the PDF and Epub reader. This will cache the file.

This only applies to Epub or PDF files

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\BookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 

try {
    $result = $apiInstance->apiBookChapterIdBookInfoGet($chapter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BookApi->apiBookChapterIdBookInfoGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  |

### Return type

[**\Pbxg33k\KavitaClient\Model\BookInfoDto**](../Model/BookInfoDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiBookChapterIdBookPageGet**
> string apiBookChapterIdBookPageGet($chapter_id, $page)

This returns a single page within the epub book. All html will be rewritten to be scoped within our reader, all css is scoped, etc.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\BookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 
$page = 56; // int | 

try {
    $result = $apiInstance->apiBookChapterIdBookPageGet($chapter_id, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BookApi->apiBookChapterIdBookPageGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  |
 **page** | **int**|  | [optional]

### Return type

**string**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiBookChapterIdBookResourcesGet**
> apiBookChapterIdBookResourcesGet($chapter_id, $file)

This is an entry point to fetch resources from within an epub chapter/book.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\BookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 
$file = "file_example"; // string | 

try {
    $apiInstance->apiBookChapterIdBookResourcesGet($chapter_id, $file);
} catch (Exception $e) {
    echo 'Exception when calling BookApi->apiBookChapterIdBookResourcesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  |
 **file** | **string**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiBookChapterIdChaptersGet**
> \Pbxg33k\KavitaClient\Model\BookChapterItem[] apiBookChapterIdChaptersGet($chapter_id)

This will return a list of mappings from ID -> page num. ID will be the xhtml key and page num will be the reading order this is used to rewrite anchors in the book text so that we always load properly in our reader.

This is essentially building the table of contents

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\BookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 

try {
    $result = $apiInstance->apiBookChapterIdChaptersGet($chapter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BookApi->apiBookChapterIdChaptersGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  |

### Return type

[**\Pbxg33k\KavitaClient\Model\BookChapterItem[]**](../Model/BookChapterItem.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

