# Pbxg33k\KavitaClient\PersonApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiPersonAllPost**](PersonApi.md#apipersonallpost) | **POST** /api/Person/all | Returns a list of authors and artists for browsing
[**apiPersonChaptersByRoleGet**](PersonApi.md#apipersonchaptersbyroleget) | **GET** /api/Person/chapters-by-role | Returns all individual chapters by role. Limited to 20 results.
[**apiPersonFetchCoverPost**](PersonApi.md#apipersonfetchcoverpost) | **POST** /api/Person/fetch-cover | Attempts to download the cover from CoversDB (Note: Not yet release in Kavita)
[**apiPersonGet**](PersonApi.md#apipersonget) | **GET** /api/Person | 
[**apiPersonMergePost**](PersonApi.md#apipersonmergepost) | **POST** /api/Person/merge | Merges Persons into one, this action is irreversible
[**apiPersonRolesGet**](PersonApi.md#apipersonrolesget) | **GET** /api/Person/roles | Returns all roles for a Person
[**apiPersonSearchGet**](PersonApi.md#apipersonsearchget) | **GET** /api/Person/search | Find a person by name or alias against a query string
[**apiPersonSeriesKnownForGet**](PersonApi.md#apipersonseriesknownforget) | **GET** /api/Person/series-known-for | Returns the top 20 series that the \&quot;person\&quot; is known for. This will use Average Rating when applicable (Kavita+ field), else it&#x27;s a random sort
[**apiPersonUpdatePost**](PersonApi.md#apipersonupdatepost) | **POST** /api/Person/update | Updates the Person
[**apiPersonValidAliasPost**](PersonApi.md#apipersonvalidaliaspost) | **POST** /api/Person/valid-alias | Ensure the alias is valid to be added. For example, the alias cannot be on another person or be the same as the current person name/alias.

# **apiPersonAllPost**
> \Pbxg33k\KavitaClient\Model\BrowsePersonDto[] apiPersonAllPost($body, $page_number, $page_size)

Returns a list of authors and artists for browsing

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\PersonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\PersonFilterDto(); // \Pbxg33k\KavitaClient\Model\PersonFilterDto | 
$page_number = 56; // int | 
$page_size = 56; // int | 

try {
    $result = $apiInstance->apiPersonAllPost($body, $page_number, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PersonApi->apiPersonAllPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\PersonFilterDto**](../Model/PersonFilterDto.md)|  | [optional]
 **page_number** | **int**|  | [optional]
 **page_size** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\BrowsePersonDto[]**](../Model/BrowsePersonDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiPersonChaptersByRoleGet**
> \Pbxg33k\KavitaClient\Model\StandaloneChapterDto[] apiPersonChaptersByRoleGet($person_id, $role)

Returns all individual chapters by role. Limited to 20 results.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\PersonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$person_id = 56; // int | 
$role = new \Pbxg33k\KavitaClient\Model\PersonRole(); // \Pbxg33k\KavitaClient\Model\PersonRole | 

try {
    $result = $apiInstance->apiPersonChaptersByRoleGet($person_id, $role);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PersonApi->apiPersonChaptersByRoleGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **person_id** | **int**|  | [optional]
 **role** | [**\Pbxg33k\KavitaClient\Model\PersonRole**](../Model/.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\StandaloneChapterDto[]**](../Model/StandaloneChapterDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiPersonFetchCoverPost**
> string apiPersonFetchCoverPost($person_id)

Attempts to download the cover from CoversDB (Note: Not yet release in Kavita)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\PersonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$person_id = 56; // int | 

try {
    $result = $apiInstance->apiPersonFetchCoverPost($person_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PersonApi->apiPersonFetchCoverPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **person_id** | **int**|  | [optional]

### Return type

**string**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiPersonGet**
> \Pbxg33k\KavitaClient\Model\PersonDto apiPersonGet($name)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\PersonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | 

try {
    $result = $apiInstance->apiPersonGet($name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PersonApi->apiPersonGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\PersonDto**](../Model/PersonDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiPersonMergePost**
> \Pbxg33k\KavitaClient\Model\PersonDto apiPersonMergePost($body)

Merges Persons into one, this action is irreversible

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\PersonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\PersonMergeDto(); // \Pbxg33k\KavitaClient\Model\PersonMergeDto | 

try {
    $result = $apiInstance->apiPersonMergePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PersonApi->apiPersonMergePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\PersonMergeDto**](../Model/PersonMergeDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\PersonDto**](../Model/PersonDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiPersonRolesGet**
> \Pbxg33k\KavitaClient\Model\PersonRole[] apiPersonRolesGet($person_id)

Returns all roles for a Person

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\PersonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$person_id = 56; // int | 

try {
    $result = $apiInstance->apiPersonRolesGet($person_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PersonApi->apiPersonRolesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **person_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\PersonRole[]**](../Model/PersonRole.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiPersonSearchGet**
> \Pbxg33k\KavitaClient\Model\PersonDto[] apiPersonSearchGet($query_string)

Find a person by name or alias against a query string

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\PersonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query_string = "query_string_example"; // string | 

try {
    $result = $apiInstance->apiPersonSearchGet($query_string);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PersonApi->apiPersonSearchGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query_string** | **string**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\PersonDto[]**](../Model/PersonDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiPersonSeriesKnownForGet**
> \Pbxg33k\KavitaClient\Model\SeriesDto[] apiPersonSeriesKnownForGet($person_id)

Returns the top 20 series that the \"person\" is known for. This will use Average Rating when applicable (Kavita+ field), else it's a random sort

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\PersonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$person_id = 56; // int | 

try {
    $result = $apiInstance->apiPersonSeriesKnownForGet($person_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PersonApi->apiPersonSeriesKnownForGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **person_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\SeriesDto[]**](../Model/SeriesDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiPersonUpdatePost**
> \Pbxg33k\KavitaClient\Model\PersonDto apiPersonUpdatePost($body)

Updates the Person

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\PersonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UpdatePersonDto(); // \Pbxg33k\KavitaClient\Model\UpdatePersonDto | 

try {
    $result = $apiInstance->apiPersonUpdatePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PersonApi->apiPersonUpdatePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UpdatePersonDto**](../Model/UpdatePersonDto.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\PersonDto**](../Model/PersonDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiPersonValidAliasPost**
> bool apiPersonValidAliasPost($body)

Ensure the alias is valid to be added. For example, the alias cannot be on another person or be the same as the current person name/alias.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\PersonApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\PersonAliasCheckDto(); // \Pbxg33k\KavitaClient\Model\PersonAliasCheckDto | alias check request

try {
    $result = $apiInstance->apiPersonValidAliasPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PersonApi->apiPersonValidAliasPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\PersonAliasCheckDto**](../Model/PersonAliasCheckDto.md)| alias check request | [optional]

### Return type

**bool**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

