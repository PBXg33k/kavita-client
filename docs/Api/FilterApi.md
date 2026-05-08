# Pbxg33k\KavitaClient\FilterApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiFilterDecodePost**](FilterApi.md#apifilterdecodepost) | **POST** /api/Filter/decode | Decodes the Filter
[**apiFilterDelete**](FilterApi.md#apifilterdelete) | **DELETE** /api/Filter | Delete the smart filter for the authenticated user
[**apiFilterEncodeAnnotationPost**](FilterApi.md#apifilterencodeannotationpost) | **POST** /api/Filter/encode/annotation | Encode an Annotation Filter
[**apiFilterEncodePersonPost**](FilterApi.md#apifilterencodepersonpost) | **POST** /api/Filter/encode/person | Encode a Person Filter
[**apiFilterEncodeReadingListPost**](FilterApi.md#apifilterencodereadinglistpost) | **POST** /api/Filter/encode/reading-list | Encode a Reading List filter
[**apiFilterEncodeSeriesPost**](FilterApi.md#apifilterencodeseriespost) | **POST** /api/Filter/encode/series | Encode a Series filter
[**apiFilterGet**](FilterApi.md#apifilterget) | **GET** /api/Filter | All Smart Filters for the authenticated user
[**apiFilterRenamePost**](FilterApi.md#apifilterrenamepost) | **POST** /api/Filter/rename | Rename a Smart Filter given the filterId and new name
[**apiFilterUpdateAnnotationPost**](FilterApi.md#apifilterupdateannotationpost) | **POST** /api/Filter/update/annotation | Creates or Updates the Reading List filter
[**apiFilterUpdatePersonPost**](FilterApi.md#apifilterupdatepersonpost) | **POST** /api/Filter/update/person | Creates or Updates the Person filter
[**apiFilterUpdateReadingListPost**](FilterApi.md#apifilterupdatereadinglistpost) | **POST** /api/Filter/update/reading-list | Creates or Updates the Reading List filter
[**apiFilterUpdateSeriesPost**](FilterApi.md#apifilterupdateseriespost) | **POST** /api/Filter/update/series | Creates or Updates the Series filter

# **apiFilterDecodePost**
> \Pbxg33k\KavitaClient\Model\IFilterDto apiFilterDecodePost($body)

Decodes the Filter

Decoded filter will always have the same shape of Kavita.Models.DTOs.Filtering.v2.IFilterDto`2.             The concrete class is driven by `EntityType`.             Classes: Kavita.Models.DTOs.Filtering.v2.Requests.SeriesFilterV2Dto, Kavita.Models.DTOs.Filtering.v2.Requests.PersonFilterDto, Kavita.Models.DTOs.Filtering.v2.Requests.AnnotationFilterDto, Kavita.Models.DTOs.Filtering.v2.Requests.ReadingListFilterDto

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\FilterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\DecodeFilterDto(); // \Pbxg33k\KavitaClient\Model\DecodeFilterDto | 

try {
    $result = $apiInstance->apiFilterDecodePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FilterApi->apiFilterDecodePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\DecodeFilterDto**](../Model/DecodeFilterDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\IFilterDto**](../Model/IFilterDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiFilterDelete**
> apiFilterDelete($filter_id)

Delete the smart filter for the authenticated user

User must not be in Kavita.Models.Constants.PolicyConstants.ReadOnlyRole

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\FilterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$filter_id = 56; // int | 

try {
    $apiInstance->apiFilterDelete($filter_id);
} catch (Exception $e) {
    echo 'Exception when calling FilterApi->apiFilterDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filter_id** | **int**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiFilterEncodeAnnotationPost**
> string apiFilterEncodeAnnotationPost($body)

Encode an Annotation Filter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\FilterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\AnnotationFilterDto(); // \Pbxg33k\KavitaClient\Model\AnnotationFilterDto | This must be entityType Annotation

try {
    $result = $apiInstance->apiFilterEncodeAnnotationPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FilterApi->apiFilterEncodeAnnotationPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\AnnotationFilterDto**](../Model/AnnotationFilterDto.md)| This must be entityType Annotation | [optional]

### Return type

**string**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiFilterEncodePersonPost**
> string apiFilterEncodePersonPost($body)

Encode a Person Filter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\FilterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\PersonFilterDto(); // \Pbxg33k\KavitaClient\Model\PersonFilterDto | This must be entityType Person

try {
    $result = $apiInstance->apiFilterEncodePersonPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FilterApi->apiFilterEncodePersonPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\PersonFilterDto**](../Model/PersonFilterDto.md)| This must be entityType Person | [optional]

### Return type

**string**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiFilterEncodeReadingListPost**
> string apiFilterEncodeReadingListPost($body)

Encode a Reading List filter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\FilterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\ReadingListFilterDto(); // \Pbxg33k\KavitaClient\Model\ReadingListFilterDto | This must be entityType ReadingList

try {
    $result = $apiInstance->apiFilterEncodeReadingListPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FilterApi->apiFilterEncodeReadingListPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\ReadingListFilterDto**](../Model/ReadingListFilterDto.md)| This must be entityType ReadingList | [optional]

### Return type

**string**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiFilterEncodeSeriesPost**
> string apiFilterEncodeSeriesPost($body)

Encode a Series filter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\FilterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\SeriesFilterV2Dto(); // \Pbxg33k\KavitaClient\Model\SeriesFilterV2Dto | This must be entityType Series

try {
    $result = $apiInstance->apiFilterEncodeSeriesPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FilterApi->apiFilterEncodeSeriesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\SeriesFilterV2Dto**](../Model/SeriesFilterV2Dto.md)| This must be entityType Series | [optional]

### Return type

**string**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiFilterGet**
> \Pbxg33k\KavitaClient\Model\SmartFilterDto[] apiFilterGet()

All Smart Filters for the authenticated user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\FilterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiFilterGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FilterApi->apiFilterGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\SmartFilterDto[]**](../Model/SmartFilterDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiFilterRenamePost**
> apiFilterRenamePost($name, $filter_id)

Rename a Smart Filter given the filterId and new name

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\FilterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | 
$filter_id = 56; // int | 

try {
    $apiInstance->apiFilterRenamePost($name, $filter_id);
} catch (Exception $e) {
    echo 'Exception when calling FilterApi->apiFilterRenamePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**|  |
 **filter_id** | **int**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiFilterUpdateAnnotationPost**
> apiFilterUpdateAnnotationPost($body)

Creates or Updates the Reading List filter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\FilterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\AnnotationFilterDto(); // \Pbxg33k\KavitaClient\Model\AnnotationFilterDto | 

try {
    $apiInstance->apiFilterUpdateAnnotationPost($body);
} catch (Exception $e) {
    echo 'Exception when calling FilterApi->apiFilterUpdateAnnotationPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\AnnotationFilterDto**](../Model/AnnotationFilterDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiFilterUpdatePersonPost**
> apiFilterUpdatePersonPost($body)

Creates or Updates the Person filter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\FilterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\PersonFilterDto(); // \Pbxg33k\KavitaClient\Model\PersonFilterDto | 

try {
    $apiInstance->apiFilterUpdatePersonPost($body);
} catch (Exception $e) {
    echo 'Exception when calling FilterApi->apiFilterUpdatePersonPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\PersonFilterDto**](../Model/PersonFilterDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiFilterUpdateReadingListPost**
> apiFilterUpdateReadingListPost($body)

Creates or Updates the Reading List filter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\FilterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\ReadingListFilterDto(); // \Pbxg33k\KavitaClient\Model\ReadingListFilterDto | 

try {
    $apiInstance->apiFilterUpdateReadingListPost($body);
} catch (Exception $e) {
    echo 'Exception when calling FilterApi->apiFilterUpdateReadingListPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\ReadingListFilterDto**](../Model/ReadingListFilterDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiFilterUpdateSeriesPost**
> apiFilterUpdateSeriesPost($body)

Creates or Updates the Series filter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\FilterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\SeriesFilterV2Dto(); // \Pbxg33k\KavitaClient\Model\SeriesFilterV2Dto | 

try {
    $apiInstance->apiFilterUpdateSeriesPost($body);
} catch (Exception $e) {
    echo 'Exception when calling FilterApi->apiFilterUpdateSeriesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\SeriesFilterV2Dto**](../Model/SeriesFilterV2Dto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

