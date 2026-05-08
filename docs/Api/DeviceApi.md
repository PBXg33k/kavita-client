# Pbxg33k\KavitaClient\DeviceApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiDeviceClientAllDevicesGet**](DeviceApi.md#apideviceclientalldevicesget) | **GET** /api/Device/client/all-devices | Get All user client devices
[**apiDeviceClientDeviceDelete**](DeviceApi.md#apideviceclientdevicedelete) | **DELETE** /api/Device/client/device | Removes the client device from DB
[**apiDeviceClientDevicesGet**](DeviceApi.md#apideviceclientdevicesget) | **GET** /api/Device/client/devices | Get my client devices
[**apiDeviceClientUpdateNamePost**](DeviceApi.md#apideviceclientupdatenamepost) | **POST** /api/Device/client/update-name | Update the friendly name of the Device
[**apiDeviceCreatePost**](DeviceApi.md#apidevicecreatepost) | **POST** /api/Device/create | Creates a new Device
[**apiDeviceDelete**](DeviceApi.md#apidevicedelete) | **DELETE** /api/Device | Deletes the device from the user
[**apiDeviceGet**](DeviceApi.md#apideviceget) | **GET** /api/Device | 
[**apiDeviceSendSeriesToPost**](DeviceApi.md#apidevicesendseriestopost) | **POST** /api/Device/send-series-to | Attempts to send a whole series to a device.
[**apiDeviceSendToPost**](DeviceApi.md#apidevicesendtopost) | **POST** /api/Device/send-to | Sends a collection of chapters to the user&#x27;s device
[**apiDeviceUpdatePost**](DeviceApi.md#apideviceupdatepost) | **POST** /api/Device/update | Updates an existing Device

# **apiDeviceClientAllDevicesGet**
> \Pbxg33k\KavitaClient\Model\ClientDeviceDto[] apiDeviceClientAllDevicesGet($include_inactive)

Get All user client devices

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$include_inactive = false; // bool | 

try {
    $result = $apiInstance->apiDeviceClientAllDevicesGet($include_inactive);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->apiDeviceClientAllDevicesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **include_inactive** | **bool**|  | [optional] [default to false]

### Return type

[**\Pbxg33k\KavitaClient\Model\ClientDeviceDto[]**](../Model/ClientDeviceDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiDeviceClientDeviceDelete**
> bool apiDeviceClientDeviceDelete($client_device_id)

Removes the client device from DB

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$client_device_id = 56; // int | 

try {
    $result = $apiInstance->apiDeviceClientDeviceDelete($client_device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->apiDeviceClientDeviceDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client_device_id** | **int**|  | [optional]

### Return type

**bool**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiDeviceClientDevicesGet**
> \Pbxg33k\KavitaClient\Model\ClientDeviceDto[] apiDeviceClientDevicesGet($include_inactive)

Get my client devices

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$include_inactive = false; // bool | 

try {
    $result = $apiInstance->apiDeviceClientDevicesGet($include_inactive);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->apiDeviceClientDevicesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **include_inactive** | **bool**|  | [optional] [default to false]

### Return type

[**\Pbxg33k\KavitaClient\Model\ClientDeviceDto[]**](../Model/ClientDeviceDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiDeviceClientUpdateNamePost**
> apiDeviceClientUpdateNamePost($body)

Update the friendly name of the Device

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateClientDeviceNameDto(); // \Pbxg33k\KavitaClient\Model\UpdateClientDeviceNameDto | 

try {
    $apiInstance->apiDeviceClientUpdateNamePost($body);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->apiDeviceClientUpdateNamePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateClientDeviceNameDto**](../Model/UpdateClientDeviceNameDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiDeviceCreatePost**
> \Pbxg33k\KavitaClient\Model\EmailDeviceDto apiDeviceCreatePost($body)

Creates a new Device

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\CreateEmailDeviceDto(); // \Pbxg33k\KavitaClient\Model\CreateEmailDeviceDto | 

try {
    $result = $apiInstance->apiDeviceCreatePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->apiDeviceCreatePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\CreateEmailDeviceDto**](../Model/CreateEmailDeviceDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\EmailDeviceDto**](../Model/EmailDeviceDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiDeviceDelete**
> apiDeviceDelete($device_id)

Deletes the device from the user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$device_id = 56; // int | 

try {
    $apiInstance->apiDeviceDelete($device_id);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->apiDeviceDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **device_id** | **int**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiDeviceGet**
> \Pbxg33k\KavitaClient\Model\EmailDeviceDto[] apiDeviceGet()



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiDeviceGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->apiDeviceGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\EmailDeviceDto[]**](../Model/EmailDeviceDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiDeviceSendSeriesToPost**
> apiDeviceSendSeriesToPost($body)

Attempts to send a whole series to a device.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\SendSeriesToEmailDeviceDto(); // \Pbxg33k\KavitaClient\Model\SendSeriesToEmailDeviceDto | 

try {
    $apiInstance->apiDeviceSendSeriesToPost($body);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->apiDeviceSendSeriesToPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\SendSeriesToEmailDeviceDto**](../Model/SendSeriesToEmailDeviceDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiDeviceSendToPost**
> apiDeviceSendToPost($body)

Sends a collection of chapters to the user's device

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\SendToEmailDeviceDto(); // \Pbxg33k\KavitaClient\Model\SendToEmailDeviceDto | 

try {
    $apiInstance->apiDeviceSendToPost($body);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->apiDeviceSendToPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\SendToEmailDeviceDto**](../Model/SendToEmailDeviceDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiDeviceUpdatePost**
> \Pbxg33k\KavitaClient\Model\EmailDeviceDto apiDeviceUpdatePost($body)

Updates an existing Device

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateEmailDeviceDto(); // \Pbxg33k\KavitaClient\Model\UpdateEmailDeviceDto | 

try {
    $result = $apiInstance->apiDeviceUpdatePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->apiDeviceUpdatePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateEmailDeviceDto**](../Model/UpdateEmailDeviceDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\EmailDeviceDto**](../Model/EmailDeviceDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

