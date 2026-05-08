# Pbxg33k\KavitaClient\KoreaderApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiKoreaderApiKeySyncsProgressEbookHashGet**](KoreaderApi.md#apikoreaderapikeysyncsprogressebookhashget) | **GET** /api/Koreader/{apiKey}/syncs/progress/{ebookHash} | Gets book progress from Kavita, if not found will return a 400
[**apiKoreaderApiKeySyncsProgressPut**](KoreaderApi.md#apikoreaderapikeysyncsprogressput) | **PUT** /api/Koreader/{apiKey}/syncs/progress | Syncs book progress with Kavita. Will attempt to save the underlying reader position if possible.
[**apiKoreaderApiKeyUsersAuthGet**](KoreaderApi.md#apikoreaderapikeyusersauthget) | **GET** /api/Koreader/{apiKey}/users/auth | 

# **apiKoreaderApiKeySyncsProgressEbookHashGet**
> apiKoreaderApiKeySyncsProgressEbookHashGet($api_key, $ebook_hash)

Gets book progress from Kavita, if not found will return a 400

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\KoreaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 
$ebook_hash = "ebook_hash_example"; // string | 

try {
    $apiInstance->apiKoreaderApiKeySyncsProgressEbookHashGet($api_key, $ebook_hash);
} catch (Exception $e) {
    echo 'Exception when calling KoreaderApi->apiKoreaderApiKeySyncsProgressEbookHashGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**|  |
 **ebook_hash** | **string**|  |

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiKoreaderApiKeySyncsProgressPut**
> \Pbxg33k\KavitaClient\Model\KoreaderProgressUpdateDto apiKoreaderApiKeySyncsProgressPut($api_key, $body)

Syncs book progress with Kavita. Will attempt to save the underlying reader position if possible.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\KoreaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 
$body = new \Pbxg33k\KavitaClient\Model\KoreaderBookDto(); // \Pbxg33k\KavitaClient\Model\KoreaderBookDto | 

try {
    $result = $apiInstance->apiKoreaderApiKeySyncsProgressPut($api_key, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling KoreaderApi->apiKoreaderApiKeySyncsProgressPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**|  |
 **body** | [**\Pbxg33k\KavitaClient\Model\KoreaderBookDto**](../Model/KoreaderBookDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\KoreaderProgressUpdateDto**](../Model/KoreaderProgressUpdateDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiKoreaderApiKeyUsersAuthGet**
> apiKoreaderApiKeyUsersAuthGet($api_key)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\KoreaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_key = "api_key_example"; // string | 

try {
    $apiInstance->apiKoreaderApiKeyUsersAuthGet($api_key);
} catch (Exception $e) {
    echo 'Exception when calling KoreaderApi->apiKoreaderApiKeyUsersAuthGet: ', $e->getMessage(), PHP_EOL;
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

