# Pbxg33k\KavitaClient\CblApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiCblBrowseGet**](CblApi.md#apicblbrowseget) | **GET** /api/Cbl/browse | Provides the browse CBL Repo interface. Requires Download role.
[**apiCblFileImportPost**](CblApi.md#apicblfileimportpost) | **POST** /api/Cbl/file-import | Saves an uploaded CBL file to disk without importing. Returns the saved file info.
[**apiCblFinalizeImportPost**](CblApi.md#apicblfinalizeimportpost) | **POST** /api/Cbl/finalize-import | Finalizes the import of a saved CBL file with user decisions
[**apiCblReValidatePost**](CblApi.md#apicblrevalidatepost) | **POST** /api/Cbl/re-validate | Validates an already-saved CBL file on disk. Called by the import modal after remap rule changes.
[**apiCblRemapRulesAllGet**](CblApi.md#apicblremaprulesallget) | **GET** /api/Cbl/remap-rules/all | Returns all rules across all users
[**apiCblRemapRulesGet**](CblApi.md#apicblremaprulesget) | **GET** /api/Cbl/remap-rules | Returns all remap rules accessible to the current user (own rules + global/admin rules).
[**apiCblRemapRulesIdDelete**](CblApi.md#apicblremaprulesiddelete) | **DELETE** /api/Cbl/remap-rules/{id} | Deletes a remap rule. Users can only delete their own rules.
[**apiCblRemapRulesIdDemotePost**](CblApi.md#apicblremaprulesiddemotepost) | **POST** /api/Cbl/remap-rules/{id}/demote | Demotes a global remap rule back to user-scoped. Admin-only.
[**apiCblRemapRulesIdPost**](CblApi.md#apicblremaprulesidpost) | **POST** /api/Cbl/remap-rules/{id} | Updates a remap rule with issue-level detail (volume/chapter).
[**apiCblRemapRulesIdPromotePost**](CblApi.md#apicblremaprulesidpromotepost) | **POST** /api/Cbl/remap-rules/{id}/promote | Promotes a remap rule to global scope. Admin-only.
[**apiCblRemapRulesPost**](CblApi.md#apicblremaprulespost) | **POST** /api/Cbl/remap-rules | Creates a new remap rule, or updates an existing one if a rule with the same CBL matching key (normalized name + volume + number) already exists for this user. When no explicit VolumeId is provided, attempts to auto-resolve a matching volume on the target series from the CBL volume string.
[**apiCblRepoImportPost**](CblApi.md#apicblrepoimportpost) | **POST** /api/Cbl/repo-import | Downloads selected CBL files from the GitHub repo and saves them to disk without importing.
[**apiCblSyncPost**](CblApi.md#apicblsyncpost) | **POST** /api/Cbl/sync | Enqueues the Reading List to be synced on a background thread. UI will be informed from Kavita.Models.DTOs.SignalR.MessageFactory.ReadingListUpdated event
[**apiCblUploadCblFilePost**](CblApi.md#apicbluploadcblfilepost) | **POST** /api/Cbl/upload-cbl-file | Downloads a CBL file from a URL and saves it to disk without importing.

# **apiCblBrowseGet**
> \Pbxg33k\KavitaClient\Model\CblRepoBrowseResultDto apiCblBrowseGet($path)

Provides the browse CBL Repo interface. Requires Download role.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CblApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$path = ""; // string | 

try {
    $result = $apiInstance->apiCblBrowseGet($path);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CblApi->apiCblBrowseGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **path** | **string**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\CblRepoBrowseResultDto**](../Model/CblRepoBrowseResultDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCblFileImportPost**
> \Pbxg33k\KavitaClient\Model\CblSavedFileDto apiCblFileImportPost($cbl_file)

Saves an uploaded CBL file to disk without importing. Returns the saved file info.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CblApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$cbl_file = "cbl_file_example"; // string | 

try {
    $result = $apiInstance->apiCblFileImportPost($cbl_file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CblApi->apiCblFileImportPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cbl_file** | **string****string**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\CblSavedFileDto**](../Model/CblSavedFileDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCblFinalizeImportPost**
> \Pbxg33k\KavitaClient\Model\CblImportSummaryDto apiCblFinalizeImportPost($body)

Finalizes the import of a saved CBL file with user decisions

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CblApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\CblFinalizeRequestDto(); // \Pbxg33k\KavitaClient\Model\CblFinalizeRequestDto | 

try {
    $result = $apiInstance->apiCblFinalizeImportPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CblApi->apiCblFinalizeImportPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\CblFinalizeRequestDto**](../Model/CblFinalizeRequestDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\CblImportSummaryDto**](../Model/CblImportSummaryDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCblReValidatePost**
> \Pbxg33k\KavitaClient\Model\CblImportSummaryDto apiCblReValidatePost($body)

Validates an already-saved CBL file on disk. Called by the import modal after remap rule changes.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CblApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\CblReValidateRequestDto(); // \Pbxg33k\KavitaClient\Model\CblReValidateRequestDto | 

try {
    $result = $apiInstance->apiCblReValidatePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CblApi->apiCblReValidatePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\CblReValidateRequestDto**](../Model/CblReValidateRequestDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\CblImportSummaryDto**](../Model/CblImportSummaryDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCblRemapRulesAllGet**
> \Pbxg33k\KavitaClient\Model\RemapRuleDto[] apiCblRemapRulesAllGet()

Returns all rules across all users

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CblApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiCblRemapRulesAllGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CblApi->apiCblRemapRulesAllGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\RemapRuleDto[]**](../Model/RemapRuleDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCblRemapRulesGet**
> \Pbxg33k\KavitaClient\Model\RemapRuleDto[] apiCblRemapRulesGet()

Returns all remap rules accessible to the current user (own rules + global/admin rules).

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CblApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiCblRemapRulesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CblApi->apiCblRemapRulesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\RemapRuleDto[]**](../Model/RemapRuleDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCblRemapRulesIdDelete**
> apiCblRemapRulesIdDelete($id)

Deletes a remap rule. Users can only delete their own rules.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CblApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | 

try {
    $apiInstance->apiCblRemapRulesIdDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling CblApi->apiCblRemapRulesIdDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**|  |

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCblRemapRulesIdDemotePost**
> \Pbxg33k\KavitaClient\Model\RemapRuleDto apiCblRemapRulesIdDemotePost($id)

Demotes a global remap rule back to user-scoped. Admin-only.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CblApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | 

try {
    $result = $apiInstance->apiCblRemapRulesIdDemotePost($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CblApi->apiCblRemapRulesIdDemotePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**|  |

### Return type

[**\Pbxg33k\KavitaClient\Model\RemapRuleDto**](../Model/RemapRuleDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCblRemapRulesIdPost**
> \Pbxg33k\KavitaClient\Model\RemapRuleDto apiCblRemapRulesIdPost($id, $body)

Updates a remap rule with issue-level detail (volume/chapter).

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CblApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | 
$body = new \Pbxg33k\KavitaClient\Model\UpdateRemapRuleDto(); // \Pbxg33k\KavitaClient\Model\UpdateRemapRuleDto | 

try {
    $result = $apiInstance->apiCblRemapRulesIdPost($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CblApi->apiCblRemapRulesIdPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**|  |
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdateRemapRuleDto**](../Model/UpdateRemapRuleDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\RemapRuleDto**](../Model/RemapRuleDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCblRemapRulesIdPromotePost**
> \Pbxg33k\KavitaClient\Model\RemapRuleDto apiCblRemapRulesIdPromotePost($id)

Promotes a remap rule to global scope. Admin-only.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CblApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | 

try {
    $result = $apiInstance->apiCblRemapRulesIdPromotePost($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CblApi->apiCblRemapRulesIdPromotePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**|  |

### Return type

[**\Pbxg33k\KavitaClient\Model\RemapRuleDto**](../Model/RemapRuleDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCblRemapRulesPost**
> \Pbxg33k\KavitaClient\Model\RemapRuleDto apiCblRemapRulesPost($body)

Creates a new remap rule, or updates an existing one if a rule with the same CBL matching key (normalized name + volume + number) already exists for this user. When no explicit VolumeId is provided, attempts to auto-resolve a matching volume on the target series from the CBL volume string.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CblApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\CreateRemapRuleDto(); // \Pbxg33k\KavitaClient\Model\CreateRemapRuleDto | 

try {
    $result = $apiInstance->apiCblRemapRulesPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CblApi->apiCblRemapRulesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\CreateRemapRuleDto**](../Model/CreateRemapRuleDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\RemapRuleDto**](../Model/RemapRuleDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCblRepoImportPost**
> \Pbxg33k\KavitaClient\Model\CblSavedFileDto[] apiCblRepoImportPost($body)

Downloads selected CBL files from the GitHub repo and saves them to disk without importing.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CblApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\CblRepoImportRequestDto(); // \Pbxg33k\KavitaClient\Model\CblRepoImportRequestDto | 

try {
    $result = $apiInstance->apiCblRepoImportPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CblApi->apiCblRepoImportPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\CblRepoImportRequestDto**](../Model/CblRepoImportRequestDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\CblSavedFileDto[]**](../Model/CblSavedFileDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCblSyncPost**
> apiCblSyncPost($reading_list_id, $force)

Enqueues the Reading List to be synced on a background thread. UI will be informed from Kavita.Models.DTOs.SignalR.MessageFactory.ReadingListUpdated event

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CblApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reading_list_id = 56; // int | 
$force = false; // bool | Ignore Hash and force sync flow

try {
    $apiInstance->apiCblSyncPost($reading_list_id, $force);
} catch (Exception $e) {
    echo 'Exception when calling CblApi->apiCblSyncPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **reading_list_id** | **int**|  | [optional]
 **force** | **bool**| Ignore Hash and force sync flow | [optional] [default to false]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiCblUploadCblFilePost**
> \Pbxg33k\KavitaClient\Model\CblSavedFileDto apiCblUploadCblFilePost($body)

Downloads a CBL file from a URL and saves it to disk without importing.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\CblApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UploadUrlDto(); // \Pbxg33k\KavitaClient\Model\UploadUrlDto | 

try {
    $result = $apiInstance->apiCblUploadCblFilePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CblApi->apiCblUploadCblFilePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UploadUrlDto**](../Model/UploadUrlDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\CblSavedFileDto**](../Model/CblSavedFileDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

