# Pbxg33k\KavitaClient\MetadataApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiMetadataAgeRatingsGet**](MetadataApi.md#apimetadataageratingsget) | **GET** /api/Metadata/age-ratings | Fetches all age ratings from the instance
[**apiMetadataAllLanguagesGet**](MetadataApi.md#apimetadataalllanguagesget) | **GET** /api/Metadata/all-languages | Returns all languages Kavita can accept
[**apiMetadataGenresGet**](MetadataApi.md#apimetadatagenresget) | **GET** /api/Metadata/genres | Fetches genres from the instance
[**apiMetadataGenresWithCountsPost**](MetadataApi.md#apimetadatagenreswithcountspost) | **POST** /api/Metadata/genres-with-counts | Returns a list of Genres with counts for counts when Genre is on Series/Chapter
[**apiMetadataLanguageTitleGet**](MetadataApi.md#apimetadatalanguagetitleget) | **GET** /api/Metadata/language-title | Given a language code returns the display name
[**apiMetadataLanguagesGet**](MetadataApi.md#apimetadatalanguagesget) | **GET** /api/Metadata/languages | Fetches all age languages from the libraries passed (or if none passed, all in the server)
[**apiMetadataPeopleByRoleGet**](MetadataApi.md#apimetadatapeoplebyroleget) | **GET** /api/Metadata/people-by-role | Fetches people from the instance by role
[**apiMetadataPeopleGet**](MetadataApi.md#apimetadatapeopleget) | **GET** /api/Metadata/people | Fetches people from the instance
[**apiMetadataPublicationStatusGet**](MetadataApi.md#apimetadatapublicationstatusget) | **GET** /api/Metadata/publication-status | Fetches all publication status&#x27; from the instance
[**apiMetadataReadinglistTagsGet**](MetadataApi.md#apimetadatareadinglisttagsget) | **GET** /api/Metadata/readinglist-tags | Fetches Reading List Tags from the instance
[**apiMetadataSeriesDetailPlusGet**](MetadataApi.md#apimetadataseriesdetailplusget) | **GET** /api/Metadata/series-detail-plus | Fetches the details needed from Kavita+ for Series Detail page
[**apiMetadataTagsGet**](MetadataApi.md#apimetadatatagsget) | **GET** /api/Metadata/tags | Fetches all tags from the instance
[**apiMetadataTagsWithCountsPost**](MetadataApi.md#apimetadatatagswithcountspost) | **POST** /api/Metadata/tags-with-counts | Returns a list of Tags with counts for counts when Tag is on Series/Chapter

# **apiMetadataAgeRatingsGet**
> \Pbxg33k\KavitaClient\Model\AgeRatingDto[] apiMetadataAgeRatingsGet($library_ids)

Fetches all age ratings from the instance

This API is cached for 1 hour, varying by libraryIds

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\MetadataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$library_ids = "library_ids_example"; // string | String separated libraryIds or null for all ratings

try {
    $result = $apiInstance->apiMetadataAgeRatingsGet($library_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetadataApi->apiMetadataAgeRatingsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **library_ids** | **string**| String separated libraryIds or null for all ratings | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\AgeRatingDto[]**](../Model/AgeRatingDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiMetadataAllLanguagesGet**
> \Pbxg33k\KavitaClient\Model\LanguageDto[] apiMetadataAllLanguagesGet()

Returns all languages Kavita can accept

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\MetadataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiMetadataAllLanguagesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetadataApi->apiMetadataAllLanguagesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\LanguageDto[]**](../Model/LanguageDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiMetadataGenresGet**
> \Pbxg33k\KavitaClient\Model\GenreTagDto[] apiMetadataGenresGet($library_ids, $context)

Fetches genres from the instance

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\MetadataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$library_ids = "library_ids_example"; // string | String separated libraryIds or null for all genres
$context = new \Pbxg33k\KavitaClient\Model\QueryContext(); // \Pbxg33k\KavitaClient\Model\QueryContext | Context from which this API was invoked

try {
    $result = $apiInstance->apiMetadataGenresGet($library_ids, $context);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetadataApi->apiMetadataGenresGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **library_ids** | **string**| String separated libraryIds or null for all genres | [optional]
 **context** | [**\Pbxg33k\KavitaClient\Model\QueryContext**](../Model/.md)| Context from which this API was invoked | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\GenreTagDto[]**](../Model/GenreTagDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiMetadataGenresWithCountsPost**
> \Pbxg33k\KavitaClient\Model\BrowseGenreDto[] apiMetadataGenresWithCountsPost($body)

Returns a list of Genres with counts for counts when Genre is on Series/Chapter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\MetadataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UserParams(); // \Pbxg33k\KavitaClient\Model\UserParams | 

try {
    $result = $apiInstance->apiMetadataGenresWithCountsPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetadataApi->apiMetadataGenresWithCountsPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UserParams**](../Model/UserParams.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\BrowseGenreDto[]**](../Model/BrowseGenreDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiMetadataLanguageTitleGet**
> string apiMetadataLanguageTitleGet($code)

Given a language code returns the display name

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\MetadataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = "code_example"; // string | 

try {
    $result = $apiInstance->apiMetadataLanguageTitleGet($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetadataApi->apiMetadataLanguageTitleGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **code** | **string**|  | [optional]

### Return type

**string**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiMetadataLanguagesGet**
> \Pbxg33k\KavitaClient\Model\LanguageDto[] apiMetadataLanguagesGet($library_ids)

Fetches all age languages from the libraries passed (or if none passed, all in the server)

This does not perform RBS for the user if they have Library access due to the non-sensitive nature of languages

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\MetadataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$library_ids = "library_ids_example"; // string | String separated libraryIds or null for all ratings

try {
    $result = $apiInstance->apiMetadataLanguagesGet($library_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetadataApi->apiMetadataLanguagesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **library_ids** | **string**| String separated libraryIds or null for all ratings | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\LanguageDto[]**](../Model/LanguageDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiMetadataPeopleByRoleGet**
> \Pbxg33k\KavitaClient\Model\PersonDto[] apiMetadataPeopleByRoleGet($role)

Fetches people from the instance by role

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\MetadataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$role = new \Pbxg33k\KavitaClient\Model\PersonRole(); // \Pbxg33k\KavitaClient\Model\PersonRole | role

try {
    $result = $apiInstance->apiMetadataPeopleByRoleGet($role);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetadataApi->apiMetadataPeopleByRoleGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **role** | [**\Pbxg33k\KavitaClient\Model\PersonRole**](../Model/.md)| role | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\PersonDto[]**](../Model/PersonDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiMetadataPeopleGet**
> \Pbxg33k\KavitaClient\Model\PersonDto[] apiMetadataPeopleGet($library_ids)

Fetches people from the instance

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\MetadataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$library_ids = "library_ids_example"; // string | String separated libraryIds or null for all people

try {
    $result = $apiInstance->apiMetadataPeopleGet($library_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetadataApi->apiMetadataPeopleGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **library_ids** | **string**| String separated libraryIds or null for all people | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\PersonDto[]**](../Model/PersonDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiMetadataPublicationStatusGet**
> \Pbxg33k\KavitaClient\Model\AgeRatingDto[] apiMetadataPublicationStatusGet($library_ids)

Fetches all publication status' from the instance

This API is cached for 1 hour, varying by libraryIds

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\MetadataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$library_ids = "library_ids_example"; // string | String separated libraryIds or null for all publication status

try {
    $result = $apiInstance->apiMetadataPublicationStatusGet($library_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetadataApi->apiMetadataPublicationStatusGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **library_ids** | **string**| String separated libraryIds or null for all publication status | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\AgeRatingDto[]**](../Model/AgeRatingDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiMetadataReadinglistTagsGet**
> \Pbxg33k\KavitaClient\Model\ReadingListTagDto[] apiMetadataReadinglistTagsGet()

Fetches Reading List Tags from the instance

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\MetadataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiMetadataReadinglistTagsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetadataApi->apiMetadataReadinglistTagsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Pbxg33k\KavitaClient\Model\ReadingListTagDto[]**](../Model/ReadingListTagDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiMetadataSeriesDetailPlusGet**
> \Pbxg33k\KavitaClient\Model\SeriesDetailPlusDto apiMetadataSeriesDetailPlusGet($series_id, $library_type)

Fetches the details needed from Kavita+ for Series Detail page

This will hit upstream K+ if the data in local db is 2 weeks old

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\MetadataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | Series Id
$library_type = new \Pbxg33k\KavitaClient\Model\LibraryType(); // \Pbxg33k\KavitaClient\Model\LibraryType | Library Type

try {
    $result = $apiInstance->apiMetadataSeriesDetailPlusGet($series_id, $library_type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetadataApi->apiMetadataSeriesDetailPlusGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**| Series Id | [optional]
 **library_type** | [**\Pbxg33k\KavitaClient\Model\LibraryType**](../Model/.md)| Library Type | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\SeriesDetailPlusDto**](../Model/SeriesDetailPlusDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiMetadataTagsGet**
> \Pbxg33k\KavitaClient\Model\TagDto[] apiMetadataTagsGet($library_ids)

Fetches all tags from the instance

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\MetadataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$library_ids = "library_ids_example"; // string | String separated libraryIds or null for all tags

try {
    $result = $apiInstance->apiMetadataTagsGet($library_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetadataApi->apiMetadataTagsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **library_ids** | **string**| String separated libraryIds or null for all tags | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\TagDto[]**](../Model/TagDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiMetadataTagsWithCountsPost**
> \Pbxg33k\KavitaClient\Model\BrowseTagDto[] apiMetadataTagsWithCountsPost($body)

Returns a list of Tags with counts for counts when Tag is on Series/Chapter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\MetadataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\UserParams(); // \Pbxg33k\KavitaClient\Model\UserParams | 

try {
    $result = $apiInstance->apiMetadataTagsWithCountsPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetadataApi->apiMetadataTagsWithCountsPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\UserParams**](../Model/UserParams.md)|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\BrowseTagDto[]**](../Model/BrowseTagDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

