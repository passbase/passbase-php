# Passbase\IdentityApi

All URIs are relative to *https://api.passbase.com/verification/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getIdentityResourceById**](IdentityApi.md#getidentityresourcebyid) | **GET** /identities/{id}/resource/{resource_id} | Get resource
[**getIdentyById**](IdentityApi.md#getidentybyid) | **GET** /identities/{id} | Get identity
[**listIdentities**](IdentityApi.md#listidentities) | **GET** /identities | List identities
[**listIdentityResources**](IdentityApi.md#listidentityresources) | **GET** /identities/{id}/resources | List resources

# **getIdentityResourceById**
> \Passbase\Models\Resource getIdentityResourceById($id, $resource_id)

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
$id = "id_example"; // string | Identity id
$resource_id = "resource_id_example"; // string | Resource id

try {
    $result = $apiInstance->getIdentityResourceById($id, $resource_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentityApi->getIdentityResourceById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Identity id |
 **resource_id** | **string**| Resource id |

### Return type

[**\Passbase\Models\Resource**](../Model/Resource.md)

### Authorization

[SecretApiKey](../../README.md#SecretApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getIdentyById**
> \Passbase\Models\Identity[] getIdentyById($id)

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
$id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Unique ID of the identity to return

try {
    $result = $apiInstance->getIdentyById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentityApi->getIdentyById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**string**](../Model/.md)| Unique ID of the identity to return |

### Return type

[**\Passbase\Models\Identity[]**](../Model/Identity.md)

### Authorization

[SecretApiKey](../../README.md#SecretApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listIdentities**
> \Passbase\Models\PaginatedIdentities listIdentities($limit, $cursor)

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
$limit = 56; // int | 
$cursor = "cursor_example"; // string | 

try {
    $result = $apiInstance->listIdentities($limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentityApi->listIdentities: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**|  | [optional]
 **cursor** | **string**|  | [optional]

### Return type

[**\Passbase\Models\PaginatedIdentities**](../Model/PaginatedIdentities.md)

### Authorization

[SecretApiKey](../../README.md#SecretApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listIdentityResources**
> \Passbase\Models\PaginatedResources listIdentityResources($id, $limit, $cursor)

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
$id = "id_example"; // string | Identity id
$limit = 56; // int | 
$cursor = "cursor_example"; // string | 

try {
    $result = $apiInstance->listIdentityResources($id, $limit, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentityApi->listIdentityResources: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Identity id |
 **limit** | **int**|  | [optional]
 **cursor** | **string**|  | [optional]

### Return type

[**\Passbase\Models\PaginatedResources**](../Model/PaginatedResources.md)

### Authorization

[SecretApiKey](../../README.md#SecretApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

