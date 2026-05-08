# Pbxg33k\KavitaClient\EmailApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiEmailAllGet**](EmailApi.md#apiemailallget) | **GET** /api/Email/all | 

# **apiEmailAllGet**
> \Pbxg33k\KavitaClient\Model\EmailHistoryDto[] apiEmailAllGet()



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\EmailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiEmailAllGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailApi->apiEmailAllGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\EmailHistoryDto[]**](../Model/EmailHistoryDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

