# Descriptors\MagnetSpecialProgramEmphasisSchoolDescriptorsApi

All URIs are relative to https://api.ed-fi.org:443/v7.1/api/data/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteMagnetSpecialProgramEmphasisSchoolDescriptorById()**](MagnetSpecialProgramEmphasisSchoolDescriptorsApi.md#deleteMagnetSpecialProgramEmphasisSchoolDescriptorById) | **DELETE** /ed-fi/magnetSpecialProgramEmphasisSchoolDescriptors/{id} | Deletes an existing resource using the resource identifier. |
| [**deletesMagnetSpecialProgramEmphasisSchoolDescriptors()**](MagnetSpecialProgramEmphasisSchoolDescriptorsApi.md#deletesMagnetSpecialProgramEmphasisSchoolDescriptors) | **GET** /ed-fi/magnetSpecialProgramEmphasisSchoolDescriptors/deletes | Retrieves deleted resources based on change version. |
| [**getMagnetSpecialProgramEmphasisSchoolDescriptors()**](MagnetSpecialProgramEmphasisSchoolDescriptorsApi.md#getMagnetSpecialProgramEmphasisSchoolDescriptors) | **GET** /ed-fi/magnetSpecialProgramEmphasisSchoolDescriptors | Retrieves specific resources using the resource&#39;s property values (using the \&quot;Get\&quot; pattern). |
| [**getMagnetSpecialProgramEmphasisSchoolDescriptorsById()**](MagnetSpecialProgramEmphasisSchoolDescriptorsApi.md#getMagnetSpecialProgramEmphasisSchoolDescriptorsById) | **GET** /ed-fi/magnetSpecialProgramEmphasisSchoolDescriptors/{id} | Retrieves a specific resource using the resource&#39;s identifier (using the \&quot;Get By Id\&quot; pattern). |
| [**keyChangesMagnetSpecialProgramEmphasisSchoolDescriptors()**](MagnetSpecialProgramEmphasisSchoolDescriptorsApi.md#keyChangesMagnetSpecialProgramEmphasisSchoolDescriptors) | **GET** /ed-fi/magnetSpecialProgramEmphasisSchoolDescriptors/keyChanges | Retrieves resources key changes based on change version. |
| [**postMagnetSpecialProgramEmphasisSchoolDescriptor()**](MagnetSpecialProgramEmphasisSchoolDescriptorsApi.md#postMagnetSpecialProgramEmphasisSchoolDescriptor) | **POST** /ed-fi/magnetSpecialProgramEmphasisSchoolDescriptors | Creates or updates resources based on the natural key values of the supplied resource. |
| [**putMagnetSpecialProgramEmphasisSchoolDescriptor()**](MagnetSpecialProgramEmphasisSchoolDescriptorsApi.md#putMagnetSpecialProgramEmphasisSchoolDescriptor) | **PUT** /ed-fi/magnetSpecialProgramEmphasisSchoolDescriptors/{id} | Updates a resource based on the resource identifier. |


## `deleteMagnetSpecialProgramEmphasisSchoolDescriptorById()`

```php
deleteMagnetSpecialProgramEmphasisSchoolDescriptorById($id, $if_match)
```

Deletes an existing resource using the resource identifier.

The DELETE operation is used to delete an existing resource by identifier. If the resource doesn't exist, an error will result (the resource will not be found).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\MagnetSpecialProgramEmphasisSchoolDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | A resource identifier that uniquely identifies the resource.
$if_match = 'if_match_example'; // string | The ETag header value used to prevent the DELETE from removing a resource modified by another consumer.

try {
    $apiInstance->deleteMagnetSpecialProgramEmphasisSchoolDescriptorById($id, $if_match);
} catch (Exception $e) {
    echo 'Exception when calling MagnetSpecialProgramEmphasisSchoolDescriptorsApi->deleteMagnetSpecialProgramEmphasisSchoolDescriptorById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| A resource identifier that uniquely identifies the resource. | |
| **if_match** | **string**| The ETag header value used to prevent the DELETE from removing a resource modified by another consumer. | [optional] |

### Return type

void (empty response body)

### Authorization

[oauth2_client_credentials](../../README.md#oauth2_client_credentials)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deletesMagnetSpecialProgramEmphasisSchoolDescriptors()`

```php
deletesMagnetSpecialProgramEmphasisSchoolDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $use_snapshot): \Descriptors\Model\TrackedChangesEdFiMagnetSpecialProgramEmphasisSchoolDescriptorDelete[]
```

Retrieves deleted resources based on change version.

This operation is used to retrieve identifying information about resources that have been deleted.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\MagnetSpecialProgramEmphasisSchoolDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$offset = 0; // int | Indicates how many items should be skipped before returning results.
$limit = 25; // int | Indicates the maximum number of items that should be returned in the results.
$min_change_version = 56; // int | Used in synchronization to set sequence minimum ChangeVersion
$max_change_version = 56; // int | Used in synchronization to set sequence maximum ChangeVersion
$total_count = false; // bool | Indicates if the total number of items available should be returned in the 'Total-Count' header of the response.  If set to false, 'Total-Count' header will not be provided.
$use_snapshot = false; // bool | Indicates if the configured Snapshot should be used.

try {
    $result = $apiInstance->deletesMagnetSpecialProgramEmphasisSchoolDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $use_snapshot);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MagnetSpecialProgramEmphasisSchoolDescriptorsApi->deletesMagnetSpecialProgramEmphasisSchoolDescriptors: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **offset** | **int**| Indicates how many items should be skipped before returning results. | [optional] [default to 0] |
| **limit** | **int**| Indicates the maximum number of items that should be returned in the results. | [optional] [default to 25] |
| **min_change_version** | **int**| Used in synchronization to set sequence minimum ChangeVersion | [optional] |
| **max_change_version** | **int**| Used in synchronization to set sequence maximum ChangeVersion | [optional] |
| **total_count** | **bool**| Indicates if the total number of items available should be returned in the &#39;Total-Count&#39; header of the response.  If set to false, &#39;Total-Count&#39; header will not be provided. | [optional] [default to false] |
| **use_snapshot** | **bool**| Indicates if the configured Snapshot should be used. | [optional] [default to false] |

### Return type

[**\Descriptors\Model\TrackedChangesEdFiMagnetSpecialProgramEmphasisSchoolDescriptorDelete[]**](../Model/TrackedChangesEdFiMagnetSpecialProgramEmphasisSchoolDescriptorDelete.md)

### Authorization

[oauth2_client_credentials](../../README.md#oauth2_client_credentials)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMagnetSpecialProgramEmphasisSchoolDescriptors()`

```php
getMagnetSpecialProgramEmphasisSchoolDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $magnet_special_program_emphasis_school_descriptor_id, $use_snapshot): \Descriptors\Model\EdFiMagnetSpecialProgramEmphasisSchoolDescriptor[]
```

Retrieves specific resources using the resource's property values (using the \"Get\" pattern).

This GET operation provides access to resources using the \"Get\" search pattern.  The values of any properties of the resource that are specified will be used to return all matching results (if it exists).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\MagnetSpecialProgramEmphasisSchoolDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$offset = 0; // int | Indicates how many items should be skipped before returning results.
$limit = 25; // int | Indicates the maximum number of items that should be returned in the results.
$min_change_version = 56; // int | Used in synchronization to set sequence minimum ChangeVersion
$max_change_version = 56; // int | Used in synchronization to set sequence maximum ChangeVersion
$total_count = false; // bool | Indicates if the total number of items available should be returned in the 'Total-Count' header of the response.  If set to false, 'Total-Count' header will not be provided.
$magnet_special_program_emphasis_school_descriptor_id = 56; // int | A unique identifier used as Primary Key, not derived from business logic, when acting as Foreign Key, references the parent table.
$use_snapshot = false; // bool | Indicates if the configured Snapshot should be used.

try {
    $result = $apiInstance->getMagnetSpecialProgramEmphasisSchoolDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $magnet_special_program_emphasis_school_descriptor_id, $use_snapshot);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MagnetSpecialProgramEmphasisSchoolDescriptorsApi->getMagnetSpecialProgramEmphasisSchoolDescriptors: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **offset** | **int**| Indicates how many items should be skipped before returning results. | [optional] [default to 0] |
| **limit** | **int**| Indicates the maximum number of items that should be returned in the results. | [optional] [default to 25] |
| **min_change_version** | **int**| Used in synchronization to set sequence minimum ChangeVersion | [optional] |
| **max_change_version** | **int**| Used in synchronization to set sequence maximum ChangeVersion | [optional] |
| **total_count** | **bool**| Indicates if the total number of items available should be returned in the &#39;Total-Count&#39; header of the response.  If set to false, &#39;Total-Count&#39; header will not be provided. | [optional] [default to false] |
| **magnet_special_program_emphasis_school_descriptor_id** | **int**| A unique identifier used as Primary Key, not derived from business logic, when acting as Foreign Key, references the parent table. | [optional] |
| **use_snapshot** | **bool**| Indicates if the configured Snapshot should be used. | [optional] [default to false] |

### Return type

[**\Descriptors\Model\EdFiMagnetSpecialProgramEmphasisSchoolDescriptor[]**](../Model/EdFiMagnetSpecialProgramEmphasisSchoolDescriptor.md)

### Authorization

[oauth2_client_credentials](../../README.md#oauth2_client_credentials)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMagnetSpecialProgramEmphasisSchoolDescriptorsById()`

```php
getMagnetSpecialProgramEmphasisSchoolDescriptorsById($id, $if_none_match, $use_snapshot): \Descriptors\Model\EdFiMagnetSpecialProgramEmphasisSchoolDescriptor
```

Retrieves a specific resource using the resource's identifier (using the \"Get By Id\" pattern).

This GET operation retrieves a resource by the specified resource identifier.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\MagnetSpecialProgramEmphasisSchoolDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | A resource identifier that uniquely identifies the resource.
$if_none_match = 'if_none_match_example'; // string | The previously returned ETag header value, used here to prevent the unnecessary data transfer of an unchanged resource.
$use_snapshot = false; // bool | Indicates if the configured Snapshot should be used.

try {
    $result = $apiInstance->getMagnetSpecialProgramEmphasisSchoolDescriptorsById($id, $if_none_match, $use_snapshot);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MagnetSpecialProgramEmphasisSchoolDescriptorsApi->getMagnetSpecialProgramEmphasisSchoolDescriptorsById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| A resource identifier that uniquely identifies the resource. | |
| **if_none_match** | **string**| The previously returned ETag header value, used here to prevent the unnecessary data transfer of an unchanged resource. | [optional] |
| **use_snapshot** | **bool**| Indicates if the configured Snapshot should be used. | [optional] [default to false] |

### Return type

[**\Descriptors\Model\EdFiMagnetSpecialProgramEmphasisSchoolDescriptor**](../Model/EdFiMagnetSpecialProgramEmphasisSchoolDescriptor.md)

### Authorization

[oauth2_client_credentials](../../README.md#oauth2_client_credentials)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `keyChangesMagnetSpecialProgramEmphasisSchoolDescriptors()`

```php
keyChangesMagnetSpecialProgramEmphasisSchoolDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $use_snapshot): \Descriptors\Model\TrackedChangesEdFiMagnetSpecialProgramEmphasisSchoolDescriptorKeyChange[]
```

Retrieves resources key changes based on change version.

This operation is used to retrieve identifying information about resources whose key values have been changed.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\MagnetSpecialProgramEmphasisSchoolDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$offset = 0; // int | Indicates how many items should be skipped before returning results.
$limit = 25; // int | Indicates the maximum number of items that should be returned in the results.
$min_change_version = 56; // int | Used in synchronization to set sequence minimum ChangeVersion
$max_change_version = 56; // int | Used in synchronization to set sequence maximum ChangeVersion
$total_count = false; // bool | Indicates if the total number of items available should be returned in the 'Total-Count' header of the response.  If set to false, 'Total-Count' header will not be provided.
$use_snapshot = false; // bool | Indicates if the configured Snapshot should be used.

try {
    $result = $apiInstance->keyChangesMagnetSpecialProgramEmphasisSchoolDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $use_snapshot);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MagnetSpecialProgramEmphasisSchoolDescriptorsApi->keyChangesMagnetSpecialProgramEmphasisSchoolDescriptors: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **offset** | **int**| Indicates how many items should be skipped before returning results. | [optional] [default to 0] |
| **limit** | **int**| Indicates the maximum number of items that should be returned in the results. | [optional] [default to 25] |
| **min_change_version** | **int**| Used in synchronization to set sequence minimum ChangeVersion | [optional] |
| **max_change_version** | **int**| Used in synchronization to set sequence maximum ChangeVersion | [optional] |
| **total_count** | **bool**| Indicates if the total number of items available should be returned in the &#39;Total-Count&#39; header of the response.  If set to false, &#39;Total-Count&#39; header will not be provided. | [optional] [default to false] |
| **use_snapshot** | **bool**| Indicates if the configured Snapshot should be used. | [optional] [default to false] |

### Return type

[**\Descriptors\Model\TrackedChangesEdFiMagnetSpecialProgramEmphasisSchoolDescriptorKeyChange[]**](../Model/TrackedChangesEdFiMagnetSpecialProgramEmphasisSchoolDescriptorKeyChange.md)

### Authorization

[oauth2_client_credentials](../../README.md#oauth2_client_credentials)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postMagnetSpecialProgramEmphasisSchoolDescriptor()`

```php
postMagnetSpecialProgramEmphasisSchoolDescriptor($ed_fi_magnet_special_program_emphasis_school_descriptor)
```

Creates or updates resources based on the natural key values of the supplied resource.

The POST operation can be used to create or update resources. In database terms, this is often referred to as an \"upsert\" operation (insert + update). Clients should NOT include the resource \"id\" in the JSON body because it will result in an error. The web service will identify whether the resource already exists based on the natural key values provided, and update or create the resource appropriately. It is recommended to use POST for both create and update except while updating natural key of a resource in which case PUT operation must be used.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\MagnetSpecialProgramEmphasisSchoolDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ed_fi_magnet_special_program_emphasis_school_descriptor = new \Descriptors\Model\EdFiMagnetSpecialProgramEmphasisSchoolDescriptor(); // \Descriptors\Model\EdFiMagnetSpecialProgramEmphasisSchoolDescriptor | The JSON representation of the \"magnetSpecialProgramEmphasisSchoolDescriptor\" resource to be created or updated.

try {
    $apiInstance->postMagnetSpecialProgramEmphasisSchoolDescriptor($ed_fi_magnet_special_program_emphasis_school_descriptor);
} catch (Exception $e) {
    echo 'Exception when calling MagnetSpecialProgramEmphasisSchoolDescriptorsApi->postMagnetSpecialProgramEmphasisSchoolDescriptor: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **ed_fi_magnet_special_program_emphasis_school_descriptor** | [**\Descriptors\Model\EdFiMagnetSpecialProgramEmphasisSchoolDescriptor**](../Model/EdFiMagnetSpecialProgramEmphasisSchoolDescriptor.md)| The JSON representation of the \&quot;magnetSpecialProgramEmphasisSchoolDescriptor\&quot; resource to be created or updated. | |

### Return type

void (empty response body)

### Authorization

[oauth2_client_credentials](../../README.md#oauth2_client_credentials)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `putMagnetSpecialProgramEmphasisSchoolDescriptor()`

```php
putMagnetSpecialProgramEmphasisSchoolDescriptor($id, $ed_fi_magnet_special_program_emphasis_school_descriptor, $if_match)
```

Updates a resource based on the resource identifier.

The PUT operation is used to update a resource by identifier. If the resource identifier (\"id\") is provided in the JSON body, it will be ignored. Additionally, this API resource is not configured for cascading natural key updates. Natural key values for this resource cannot be changed using PUT operation, so the recommendation is to use POST as that supports upsert behavior.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\MagnetSpecialProgramEmphasisSchoolDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | A resource identifier that uniquely identifies the resource.
$ed_fi_magnet_special_program_emphasis_school_descriptor = new \Descriptors\Model\EdFiMagnetSpecialProgramEmphasisSchoolDescriptor(); // \Descriptors\Model\EdFiMagnetSpecialProgramEmphasisSchoolDescriptor | The JSON representation of the \"magnetSpecialProgramEmphasisSchoolDescriptor\" resource to be created or updated.
$if_match = 'if_match_example'; // string | The ETag header value used to prevent the PUT from updating a resource modified by another consumer.

try {
    $apiInstance->putMagnetSpecialProgramEmphasisSchoolDescriptor($id, $ed_fi_magnet_special_program_emphasis_school_descriptor, $if_match);
} catch (Exception $e) {
    echo 'Exception when calling MagnetSpecialProgramEmphasisSchoolDescriptorsApi->putMagnetSpecialProgramEmphasisSchoolDescriptor: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| A resource identifier that uniquely identifies the resource. | |
| **ed_fi_magnet_special_program_emphasis_school_descriptor** | [**\Descriptors\Model\EdFiMagnetSpecialProgramEmphasisSchoolDescriptor**](../Model/EdFiMagnetSpecialProgramEmphasisSchoolDescriptor.md)| The JSON representation of the \&quot;magnetSpecialProgramEmphasisSchoolDescriptor\&quot; resource to be created or updated. | |
| **if_match** | **string**| The ETag header value used to prevent the PUT from updating a resource modified by another consumer. | [optional] |

### Return type

void (empty response body)

### Authorization

[oauth2_client_credentials](../../README.md#oauth2_client_credentials)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)