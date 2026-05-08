# Pbxg33k\KavitaClient\ManageApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiManageSeriesMetadataPost**](ManageApi.md#apimanageseriesmetadatapost) | **POST** /api/Manage/series-metadata | Returns a list of all Series that is Kavita+ applicable to metadata match and the status of it

# **apiManageSeriesMetadataPost**
> \Pbxg33k\KavitaClient\Model\ManageMatchSeriesDto[] apiManageSeriesMetadataPost($body, $page_number, $page_size)

Returns a list of all Series that is Kavita+ applicable to metadata match and the status of it

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ManageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\ManageMatchFilterDto(); // \Pbxg33k\KavitaClient\Model\ManageMatchFilterDto | 
$page_number = 56; // int | 
$page_size = 56; // int | 

try {
    $result = $apiInstance->apiManageSeriesMetadataPost($body, $page_number, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ManageApi->apiManageSeriesMetadataPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\ManageMatchFilterDto**](../Model/ManageMatchFilterDto.md)|  | [optional]
 **page_number** | **int**|  | [optional]
 **page_size** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ManageMatchSeriesDto[]**](../Model/ManageMatchSeriesDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

