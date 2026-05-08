# Pbxg33k\KavitaClient\ThemeApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiThemeBrowseGet**](ThemeApi.md#apithemebrowseget) | **GET** /api/Theme/browse | Browse themes that can be used on this server
[**apiThemeDelete**](ThemeApi.md#apithemedelete) | **DELETE** /api/Theme | Attempts to delete a theme. If already in use by users, will not allow
[**apiThemeDownloadContentGet**](ThemeApi.md#apithemedownloadcontentget) | **GET** /api/Theme/download-content | Returns css content to the UI. UI is expected to escape the content
[**apiThemeDownloadThemePost**](ThemeApi.md#apithemedownloadthemepost) | **POST** /api/Theme/download-theme | Downloads a SiteTheme from upstream
[**apiThemeGet**](ThemeApi.md#apithemeget) | **GET** /api/Theme | 
[**apiThemeUpdateDefaultPost**](ThemeApi.md#apithemeupdatedefaultpost) | **POST** /api/Theme/update-default | 
[**apiThemeUploadThemePost**](ThemeApi.md#apithemeuploadthemepost) | **POST** /api/Theme/upload-theme | Uploads a new theme file

# **apiThemeBrowseGet**
> \Pbxg33k\KavitaClient\Model\DownloadableSiteThemeDto[] apiThemeBrowseGet()

Browse themes that can be used on this server

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ThemeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiThemeBrowseGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ThemeApi->apiThemeBrowseGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\DownloadableSiteThemeDto[]**](../Model/DownloadableSiteThemeDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiThemeDelete**
> \Pbxg33k\KavitaClient\Model\DownloadableSiteThemeDto[] apiThemeDelete($theme_id)

Attempts to delete a theme. If already in use by users, will not allow

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ThemeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$theme_id = 56; // int | 

try {
    $result = $apiInstance->apiThemeDelete($theme_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ThemeApi->apiThemeDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **theme_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\DownloadableSiteThemeDto[]**](../Model/DownloadableSiteThemeDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiThemeDownloadContentGet**
> string apiThemeDownloadContentGet($theme_id)

Returns css content to the UI. UI is expected to escape the content

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ThemeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$theme_id = 56; // int | 

try {
    $result = $apiInstance->apiThemeDownloadContentGet($theme_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ThemeApi->apiThemeDownloadContentGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **theme_id** | **int**|  | [optional]

### Return type

**string**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiThemeDownloadThemePost**
> \Pbxg33k\KavitaClient\Model\SiteThemeDto apiThemeDownloadThemePost($body)

Downloads a SiteTheme from upstream

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ThemeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\DownloadableSiteThemeDto(); // \Pbxg33k\KavitaClient\Model\DownloadableSiteThemeDto | 

try {
    $result = $apiInstance->apiThemeDownloadThemePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ThemeApi->apiThemeDownloadThemePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\DownloadableSiteThemeDto**](../Model/DownloadableSiteThemeDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\SiteThemeDto**](../Model/SiteThemeDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiThemeGet**
> \Pbxg33k\KavitaClient\Model\SiteThemeDto[] apiThemeGet()



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ThemeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiThemeGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ThemeApi->apiThemeGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\SiteThemeDto[]**](../Model/SiteThemeDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiThemeUpdateDefaultPost**
> apiThemeUpdateDefaultPost($body)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ThemeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateDefaultThemeDto(); // \Pbxg33k\KavitaClient\Model\UpdateDefaultThemeDto | 

try {
    $apiInstance->apiThemeUpdateDefaultPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ThemeApi->apiThemeUpdateDefaultPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateDefaultThemeDto**](../Model/UpdateDefaultThemeDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiThemeUploadThemePost**
> \Pbxg33k\KavitaClient\Model\SiteThemeDto apiThemeUploadThemePost($form_file)

Uploads a new theme file

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ThemeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$form_file = "form_file_example"; // string | 

try {
    $result = $apiInstance->apiThemeUploadThemePost($form_file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ThemeApi->apiThemeUploadThemePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **form_file** | **string****string**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\SiteThemeDto**](../Model/SiteThemeDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

