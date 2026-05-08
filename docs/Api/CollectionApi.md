# Pbxg33k\KavitaClient\CollectionApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiCollectionAllSeriesGet**](CollectionApi.md#apicollectionallseriesget) | **GET** /api/Collection/all-series | Returns all collections that contain the Series for the user with the option to allow for promoted collections (non-user owned)
[**apiCollectionDelete**](CollectionApi.md#apicollectiondelete) | **DELETE** /api/Collection | Removes the collection tag from the user
[**apiCollectionDeleteMultiplePost**](CollectionApi.md#apicollectiondeletemultiplepost) | **POST** /api/Collection/delete-multiple | Delete multiple collections in one go
[**apiCollectionGet**](CollectionApi.md#apicollectionget) | **GET** /api/Collection | Returns all Collection tags for a given User
[**apiCollectionImportStackPost**](CollectionApi.md#apicollectionimportstackpost) | **POST** /api/Collection/import-stack | Imports a MAL Stack into Kavita
[**apiCollectionMalStacksGet**](CollectionApi.md#apicollectionmalstacksget) | **GET** /api/Collection/mal-stacks | For the authenticated user, if they have an active Kavita+ subscription and a MAL username on record, fetch their Mal interest stacks (including restacks)
[**apiCollectionNameExistsGet**](CollectionApi.md#apicollectionnameexistsget) | **GET** /api/Collection/name-exists | Checks if a collection exists with the name
[**apiCollectionPromoteMultiplePost**](CollectionApi.md#apicollectionpromotemultiplepost) | **POST** /api/Collection/promote-multiple | Promote/UnPromote multiple collections in one go. Will only update the authenticated user&#x27;s collections and will only work if the user has promotion role
[**apiCollectionSingleGet**](CollectionApi.md#apicollectionsingleget) | **GET** /api/Collection/single | Returns a single Collection tag by Id for a given user
[**apiCollectionUpdateForSeriesPost**](CollectionApi.md#apicollectionupdateforseriespost) | **POST** /api/Collection/update-for-series | Adds multiple series to a collection. If tag id is 0, this will create a new tag.
[**apiCollectionUpdatePost**](CollectionApi.md#apicollectionupdatepost) | **POST** /api/Collection/update | Updates an existing tag with a new title, promotion status, and summary. &lt;remarks&gt;UI does not contain controls to update title&lt;/remarks&gt;
[**apiCollectionUpdateSeriesPost**](CollectionApi.md#apicollectionupdateseriespost) | **POST** /api/Collection/update-series | For a given tag, update the summary if summary has changed and remove a set of series from the tag.

# **apiCollectionAllSeriesGet**
> \Pbxg33k\KavitaClient\Model\AppUserCollectionDto[] apiCollectionAllSeriesGet($series_id, $owned_only)

Returns all collections that contain the Series for the user with the option to allow for promoted collections (non-user owned)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CollectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 
$owned_only = false; // bool | 

try {
    $result = $apiInstance->apiCollectionAllSeriesGet($series_id, $owned_only);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionApi->apiCollectionAllSeriesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]
 **owned_only** | **bool**|  | [optional] [default to false]

### Return type

[**\Pbxg33k\KavitaClient\Model\AppUserCollectionDto[]**](../Model/AppUserCollectionDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCollectionDelete**
> apiCollectionDelete($tag_id)

Removes the collection tag from the user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CollectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tag_id = 56; // int | 

try {
    $apiInstance->apiCollectionDelete($tag_id);
} catch (Exception $e) {
    echo 'Exception when calling CollectionApi->apiCollectionDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tag_id** | **int**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCollectionDeleteMultiplePost**
> apiCollectionDeleteMultiplePost($body)

Delete multiple collections in one go

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CollectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\DeleteCollectionsDto(); // \Pbxg33k\KavitaClient\Model\DeleteCollectionsDto | 

try {
    $apiInstance->apiCollectionDeleteMultiplePost($body);
} catch (Exception $e) {
    echo 'Exception when calling CollectionApi->apiCollectionDeleteMultiplePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\DeleteCollectionsDto**](../Model/DeleteCollectionsDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCollectionGet**
> \Pbxg33k\KavitaClient\Model\AppUserCollectionDto[] apiCollectionGet($owned_only, $sort_by_last_modified)

Returns all Collection tags for a given User

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CollectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$owned_only = false; // bool | Exclude Promoted
$sort_by_last_modified = false; // bool | Order by Last Modified rather than on Title

try {
    $result = $apiInstance->apiCollectionGet($owned_only, $sort_by_last_modified);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionApi->apiCollectionGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owned_only** | **bool**| Exclude Promoted | [optional] [default to false]
 **sort_by_last_modified** | **bool**| Order by Last Modified rather than on Title | [optional] [default to false]

### Return type

[**\Pbxg33k\KavitaClient\Model\AppUserCollectionDto[]**](../Model/AppUserCollectionDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCollectionImportStackPost**
> apiCollectionImportStackPost($body)

Imports a MAL Stack into Kavita

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CollectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\MalStackDto(); // \Pbxg33k\KavitaClient\Model\MalStackDto | 

try {
    $apiInstance->apiCollectionImportStackPost($body);
} catch (Exception $e) {
    echo 'Exception when calling CollectionApi->apiCollectionImportStackPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\MalStackDto**](../Model/MalStackDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCollectionMalStacksGet**
> \Pbxg33k\KavitaClient\Model\MalStackDto[] apiCollectionMalStacksGet()

For the authenticated user, if they have an active Kavita+ subscription and a MAL username on record, fetch their Mal interest stacks (including restacks)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CollectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiCollectionMalStacksGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionApi->apiCollectionMalStacksGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\MalStackDto[]**](../Model/MalStackDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCollectionNameExistsGet**
> bool apiCollectionNameExistsGet($name)

Checks if a collection exists with the name

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CollectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | If empty or null, will return true as that is invalid

try {
    $result = $apiInstance->apiCollectionNameExistsGet($name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionApi->apiCollectionNameExistsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| If empty or null, will return true as that is invalid | [optional]

### Return type

**bool**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCollectionPromoteMultiplePost**
> apiCollectionPromoteMultiplePost($body)

Promote/UnPromote multiple collections in one go. Will only update the authenticated user's collections and will only work if the user has promotion role

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CollectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\PromoteCollectionsDto(); // \Pbxg33k\KavitaClient\Model\PromoteCollectionsDto | 

try {
    $apiInstance->apiCollectionPromoteMultiplePost($body);
} catch (Exception $e) {
    echo 'Exception when calling CollectionApi->apiCollectionPromoteMultiplePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\PromoteCollectionsDto**](../Model/PromoteCollectionsDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCollectionSingleGet**
> \Pbxg33k\KavitaClient\Model\AppUserCollectionDto apiCollectionSingleGet($collection_id)

Returns a single Collection tag by Id for a given user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CollectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$collection_id = 56; // int | 

try {
    $result = $apiInstance->apiCollectionSingleGet($collection_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionApi->apiCollectionSingleGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **collection_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\AppUserCollectionDto**](../Model/AppUserCollectionDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCollectionUpdateForSeriesPost**
> apiCollectionUpdateForSeriesPost($body)

Adds multiple series to a collection. If tag id is 0, this will create a new tag.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CollectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\CollectionTagBulkAddDto(); // \Pbxg33k\KavitaClient\Model\CollectionTagBulkAddDto | 

try {
    $apiInstance->apiCollectionUpdateForSeriesPost($body);
} catch (Exception $e) {
    echo 'Exception when calling CollectionApi->apiCollectionUpdateForSeriesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\CollectionTagBulkAddDto**](../Model/CollectionTagBulkAddDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCollectionUpdatePost**
> \Pbxg33k\KavitaClient\Model\AppUserCollectionDto apiCollectionUpdatePost($body)

Updates an existing tag with a new title, promotion status, and summary. <remarks>UI does not contain controls to update title</remarks>

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CollectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\AppUserCollectionDto(); // \Pbxg33k\KavitaClient\Model\AppUserCollectionDto | 

try {
    $result = $apiInstance->apiCollectionUpdatePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionApi->apiCollectionUpdatePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\AppUserCollectionDto**](../Model/AppUserCollectionDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\AppUserCollectionDto**](../Model/AppUserCollectionDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCollectionUpdateSeriesPost**
> apiCollectionUpdateSeriesPost($body)

For a given tag, update the summary if summary has changed and remove a set of series from the tag.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CollectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateSeriesForTagDto(); // \Pbxg33k\KavitaClient\Model\UpdateSeriesForTagDto | 

try {
    $apiInstance->apiCollectionUpdateSeriesPost($body);
} catch (Exception $e) {
    echo 'Exception when calling CollectionApi->apiCollectionUpdateSeriesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateSeriesForTagDto**](../Model/UpdateSeriesForTagDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

