# OpenAPI\Client\GunFreeSchoolsActReportingStatusDescriptorsApi

All URIs are relative to https://api.ed-fi.org:443/v7.1/api/data/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteGunFreeSchoolsActReportingStatusDescriptorById()**](GunFreeSchoolsActReportingStatusDescriptorsApi.md#deleteGunFreeSchoolsActReportingStatusDescriptorById) | **DELETE** /ed-fi/gunFreeSchoolsActReportingStatusDescriptors/{id} | Deletes an existing resource using the resource identifier. |
| [**deletesGunFreeSchoolsActReportingStatusDescriptors()**](GunFreeSchoolsActReportingStatusDescriptorsApi.md#deletesGunFreeSchoolsActReportingStatusDescriptors) | **GET** /ed-fi/gunFreeSchoolsActReportingStatusDescriptors/deletes | Retrieves deleted resources based on change version. |
| [**getGunFreeSchoolsActReportingStatusDescriptors()**](GunFreeSchoolsActReportingStatusDescriptorsApi.md#getGunFreeSchoolsActReportingStatusDescriptors) | **GET** /ed-fi/gunFreeSchoolsActReportingStatusDescriptors | Retrieves specific resources using the resource&#39;s property values (using the \&quot;Get\&quot; pattern). |
| [**getGunFreeSchoolsActReportingStatusDescriptorsById()**](GunFreeSchoolsActReportingStatusDescriptorsApi.md#getGunFreeSchoolsActReportingStatusDescriptorsById) | **GET** /ed-fi/gunFreeSchoolsActReportingStatusDescriptors/{id} | Retrieves a specific resource using the resource&#39;s identifier (using the \&quot;Get By Id\&quot; pattern). |
| [**keyChangesGunFreeSchoolsActReportingStatusDescriptors()**](GunFreeSchoolsActReportingStatusDescriptorsApi.md#keyChangesGunFreeSchoolsActReportingStatusDescriptors) | **GET** /ed-fi/gunFreeSchoolsActReportingStatusDescriptors/keyChanges | Retrieves resources key changes based on change version. |
| [**postGunFreeSchoolsActReportingStatusDescriptor()**](GunFreeSchoolsActReportingStatusDescriptorsApi.md#postGunFreeSchoolsActReportingStatusDescriptor) | **POST** /ed-fi/gunFreeSchoolsActReportingStatusDescriptors | Creates or updates resources based on the natural key values of the supplied resource. |
| [**putGunFreeSchoolsActReportingStatusDescriptor()**](GunFreeSchoolsActReportingStatusDescriptorsApi.md#putGunFreeSchoolsActReportingStatusDescriptor) | **PUT** /ed-fi/gunFreeSchoolsActReportingStatusDescriptors/{id} | Updates a resource based on the resource identifier. |


## `deleteGunFreeSchoolsActReportingStatusDescriptorById()`

```php
deleteGunFreeSchoolsActReportingStatusDescriptorById($id, $if_match)
```

Deletes an existing resource using the resource identifier.

The DELETE operation is used to delete an existing resource by identifier. If the resource doesn't exist, an error will result (the resource will not be found).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\GunFreeSchoolsActReportingStatusDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | A resource identifier that uniquely identifies the resource.
$if_match = 'if_match_example'; // string | The ETag header value used to prevent the DELETE from removing a resource modified by another consumer.

try {
    $apiInstance->deleteGunFreeSchoolsActReportingStatusDescriptorById($id, $if_match);
} catch (Exception $e) {
    echo 'Exception when calling GunFreeSchoolsActReportingStatusDescriptorsApi->deleteGunFreeSchoolsActReportingStatusDescriptorById: ', $e->getMessage(), PHP_EOL;
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

## `deletesGunFreeSchoolsActReportingStatusDescriptors()`

```php
deletesGunFreeSchoolsActReportingStatusDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $use_snapshot): \OpenAPI\Client\Model\TrackedChangesEdFiGunFreeSchoolsActReportingStatusDescriptorDelete[]
```

Retrieves deleted resources based on change version.

This operation is used to retrieve identifying information about resources that have been deleted.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\GunFreeSchoolsActReportingStatusDescriptorsApi(
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
    $result = $apiInstance->deletesGunFreeSchoolsActReportingStatusDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $use_snapshot);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GunFreeSchoolsActReportingStatusDescriptorsApi->deletesGunFreeSchoolsActReportingStatusDescriptors: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\TrackedChangesEdFiGunFreeSchoolsActReportingStatusDescriptorDelete[]**](../Model/TrackedChangesEdFiGunFreeSchoolsActReportingStatusDescriptorDelete.md)

### Authorization

[oauth2_client_credentials](../../README.md#oauth2_client_credentials)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getGunFreeSchoolsActReportingStatusDescriptors()`

```php
getGunFreeSchoolsActReportingStatusDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $gun_free_schools_act_reporting_status_descriptor_id, $use_snapshot): \OpenAPI\Client\Model\EdFiGunFreeSchoolsActReportingStatusDescriptor[]
```

Retrieves specific resources using the resource's property values (using the \"Get\" pattern).

This GET operation provides access to resources using the \"Get\" search pattern.  The values of any properties of the resource that are specified will be used to return all matching results (if it exists).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\GunFreeSchoolsActReportingStatusDescriptorsApi(
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
$gun_free_schools_act_reporting_status_descriptor_id = 56; // int | A unique identifier used as Primary Key, not derived from business logic, when acting as Foreign Key, references the parent table.
$use_snapshot = false; // bool | Indicates if the configured Snapshot should be used.

try {
    $result = $apiInstance->getGunFreeSchoolsActReportingStatusDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $gun_free_schools_act_reporting_status_descriptor_id, $use_snapshot);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GunFreeSchoolsActReportingStatusDescriptorsApi->getGunFreeSchoolsActReportingStatusDescriptors: ', $e->getMessage(), PHP_EOL;
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
| **gun_free_schools_act_reporting_status_descriptor_id** | **int**| A unique identifier used as Primary Key, not derived from business logic, when acting as Foreign Key, references the parent table. | [optional] |
| **use_snapshot** | **bool**| Indicates if the configured Snapshot should be used. | [optional] [default to false] |

### Return type

[**\OpenAPI\Client\Model\EdFiGunFreeSchoolsActReportingStatusDescriptor[]**](../Model/EdFiGunFreeSchoolsActReportingStatusDescriptor.md)

### Authorization

[oauth2_client_credentials](../../README.md#oauth2_client_credentials)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getGunFreeSchoolsActReportingStatusDescriptorsById()`

```php
getGunFreeSchoolsActReportingStatusDescriptorsById($id, $if_none_match, $use_snapshot): \OpenAPI\Client\Model\EdFiGunFreeSchoolsActReportingStatusDescriptor
```

Retrieves a specific resource using the resource's identifier (using the \"Get By Id\" pattern).

This GET operation retrieves a resource by the specified resource identifier.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\GunFreeSchoolsActReportingStatusDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | A resource identifier that uniquely identifies the resource.
$if_none_match = 'if_none_match_example'; // string | The previously returned ETag header value, used here to prevent the unnecessary data transfer of an unchanged resource.
$use_snapshot = false; // bool | Indicates if the configured Snapshot should be used.

try {
    $result = $apiInstance->getGunFreeSchoolsActReportingStatusDescriptorsById($id, $if_none_match, $use_snapshot);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GunFreeSchoolsActReportingStatusDescriptorsApi->getGunFreeSchoolsActReportingStatusDescriptorsById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| A resource identifier that uniquely identifies the resource. | |
| **if_none_match** | **string**| The previously returned ETag header value, used here to prevent the unnecessary data transfer of an unchanged resource. | [optional] |
| **use_snapshot** | **bool**| Indicates if the configured Snapshot should be used. | [optional] [default to false] |

### Return type

[**\OpenAPI\Client\Model\EdFiGunFreeSchoolsActReportingStatusDescriptor**](../Model/EdFiGunFreeSchoolsActReportingStatusDescriptor.md)

### Authorization

[oauth2_client_credentials](../../README.md#oauth2_client_credentials)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `keyChangesGunFreeSchoolsActReportingStatusDescriptors()`

```php
keyChangesGunFreeSchoolsActReportingStatusDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $use_snapshot): \OpenAPI\Client\Model\TrackedChangesEdFiGunFreeSchoolsActReportingStatusDescriptorKeyChange[]
```

Retrieves resources key changes based on change version.

This operation is used to retrieve identifying information about resources whose key values have been changed.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\GunFreeSchoolsActReportingStatusDescriptorsApi(
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
    $result = $apiInstance->keyChangesGunFreeSchoolsActReportingStatusDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $use_snapshot);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GunFreeSchoolsActReportingStatusDescriptorsApi->keyChangesGunFreeSchoolsActReportingStatusDescriptors: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\TrackedChangesEdFiGunFreeSchoolsActReportingStatusDescriptorKeyChange[]**](../Model/TrackedChangesEdFiGunFreeSchoolsActReportingStatusDescriptorKeyChange.md)

### Authorization

[oauth2_client_credentials](../../README.md#oauth2_client_credentials)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postGunFreeSchoolsActReportingStatusDescriptor()`

```php
postGunFreeSchoolsActReportingStatusDescriptor($ed_fi_gun_free_schools_act_reporting_status_descriptor)
```

Creates or updates resources based on the natural key values of the supplied resource.

The POST operation can be used to create or update resources. In database terms, this is often referred to as an \"upsert\" operation (insert + update). Clients should NOT include the resource \"id\" in the JSON body because it will result in an error. The web service will identify whether the resource already exists based on the natural key values provided, and update or create the resource appropriately. It is recommended to use POST for both create and update except while updating natural key of a resource in which case PUT operation must be used.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\GunFreeSchoolsActReportingStatusDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ed_fi_gun_free_schools_act_reporting_status_descriptor = new \OpenAPI\Client\Model\EdFiGunFreeSchoolsActReportingStatusDescriptor(); // \OpenAPI\Client\Model\EdFiGunFreeSchoolsActReportingStatusDescriptor | The JSON representation of the \"gunFreeSchoolsActReportingStatusDescriptor\" resource to be created or updated.

try {
    $apiInstance->postGunFreeSchoolsActReportingStatusDescriptor($ed_fi_gun_free_schools_act_reporting_status_descriptor);
} catch (Exception $e) {
    echo 'Exception when calling GunFreeSchoolsActReportingStatusDescriptorsApi->postGunFreeSchoolsActReportingStatusDescriptor: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **ed_fi_gun_free_schools_act_reporting_status_descriptor** | [**\OpenAPI\Client\Model\EdFiGunFreeSchoolsActReportingStatusDescriptor**](../Model/EdFiGunFreeSchoolsActReportingStatusDescriptor.md)| The JSON representation of the \&quot;gunFreeSchoolsActReportingStatusDescriptor\&quot; resource to be created or updated. | |

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

## `putGunFreeSchoolsActReportingStatusDescriptor()`

```php
putGunFreeSchoolsActReportingStatusDescriptor($id, $ed_fi_gun_free_schools_act_reporting_status_descriptor, $if_match)
```

Updates a resource based on the resource identifier.

The PUT operation is used to update a resource by identifier. If the resource identifier (\"id\") is provided in the JSON body, it will be ignored. Additionally, this API resource is not configured for cascading natural key updates. Natural key values for this resource cannot be changed using PUT operation, so the recommendation is to use POST as that supports upsert behavior.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\GunFreeSchoolsActReportingStatusDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | A resource identifier that uniquely identifies the resource.
$ed_fi_gun_free_schools_act_reporting_status_descriptor = new \OpenAPI\Client\Model\EdFiGunFreeSchoolsActReportingStatusDescriptor(); // \OpenAPI\Client\Model\EdFiGunFreeSchoolsActReportingStatusDescriptor | The JSON representation of the \"gunFreeSchoolsActReportingStatusDescriptor\" resource to be created or updated.
$if_match = 'if_match_example'; // string | The ETag header value used to prevent the PUT from updating a resource modified by another consumer.

try {
    $apiInstance->putGunFreeSchoolsActReportingStatusDescriptor($id, $ed_fi_gun_free_schools_act_reporting_status_descriptor, $if_match);
} catch (Exception $e) {
    echo 'Exception when calling GunFreeSchoolsActReportingStatusDescriptorsApi->putGunFreeSchoolsActReportingStatusDescriptor: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| A resource identifier that uniquely identifies the resource. | |
| **ed_fi_gun_free_schools_act_reporting_status_descriptor** | [**\OpenAPI\Client\Model\EdFiGunFreeSchoolsActReportingStatusDescriptor**](../Model/EdFiGunFreeSchoolsActReportingStatusDescriptor.md)| The JSON representation of the \&quot;gunFreeSchoolsActReportingStatusDescriptor\&quot; resource to be created or updated. | |
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
