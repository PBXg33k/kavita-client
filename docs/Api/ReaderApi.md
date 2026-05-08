# Pbxg33k\KavitaClient\ReaderApi

All URIs are relative to *{protocol}://{hostpath}*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiReaderAllBookmarksPost**](ReaderApi.md#apireaderallbookmarkspost) | **POST** /api/Reader/all-bookmarks | Returns a list of all bookmarked pages for a User
[**apiReaderBookmarkImageGet**](ReaderApi.md#apireaderbookmarkimageget) | **GET** /api/Reader/bookmark-image | Returns an image for a given bookmark series. Side effect: This will cache the bookmark images for reading.
[**apiReaderBookmarkInfoGet**](ReaderApi.md#apireaderbookmarkinfoget) | **GET** /api/Reader/bookmark-info | Returns various information about all bookmark files for a Series. Side effect: This will cache the bookmark images for reading.
[**apiReaderBookmarkPost**](ReaderApi.md#apireaderbookmarkpost) | **POST** /api/Reader/bookmark | Bookmarks a page against a Chapter
[**apiReaderBulkRemoveBookmarksPost**](ReaderApi.md#apireaderbulkremovebookmarkspost) | **POST** /api/Reader/bulk-remove-bookmarks | Removes all bookmarks for all chapters linked to a Series
[**apiReaderChapterBookmarksGet**](ReaderApi.md#apireaderchapterbookmarksget) | **GET** /api/Reader/chapter-bookmarks | Returns a list of bookmarked pages for a given Chapter
[**apiReaderChapterInfoGet**](ReaderApi.md#apireaderchapterinfoget) | **GET** /api/Reader/chapter-info | Returns various information about a Chapter. Side effect: This will cache the chapter images for reading.
[**apiReaderContinuePointGet**](ReaderApi.md#apireadercontinuepointget) | **GET** /api/Reader/continue-point | Continue point is the chapter which you should start reading again from. If there is no progress on a series, then the first chapter will be returned (non-special unless only specials). Otherwise, loop through the chapters and volumes in order to find the next chapter which has progress.
[**apiReaderCreatePtocPost**](ReaderApi.md#apireadercreateptocpost) | **POST** /api/Reader/create-ptoc | Create a new personal table of content entry for a given chapter
[**apiReaderFileDimensionsGet**](ReaderApi.md#apireaderfiledimensionsget) | **GET** /api/Reader/file-dimensions | Returns the file dimensions for all pages in a chapter. If the underlying chapter is PDF, use extractPDF to unpack as images.
[**apiReaderFirstProgressDateGet**](ReaderApi.md#apireaderfirstprogressdateget) | **GET** /api/Reader/first-progress-date | 
[**apiReaderGetProgressGet**](ReaderApi.md#apireadergetprogressget) | **GET** /api/Reader/get-progress | Returns Progress (page number) for a chapter for the logged in user
[**apiReaderHasProgressGet**](ReaderApi.md#apireaderhasprogressget) | **GET** /api/Reader/has-progress | Returns if the user has reading progress on the Series
[**apiReaderImageGet**](ReaderApi.md#apireaderimageget) | **GET** /api/Reader/image | Returns an image for a given chapter. Will perform bounding checks
[**apiReaderMarkChapterReadPost**](ReaderApi.md#apireadermarkchapterreadpost) | **POST** /api/Reader/mark-chapter-read | Mark a single chapter as read
[**apiReaderMarkMultipleReadPost**](ReaderApi.md#apireadermarkmultiplereadpost) | **POST** /api/Reader/mark-multiple-read | Marks all chapters within a list of volumes as Read. All volumes must belong to the same Series.
[**apiReaderMarkMultipleSeriesReadPost**](ReaderApi.md#apireadermarkmultipleseriesreadpost) | **POST** /api/Reader/mark-multiple-series-read | Marks all chapters within a list of series as Read.
[**apiReaderMarkMultipleSeriesUnreadPost**](ReaderApi.md#apireadermarkmultipleseriesunreadpost) | **POST** /api/Reader/mark-multiple-series-unread | Marks all chapters within a list of series as Unread.
[**apiReaderMarkMultipleUnreadPost**](ReaderApi.md#apireadermarkmultipleunreadpost) | **POST** /api/Reader/mark-multiple-unread | Marks all chapters within a list of volumes as Unread. All volumes must belong to the same Series.
[**apiReaderMarkReadPost**](ReaderApi.md#apireadermarkreadpost) | **POST** /api/Reader/mark-read | Marks a Series as read. All volumes and chapters will be marked as read during this process.
[**apiReaderMarkUnreadPost**](ReaderApi.md#apireadermarkunreadpost) | **POST** /api/Reader/mark-unread | Marks a Series as Unread. All volumes and chapters will be marked as unread during this process.
[**apiReaderMarkVolumeReadPost**](ReaderApi.md#apireadermarkvolumereadpost) | **POST** /api/Reader/mark-volume-read | Marks all chapters within a volume as Read
[**apiReaderMarkVolumeUnreadPost**](ReaderApi.md#apireadermarkvolumeunreadpost) | **POST** /api/Reader/mark-volume-unread | Marks all chapters within a volume as unread
[**apiReaderNextChapterGet**](ReaderApi.md#apireadernextchapterget) | **GET** /api/Reader/next-chapter | Returns the next logical chapter from the series.
[**apiReaderPdfGet**](ReaderApi.md#apireaderpdfget) | **GET** /api/Reader/pdf | Returns the PDF for the chapterId.
[**apiReaderPrevChapterGet**](ReaderApi.md#apireaderprevchapterget) | **GET** /api/Reader/prev-chapter | Returns the previous logical chapter from the series.
[**apiReaderProgressPost**](ReaderApi.md#apireaderprogresspost) | **POST** /api/Reader/progress | Save page against Chapter for authenticated user
[**apiReaderPromptRereadChapterGet**](ReaderApi.md#apireaderpromptrereadchapterget) | **GET** /api/Reader/prompt-reread/chapter | Check if we should prompt the user for rereads for the given chapter
[**apiReaderPromptRereadSeriesGet**](ReaderApi.md#apireaderpromptrereadseriesget) | **GET** /api/Reader/prompt-reread/series | Check if we should prompt the user for rereads for the given series
[**apiReaderPromptRereadVolumeGet**](ReaderApi.md#apireaderpromptrereadvolumeget) | **GET** /api/Reader/prompt-reread/volume | Check if we should prompt the user for rereads for the given volume
[**apiReaderPtocDelete**](ReaderApi.md#apireaderptocdelete) | **DELETE** /api/Reader/ptoc | Deletes the user&#x27;s personal table of content for the given chapter
[**apiReaderPtocGet**](ReaderApi.md#apireaderptocget) | **GET** /api/Reader/ptoc | Returns the user&#x27;s personal table of contents for the given chapter
[**apiReaderRemoveBookmarksPost**](ReaderApi.md#apireaderremovebookmarkspost) | **POST** /api/Reader/remove-bookmarks | Removes all bookmarks for all chapters linked to a Series
[**apiReaderSeriesBookmarksGet**](ReaderApi.md#apireaderseriesbookmarksget) | **GET** /api/Reader/series-bookmarks | Returns all bookmarked pages for a given series
[**apiReaderThumbnailGet**](ReaderApi.md#apireaderthumbnailget) | **GET** /api/Reader/thumbnail | Returns a thumbnail for the given page number
[**apiReaderTimeLeftForChapterGet**](ReaderApi.md#apireadertimeleftforchapterget) | **GET** /api/Reader/time-left-for-chapter | For the current user, returns an estimate on how long it would take to finish reading the chapter.
[**apiReaderTimeLeftGet**](ReaderApi.md#apireadertimeleftget) | **GET** /api/Reader/time-left | For the current user, returns an estimate on how long it would take to finish reading the series.
[**apiReaderUnbookmarkPost**](ReaderApi.md#apireaderunbookmarkpost) | **POST** /api/Reader/unbookmark | Removes a bookmarked page for a Chapter
[**apiReaderVolumeBookmarksGet**](ReaderApi.md#apireadervolumebookmarksget) | **GET** /api/Reader/volume-bookmarks | Returns all bookmarked pages for a given volume

# **apiReaderAllBookmarksPost**
> \Pbxg33k\KavitaClient\Model\BookmarkDto[] apiReaderAllBookmarksPost($body)

Returns a list of all bookmarked pages for a User

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\SeriesFilterV2Dto(); // \Pbxg33k\KavitaClient\Model\SeriesFilterV2Dto | Only supports SeriesNameQuery

try {
    $result = $apiInstance->apiReaderAllBookmarksPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderAllBookmarksPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\SeriesFilterV2Dto**](../Model/SeriesFilterV2Dto.md)| Only supports SeriesNameQuery | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\BookmarkDto[]**](../Model/BookmarkDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderBookmarkImageGet**
> apiReaderBookmarkImageGet($series_id, $api_key, $page)

Returns an image for a given bookmark series. Side effect: This will cache the bookmark images for reading.

We must use api key as bookmarks could be leaked to other users via the API

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 
$api_key = "api_key_example"; // string | Api key for the user the bookmarks are on
$page = 56; // int | 

try {
    $apiInstance->apiReaderBookmarkImageGet($series_id, $api_key, $page);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderBookmarkImageGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]
 **api_key** | **string**| Api key for the user the bookmarks are on | [optional]
 **page** | **int**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderBookmarkInfoGet**
> \Pbxg33k\KavitaClient\Model\BookmarkInfoDto apiReaderBookmarkInfoGet($series_id, $include_dimensions)

Returns various information about all bookmark files for a Series. Side effect: This will cache the bookmark images for reading.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | Series Id for all bookmarks
$include_dimensions = true; // bool | Include file dimensions (extra I/O). Defaults to true.

try {
    $result = $apiInstance->apiReaderBookmarkInfoGet($series_id, $include_dimensions);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderBookmarkInfoGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**| Series Id for all bookmarks | [optional]
 **include_dimensions** | **bool**| Include file dimensions (extra I/O). Defaults to true. | [optional] [default to true]

### Return type

[**\Pbxg33k\KavitaClient\Model\BookmarkInfoDto**](../Model/BookmarkInfoDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderBookmarkPost**
> apiReaderBookmarkPost($body)

Bookmarks a page against a Chapter

This has a side effect of caching the chapter files to disk

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\BookmarkDto(); // \Pbxg33k\KavitaClient\Model\BookmarkDto | 

try {
    $apiInstance->apiReaderBookmarkPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderBookmarkPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\BookmarkDto**](../Model/BookmarkDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderBulkRemoveBookmarksPost**
> apiReaderBulkRemoveBookmarksPost($body)

Removes all bookmarks for all chapters linked to a Series

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\BulkRemoveBookmarkForSeriesDto(); // \Pbxg33k\KavitaClient\Model\BulkRemoveBookmarkForSeriesDto | 

try {
    $apiInstance->apiReaderBulkRemoveBookmarksPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderBulkRemoveBookmarksPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\BulkRemoveBookmarkForSeriesDto**](../Model/BulkRemoveBookmarkForSeriesDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderChapterBookmarksGet**
> \Pbxg33k\KavitaClient\Model\BookmarkDto[] apiReaderChapterBookmarksGet($chapter_id)

Returns a list of bookmarked pages for a given Chapter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 

try {
    $result = $apiInstance->apiReaderChapterBookmarksGet($chapter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderChapterBookmarksGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\BookmarkDto[]**](../Model/BookmarkDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderChapterInfoGet**
> \Pbxg33k\KavitaClient\Model\ChapterInfoDto apiReaderChapterInfoGet($chapter_id, $extract_pdf, $include_dimensions)

Returns various information about a Chapter. Side effect: This will cache the chapter images for reading.

This is generally the first call when attempting to read to allow pre-generation of assets needed for reading

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 
$extract_pdf = false; // bool | Should Kavita extract pdf into images. Defaults to false.
$include_dimensions = false; // bool | Include file dimensions. Only useful for image-based reading

try {
    $result = $apiInstance->apiReaderChapterInfoGet($chapter_id, $extract_pdf, $include_dimensions);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderChapterInfoGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  | [optional]
 **extract_pdf** | **bool**| Should Kavita extract pdf into images. Defaults to false. | [optional] [default to false]
 **include_dimensions** | **bool**| Include file dimensions. Only useful for image-based reading | [optional] [default to false]

### Return type

[**\Pbxg33k\KavitaClient\Model\ChapterInfoDto**](../Model/ChapterInfoDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderContinuePointGet**
> \Pbxg33k\KavitaClient\Model\ChapterDto apiReaderContinuePointGet($series_id)

Continue point is the chapter which you should start reading again from. If there is no progress on a series, then the first chapter will be returned (non-special unless only specials). Otherwise, loop through the chapters and volumes in order to find the next chapter which has progress.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $result = $apiInstance->apiReaderContinuePointGet($series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderContinuePointGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ChapterDto**](../Model/ChapterDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderCreatePtocPost**
> apiReaderCreatePtocPost($body)

Create a new personal table of content entry for a given chapter

The title and page number must be unique to that book

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\CreatePersonalToCDto(); // \Pbxg33k\KavitaClient\Model\CreatePersonalToCDto | 

try {
    $apiInstance->apiReaderCreatePtocPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderCreatePtocPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\CreatePersonalToCDto**](../Model/CreatePersonalToCDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderFileDimensionsGet**
> \Pbxg33k\KavitaClient\Model\FileDimensionDto[] apiReaderFileDimensionsGet($chapter_id, $extract_pdf)

Returns the file dimensions for all pages in a chapter. If the underlying chapter is PDF, use extractPDF to unpack as images.

This has a side effect of caching the images.             This will only be populated on archive filetypes and not in bookmark mode

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 
$extract_pdf = false; // bool | 

try {
    $result = $apiInstance->apiReaderFileDimensionsGet($chapter_id, $extract_pdf);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderFileDimensionsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  | [optional]
 **extract_pdf** | **bool**|  | [optional] [default to false]

### Return type

[**\Pbxg33k\KavitaClient\Model\FileDimensionDto[]**](../Model/FileDimensionDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderFirstProgressDateGet**
> \DateTime apiReaderFirstProgressDateGet($user_id)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 56; // int | 

try {
    $result = $apiInstance->apiReaderFirstProgressDateGet($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderFirstProgressDateGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **int**|  | [optional]

### Return type

[**\DateTime**](../Model/\DateTime.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderGetProgressGet**
> \Pbxg33k\KavitaClient\Model\ProgressDto apiReaderGetProgressGet($chapter_id)

Returns Progress (page number) for a chapter for the logged in user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 

try {
    $result = $apiInstance->apiReaderGetProgressGet($chapter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderGetProgressGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\ProgressDto**](../Model/ProgressDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderHasProgressGet**
> bool apiReaderHasProgressGet($series_id)

Returns if the user has reading progress on the Series

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $result = $apiInstance->apiReaderHasProgressGet($series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderHasProgressGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]

### Return type

**bool**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderImageGet**
> apiReaderImageGet($chapter_id, $page, $api_key, $extract_pdf)

Returns an image for a given chapter. Will perform bounding checks

This will cache the chapter images for reading

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | Chapter Id
$page = 56; // int | Page in question
$api_key = "api_key_example"; // string | User's API Key for authentication
$extract_pdf = false; // bool | Should Kavita extract pdf into images. Defaults to false.

try {
    $apiInstance->apiReaderImageGet($chapter_id, $page, $api_key, $extract_pdf);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderImageGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**| Chapter Id | [optional]
 **page** | **int**| Page in question | [optional]
 **api_key** | **string**| User&#x27;s API Key for authentication | [optional]
 **extract_pdf** | **bool**| Should Kavita extract pdf into images. Defaults to false. | [optional] [default to false]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderMarkChapterReadPost**
> apiReaderMarkChapterReadPost($body)

Mark a single chapter as read

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\MarkChapterReadDto(); // \Pbxg33k\KavitaClient\Model\MarkChapterReadDto | 

try {
    $apiInstance->apiReaderMarkChapterReadPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderMarkChapterReadPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\MarkChapterReadDto**](../Model/MarkChapterReadDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderMarkMultipleReadPost**
> apiReaderMarkMultipleReadPost($body)

Marks all chapters within a list of volumes as Read. All volumes must belong to the same Series.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\MarkVolumesReadDto(); // \Pbxg33k\KavitaClient\Model\MarkVolumesReadDto | 

try {
    $apiInstance->apiReaderMarkMultipleReadPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderMarkMultipleReadPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\MarkVolumesReadDto**](../Model/MarkVolumesReadDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderMarkMultipleSeriesReadPost**
> apiReaderMarkMultipleSeriesReadPost($body)

Marks all chapters within a list of series as Read.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\MarkMultipleSeriesAsReadDto(); // \Pbxg33k\KavitaClient\Model\MarkMultipleSeriesAsReadDto | 

try {
    $apiInstance->apiReaderMarkMultipleSeriesReadPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderMarkMultipleSeriesReadPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\MarkMultipleSeriesAsReadDto**](../Model/MarkMultipleSeriesAsReadDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderMarkMultipleSeriesUnreadPost**
> apiReaderMarkMultipleSeriesUnreadPost($body)

Marks all chapters within a list of series as Unread.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\MarkMultipleSeriesAsReadDto(); // \Pbxg33k\KavitaClient\Model\MarkMultipleSeriesAsReadDto | 

try {
    $apiInstance->apiReaderMarkMultipleSeriesUnreadPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderMarkMultipleSeriesUnreadPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\MarkMultipleSeriesAsReadDto**](../Model/MarkMultipleSeriesAsReadDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderMarkMultipleUnreadPost**
> apiReaderMarkMultipleUnreadPost($body)

Marks all chapters within a list of volumes as Unread. All volumes must belong to the same Series.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\MarkVolumesReadDto(); // \Pbxg33k\KavitaClient\Model\MarkVolumesReadDto | 

try {
    $apiInstance->apiReaderMarkMultipleUnreadPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderMarkMultipleUnreadPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\MarkVolumesReadDto**](../Model/MarkVolumesReadDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderMarkReadPost**
> apiReaderMarkReadPost($body)

Marks a Series as read. All volumes and chapters will be marked as read during this process.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\MarkReadDto(); // \Pbxg33k\KavitaClient\Model\MarkReadDto | 

try {
    $apiInstance->apiReaderMarkReadPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderMarkReadPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\MarkReadDto**](../Model/MarkReadDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderMarkUnreadPost**
> apiReaderMarkUnreadPost($body)

Marks a Series as Unread. All volumes and chapters will be marked as unread during this process.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\MarkReadDto(); // \Pbxg33k\KavitaClient\Model\MarkReadDto | 

try {
    $apiInstance->apiReaderMarkUnreadPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderMarkUnreadPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\MarkReadDto**](../Model/MarkReadDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderMarkVolumeReadPost**
> apiReaderMarkVolumeReadPost($body)

Marks all chapters within a volume as Read

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\MarkVolumeReadDto(); // \Pbxg33k\KavitaClient\Model\MarkVolumeReadDto | 

try {
    $apiInstance->apiReaderMarkVolumeReadPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderMarkVolumeReadPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\MarkVolumeReadDto**](../Model/MarkVolumeReadDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderMarkVolumeUnreadPost**
> apiReaderMarkVolumeUnreadPost($body)

Marks all chapters within a volume as unread

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\MarkVolumeReadDto(); // \Pbxg33k\KavitaClient\Model\MarkVolumeReadDto | 

try {
    $apiInstance->apiReaderMarkVolumeUnreadPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderMarkVolumeUnreadPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\MarkVolumeReadDto**](../Model/MarkVolumeReadDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderNextChapterGet**
> int apiReaderNextChapterGet($series_id, $volume_id, $current_chapter_id)

Returns the next logical chapter from the series.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 
$volume_id = 56; // int | 
$current_chapter_id = 56; // int | 

try {
    $result = $apiInstance->apiReaderNextChapterGet($series_id, $volume_id, $current_chapter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderNextChapterGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]
 **volume_id** | **int**|  | [optional]
 **current_chapter_id** | **int**|  | [optional]

### Return type

**int**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderPdfGet**
> apiReaderPdfGet($chapter_id, $api_key, $extract_pdf)

Returns the PDF for the chapterId.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 
$api_key = "api_key_example"; // string | Auth Key for authentication
$extract_pdf = false; // bool | Converts PDF into images per-page - Used for Mihon mainly

try {
    $apiInstance->apiReaderPdfGet($chapter_id, $api_key, $extract_pdf);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderPdfGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  | [optional]
 **api_key** | **string**| Auth Key for authentication | [optional]
 **extract_pdf** | **bool**| Converts PDF into images per-page - Used for Mihon mainly | [optional] [default to false]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderPrevChapterGet**
> int apiReaderPrevChapterGet($series_id, $volume_id, $current_chapter_id)

Returns the previous logical chapter from the series.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 
$volume_id = 56; // int | 
$current_chapter_id = 56; // int | 

try {
    $result = $apiInstance->apiReaderPrevChapterGet($series_id, $volume_id, $current_chapter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderPrevChapterGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]
 **volume_id** | **int**|  | [optional]
 **current_chapter_id** | **int**|  | [optional]

### Return type

**int**

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderProgressPost**
> apiReaderProgressPost($body)

Save page against Chapter for authenticated user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\ProgressDto(); // \Pbxg33k\KavitaClient\Model\ProgressDto | 

try {
    $apiInstance->apiReaderProgressPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderProgressPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\ProgressDto**](../Model/ProgressDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderPromptRereadChapterGet**
> \Pbxg33k\KavitaClient\Model\RereadDto apiReaderPromptRereadChapterGet($library_id, $series_id, $chapter_id)

Check if we should prompt the user for rereads for the given chapter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$library_id = 56; // int | 
$series_id = 56; // int | 
$chapter_id = 56; // int | 

try {
    $result = $apiInstance->apiReaderPromptRereadChapterGet($library_id, $series_id, $chapter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderPromptRereadChapterGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **library_id** | **int**|  | [optional]
 **series_id** | **int**|  | [optional]
 **chapter_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\RereadDto**](../Model/RereadDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderPromptRereadSeriesGet**
> \Pbxg33k\KavitaClient\Model\RereadDto apiReaderPromptRereadSeriesGet($series_id, $library_id)

Check if we should prompt the user for rereads for the given series

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 
$library_id = 56; // int | 

try {
    $result = $apiInstance->apiReaderPromptRereadSeriesGet($series_id, $library_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderPromptRereadSeriesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]
 **library_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\RereadDto**](../Model/RereadDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderPromptRereadVolumeGet**
> \Pbxg33k\KavitaClient\Model\RereadDto apiReaderPromptRereadVolumeGet($library_id, $series_id, $volume_id)

Check if we should prompt the user for rereads for the given volume

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$library_id = 56; // int | 
$series_id = 56; // int | 
$volume_id = 56; // int | 

try {
    $result = $apiInstance->apiReaderPromptRereadVolumeGet($library_id, $series_id, $volume_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderPromptRereadVolumeGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **library_id** | **int**|  | [optional]
 **series_id** | **int**|  | [optional]
 **volume_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\RereadDto**](../Model/RereadDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderPtocDelete**
> apiReaderPtocDelete($chapter_id, $page_num, $title)

Deletes the user's personal table of content for the given chapter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 
$page_num = 56; // int | 
$title = "title_example"; // string | 

try {
    $apiInstance->apiReaderPtocDelete($chapter_id, $page_num, $title);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderPtocDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  | [optional]
 **page_num** | **int**|  | [optional]
 **title** | **string**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderPtocGet**
> \Pbxg33k\KavitaClient\Model\PersonalToCDto[] apiReaderPtocGet($chapter_id)

Returns the user's personal table of contents for the given chapter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 

try {
    $result = $apiInstance->apiReaderPtocGet($chapter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderPtocGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\PersonalToCDto[]**](../Model/PersonalToCDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderRemoveBookmarksPost**
> apiReaderRemoveBookmarksPost($body)

Removes all bookmarks for all chapters linked to a Series

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\RemoveBookmarkForSeriesDto(); // \Pbxg33k\KavitaClient\Model\RemoveBookmarkForSeriesDto | 

try {
    $apiInstance->apiReaderRemoveBookmarksPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderRemoveBookmarksPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\RemoveBookmarkForSeriesDto**](../Model/RemoveBookmarkForSeriesDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderSeriesBookmarksGet**
> \Pbxg33k\KavitaClient\Model\BookmarkDto[] apiReaderSeriesBookmarksGet($series_id)

Returns all bookmarked pages for a given series

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $result = $apiInstance->apiReaderSeriesBookmarksGet($series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderSeriesBookmarksGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\BookmarkDto[]**](../Model/BookmarkDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderThumbnailGet**
> apiReaderThumbnailGet($chapter_id, $page_num, $api_key)

Returns a thumbnail for the given page number

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chapter_id = 56; // int | 
$page_num = 56; // int | 
$api_key = "api_key_example"; // string | 

try {
    $apiInstance->apiReaderThumbnailGet($chapter_id, $page_num, $api_key);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderThumbnailGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chapter_id** | **int**|  | [optional]
 **page_num** | **int**|  | [optional]
 **api_key** | **string**|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderTimeLeftForChapterGet**
> \Pbxg33k\KavitaClient\Model\HourEstimateRangeDto apiReaderTimeLeftForChapterGet($series_id, $chapter_id)

For the current user, returns an estimate on how long it would take to finish reading the chapter.

For Epubs, this does not check words inside a chapter due to overhead so may not work in all cases.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 
$chapter_id = 56; // int | 

try {
    $result = $apiInstance->apiReaderTimeLeftForChapterGet($series_id, $chapter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderTimeLeftForChapterGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]
 **chapter_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\HourEstimateRangeDto**](../Model/HourEstimateRangeDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderTimeLeftGet**
> \Pbxg33k\KavitaClient\Model\HourEstimateRangeDto apiReaderTimeLeftGet($series_id)

For the current user, returns an estimate on how long it would take to finish reading the series.

For Epubs, this does not check words inside a chapter due to overhead so may not work in all cases.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$series_id = 56; // int | 

try {
    $result = $apiInstance->apiReaderTimeLeftGet($series_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderTimeLeftGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **series_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\HourEstimateRangeDto**](../Model/HourEstimateRangeDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderUnbookmarkPost**
> apiReaderUnbookmarkPost($body)

Removes a bookmarked page for a Chapter

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Pbxg33k\KavitaClient\Model\BookmarkDto(); // \Pbxg33k\KavitaClient\Model\BookmarkDto | 

try {
    $apiInstance->apiReaderUnbookmarkPost($body);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderUnbookmarkPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Pbxg33k\KavitaClient\Model\BookmarkDto**](../Model/BookmarkDto.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **apiReaderVolumeBookmarksGet**
> \Pbxg33k\KavitaClient\Model\BookmarkDto[] apiReaderVolumeBookmarksGet($volume_id)

Returns all bookmarked pages for a given volume

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: AuthKey
$config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Pbxg33k\KavitaClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new Pbxg33k\KavitaClient\Api\ReaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$volume_id = 56; // int | 

try {
    $result = $apiInstance->apiReaderVolumeBookmarksGet($volume_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReaderApi->apiReaderVolumeBookmarksGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **volume_id** | **int**|  | [optional]

### Return type

[**\Pbxg33k\KavitaClient\Model\BookmarkDto[]**](../Model/BookmarkDto.md)

### Authorization

[AuthKey](../../README.md#AuthKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

