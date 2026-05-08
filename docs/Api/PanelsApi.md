# Pbxg33k\KavitaClient\PanelsApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiPanelsGetProgressGet**](PanelsApi.md#apipanelsgetprogressget) | **GET** /api/Panels/get-progress | Gets the Progress of a given chapter
[**apiPanelsSaveProgressPost**](PanelsApi.md#apipanelssaveprogresspost) | **POST** /api/Panels/save-progress | Saves the progress of a given chapter. This will generate a reading session with the estimated time from the last progress till the current

# **apiPanelsGetProgressGet**
> \Pbxg33k\KavitaClient\Model\ProgressDto apiPanelsGetProgressGet($chapter_id, $api_key)

Gets the Progress of a given chapter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\PanelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 
$api_key = "api_key_example"; // string | 

try {
    $result = $apiInstance->apiPanelsGetProgressGet($chapter_id, $api_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PanelsApi->apiPanelsGetProgressGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  | [optional]
 **api_key** | **string**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ProgressDto**](../Model/ProgressDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiPanelsSaveProgressPost**
> apiPanelsSaveProgressPost($body, $api_key)

Saves the progress of a given chapter. This will generate a reading session with the estimated time from the last progress till the current

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\PanelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\ProgressDto(); // \Pbxg33k\KavitaClient\Model\ProgressDto | 
$api_key = "api_key_example"; // string | 

try {
    $apiInstance->apiPanelsSaveProgressPost($body, $api_key);
} catch (Exception $e) {
    echo 'Exception when calling PanelsApi->apiPanelsSaveProgressPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\ProgressDto**](../Model/ProgressDto.md)|  | [optional]
 **api_key** | **string**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

