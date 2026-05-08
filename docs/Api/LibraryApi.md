# Pbxg33k\KavitaClient\LibraryApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiLibraryCopySettingsFromPost**](LibraryApi.md#apilibrarycopysettingsfrompost) | **POST** /api/Library/copy-settings-from | Copy the library settings (adv tab + optional type) to a set of other libraries.
[**apiLibraryCreatePost**](LibraryApi.md#apilibrarycreatepost) | **POST** /api/Library/create | Creates a new Library. Upon library creation, adds new library to all Admin accounts.
[**apiLibraryDeleteDelete**](LibraryApi.md#apilibrarydeletedelete) | **DELETE** /api/Library/delete | Deletes the library and all series within it.
[**apiLibraryDeleteMultipleDelete**](LibraryApi.md#apilibrarydeletemultipledelete) | **DELETE** /api/Library/delete-multiple | Deletes multiple libraries and all series within it.
[**apiLibraryGet**](LibraryApi.md#apilibraryget) | **GET** /api/Library | Return a specific library
[**apiLibraryGrantAccessPost**](LibraryApi.md#apilibrarygrantaccesspost) | **POST** /api/Library/grant-access | Grants a user account access to a Library
[**apiLibraryHasFilesAtRootPost**](LibraryApi.md#apilibraryhasfilesatrootpost) | **POST** /api/Library/has-files-at-root | For each root, checks if there are any supported files at root to warn the user during library creation about an invalid setup
[**apiLibraryJumpBarGet**](LibraryApi.md#apilibraryjumpbarget) | **GET** /api/Library/jump-bar | For a given library, generate the jump bar information
[**apiLibraryLibrariesGet**](LibraryApi.md#apilibrarylibrariesget) | **GET** /api/Library/libraries | Return all libraries in the Server
[**apiLibraryListGet**](LibraryApi.md#apilibrarylistget) | **GET** /api/Library/list | Returns a list of directories for a given path. If path is empty, returns root drives.
[**apiLibraryNameExistsGet**](LibraryApi.md#apilibrarynameexistsget) | **GET** /api/Library/name-exists | Checks if the library name exists or not
[**apiLibraryRefreshMetadataMultiplePost**](LibraryApi.md#apilibraryrefreshmetadatamultiplepost) | **POST** /api/Library/refresh-metadata-multiple | 
[**apiLibraryRefreshMetadataPost**](LibraryApi.md#apilibraryrefreshmetadatapost) | **POST** /api/Library/refresh-metadata | 
[**apiLibraryScanAllPost**](LibraryApi.md#apilibraryscanallpost) | **POST** /api/Library/scan-all | Scans a given library for file changes. If another scan task is in progress, will reschedule the invocation for 3 hours in future.
[**apiLibraryScanFolderPost**](LibraryApi.md#apilibraryscanfolderpost) | **POST** /api/Library/scan-folder | Given a valid path, will invoke either a Scan Series or Scan Library. If the folder does not exist within Kavita, the request will be ignored
[**apiLibraryScanMultiplePost**](LibraryApi.md#apilibraryscanmultiplepost) | **POST** /api/Library/scan-multiple | Enqueues a bunch of library scans
[**apiLibraryScanPost**](LibraryApi.md#apilibraryscanpost) | **POST** /api/Library/scan | Scans a given library for file changes.
[**apiLibraryTypeGet**](LibraryApi.md#apilibrarytypeget) | **GET** /api/Library/type | Returns the type of the underlying library
[**apiLibraryUpdatePost**](LibraryApi.md#apilibraryupdatepost) | **POST** /api/Library/update | Updates an existing Library with new name, folders, and/or type.
[**apiLibraryUserLibrariesGet**](LibraryApi.md#apilibraryuserlibrariesget) | **GET** /api/Library/user-libraries | Gets libraries for the given user that you also have access to

# **apiLibraryCopySettingsFromPost**
> apiLibraryCopySettingsFromPost($body)

Copy the library settings (adv tab + optional type) to a set of other libraries.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\LibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\CopySettingsFromLibraryDto(); // \Pbxg33k\KavitaClient\Model\CopySettingsFromLibraryDto | 

try {
    $apiInstance->apiLibraryCopySettingsFromPost($body);
} catch (Exception $e) {
    echo 'Exception when calling LibraryApi->apiLibraryCopySettingsFromPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\CopySettingsFromLibraryDto**](../Model/CopySettingsFromLibraryDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiLibraryCreatePost**
> \Pbxg33k\KavitaClient\Model\LibraryDto apiLibraryCreatePost($body)

Creates a new Library. Upon library creation, adds new library to all Admin accounts.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\LibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateLibraryDto(); // \Pbxg33k\KavitaClient\Model\UpdateLibraryDto | 

try {
    $result = $apiInstance->apiLibraryCreatePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LibraryApi->apiLibraryCreatePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateLibraryDto**](../Model/UpdateLibraryDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\LibraryDto**](../Model/LibraryDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiLibraryDeleteDelete**
> bool apiLibraryDeleteDelete($library_id)

Deletes the library and all series within it.

This does not touch any files

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\LibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$library_id = 56; // int | 

try {
    $result = $apiInstance->apiLibraryDeleteDelete($library_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LibraryApi->apiLibraryDeleteDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **library_id** | **int**|  | [optional]

### Return type

**bool**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiLibraryDeleteMultipleDelete**
> bool apiLibraryDeleteMultipleDelete($body)

Deletes multiple libraries and all series within it.

This does not touch any files

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\LibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = array(56); // int[] | 

try {
    $result = $apiInstance->apiLibraryDeleteMultipleDelete($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LibraryApi->apiLibraryDeleteMultipleDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**int[]**](../Model/int.md)|  | [optional]

### Return type

**bool**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiLibraryGet**
> \Pbxg33k\KavitaClient\Model\LibraryDto apiLibraryGet($library_id)

Return a specific library

If the user is not an admin, only id, type, and name will be returned (Kavita.Models.DTOs.LiteLibraryDto)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\LibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$library_id = 56; // int | 

try {
    $result = $apiInstance->apiLibraryGet($library_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LibraryApi->apiLibraryGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **library_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\LibraryDto**](../Model/LibraryDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiLibraryGrantAccessPost**
> \Pbxg33k\KavitaClient\Model\MemberDto apiLibraryGrantAccessPost($body)

Grants a user account access to a Library

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\LibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateLibraryForUserDto(); // \Pbxg33k\KavitaClient\Model\UpdateLibraryForUserDto | 

try {
    $result = $apiInstance->apiLibraryGrantAccessPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LibraryApi->apiLibraryGrantAccessPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateLibraryForUserDto**](../Model/UpdateLibraryForUserDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\MemberDto**](../Model/MemberDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiLibraryHasFilesAtRootPost**
> string[] apiLibraryHasFilesAtRootPost($body)

For each root, checks if there are any supported files at root to warn the user during library creation about an invalid setup

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\LibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\CheckForFilesInFolderRootsDto(); // \Pbxg33k\KavitaClient\Model\CheckForFilesInFolderRootsDto | 

try {
    $result = $apiInstance->apiLibraryHasFilesAtRootPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LibraryApi->apiLibraryHasFilesAtRootPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\CheckForFilesInFolderRootsDto**](../Model/CheckForFilesInFolderRootsDto.md)|  | [optional]

### Return type

**string[]**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiLibraryJumpBarGet**
> \Pbxg33k\KavitaClient\Model\JumpKeyDto[] apiLibraryJumpBarGet($library_id)

For a given library, generate the jump bar information

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\LibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$library_id = 56; // int | 

try {
    $result = $apiInstance->apiLibraryJumpBarGet($library_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LibraryApi->apiLibraryJumpBarGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **library_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\JumpKeyDto[]**](../Model/JumpKeyDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiLibraryLibrariesGet**
> \Pbxg33k\KavitaClient\Model\LibraryDto[] apiLibraryLibrariesGet()

Return all libraries in the Server

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\LibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiLibraryLibrariesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LibraryApi->apiLibraryLibrariesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\LibraryDto[]**](../Model/LibraryDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiLibraryListGet**
> \Pbxg33k\KavitaClient\Model\DirectoryDto[] apiLibraryListGet($path)

Returns a list of directories for a given path. If path is empty, returns root drives.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\LibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$path = "path_example"; // string | 

try {
    $result = $apiInstance->apiLibraryListGet($path);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LibraryApi->apiLibraryListGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **path** | **string**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\DirectoryDto[]**](../Model/DirectoryDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiLibraryNameExistsGet**
> bool apiLibraryNameExistsGet($name)

Checks if the library name exists or not

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\LibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | If empty or null, will return true as that is invalid

try {
    $result = $apiInstance->apiLibraryNameExistsGet($name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LibraryApi->apiLibraryNameExistsGet: ', $e->getMessage(), PHP_EOL;
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

# **apiLibraryRefreshMetadataMultiplePost**
> apiLibraryRefreshMetadataMultiplePost($body, $force_colorscape)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\LibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\BulkActionDto(); // \Pbxg33k\KavitaClient\Model\BulkActionDto | 
$force_colorscape = true; // bool | 

try {
    $apiInstance->apiLibraryRefreshMetadataMultiplePost($body, $force_colorscape);
} catch (Exception $e) {
    echo 'Exception when calling LibraryApi->apiLibraryRefreshMetadataMultiplePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\BulkActionDto**](../Model/BulkActionDto.md)|  | [optional]
 **force_colorscape** | **bool**|  | [optional] [default to true]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiLibraryRefreshMetadataPost**
> apiLibraryRefreshMetadataPost($library_id, $force, $force_colorscape)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\LibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$library_id = 56; // int | 
$force = true; // bool | 
$force_colorscape = true; // bool | 

try {
    $apiInstance->apiLibraryRefreshMetadataPost($library_id, $force, $force_colorscape);
} catch (Exception $e) {
    echo 'Exception when calling LibraryApi->apiLibraryRefreshMetadataPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **library_id** | **int**|  | [optional]
 **force** | **bool**|  | [optional] [default to true]
 **force_colorscape** | **bool**|  | [optional] [default to true]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiLibraryScanAllPost**
> apiLibraryScanAllPost($force)

Scans a given library for file changes. If another scan task is in progress, will reschedule the invocation for 3 hours in future.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\LibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$force = false; // bool | If true, will ignore any optimizations to avoid file I/O and will treat similar to a first scan

try {
    $apiInstance->apiLibraryScanAllPost($force);
} catch (Exception $e) {
    echo 'Exception when calling LibraryApi->apiLibraryScanAllPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **force** | **bool**| If true, will ignore any optimizations to avoid file I/O and will treat similar to a first scan | [optional] [default to false]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiLibraryScanFolderPost**
> apiLibraryScanFolderPost($body)

Given a valid path, will invoke either a Scan Series or Scan Library. If the folder does not exist within Kavita, the request will be ignored

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\LibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\ScanFolderDto(); // \Pbxg33k\KavitaClient\Model\ScanFolderDto | 

try {
    $apiInstance->apiLibraryScanFolderPost($body);
} catch (Exception $e) {
    echo 'Exception when calling LibraryApi->apiLibraryScanFolderPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\ScanFolderDto**](../Model/ScanFolderDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiLibraryScanMultiplePost**
> apiLibraryScanMultiplePost($body)

Enqueues a bunch of library scans

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\LibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\BulkActionDto(); // \Pbxg33k\KavitaClient\Model\BulkActionDto | 

try {
    $apiInstance->apiLibraryScanMultiplePost($body);
} catch (Exception $e) {
    echo 'Exception when calling LibraryApi->apiLibraryScanMultiplePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\BulkActionDto**](../Model/BulkActionDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiLibraryScanPost**
> apiLibraryScanPost($library_id, $force)

Scans a given library for file changes.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\LibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$library_id = 56; // int | 
$force = false; // bool | If true, will ignore any optimizations to avoid file I/O and will treat similar to a first scan

try {
    $apiInstance->apiLibraryScanPost($library_id, $force);
} catch (Exception $e) {
    echo 'Exception when calling LibraryApi->apiLibraryScanPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **library_id** | **int**|  | [optional]
 **force** | **bool**| If true, will ignore any optimizations to avoid file I/O and will treat similar to a first scan | [optional] [default to false]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiLibraryTypeGet**
> \Pbxg33k\KavitaClient\Model\LibraryType apiLibraryTypeGet($library_id)

Returns the type of the underlying library

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\LibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$library_id = 56; // int | 

try {
    $result = $apiInstance->apiLibraryTypeGet($library_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LibraryApi->apiLibraryTypeGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **library_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\LibraryType**](../Model/LibraryType.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiLibraryUpdatePost**
> apiLibraryUpdatePost($body)

Updates an existing Library with new name, folders, and/or type.

Any folder or type change will invoke a scan.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\LibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdateLibraryDto(); // \Pbxg33k\KavitaClient\Model\UpdateLibraryDto | 

try {
    $apiInstance->apiLibraryUpdatePost($body);
} catch (Exception $e) {
    echo 'Exception when calling LibraryApi->apiLibraryUpdatePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateLibraryDto**](../Model/UpdateLibraryDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiLibraryUserLibrariesGet**
> \Pbxg33k\KavitaClient\Model\LibraryDto[] apiLibraryUserLibrariesGet($user_id)

Gets libraries for the given user that you also have access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\LibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 56; // int | 

try {
    $result = $apiInstance->apiLibraryUserLibrariesGet($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LibraryApi->apiLibraryUserLibrariesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\LibraryDto[]**](../Model/LibraryDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

