# Descriptors\EligibilityEvaluationTypeDescriptorsApi

All URIs are relative to https://api.ed-fi.org:443/v7.3/api/data/v3, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteEligibilityEvaluationTypeDescriptorById()**](EligibilityEvaluationTypeDescriptorsApi.md#deleteEligibilityEvaluationTypeDescriptorById) | **DELETE** /ed-fi/eligibilityEvaluationTypeDescriptors/{id} | Deletes an existing resource using the resource identifier. |
| [**deletesEligibilityEvaluationTypeDescriptors()**](EligibilityEvaluationTypeDescriptorsApi.md#deletesEligibilityEvaluationTypeDescriptors) | **GET** /ed-fi/eligibilityEvaluationTypeDescriptors/deletes | Retrieves deleted resources based on change version. |
| [**getEligibilityEvaluationTypeDescriptors()**](EligibilityEvaluationTypeDescriptorsApi.md#getEligibilityEvaluationTypeDescriptors) | **GET** /ed-fi/eligibilityEvaluationTypeDescriptors | Retrieves specific resources using the resource&#39;s property values (using the \&quot;Get\&quot; pattern). |
| [**getEligibilityEvaluationTypeDescriptorsById()**](EligibilityEvaluationTypeDescriptorsApi.md#getEligibilityEvaluationTypeDescriptorsById) | **GET** /ed-fi/eligibilityEvaluationTypeDescriptors/{id} | Retrieves a specific resource using the resource&#39;s identifier (using the \&quot;Get By Id\&quot; pattern). |
| [**getEligibilityEvaluationTypeDescriptorsPartitions()**](EligibilityEvaluationTypeDescriptorsApi.md#getEligibilityEvaluationTypeDescriptorsPartitions) | **GET** /ed-fi/eligibilityEvaluationTypeDescriptors/partitions | Retrieves a set of page tokens to be used for efficient client-side parallel processing. |
| [**keyChangesEligibilityEvaluationTypeDescriptors()**](EligibilityEvaluationTypeDescriptorsApi.md#keyChangesEligibilityEvaluationTypeDescriptors) | **GET** /ed-fi/eligibilityEvaluationTypeDescriptors/keyChanges | Retrieves resources key changes based on change version. |
| [**postEligibilityEvaluationTypeDescriptor()**](EligibilityEvaluationTypeDescriptorsApi.md#postEligibilityEvaluationTypeDescriptor) | **POST** /ed-fi/eligibilityEvaluationTypeDescriptors | Creates or updates resources based on the natural key values of the supplied resource. |
| [**putEligibilityEvaluationTypeDescriptor()**](EligibilityEvaluationTypeDescriptorsApi.md#putEligibilityEvaluationTypeDescriptor) | **PUT** /ed-fi/eligibilityEvaluationTypeDescriptors/{id} | Updates a resource based on the resource identifier. |


## `deleteEligibilityEvaluationTypeDescriptorById()`

```php
deleteEligibilityEvaluationTypeDescriptorById($id, $if_match)
```

Deletes an existing resource using the resource identifier.

The DELETE operation is used to delete an existing resource by identifier. If the resource doesn't exist, an error will result (the resource will not be found).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\EligibilityEvaluationTypeDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | A resource identifier that uniquely identifies the resource.
$if_match = 'if_match_example'; // string | The ETag header value used to prevent the DELETE from removing a resource modified by another consumer.

try {
    $apiInstance->deleteEligibilityEvaluationTypeDescriptorById($id, $if_match);
} catch (Exception $e) {
    echo 'Exception when calling EligibilityEvaluationTypeDescriptorsApi->deleteEligibilityEvaluationTypeDescriptorById: ', $e->getMessage(), PHP_EOL;
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

## `deletesEligibilityEvaluationTypeDescriptors()`

```php
deletesEligibilityEvaluationTypeDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $use_snapshot): \Descriptors\Model\TrackedChangesEdFiEligibilityEvaluationTypeDescriptorDelete[]
```

Retrieves deleted resources based on change version.

This operation is used to retrieve identifying information about resources that have been deleted.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\EligibilityEvaluationTypeDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$offset = 56; // int | Indicates how many items should be skipped before returning results.
$limit = 25; // int | Indicates the maximum number of items that should be returned in the results.
$min_change_version = 56; // int | Used in synchronization to set sequence minimum ChangeVersion
$max_change_version = 56; // int | Used in synchronization to set sequence maximum ChangeVersion
$total_count = false; // bool | Indicates if the total number of items available should be returned in the 'Total-Count' header of the response.  If set to false, 'Total-Count' header will not be provided. Must be false when using cursor paging (with pageToken).
$use_snapshot = false; // bool | Indicates if the configured Snapshot should be used.

try {
    $result = $apiInstance->deletesEligibilityEvaluationTypeDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $use_snapshot);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EligibilityEvaluationTypeDescriptorsApi->deletesEligibilityEvaluationTypeDescriptors: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **offset** | **int**| Indicates how many items should be skipped before returning results. | [optional] |
| **limit** | **int**| Indicates the maximum number of items that should be returned in the results. | [optional] [default to 25] |
| **min_change_version** | **int**| Used in synchronization to set sequence minimum ChangeVersion | [optional] |
| **max_change_version** | **int**| Used in synchronization to set sequence maximum ChangeVersion | [optional] |
| **total_count** | **bool**| Indicates if the total number of items available should be returned in the &#39;Total-Count&#39; header of the response.  If set to false, &#39;Total-Count&#39; header will not be provided. Must be false when using cursor paging (with pageToken). | [optional] [default to false] |
| **use_snapshot** | **bool**| Indicates if the configured Snapshot should be used. | [optional] [default to false] |

### Return type

[**\Descriptors\Model\TrackedChangesEdFiEligibilityEvaluationTypeDescriptorDelete[]**](../Model/TrackedChangesEdFiEligibilityEvaluationTypeDescriptorDelete.md)

### Authorization

[oauth2_client_credentials](../../README.md#oauth2_client_credentials)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEligibilityEvaluationTypeDescriptors()`

```php
getEligibilityEvaluationTypeDescriptors($offset, $limit, $page_token, $page_size, $min_change_version, $max_change_version, $total_count, $code_value, $description, $effective_begin_date, $effective_end_date, $id, $namespace, $short_description, $use_snapshot): \Descriptors\Model\EdFiEligibilityEvaluationTypeDescriptor[]
```

Retrieves specific resources using the resource's property values (using the \"Get\" pattern).

This GET operation provides access to resources using the \"Get\" search pattern.  The values of any properties of the resource that are specified will be used to return all matching results (if it exists).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\EligibilityEvaluationTypeDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$offset = 56; // int | Indicates how many items should be skipped before returning results.
$limit = 25; // int | Indicates the maximum number of items that should be returned in the results.
$page_token = 'page_token_example'; // string | The token of the page to retrieve, obtained either from the \"Next-Page-Token\" header of the previous request, or from the \"partitions\" endpoint for the resource. Cannot be used with limit/offset paging.
$page_size = 25; // int | The maximum number of items to retrieve in the page. For use with pageToken (cursor paging) only.
$min_change_version = 56; // int | Used in synchronization to set sequence minimum ChangeVersion
$max_change_version = 56; // int | Used in synchronization to set sequence maximum ChangeVersion
$total_count = false; // bool | Indicates if the total number of items available should be returned in the 'Total-Count' header of the response.  If set to false, 'Total-Count' header will not be provided. Must be false when using cursor paging (with pageToken).
$code_value = 'code_value_example'; // string | A code or abbreviation that is used to refer to the descriptor.
$description = 'description_example'; // string | The description of the descriptor.
$effective_begin_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | The beginning date of the period when the descriptor is in effect. If omitted, the default is immediate effectiveness.
$effective_end_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | The end date of the period when the descriptor is in effect.
$id = 'id_example'; // string | 
$namespace = 'namespace_example'; // string | A globally unique namespace that identifies this descriptor set. Author is strongly encouraged to use the Universal Resource Identifier (http, ftp, file, etc.) for the source of the descriptor definition. Best practice is for this source to be the descriptor file itself, so that it can be machine-readable and be fetched in real-time, if necessary.
$short_description = 'short_description_example'; // string | A shortened description for the descriptor.
$use_snapshot = false; // bool | Indicates if the configured Snapshot should be used.

try {
    $result = $apiInstance->getEligibilityEvaluationTypeDescriptors($offset, $limit, $page_token, $page_size, $min_change_version, $max_change_version, $total_count, $code_value, $description, $effective_begin_date, $effective_end_date, $id, $namespace, $short_description, $use_snapshot);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EligibilityEvaluationTypeDescriptorsApi->getEligibilityEvaluationTypeDescriptors: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **offset** | **int**| Indicates how many items should be skipped before returning results. | [optional] |
| **limit** | **int**| Indicates the maximum number of items that should be returned in the results. | [optional] [default to 25] |
| **page_token** | **string**| The token of the page to retrieve, obtained either from the \&quot;Next-Page-Token\&quot; header of the previous request, or from the \&quot;partitions\&quot; endpoint for the resource. Cannot be used with limit/offset paging. | [optional] |
| **page_size** | **int**| The maximum number of items to retrieve in the page. For use with pageToken (cursor paging) only. | [optional] [default to 25] |
| **min_change_version** | **int**| Used in synchronization to set sequence minimum ChangeVersion | [optional] |
| **max_change_version** | **int**| Used in synchronization to set sequence maximum ChangeVersion | [optional] |
| **total_count** | **bool**| Indicates if the total number of items available should be returned in the &#39;Total-Count&#39; header of the response.  If set to false, &#39;Total-Count&#39; header will not be provided. Must be false when using cursor paging (with pageToken). | [optional] [default to false] |
| **code_value** | **string**| A code or abbreviation that is used to refer to the descriptor. | [optional] |
| **description** | **string**| The description of the descriptor. | [optional] |
| **effective_begin_date** | **\DateTime**| The beginning date of the period when the descriptor is in effect. If omitted, the default is immediate effectiveness. | [optional] |
| **effective_end_date** | **\DateTime**| The end date of the period when the descriptor is in effect. | [optional] |
| **id** | **string**|  | [optional] |
| **namespace** | **string**| A globally unique namespace that identifies this descriptor set. Author is strongly encouraged to use the Universal Resource Identifier (http, ftp, file, etc.) for the source of the descriptor definition. Best practice is for this source to be the descriptor file itself, so that it can be machine-readable and be fetched in real-time, if necessary. | [optional] |
| **short_description** | **string**| A shortened description for the descriptor. | [optional] |
| **use_snapshot** | **bool**| Indicates if the configured Snapshot should be used. | [optional] [default to false] |

### Return type

[**\Descriptors\Model\EdFiEligibilityEvaluationTypeDescriptor[]**](../Model/EdFiEligibilityEvaluationTypeDescriptor.md)

### Authorization

[oauth2_client_credentials](../../README.md#oauth2_client_credentials)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEligibilityEvaluationTypeDescriptorsById()`

```php
getEligibilityEvaluationTypeDescriptorsById($id, $if_none_match, $use_snapshot): \Descriptors\Model\EdFiEligibilityEvaluationTypeDescriptor
```

Retrieves a specific resource using the resource's identifier (using the \"Get By Id\" pattern).

This GET operation retrieves a resource by the specified resource identifier.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\EligibilityEvaluationTypeDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | A resource identifier that uniquely identifies the resource.
$if_none_match = 'if_none_match_example'; // string | The previously returned ETag header value, used here to prevent the unnecessary data transfer of an unchanged resource.
$use_snapshot = false; // bool | Indicates if the configured Snapshot should be used.

try {
    $result = $apiInstance->getEligibilityEvaluationTypeDescriptorsById($id, $if_none_match, $use_snapshot);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EligibilityEvaluationTypeDescriptorsApi->getEligibilityEvaluationTypeDescriptorsById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| A resource identifier that uniquely identifies the resource. | |
| **if_none_match** | **string**| The previously returned ETag header value, used here to prevent the unnecessary data transfer of an unchanged resource. | [optional] |
| **use_snapshot** | **bool**| Indicates if the configured Snapshot should be used. | [optional] [default to false] |

### Return type

[**\Descriptors\Model\EdFiEligibilityEvaluationTypeDescriptor**](../Model/EdFiEligibilityEvaluationTypeDescriptor.md)

### Authorization

[oauth2_client_credentials](../../README.md#oauth2_client_credentials)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getEligibilityEvaluationTypeDescriptorsPartitions()`

```php
getEligibilityEvaluationTypeDescriptorsPartitions($number, $min_change_version, $max_change_version, $code_value, $description, $effective_begin_date, $effective_end_date, $id, $namespace, $short_description, $use_snapshot): \Descriptors\Model\GetAbsenceEventCategoryDescriptorsPartitions200Response
```

Retrieves a set of page tokens to be used for efficient client-side parallel processing.

Computes an evenly distributed set of partitions over the accessible data and returns a set of page tokens, each representing the first page of one of the partitions.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\EligibilityEvaluationTypeDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$number = 56; // int | The number of evenly distributed partitions to provide for client-side parallel processing. If unspecified, a reasonable set of partitions will be determined based on the total number of accessible items.
$min_change_version = 56; // int | Used in synchronization to set sequence minimum ChangeVersion
$max_change_version = 56; // int | Used in synchronization to set sequence maximum ChangeVersion
$code_value = 'code_value_example'; // string | A code or abbreviation that is used to refer to the descriptor.
$description = 'description_example'; // string | The description of the descriptor.
$effective_begin_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | The beginning date of the period when the descriptor is in effect. If omitted, the default is immediate effectiveness.
$effective_end_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | The end date of the period when the descriptor is in effect.
$id = 'id_example'; // string | 
$namespace = 'namespace_example'; // string | A globally unique namespace that identifies this descriptor set. Author is strongly encouraged to use the Universal Resource Identifier (http, ftp, file, etc.) for the source of the descriptor definition. Best practice is for this source to be the descriptor file itself, so that it can be machine-readable and be fetched in real-time, if necessary.
$short_description = 'short_description_example'; // string | A shortened description for the descriptor.
$use_snapshot = false; // bool | Indicates if the configured Snapshot should be used.

try {
    $result = $apiInstance->getEligibilityEvaluationTypeDescriptorsPartitions($number, $min_change_version, $max_change_version, $code_value, $description, $effective_begin_date, $effective_end_date, $id, $namespace, $short_description, $use_snapshot);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EligibilityEvaluationTypeDescriptorsApi->getEligibilityEvaluationTypeDescriptorsPartitions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **number** | **int**| The number of evenly distributed partitions to provide for client-side parallel processing. If unspecified, a reasonable set of partitions will be determined based on the total number of accessible items. | [optional] |
| **min_change_version** | **int**| Used in synchronization to set sequence minimum ChangeVersion | [optional] |
| **max_change_version** | **int**| Used in synchronization to set sequence maximum ChangeVersion | [optional] |
| **code_value** | **string**| A code or abbreviation that is used to refer to the descriptor. | [optional] |
| **description** | **string**| The description of the descriptor. | [optional] |
| **effective_begin_date** | **\DateTime**| The beginning date of the period when the descriptor is in effect. If omitted, the default is immediate effectiveness. | [optional] |
| **effective_end_date** | **\DateTime**| The end date of the period when the descriptor is in effect. | [optional] |
| **id** | **string**|  | [optional] |
| **namespace** | **string**| A globally unique namespace that identifies this descriptor set. Author is strongly encouraged to use the Universal Resource Identifier (http, ftp, file, etc.) for the source of the descriptor definition. Best practice is for this source to be the descriptor file itself, so that it can be machine-readable and be fetched in real-time, if necessary. | [optional] |
| **short_description** | **string**| A shortened description for the descriptor. | [optional] |
| **use_snapshot** | **bool**| Indicates if the configured Snapshot should be used. | [optional] [default to false] |

### Return type

[**\Descriptors\Model\GetAbsenceEventCategoryDescriptorsPartitions200Response**](../Model/GetAbsenceEventCategoryDescriptorsPartitions200Response.md)

### Authorization

[oauth2_client_credentials](../../README.md#oauth2_client_credentials)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `keyChangesEligibilityEvaluationTypeDescriptors()`

```php
keyChangesEligibilityEvaluationTypeDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $use_snapshot): \Descriptors\Model\TrackedChangesEdFiEligibilityEvaluationTypeDescriptorKeyChange[]
```

Retrieves resources key changes based on change version.

This operation is used to retrieve identifying information about resources whose key values have been changed.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\EligibilityEvaluationTypeDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$offset = 56; // int | Indicates how many items should be skipped before returning results.
$limit = 25; // int | Indicates the maximum number of items that should be returned in the results.
$min_change_version = 56; // int | Used in synchronization to set sequence minimum ChangeVersion
$max_change_version = 56; // int | Used in synchronization to set sequence maximum ChangeVersion
$total_count = false; // bool | Indicates if the total number of items available should be returned in the 'Total-Count' header of the response.  If set to false, 'Total-Count' header will not be provided. Must be false when using cursor paging (with pageToken).
$use_snapshot = false; // bool | Indicates if the configured Snapshot should be used.

try {
    $result = $apiInstance->keyChangesEligibilityEvaluationTypeDescriptors($offset, $limit, $min_change_version, $max_change_version, $total_count, $use_snapshot);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EligibilityEvaluationTypeDescriptorsApi->keyChangesEligibilityEvaluationTypeDescriptors: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **offset** | **int**| Indicates how many items should be skipped before returning results. | [optional] |
| **limit** | **int**| Indicates the maximum number of items that should be returned in the results. | [optional] [default to 25] |
| **min_change_version** | **int**| Used in synchronization to set sequence minimum ChangeVersion | [optional] |
| **max_change_version** | **int**| Used in synchronization to set sequence maximum ChangeVersion | [optional] |
| **total_count** | **bool**| Indicates if the total number of items available should be returned in the &#39;Total-Count&#39; header of the response.  If set to false, &#39;Total-Count&#39; header will not be provided. Must be false when using cursor paging (with pageToken). | [optional] [default to false] |
| **use_snapshot** | **bool**| Indicates if the configured Snapshot should be used. | [optional] [default to false] |

### Return type

[**\Descriptors\Model\TrackedChangesEdFiEligibilityEvaluationTypeDescriptorKeyChange[]**](../Model/TrackedChangesEdFiEligibilityEvaluationTypeDescriptorKeyChange.md)

### Authorization

[oauth2_client_credentials](../../README.md#oauth2_client_credentials)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postEligibilityEvaluationTypeDescriptor()`

```php
postEligibilityEvaluationTypeDescriptor($ed_fi_eligibility_evaluation_type_descriptor)
```

Creates or updates resources based on the natural key values of the supplied resource.

The POST operation can be used to create or update resources. In database terms, this is often referred to as an \"upsert\" operation (insert + update). Clients should NOT include the resource \"id\" in the JSON body because it will result in an error. The web service will identify whether the resource already exists based on the natural key values provided, and update or create the resource appropriately. It is recommended to use POST for both create and update except while updating natural key of a resource in which case PUT operation must be used.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\EligibilityEvaluationTypeDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ed_fi_eligibility_evaluation_type_descriptor = new \Descriptors\Model\EdFiEligibilityEvaluationTypeDescriptor(); // \Descriptors\Model\EdFiEligibilityEvaluationTypeDescriptor | The JSON representation of the \"eligibilityEvaluationTypeDescriptor\" resource to be created or updated.

try {
    $apiInstance->postEligibilityEvaluationTypeDescriptor($ed_fi_eligibility_evaluation_type_descriptor);
} catch (Exception $e) {
    echo 'Exception when calling EligibilityEvaluationTypeDescriptorsApi->postEligibilityEvaluationTypeDescriptor: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **ed_fi_eligibility_evaluation_type_descriptor** | [**\Descriptors\Model\EdFiEligibilityEvaluationTypeDescriptor**](../Model/EdFiEligibilityEvaluationTypeDescriptor.md)| The JSON representation of the \&quot;eligibilityEvaluationTypeDescriptor\&quot; resource to be created or updated. | |

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

## `putEligibilityEvaluationTypeDescriptor()`

```php
putEligibilityEvaluationTypeDescriptor($id, $ed_fi_eligibility_evaluation_type_descriptor, $if_match)
```

Updates a resource based on the resource identifier.

The PUT operation is used to update a resource by identifier. If the resource identifier (\"id\") is provided in the JSON body, it will be ignored. Additionally, this API resource is not configured for cascading natural key updates. Natural key values for this resource cannot be changed using PUT operation, so the recommendation is to use POST as that supports upsert behavior.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2_client_credentials
$config = Descriptors\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Descriptors\Api\EligibilityEvaluationTypeDescriptorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | A resource identifier that uniquely identifies the resource.
$ed_fi_eligibility_evaluation_type_descriptor = new \Descriptors\Model\EdFiEligibilityEvaluationTypeDescriptor(); // \Descriptors\Model\EdFiEligibilityEvaluationTypeDescriptor | The JSON representation of the \"eligibilityEvaluationTypeDescriptor\" resource to be created or updated.
$if_match = 'if_match_example'; // string | The ETag header value used to prevent the PUT from updating a resource modified by another consumer.

try {
    $apiInstance->putEligibilityEvaluationTypeDescriptor($id, $ed_fi_eligibility_evaluation_type_descriptor, $if_match);
} catch (Exception $e) {
    echo 'Exception when calling EligibilityEvaluationTypeDescriptorsApi->putEligibilityEvaluationTypeDescriptor: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| A resource identifier that uniquely identifies the resource. | |
| **ed_fi_eligibility_evaluation_type_descriptor** | [**\Descriptors\Model\EdFiEligibilityEvaluationTypeDescriptor**](../Model/EdFiEligibilityEvaluationTypeDescriptor.md)| The JSON representation of the \&quot;eligibilityEvaluationTypeDescriptor\&quot; resource to be created or updated. | |
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
