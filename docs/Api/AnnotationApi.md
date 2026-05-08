# Pbxg33k\KavitaClient\AnnotationApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiAnnotationAllFilteredPost**](AnnotationApi.md#apiannotationallfilteredpost) | **POST** /api/Annotation/all-filtered | Returns a list of annotations for browsing
[**apiAnnotationAllForSeriesGet**](AnnotationApi.md#apiannotationallforseriesget) | **GET** /api/Annotation/all-for-series | Returns all annotations by Series
[**apiAnnotationAllGet**](AnnotationApi.md#apiannotationallget) | **GET** /api/Annotation/all | Returns the annotations for the given chapter
[**apiAnnotationAnnotationIdGet**](AnnotationApi.md#apiannotationannotationidget) | **GET** /api/Annotation/{annotationId} | Returns the Annotation by Id. User must have access to annotation.
[**apiAnnotationBulkDeletePost**](AnnotationApi.md#apiannotationbulkdeletepost) | **POST** /api/Annotation/bulk-delete | Removes annotations in bulk. Requires every annotation to be owned by the authenticated user
[**apiAnnotationCreatePost**](AnnotationApi.md#apiannotationcreatepost) | **POST** /api/Annotation/create | Create a new Annotation for the user against a Chapter
[**apiAnnotationDelete**](AnnotationApi.md#apiannotationdelete) | **DELETE** /api/Annotation | Delete the annotation for the user
[**apiAnnotationExportFilterPost**](AnnotationApi.md#apiannotationexportfilterpost) | **POST** /api/Annotation/export-filter | Exports annotations for the given users
[**apiAnnotationExportPost**](AnnotationApi.md#apiannotationexportpost) | **POST** /api/Annotation/export | Exports Annotations for the User
[**apiAnnotationLikePost**](AnnotationApi.md#apiannotationlikepost) | **POST** /api/Annotation/like | Adds a like for the currently authenticated user if not already from the annotations with given ids
[**apiAnnotationUnlikePost**](AnnotationApi.md#apiannotationunlikepost) | **POST** /api/Annotation/unlike | Removes likes for the currently authenticated user if present from the annotations with given ids
[**apiAnnotationUpdatePost**](AnnotationApi.md#apiannotationupdatepost) | **POST** /api/Annotation/update | Update the modifiable fields (Spoiler, highlight slot, and comment) for an annotation

# **apiAnnotationAllFilteredPost**
> \Pbxg33k\KavitaClient\Model\AnnotationDto[] apiAnnotationAllFilteredPost($body, $page_number, $page_size)

Returns a list of annotations for browsing

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AnnotationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\AnnotationFilterDto(); // \Pbxg33k\KavitaClient\Model\AnnotationFilterDto | 
$page_number = 56; // int | 
$page_size = 56; // int | 

try {
    $result = $apiInstance->apiAnnotationAllFilteredPost($body, $page_number, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AnnotationApi->apiAnnotationAllFilteredPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\AnnotationFilterDto**](../Model/AnnotationFilterDto.md)|  | [optional]
 **page_number** | **int**|  | [optional]
 **page_size** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\AnnotationDto[]**](../Model/AnnotationDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAnnotationAllForSeriesGet**
> \Pbxg33k\KavitaClient\Model\AnnotationDto apiAnnotationAllForSeriesGet($series_id)

Returns all annotations by Series

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AnnotationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $result = $apiInstance->apiAnnotationAllForSeriesGet($series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AnnotationApi->apiAnnotationAllForSeriesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\AnnotationDto**](../Model/AnnotationDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAnnotationAllGet**
> \Pbxg33k\KavitaClient\Model\AnnotationDto[] apiAnnotationAllGet($chapter_id)

Returns the annotations for the given chapter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AnnotationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 

try {
    $result = $apiInstance->apiAnnotationAllGet($chapter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AnnotationApi->apiAnnotationAllGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\AnnotationDto[]**](../Model/AnnotationDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAnnotationAnnotationIdGet**
> \Pbxg33k\KavitaClient\Model\AnnotationDto apiAnnotationAnnotationIdGet($annotation_id)

Returns the Annotation by Id. User must have access to annotation.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AnnotationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$annotation_id = 56; // int | 

try {
    $result = $apiInstance->apiAnnotationAnnotationIdGet($annotation_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AnnotationApi->apiAnnotationAnnotationIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **annotation_id** | **int**|  |

### Return type

[**\Pbxg33k\KavitaClient\Model\AnnotationDto**](../Model/AnnotationDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAnnotationBulkDeletePost**
> apiAnnotationBulkDeletePost($body)

Removes annotations in bulk. Requires every annotation to be owned by the authenticated user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AnnotationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = array(56); // int[] | 

try {
    $apiInstance->apiAnnotationBulkDeletePost($body);
} catch (Exception $e) {
    echo 'Exception when calling AnnotationApi->apiAnnotationBulkDeletePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**int[]**](../Model/int.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAnnotationCreatePost**
> \Pbxg33k\KavitaClient\Model\AnnotationDto apiAnnotationCreatePost($body)

Create a new Annotation for the user against a Chapter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AnnotationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\AnnotationDto(); // \Pbxg33k\KavitaClient\Model\AnnotationDto | 

try {
    $result = $apiInstance->apiAnnotationCreatePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AnnotationApi->apiAnnotationCreatePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\AnnotationDto**](../Model/AnnotationDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\AnnotationDto**](../Model/AnnotationDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAnnotationDelete**
> apiAnnotationDelete($annotation_id)

Delete the annotation for the user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AnnotationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$annotation_id = 56; // int | 

try {
    $apiInstance->apiAnnotationDelete($annotation_id);
} catch (Exception $e) {
    echo 'Exception when calling AnnotationApi->apiAnnotationDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **annotation_id** | **int**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAnnotationExportFilterPost**
> apiAnnotationExportFilterPost($body, $page_number, $page_size)

Exports annotations for the given users

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AnnotationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\AnnotationFilterDto(); // \Pbxg33k\KavitaClient\Model\AnnotationFilterDto | 
$page_number = 56; // int | 
$page_size = 56; // int | 

try {
    $apiInstance->apiAnnotationExportFilterPost($body, $page_number, $page_size);
} catch (Exception $e) {
    echo 'Exception when calling AnnotationApi->apiAnnotationExportFilterPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\AnnotationFilterDto**](../Model/AnnotationFilterDto.md)|  | [optional]
 **page_number** | **int**|  | [optional]
 **page_size** | **int**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAnnotationExportPost**
> apiAnnotationExportPost($body)

Exports Annotations for the User

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AnnotationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = array(56); // int[] | Export annotations with the given ids

try {
    $apiInstance->apiAnnotationExportPost($body);
} catch (Exception $e) {
    echo 'Exception when calling AnnotationApi->apiAnnotationExportPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**int[]**](../Model/int.md)| Export annotations with the given ids | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAnnotationLikePost**
> apiAnnotationLikePost($body)

Adds a like for the currently authenticated user if not already from the annotations with given ids

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AnnotationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = array(56); // int[] | 

try {
    $apiInstance->apiAnnotationLikePost($body);
} catch (Exception $e) {
    echo 'Exception when calling AnnotationApi->apiAnnotationLikePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**int[]**](../Model/int.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAnnotationUnlikePost**
> apiAnnotationUnlikePost($body)

Removes likes for the currently authenticated user if present from the annotations with given ids

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AnnotationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = array(56); // int[] | 

try {
    $apiInstance->apiAnnotationUnlikePost($body);
} catch (Exception $e) {
    echo 'Exception when calling AnnotationApi->apiAnnotationUnlikePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**int[]**](../Model/int.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiAnnotationUpdatePost**
> \Pbxg33k\KavitaClient\Model\AnnotationDto apiAnnotationUpdatePost($body)

Update the modifiable fields (Spoiler, highlight slot, and comment) for an annotation

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\AnnotationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\AnnotationDto(); // \Pbxg33k\KavitaClient\Model\AnnotationDto | 

try {
    $result = $apiInstance->apiAnnotationUpdatePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AnnotationApi->apiAnnotationUpdatePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\AnnotationDto**](../Model/AnnotationDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\AnnotationDto**](../Model/AnnotationDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

