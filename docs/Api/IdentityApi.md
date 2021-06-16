# Passbase\IdentityApi

All URIs are relative to https://api.passbase.com/verification/v2.

Method | HTTP request | Description
------------- | ------------- | -------------
[**getIdentityById()**](IdentityApi.md#getIdentityById) | **GET** /identities/{id} | Get identity
[**getIdentityResourceById()**](IdentityApi.md#getIdentityResourceById) | **GET** /identity/{id}/resources/{resource_id} | Get resource
[**getIdentityResourceFileById()**](IdentityApi.md#getIdentityResourceFileById) | **GET** /identity/{id}/resources/{resource_id}/resource_files/{resource_file_id} | Get resource file
[**listIdentities()**](IdentityApi.md#listIdentities) | **GET** /identities | List identities
[**listIdentityResources()**](IdentityApi.md#listIdentityResources) | **GET** /identity/{id}/resources | List resources


## `getIdentityById()`

```php
getIdentityById($id): \Passbase\models\Identity
```

Get identity

Retrieve an identity by providing the identity ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: SecretApiKey
$config = Passbase\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Passbase\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new Passbase\Api\IdentityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Unique ID of the identity to return

try {
    $result = $apiInstance->getIdentityById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentityApi->getIdentityById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**string**](../Model/.md)| Unique ID of the identity to return |

### Return type

[**\Passbase\models\Identity**](../Model/Identity.md)

### Authorization

[SecretApiKey](../../README.md#SecretApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getIdentityResourceById()`

```php
getIdentityResourceById($id, $resource_id): \Passbase\models\Resource
```

Get resource

Get a resource attached to an identity by providing the resource ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: SecretApiKey
$config = Passbase\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Passbase\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new Passbase\Api\IdentityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Identity id
$resource_id = 'resource_id_example'; // string | Resource id

try {
    $result = $apiInstance->getIdentityResourceById($id, $resource_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentityApi->getIdentityResourceById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Identity id |
 **resource_id** | **string**| Resource id |

### Return type

[**\Passbase\models\Resource**](../Model/Resource.md)

### Authorization

[SecretApiKey](../../README.md#SecretApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getIdentityResourceFileById()`

```php
getIdentityResourceFileById($id, $resource_id, $resource_file_id): \Passbase\models\ResourceFile
```

Get resource file

Get a raw resource file attached to an identity by providing the resource ID and the resource file ID. This is a protected route and you'll need a specific government authorization to access it.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: SecretApiKey
$config = Passbase\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Passbase\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new Passbase\Api\IdentityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Identity id
$resource_id = 'resource_id_example'; // string | Resource id
$resource_file_id = 'resource_file_id_example'; // string | Resource file id

try {
    $result = $apiInstance->getIdentityResourceFileById($id, $resource_id, $resource_file_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentityApi->getIdentityResourceFileById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Identity id |
 **resource_id** | **string**| Resource id |
 **resource_file_id** | **string**| Resource file id |

### Return type

[**\Passbase\models\ResourceFile**](../Model/ResourceFile.md)

### Authorization

[SecretApiKey](../../README.md#SecretApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listIdentities()`

```php
listIdentities($limit, $cursor): \Passbase\models\PaginatedIdentities
```

List identities

List all the identities retrievable by the provided API Secret Key.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: SecretApiKey
$config = Passbase\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Passbase\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new Passbase\Api\IdentityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 100; // int
$cursor = aWQ6NDA3MQ%3D%3D; // string

try {
    $result = $apiInstance->listIdentities($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentityApi->listIdentities: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**|  | [optional]
 **cursor** | **string**|  | [optional]

### Return type

[**\Passbase\models\PaginatedIdentities**](../Model/PaginatedIdentities.md)

### Authorization

[SecretApiKey](../../README.md#SecretApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listIdentityResources()`

```php
listIdentityResources($id, $limit, $cursor): \Passbase\models\PaginatedResources
```

List resources

List resources attached to an identity by providing the identity ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: SecretApiKey
$config = Passbase\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Passbase\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new Passbase\Api\IdentityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Identity id
$limit = 100; // int
$cursor = aWQ6NDA3MQ%3D%3D; // string

try {
    $result = $apiInstance->listIdentityResources($id, $limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentityApi->listIdentityResources: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Identity id |
 **limit** | **int**|  | [optional]
 **cursor** | **string**|  | [optional]

### Return type

[**\Passbase\models\PaginatedResources**](../Model/PaginatedResources.md)

### Authorization

[SecretApiKey](../../README.md#SecretApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
