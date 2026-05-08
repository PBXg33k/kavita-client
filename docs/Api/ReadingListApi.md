# Pbxg33k\KavitaClient\ReadingListApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiReadingListAllPeopleGet**](ReadingListApi.md#apireadinglistallpeopleget) | **GET** /api/ReadingList/all-people | Returns all people in given roles for a reading list
[**apiReadingListAllPost**](ReadingListApi.md#apireadinglistallpost) | **POST** /api/ReadingList/all | Returns reading lists (paginated) for a given user.
[**apiReadingListCreatePost**](ReadingListApi.md#apireadinglistcreatepost) | **POST** /api/ReadingList/create | Creates a new List with a unique title. Returns the new ReadingList back
[**apiReadingListDelete**](ReadingListApi.md#apireadinglistdelete) | **DELETE** /api/ReadingList | Deletes a reading list
[**apiReadingListDeleteItemPost**](ReadingListApi.md#apireadinglistdeleteitempost) | **POST** /api/ReadingList/delete-item | Deletes a list item from the list. Item orders will update as a result.
[**apiReadingListDeleteMultiplePost**](ReadingListApi.md#apireadinglistdeletemultiplepost) | **POST** /api/ReadingList/delete-multiple | Delete multiple reading lists in one go
[**apiReadingListExportAsCblPost**](ReadingListApi.md#apireadinglistexportascblpost) | **POST** /api/ReadingList/export-as-cbl | Export a Reading List to CBL format
[**apiReadingListGet**](ReadingListApi.md#apireadinglistget) | **GET** /api/ReadingList | Fetches a single Reading List
[**apiReadingListInfoGet**](ReadingListApi.md#apireadinglistinfoget) | **GET** /api/ReadingList/info | Returns random information about a Reading List
[**apiReadingListItemsGet**](ReadingListApi.md#apireadinglistitemsget) | **GET** /api/ReadingList/items | Fetches all reading list items for a given list including rich metadata around series, volume, chapters, and progress
[**apiReadingListListsForChapterGet**](ReadingListApi.md#apireadinglistlistsforchapterget) | **GET** /api/ReadingList/lists-for-chapter | Returns all Reading Lists the user has access to that has the given chapter within it.
[**apiReadingListListsForSeriesGet**](ReadingListApi.md#apireadinglistlistsforseriesget) | **GET** /api/ReadingList/lists-for-series | Returns all Reading Lists the user has access to that the given series within it.
[**apiReadingListListsPost**](ReadingListApi.md#apireadinglistlistspost) | **POST** /api/ReadingList/lists | Returns reading lists (paginated) for a given user.
[**apiReadingListNameExistsGet**](ReadingListApi.md#apireadinglistnameexistsget) | **GET** /api/ReadingList/name-exists | Checks if a reading list exists with the name
[**apiReadingListNextChapterGet**](ReadingListApi.md#apireadinglistnextchapterget) | **GET** /api/ReadingList/next-chapter | Returns the next chapter within the reading list
[**apiReadingListPeopleGet**](ReadingListApi.md#apireadinglistpeopleget) | **GET** /api/ReadingList/people | Returns a list of a given role associated with the reading list
[**apiReadingListPrevChapterGet**](ReadingListApi.md#apireadinglistprevchapterget) | **GET** /api/ReadingList/prev-chapter | Returns the prev chapter within the reading list
[**apiReadingListPromoteMultiplePost**](ReadingListApi.md#apireadinglistpromotemultiplepost) | **POST** /api/ReadingList/promote-multiple | Promote/UnPromote multiple reading lists in one go. Will only update the authenticated user&#x27;s reading lists and will only work if the user has promotion role
[**apiReadingListRegenerateCoverPost**](ReadingListApi.md#apireadinglistregeneratecoverpost) | **POST** /api/ReadingList/regenerate-cover | Regenerates the cover image for a reading list, you must own the given reading list to do this
[**apiReadingListRemoveReadPost**](ReadingListApi.md#apireadinglistremovereadpost) | **POST** /api/ReadingList/remove-read | Removes all entries that are fully read from the reading list
[**apiReadingListUpdateByChapterPost**](ReadingListApi.md#apireadinglistupdatebychapterpost) | **POST** /api/ReadingList/update-by-chapter | 
[**apiReadingListUpdateByMultiplePost**](ReadingListApi.md#apireadinglistupdatebymultiplepost) | **POST** /api/ReadingList/update-by-multiple | Adds all chapters from a list of volumes and chapters to a reading list
[**apiReadingListUpdateByMultipleSeriesPost**](ReadingListApi.md#apireadinglistupdatebymultipleseriespost) | **POST** /api/ReadingList/update-by-multiple-series | Adds all chapters from a list of series to a reading list
[**apiReadingListUpdateBySeriesPost**](ReadingListApi.md#apireadinglistupdatebyseriespost) | **POST** /api/ReadingList/update-by-series | Adds all chapters from a Series to a reading list
[**apiReadingListUpdateByVolumePost**](ReadingListApi.md#apireadinglistupdatebyvolumepost) | **POST** /api/ReadingList/update-by-volume | 
[**apiReadingListUpdatePositionPost**](ReadingListApi.md#apireadinglistupdatepositionpost) | **POST** /api/ReadingList/update-position | Updates an items position
[**apiReadingListUpdatePost**](ReadingListApi.md#apireadinglistupdatepost) | **POST** /api/ReadingList/update | Update the properties (title, summary) of a reading list

# **apiReadingListAllPeopleGet**
> \Pbxg33k\KavitaClient\Model\PersonDto[] apiReadingListAllPeopleGet($reading_list_id)

Returns all people in given roles for a reading list

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reading_list_id = 56; // int | 

try {
    $result = $apiInstance->apiReadingListAllPeopleGet($reading_list_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListAllPeopleGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **reading_list_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\PersonDto[]**](../Model/PersonDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListAllPost**
> \Pbxg33k\KavitaClient\Model\ReadingListDto[] apiReadingListAllPost($body, $page_number, $page_size)

Returns reading lists (paginated) for a given user.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\ReadingListFilterDto(); // \Pbxg33k\KavitaClient\Model\ReadingListFilterDto | 
$page_number = 56; // int | 
$page_size = 56; // int | 

try {
    $result = $apiInstance->apiReadingListAllPost($body, $page_number, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListAllPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\ReadingListFilterDto**](../Model/ReadingListFilterDto.md)|  | [optional]
 **page_number** | **int**|  | [optional]
 **page_size** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ReadingListDto[]**](../Model/ReadingListDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListCreatePost**
> \Pbxg33k\KavitaClient\Model\ReadingListDto apiReadingListCreatePost($body)

Creates a new List with a unique title. Returns the new ReadingList back

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\CreateReadingListDto(); // \Pbxg33k\KavitaClient\Model\CreateReadingListDto | 

try {
    $result = $apiInstance->apiReadingListCreatePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListCreatePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\CreateReadingListDto**](../Model/CreateReadingListDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ReadingListDto**](../Model/ReadingListDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListDelete**
> apiReadingListDelete($reading_list_id)

Deletes a reading list

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reading_list_id = 56; // int | 

try {
    $apiInstance->apiReadingListDelete($reading_list_id);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **reading_list_id** | **int**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListDeleteItemPost**
> apiReadingListDeleteItemPost($body)

Deletes a list item from the list. Item orders will update as a result.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateReadingListPosition(); // \Pbxg33k\KavitaClient\Model\UpdateReadingListPosition | 

try {
    $apiInstance->apiReadingListDeleteItemPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListDeleteItemPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateReadingListPosition**](../Model/UpdateReadingListPosition.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListDeleteMultiplePost**
> apiReadingListDeleteMultiplePost($body)

Delete multiple reading lists in one go

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\DeleteReadingListsDto(); // \Pbxg33k\KavitaClient\Model\DeleteReadingListsDto | 

try {
    $apiInstance->apiReadingListDeleteMultiplePost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListDeleteMultiplePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\DeleteReadingListsDto**](../Model/DeleteReadingListsDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListExportAsCblPost**
> apiReadingListExportAsCblPost($reading_list_id, $as_v2)

Export a Reading List to CBL format

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reading_list_id = 56; // int | 
$as_v2 = false; // bool | 

try {
    $apiInstance->apiReadingListExportAsCblPost($reading_list_id, $as_v2);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListExportAsCblPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **reading_list_id** | **int**|  | [optional]
 **as_v2** | **bool**|  | [optional] [default to false]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListGet**
> \Pbxg33k\KavitaClient\Model\ReadingListDto apiReadingListGet($reading_list_id)

Fetches a single Reading List

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reading_list_id = 56; // int | 

try {
    $result = $apiInstance->apiReadingListGet($reading_list_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **reading_list_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ReadingListDto**](../Model/ReadingListDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListInfoGet**
> \Pbxg33k\KavitaClient\Model\ReadingListInfoDto apiReadingListInfoGet($reading_list_id)

Returns random information about a Reading List

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reading_list_id = 56; // int | 

try {
    $result = $apiInstance->apiReadingListInfoGet($reading_list_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListInfoGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **reading_list_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ReadingListInfoDto**](../Model/ReadingListInfoDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListItemsGet**
> \Pbxg33k\KavitaClient\Model\ReadingListItemDto[] apiReadingListItemsGet($reading_list_id)

Fetches all reading list items for a given list including rich metadata around series, volume, chapters, and progress

This call is expensive

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reading_list_id = 56; // int | 

try {
    $result = $apiInstance->apiReadingListItemsGet($reading_list_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListItemsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **reading_list_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ReadingListItemDto[]**](../Model/ReadingListItemDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListListsForChapterGet**
> \Pbxg33k\KavitaClient\Model\ReadingListDto[] apiReadingListListsForChapterGet($chapter_id)

Returns all Reading Lists the user has access to that has the given chapter within it.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 

try {
    $result = $apiInstance->apiReadingListListsForChapterGet($chapter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListListsForChapterGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ReadingListDto[]**](../Model/ReadingListDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListListsForSeriesGet**
> \Pbxg33k\KavitaClient\Model\ReadingListDto[] apiReadingListListsForSeriesGet($series_id)

Returns all Reading Lists the user has access to that the given series within it.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $result = $apiInstance->apiReadingListListsForSeriesGet($series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListListsForSeriesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ReadingListDto[]**](../Model/ReadingListDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListListsPost**
> \Pbxg33k\KavitaClient\Model\ReadingListDto[] apiReadingListListsPost($page_number, $page_size, $include_promoted, $sort_by_last_modified)

Returns reading lists (paginated) for a given user.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page_number = 56; // int | 
$page_size = 56; // int | 
$include_promoted = true; // bool | Include Promoted Reading Lists along with user's Reading Lists. Defaults to true
$sort_by_last_modified = false; // bool | Sort by last modified (most recent first) or by title (alphabetical)

try {
    $result = $apiInstance->apiReadingListListsPost($page_number, $page_size, $include_promoted, $sort_by_last_modified);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListListsPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page_number** | **int**|  | [optional]
 **page_size** | **int**|  | [optional]
 **include_promoted** | **bool**| Include Promoted Reading Lists along with user&#x27;s Reading Lists. Defaults to true | [optional] [default to true]
 **sort_by_last_modified** | **bool**| Sort by last modified (most recent first) or by title (alphabetical) | [optional] [default to false]

### Return type

[**\Pbxg33k\KavitaClient\Model\ReadingListDto[]**](../Model/ReadingListDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListNameExistsGet**
> bool apiReadingListNameExistsGet($name)

Checks if a reading list exists with the name

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | If empty or null, will return true as that is invalid

try {
    $result = $apiInstance->apiReadingListNameExistsGet($name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListNameExistsGet: ', $e->getMessage(), PHP_EOL;
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

# **apiReadingListNextChapterGet**
> int apiReadingListNextChapterGet($current_chapter_id, $reading_list_id)

Returns the next chapter within the reading list

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$current_chapter_id = 56; // int | 
$reading_list_id = 56; // int | 

try {
    $result = $apiInstance->apiReadingListNextChapterGet($current_chapter_id, $reading_list_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListNextChapterGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **current_chapter_id** | **int**|  | [optional]
 **reading_list_id** | **int**|  | [optional]

### Return type

**int**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListPeopleGet**
> \Pbxg33k\KavitaClient\Model\PersonDto[] apiReadingListPeopleGet($reading_list_id, $role)

Returns a list of a given role associated with the reading list

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reading_list_id = 56; // int | 
$role = new \Pbxg33k\KavitaClient\Model\PersonRole(); // \Pbxg33k\KavitaClient\Model\PersonRole | PersonRole

try {
    $result = $apiInstance->apiReadingListPeopleGet($reading_list_id, $role);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListPeopleGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **reading_list_id** | **int**|  | [optional]
 **role** | [**\Pbxg33k\KavitaClient\Model\PersonRole**](../Model/.md)| PersonRole | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\PersonDto[]**](../Model/PersonDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListPrevChapterGet**
> int apiReadingListPrevChapterGet($current_chapter_id, $reading_list_id)

Returns the prev chapter within the reading list

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$current_chapter_id = 56; // int | 
$reading_list_id = 56; // int | 

try {
    $result = $apiInstance->apiReadingListPrevChapterGet($current_chapter_id, $reading_list_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListPrevChapterGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **current_chapter_id** | **int**|  | [optional]
 **reading_list_id** | **int**|  | [optional]

### Return type

**int**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListPromoteMultiplePost**
> apiReadingListPromoteMultiplePost($body)

Promote/UnPromote multiple reading lists in one go. Will only update the authenticated user's reading lists and will only work if the user has promotion role

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\PromoteReadingListsDto(); // \Pbxg33k\KavitaClient\Model\PromoteReadingListsDto | 

try {
    $apiInstance->apiReadingListPromoteMultiplePost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListPromoteMultiplePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\PromoteReadingListsDto**](../Model/PromoteReadingListsDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListRegenerateCoverPost**
> apiReadingListRegenerateCoverPost($reading_list_id)

Regenerates the cover image for a reading list, you must own the given reading list to do this

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reading_list_id = 56; // int | 

try {
    $apiInstance->apiReadingListRegenerateCoverPost($reading_list_id);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListRegenerateCoverPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **reading_list_id** | **int**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListRemoveReadPost**
> apiReadingListRemoveReadPost($reading_list_id)

Removes all entries that are fully read from the reading list

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reading_list_id = 56; // int | 

try {
    $apiInstance->apiReadingListRemoveReadPost($reading_list_id);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListRemoveReadPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **reading_list_id** | **int**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListUpdateByChapterPost**
> apiReadingListUpdateByChapterPost($body)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateReadingListByChapterDto(); // \Pbxg33k\KavitaClient\Model\UpdateReadingListByChapterDto | 

try {
    $apiInstance->apiReadingListUpdateByChapterPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListUpdateByChapterPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateReadingListByChapterDto**](../Model/UpdateReadingListByChapterDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListUpdateByMultiplePost**
> apiReadingListUpdateByMultiplePost($body)

Adds all chapters from a list of volumes and chapters to a reading list

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateReadingListByMultipleDto(); // \Pbxg33k\KavitaClient\Model\UpdateReadingListByMultipleDto | 

try {
    $apiInstance->apiReadingListUpdateByMultiplePost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListUpdateByMultiplePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateReadingListByMultipleDto**](../Model/UpdateReadingListByMultipleDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListUpdateByMultipleSeriesPost**
> apiReadingListUpdateByMultipleSeriesPost($body)

Adds all chapters from a list of series to a reading list

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateReadingListByMultipleSeriesDto(); // \Pbxg33k\KavitaClient\Model\UpdateReadingListByMultipleSeriesDto | 

try {
    $apiInstance->apiReadingListUpdateByMultipleSeriesPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListUpdateByMultipleSeriesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateReadingListByMultipleSeriesDto**](../Model/UpdateReadingListByMultipleSeriesDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListUpdateBySeriesPost**
> apiReadingListUpdateBySeriesPost($body)

Adds all chapters from a Series to a reading list

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateReadingListBySeriesDto(); // \Pbxg33k\KavitaClient\Model\UpdateReadingListBySeriesDto | 

try {
    $apiInstance->apiReadingListUpdateBySeriesPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListUpdateBySeriesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateReadingListBySeriesDto**](../Model/UpdateReadingListBySeriesDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListUpdateByVolumePost**
> apiReadingListUpdateByVolumePost($body)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateReadingListByVolumeDto(); // \Pbxg33k\KavitaClient\Model\UpdateReadingListByVolumeDto | 

try {
    $apiInstance->apiReadingListUpdateByVolumePost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListUpdateByVolumePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateReadingListByVolumeDto**](../Model/UpdateReadingListByVolumeDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListUpdatePositionPost**
> apiReadingListUpdatePositionPost($body)

Updates an items position

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateReadingListPosition(); // \Pbxg33k\KavitaClient\Model\UpdateReadingListPosition | 

try {
    $apiInstance->apiReadingListUpdatePositionPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListUpdatePositionPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateReadingListPosition**](../Model/UpdateReadingListPosition.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReadingListUpdatePost**
> \Pbxg33k\KavitaClient\Model\ReadingListDto apiReadingListUpdatePost($body)

Update the properties (title, summary) of a reading list

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReadingListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateReadingListDto(); // \Pbxg33k\KavitaClient\Model\UpdateReadingListDto | 

try {
    $result = $apiInstance->apiReadingListUpdatePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReadingListApi->apiReadingListUpdatePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateReadingListDto**](../Model/UpdateReadingListDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ReadingListDto**](../Model/ReadingListDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

