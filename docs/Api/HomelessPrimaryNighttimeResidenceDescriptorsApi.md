# Descriptors\HomelessPrimaryNighttimeResidenceDescriptorsApi

All URIs are relative to https://api.ed-fi.org:443/v7.1/api/data/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteHomelessPrimaryNighttimeResidenceDescriptorById()**](HomelessPrimaryNighttimeResidenceDescriptorsApi.md#deleteHomelessPrimaryNighttimeResidenceDescriptorById) | **DELETE** /ed-fi/homelessPrimaryNighttimeResidenceDescriptors/{id} | Deletes an existing resource using the resource identifier. |
| [**deletesHomelessPrimaryNighttimeResidenceDescriptors()**](HomelessPrimaryNighttimeResidenceDescriptorsApi.md#deletesHomelessPrimaryNighttimeResidenceDescriptors) | **GET** /ed-fi/homelessPrimaryNighttimeResidenceDescriptors/deletes | Retrieves deleted resources based on change version. |
| [**getHomelessPrimaryNighttimeResidenceDescriptors()**](HomelessPrimaryNighttimeResidenceDescriptorsApi.md#getHomelessPrimaryNighttimeResidenceDescriptors) | **GET** /ed-fi/homelessPrimaryNighttimeResidenceDescriptors | Retrieves specific resources using the resource&#39;s property values (using the \&quot;Get\&quot; pattern). |
| [**getHomelessPrimaryNighttimeResidenceDescriptorsById()**](HomelessPrimaryNighttimeResidenceDescriptorsApi.md#getHomelessPrimaryNighttimeResidenceDescriptorsById) | **GET** /ed-fi/homelessPrimaryNighttimeResidenceDescriptors/{id} | Retrieves a specific resource using the resource&#39;s identifier (using the \&quot;Get By Id\&quot; pattern). |
| [**keyChangesHomelessPrimaryNighttimeResidenceDescriptors()**](HomelessPrimaryNighttimeResidenceDescriptorsApi.md#keyChangesHomelessPrimaryNighttimeResidenceDescriptors) | **GET** /ed-fi/homelessPrimaryNighttimeResidenceDescriptors/keyChanges | Retrieves resources key changes based on change version. |
| [**postHomelessPrimaryNighttimeResidenceDescriptor()**](HomelessPrimaryNighttimeResidenceDescriptorsApi.md#postHomelessPrimaryNighttimeResidenceDescriptor) | **POST** /ed-fi/homelessPrimaryNighttimeResidenceDescriptors | Creates or updates resources based on the natural key values of the supplied resource. |
| [**putHomelessPrimaryNighttimeResidenceDescriptor()**](HomelessPrimaryNighttimeResidenceDescriptorsApi.md#putHomelessPrimaryNighttimeResidenceDescriptor) | **PUT** /ed-fi/homelessPrimaryNighttimeResidenceDescriptors/{id} | Updates a resource based on the resource identifier. |


## `deleteHomelessPrimaryNighttimeResidenceDescriptorById()`

```php
deleteHomelessPrimaryNighttimeResidenceDescriptorById($id, $if_match)
```

Deletes an existing resource using the resource identifier.

The DELETE operation is used to delete an existing resource by identifier. If the resource doesn't exist, an error will result (the resource will not be found).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\HomelessPrimaryNighttimeResidenceDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | A resource identifier that uniquely identifies the resource.
$if_match = 'if_match_example'; // string | The ETag header value used to prevent the DELETE from removing a resource modified by another consumer.

try {
    $apiInstance->deleteHomelessPrimaryNighttimeResidenceDescriptorById($id, $if_match);
} catch (Exception $e) {
    echo 'Exception when calling HomelessPrimaryNighttimeResidenceDescriptorsApi->deleteHomelessPrimaryNighttimeResidenceDescriptorById: ', $e->getMessage(), PHP_EOL;
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

## `deletesHomelessPrimaryNighttimeResidenceDescriptors()`

```php
deletesHomelessPrimaryNighttimeResidenceDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $use_snapshot): \Descriptors\Model\TrackedChangesEdFiHomelessPrimaryNighttimeResidenceDescriptorDelete[]
```

Retrieves deleted resources based on change version.

This operation is used to retrieve identifying information about resources that have been deleted.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\HomelessPrimaryNighttimeResidenceDescriptorsApi(
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
    $result = $apiInstance->deletesHomelessPrimaryNighttimeResidenceDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $use_snapshot);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HomelessPrimaryNighttimeResidenceDescriptorsApi->deletesHomelessPrimaryNighttimeResidenceDescriptors: ', $e->getMessage(), PHP_EOL;
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

[**\Descriptors\Model\TrackedChangesEdFiHomelessPrimaryNighttimeResidenceDescriptorDelete[]**](../Model/TrackedChangesEdFiHomelessPrimaryNighttimeResidenceDescriptorDelete.md)

### Authorization

[oauth2_client_credentials](../../README.md#oauth2_client_credentials)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getHomelessPrimaryNighttimeResidenceDescriptors()`

```php
getHomelessPrimaryNighttimeResidenceDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $homeless_primary_nighttime_residence_descriptor_id, $use_snapshot): \Descriptors\Model\EdFiHomelessPrimaryNighttimeResidenceDescriptor[]
```

Retrieves specific resources using the resource's property values (using the \"Get\" pattern).

This GET operation provides access to resources using the \"Get\" search pattern.  The values of any properties of the resource that are specified will be used to return all matching results (if it exists).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\HomelessPrimaryNighttimeResidenceDescriptorsApi(
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
$homeless_primary_nighttime_residence_descriptor_id = 56; // int | A unique identifier used as Primary Key, not derived from business logic, when acting as Foreign Key, references the parent table.
$use_snapshot = false; // bool | Indicates if the configured Snapshot should be used.

try {
    $result = $apiInstance->getHomelessPrimaryNighttimeResidenceDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $homeless_primary_nighttime_residence_descriptor_id, $use_snapshot);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HomelessPrimaryNighttimeResidenceDescriptorsApi->getHomelessPrimaryNighttimeResidenceDescriptors: ', $e->getMessage(), PHP_EOL;
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
| **homeless_primary_nighttime_residence_descriptor_id** | **int**| A unique identifier used as Primary Key, not derived from business logic, when acting as Foreign Key, references the parent table. | [optional] |
| **use_snapshot** | **bool**| Indicates if the configured Snapshot should be used. | [optional] [default to false] |

### Return type

[**\Descriptors\Model\EdFiHomelessPrimaryNighttimeResidenceDescriptor[]**](../Model/EdFiHomelessPrimaryNighttimeResidenceDescriptor.md)

### Authorization

[oauth2_client_credentials](../../README.md#oauth2_client_credentials)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getHomelessPrimaryNighttimeResidenceDescriptorsById()`

```php
getHomelessPrimaryNighttimeResidenceDescriptorsById($id, $if_none_match, $use_snapshot): \Descriptors\Model\EdFiHomelessPrimaryNighttimeResidenceDescriptor
```

Retrieves a specific resource using the resource's identifier (using the \"Get By Id\" pattern).

This GET operation retrieves a resource by the specified resource identifier.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\HomelessPrimaryNighttimeResidenceDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | A resource identifier that uniquely identifies the resource.
$if_none_match = 'if_none_match_example'; // string | The previously returned ETag header value, used here to prevent the unnecessary data transfer of an unchanged resource.
$use_snapshot = false; // bool | Indicates if the configured Snapshot should be used.

try {
    $result = $apiInstance->getHomelessPrimaryNighttimeResidenceDescriptorsById($id, $if_none_match, $use_snapshot);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HomelessPrimaryNighttimeResidenceDescriptorsApi->getHomelessPrimaryNighttimeResidenceDescriptorsById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| A resource identifier that uniquely identifies the resource. | |
| **if_none_match** | **string**| The previously returned ETag header value, used here to prevent the unnecessary data transfer of an unchanged resource. | [optional] |
| **use_snapshot** | **bool**| Indicates if the configured Snapshot should be used. | [optional] [default to false] |

### Return type

[**\Descriptors\Model\EdFiHomelessPrimaryNighttimeResidenceDescriptor**](../Model/EdFiHomelessPrimaryNighttimeResidenceDescriptor.md)

### Authorization

[oauth2_client_credentials](../../README.md#oauth2_client_credentials)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `keyChangesHomelessPrimaryNighttimeResidenceDescriptors()`

```php
keyChangesHomelessPrimaryNighttimeResidenceDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $use_snapshot): \Descriptors\Model\TrackedChangesEdFiHomelessPrimaryNighttimeResidenceDescriptorKeyChange[]
```

Retrieves resources key changes based on change version.

This operation is used to retrieve identifying information about resources whose key values have been changed.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\HomelessPrimaryNighttimeResidenceDescriptorsApi(
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
    $result = $apiInstance->keyChangesHomelessPrimaryNighttimeResidenceDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $use_snapshot);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HomelessPrimaryNighttimeResidenceDescriptorsApi->keyChangesHomelessPrimaryNighttimeResidenceDescriptors: ', $e->getMessage(), PHP_EOL;
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

[**\Descriptors\Model\TrackedChangesEdFiHomelessPrimaryNighttimeResidenceDescriptorKeyChange[]**](../Model/TrackedChangesEdFiHomelessPrimaryNighttimeResidenceDescriptorKeyChange.md)

### Authorization

[oauth2_client_credentials](../../README.md#oauth2_client_credentials)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postHomelessPrimaryNighttimeResidenceDescriptor()`

```php
postHomelessPrimaryNighttimeResidenceDescriptor($ed_fi_homeless_primary_nighttime_residence_descriptor)
```

Creates or updates resources based on the natural key values of the supplied resource.

The POST operation can be used to create or update resources. In database terms, this is often referred to as an \"upsert\" operation (insert + update). Clients should NOT include the resource \"id\" in the JSON body because it will result in an error. The web service will identify whether the resource already exists based on the natural key values provided, and update or create the resource appropriately. It is recommended to use POST for both create and update except while updating natural key of a resource in which case PUT operation must be used.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\HomelessPrimaryNighttimeResidenceDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ed_fi_homeless_primary_nighttime_residence_descriptor = new \Descriptors\Model\EdFiHomelessPrimaryNighttimeResidenceDescriptor(); // \Descriptors\Model\EdFiHomelessPrimaryNighttimeResidenceDescriptor | The JSON representation of the \"homelessPrimaryNighttimeResidenceDescriptor\" resource to be created or updated.

try {
    $apiInstance->postHomelessPrimaryNighttimeResidenceDescriptor($ed_fi_homeless_primary_nighttime_residence_descriptor);
} catch (Exception $e) {
    echo 'Exception when calling HomelessPrimaryNighttimeResidenceDescriptorsApi->postHomelessPrimaryNighttimeResidenceDescriptor: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **ed_fi_homeless_primary_nighttime_residence_descriptor** | [**\Descriptors\Model\EdFiHomelessPrimaryNighttimeResidenceDescriptor**](../Model/EdFiHomelessPrimaryNighttimeResidenceDescriptor.md)| The JSON representation of the \&quot;homelessPrimaryNighttimeResidenceDescriptor\&quot; resource to be created or updated. | |

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

## `putHomelessPrimaryNighttimeResidenceDescriptor()`

```php
putHomelessPrimaryNighttimeResidenceDescriptor($id, $ed_fi_homeless_primary_nighttime_residence_descriptor, $if_match)
```

Updates a resource based on the resource identifier.

The PUT operation is used to update a resource by identifier. If the resource identifier (\"id\") is provided in the JSON body, it will be ignored. Additionally, this API resource is not configured for cascading natural key updates. Natural key values for this resource cannot be changed using PUT operation, so the recommendation is to use POST as that supports upsert behavior.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\HomelessPrimaryNighttimeResidenceDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | A resource identifier that uniquely identifies the resource.
$ed_fi_homeless_primary_nighttime_residence_descriptor = new \Descriptors\Model\EdFiHomelessPrimaryNighttimeResidenceDescriptor(); // \Descriptors\Model\EdFiHomelessPrimaryNighttimeResidenceDescriptor | The JSON representation of the \"homelessPrimaryNighttimeResidenceDescriptor\" resource to be created or updated.
$if_match = 'if_match_example'; // string | The ETag header value used to prevent the PUT from updating a resource modified by another consumer.

try {
    $apiInstance->putHomelessPrimaryNighttimeResidenceDescriptor($id, $ed_fi_homeless_primary_nighttime_residence_descriptor, $if_match);
} catch (Exception $e) {
    echo 'Exception when calling HomelessPrimaryNighttimeResidenceDescriptorsApi->putHomelessPrimaryNighttimeResidenceDescriptor: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| A resource identifier that uniquely identifies the resource. | |
| **ed_fi_homeless_primary_nighttime_residence_descriptor** | [**\Descriptors\Model\EdFiHomelessPrimaryNighttimeResidenceDescriptor**](../Model/EdFiHomelessPrimaryNighttimeResidenceDescriptor.md)| The JSON representation of the \&quot;homelessPrimaryNighttimeResidenceDescriptor\&quot; resource to be created or updated. | |
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