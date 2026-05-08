# Pbxg33k\KavitaClient\StreamApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiStreamAddDashboardStreamPost**](StreamApi.md#apistreamadddashboardstreampost) | **POST** /api/Stream/add-dashboard-stream | Creates a Dashboard Stream from a SmartFilter and adds it to the user&#x27;s dashboard as visible
[**apiStreamAddSidenavStreamFromExternalSourcePost**](StreamApi.md#apistreamaddsidenavstreamfromexternalsourcepost) | **POST** /api/Stream/add-sidenav-stream-from-external-source | Creates a SideNav Stream from a SmartFilter and adds it to the user&#x27;s sidenav as visible
[**apiStreamAddSidenavStreamPost**](StreamApi.md#apistreamaddsidenavstreampost) | **POST** /api/Stream/add-sidenav-stream | Creates a SideNav Stream from a SmartFilter and adds it to the user&#x27;s sidenav as visible
[**apiStreamBulkSidenavStreamVisibilityPost**](StreamApi.md#apistreambulksidenavstreamvisibilitypost) | **POST** /api/Stream/bulk-sidenav-stream-visibility | 
[**apiStreamCreateExternalSourcePost**](StreamApi.md#apistreamcreateexternalsourcepost) | **POST** /api/Stream/create-external-source | Create an external Source
[**apiStreamDashboardGet**](StreamApi.md#apistreamdashboardget) | **GET** /api/Stream/dashboard | Returns the layout of the user&#x27;s dashboard
[**apiStreamDeleteExternalSourceDelete**](StreamApi.md#apistreamdeleteexternalsourcedelete) | **DELETE** /api/Stream/delete-external-source | Delete&#x27;s the external source
[**apiStreamExternalSourceExistsPost**](StreamApi.md#apistreamexternalsourceexistspost) | **POST** /api/Stream/external-source-exists | Validates the external source by host is unique (for this user)
[**apiStreamExternalSourcesGet**](StreamApi.md#apistreamexternalsourcesget) | **GET** /api/Stream/external-sources | Return&#x27;s the user&#x27;s external sources
[**apiStreamSidenavGet**](StreamApi.md#apistreamsidenavget) | **GET** /api/Stream/sidenav | Return&#x27;s the user&#x27;s side nav
[**apiStreamSmartFilterDashboardStreamDelete**](StreamApi.md#apistreamsmartfilterdashboardstreamdelete) | **DELETE** /api/Stream/smart-filter-dashboard-stream | Removes a Smart Filter from a user&#x27;s Dashboard Streams
[**apiStreamSmartFilterSideNavStreamDelete**](StreamApi.md#apistreamsmartfiltersidenavstreamdelete) | **DELETE** /api/Stream/smart-filter-side-nav-stream | Removes a Smart Filter from a user&#x27;s SideNav Streams
[**apiStreamUpdateDashboardPositionPost**](StreamApi.md#apistreamupdatedashboardpositionpost) | **POST** /api/Stream/update-dashboard-position | Updates the position of a dashboard stream
[**apiStreamUpdateDashboardStreamPost**](StreamApi.md#apistreamupdatedashboardstreampost) | **POST** /api/Stream/update-dashboard-stream | Updates the visibility of a dashboard stream
[**apiStreamUpdateExternalSourcePost**](StreamApi.md#apistreamupdateexternalsourcepost) | **POST** /api/Stream/update-external-source | Updates an existing external source
[**apiStreamUpdateSidenavPositionPost**](StreamApi.md#apistreamupdatesidenavpositionpost) | **POST** /api/Stream/update-sidenav-position | Updates the position of a dashboard stream
[**apiStreamUpdateSidenavStreamPost**](StreamApi.md#apistreamupdatesidenavstreampost) | **POST** /api/Stream/update-sidenav-stream | Updates the visibility of a dashboard stream

# **apiStreamAddDashboardStreamPost**
> \Pbxg33k\KavitaClient\Model\DashboardStreamDto apiStreamAddDashboardStreamPost($smart_filter_id)

Creates a Dashboard Stream from a SmartFilter and adds it to the user's dashboard as visible

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StreamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$smart_filter_id = 56; // int | 

try {
    $result = $apiInstance->apiStreamAddDashboardStreamPost($smart_filter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StreamApi->apiStreamAddDashboardStreamPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **smart_filter_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\DashboardStreamDto**](../Model/DashboardStreamDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStreamAddSidenavStreamFromExternalSourcePost**
> \Pbxg33k\KavitaClient\Model\SideNavStreamDto apiStreamAddSidenavStreamFromExternalSourcePost($external_source_id)

Creates a SideNav Stream from a SmartFilter and adds it to the user's sidenav as visible

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StreamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$external_source_id = 56; // int | 

try {
    $result = $apiInstance->apiStreamAddSidenavStreamFromExternalSourcePost($external_source_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StreamApi->apiStreamAddSidenavStreamFromExternalSourcePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **external_source_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\SideNavStreamDto**](../Model/SideNavStreamDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStreamAddSidenavStreamPost**
> \Pbxg33k\KavitaClient\Model\SideNavStreamDto apiStreamAddSidenavStreamPost($smart_filter_id)

Creates a SideNav Stream from a SmartFilter and adds it to the user's sidenav as visible

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StreamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$smart_filter_id = 56; // int | 

try {
    $result = $apiInstance->apiStreamAddSidenavStreamPost($smart_filter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StreamApi->apiStreamAddSidenavStreamPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **smart_filter_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\SideNavStreamDto**](../Model/SideNavStreamDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStreamBulkSidenavStreamVisibilityPost**
> apiStreamBulkSidenavStreamVisibilityPost($body)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StreamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\BulkUpdateSideNavStreamVisibilityDto(); // \Pbxg33k\KavitaClient\Model\BulkUpdateSideNavStreamVisibilityDto | 

try {
    $apiInstance->apiStreamBulkSidenavStreamVisibilityPost($body);
} catch (Exception $e) {
    echo 'Exception when calling StreamApi->apiStreamBulkSidenavStreamVisibilityPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\BulkUpdateSideNavStreamVisibilityDto**](../Model/BulkUpdateSideNavStreamVisibilityDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStreamCreateExternalSourcePost**
> \Pbxg33k\KavitaClient\Model\ExternalSourceDto apiStreamCreateExternalSourcePost($body)

Create an external Source

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StreamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\ExternalSourceDto(); // \Pbxg33k\KavitaClient\Model\ExternalSourceDto | 

try {
    $result = $apiInstance->apiStreamCreateExternalSourcePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StreamApi->apiStreamCreateExternalSourcePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\ExternalSourceDto**](../Model/ExternalSourceDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ExternalSourceDto**](../Model/ExternalSourceDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStreamDashboardGet**
> \Pbxg33k\KavitaClient\Model\DashboardStreamDto[] apiStreamDashboardGet($visible_only)

Returns the layout of the user's dashboard

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StreamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$visible_only = true; // bool | 

try {
    $result = $apiInstance->apiStreamDashboardGet($visible_only);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StreamApi->apiStreamDashboardGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **visible_only** | **bool**|  | [optional] [default to true]

### Return type

[**\Pbxg33k\KavitaClient\Model\DashboardStreamDto[]**](../Model/DashboardStreamDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStreamDeleteExternalSourceDelete**
> apiStreamDeleteExternalSourceDelete($external_source_id)

Delete's the external source

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StreamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$external_source_id = 56; // int | 

try {
    $apiInstance->apiStreamDeleteExternalSourceDelete($external_source_id);
} catch (Exception $e) {
    echo 'Exception when calling StreamApi->apiStreamDeleteExternalSourceDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **external_source_id** | **int**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStreamExternalSourceExistsPost**
> bool apiStreamExternalSourceExistsPost($body)

Validates the external source by host is unique (for this user)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StreamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\ExternalSourceDto(); // \Pbxg33k\KavitaClient\Model\ExternalSourceDto | 

try {
    $result = $apiInstance->apiStreamExternalSourceExistsPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StreamApi->apiStreamExternalSourceExistsPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\ExternalSourceDto**](../Model/ExternalSourceDto.md)|  | [optional]

### Return type

**bool**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStreamExternalSourcesGet**
> \Pbxg33k\KavitaClient\Model\ExternalSourceDto[] apiStreamExternalSourcesGet()

Return's the user's external sources

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StreamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiStreamExternalSourcesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StreamApi->apiStreamExternalSourcesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\ExternalSourceDto[]**](../Model/ExternalSourceDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStreamSidenavGet**
> \Pbxg33k\KavitaClient\Model\SideNavStreamDto[] apiStreamSidenavGet($visible_only)

Return's the user's side nav

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StreamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$visible_only = true; // bool | 

try {
    $result = $apiInstance->apiStreamSidenavGet($visible_only);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StreamApi->apiStreamSidenavGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **visible_only** | **bool**|  | [optional] [default to true]

### Return type

[**\Pbxg33k\KavitaClient\Model\SideNavStreamDto[]**](../Model/SideNavStreamDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStreamSmartFilterDashboardStreamDelete**
> apiStreamSmartFilterDashboardStreamDelete($dashboard_stream_id)

Removes a Smart Filter from a user's Dashboard Streams

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StreamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$dashboard_stream_id = 56; // int | 

try {
    $apiInstance->apiStreamSmartFilterDashboardStreamDelete($dashboard_stream_id);
} catch (Exception $e) {
    echo 'Exception when calling StreamApi->apiStreamSmartFilterDashboardStreamDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **dashboard_stream_id** | **int**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStreamSmartFilterSideNavStreamDelete**
> apiStreamSmartFilterSideNavStreamDelete($side_nav_stream_id)

Removes a Smart Filter from a user's SideNav Streams

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StreamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$side_nav_stream_id = 56; // int | 

try {
    $apiInstance->apiStreamSmartFilterSideNavStreamDelete($side_nav_stream_id);
} catch (Exception $e) {
    echo 'Exception when calling StreamApi->apiStreamSmartFilterSideNavStreamDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **side_nav_stream_id** | **int**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStreamUpdateDashboardPositionPost**
> apiStreamUpdateDashboardPositionPost($body)

Updates the position of a dashboard stream

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StreamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateStreamPositionDto(); // \Pbxg33k\KavitaClient\Model\UpdateStreamPositionDto | 

try {
    $apiInstance->apiStreamUpdateDashboardPositionPost($body);
} catch (Exception $e) {
    echo 'Exception when calling StreamApi->apiStreamUpdateDashboardPositionPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateStreamPositionDto**](../Model/UpdateStreamPositionDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStreamUpdateDashboardStreamPost**
> apiStreamUpdateDashboardStreamPost($body)

Updates the visibility of a dashboard stream

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StreamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\DashboardStreamDto(); // \Pbxg33k\KavitaClient\Model\DashboardStreamDto | 

try {
    $apiInstance->apiStreamUpdateDashboardStreamPost($body);
} catch (Exception $e) {
    echo 'Exception when calling StreamApi->apiStreamUpdateDashboardStreamPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\DashboardStreamDto**](../Model/DashboardStreamDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStreamUpdateExternalSourcePost**
> \Pbxg33k\KavitaClient\Model\ExternalSourceDto apiStreamUpdateExternalSourcePost($body)

Updates an existing external source

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StreamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\ExternalSourceDto(); // \Pbxg33k\KavitaClient\Model\ExternalSourceDto | 

try {
    $result = $apiInstance->apiStreamUpdateExternalSourcePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StreamApi->apiStreamUpdateExternalSourcePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\ExternalSourceDto**](../Model/ExternalSourceDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ExternalSourceDto**](../Model/ExternalSourceDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStreamUpdateSidenavPositionPost**
> apiStreamUpdateSidenavPositionPost($body)

Updates the position of a dashboard stream

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StreamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateStreamPositionDto(); // \Pbxg33k\KavitaClient\Model\UpdateStreamPositionDto | 

try {
    $apiInstance->apiStreamUpdateSidenavPositionPost($body);
} catch (Exception $e) {
    echo 'Exception when calling StreamApi->apiStreamUpdateSidenavPositionPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateStreamPositionDto**](../Model/UpdateStreamPositionDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiStreamUpdateSidenavStreamPost**
> apiStreamUpdateSidenavStreamPost($body)

Updates the visibility of a dashboard stream

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\StreamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\SideNavStreamDto(); // \Pbxg33k\KavitaClient\Model\SideNavStreamDto | 

try {
    $apiInstance->apiStreamUpdateSidenavStreamPost($body);
} catch (Exception $e) {
    echo 'Exception when calling StreamApi->apiStreamUpdateSidenavStreamPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\SideNavStreamDto**](../Model/SideNavStreamDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

