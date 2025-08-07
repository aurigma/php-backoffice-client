# Aurigma\BackOffice\ProductReferencesManagementApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**productReferencesManagementCreate()**](ProductReferencesManagementApi.md#productReferencesManagementCreate) | **POST** /api/backoffice/v1/product-references | Creates a new storefront product reference. |
| [**productReferencesManagementDelete()**](ProductReferencesManagementApi.md#productReferencesManagementDelete) | **DELETE** /api/backoffice/v1/product-references/{reference} | Deletes the storefront product reference. |
| [**productReferencesManagementGet()**](ProductReferencesManagementApi.md#productReferencesManagementGet) | **GET** /api/backoffice/v1/product-references/{reference} | Returns a storefront product reference. |
| [**productReferencesManagementGetAll()**](ProductReferencesManagementApi.md#productReferencesManagementGetAll) | **GET** /api/backoffice/v1/product-references | Returns all storefront product references relevant to the specified query parameters. |


## `productReferencesManagementCreate()`

```php
productReferencesManagementCreate($storefront_id, $tenant_id, $create_product_reference_dto): \Aurigma\BackOffice\Model\ProductReferenceDto
```

Creates a new storefront product reference.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

// Configure OAuth2 access token for authorization: OAuth2ClientCredentials
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure OAuth2 access token for authorization: OAuth2Implicit
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure API key authorization: Bearer
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Aurigma\BackOffice\Api\ProductReferencesManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$storefront_id = 56; // int | Storefront identifier.
$tenant_id = 56; // int | Tenant identifier.
$create_product_reference_dto = new \Aurigma\BackOffice\Model\CreateProductReferenceDto(); // \Aurigma\BackOffice\Model\CreateProductReferenceDto | Create operation parameters.

try {
    $result = $apiInstance->productReferencesManagementCreate($storefront_id, $tenant_id, $create_product_reference_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductReferencesManagementApi->productReferencesManagementCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **storefront_id** | **int**| Storefront identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **create_product_reference_dto** | [**\Aurigma\BackOffice\Model\CreateProductReferenceDto**](../Model/CreateProductReferenceDto.md)| Create operation parameters. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\ProductReferenceDto**](../Model/ProductReferenceDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productReferencesManagementDelete()`

```php
productReferencesManagementDelete($reference, $storefront_id, $tenant_id): \Aurigma\BackOffice\Model\ProductReferenceDto
```

Deletes the storefront product reference.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

// Configure OAuth2 access token for authorization: OAuth2ClientCredentials
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure OAuth2 access token for authorization: OAuth2Implicit
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure API key authorization: Bearer
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Aurigma\BackOffice\Api\ProductReferencesManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reference = 'reference_example'; // string | Product reference - external reference to Customer's Canvas product specification, e.g online store product identifier.
$storefront_id = 56; // int | Storefront identifier.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->productReferencesManagementDelete($reference, $storefront_id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductReferencesManagementApi->productReferencesManagementDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference** | **string**| Product reference - external reference to Customer&#39;s Canvas product specification, e.g online store product identifier. | |
| **storefront_id** | **int**| Storefront identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\ProductReferenceDto**](../Model/ProductReferenceDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productReferencesManagementGet()`

```php
productReferencesManagementGet($reference, $storefront_id, $tenant_id): \Aurigma\BackOffice\Model\ProductReferenceDto
```

Returns a storefront product reference.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

// Configure OAuth2 access token for authorization: OAuth2ClientCredentials
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure OAuth2 access token for authorization: OAuth2Implicit
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure API key authorization: Bearer
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Aurigma\BackOffice\Api\ProductReferencesManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reference = 'reference_example'; // string | An external reference to Customer's Canvas product, e.g online store product identifier.
$storefront_id = 56; // int | Storefront identifier.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->productReferencesManagementGet($reference, $storefront_id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductReferencesManagementApi->productReferencesManagementGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference** | **string**| An external reference to Customer&#39;s Canvas product, e.g online store product identifier. | |
| **storefront_id** | **int**| Storefront identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\ProductReferenceDto**](../Model/ProductReferenceDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productReferencesManagementGetAll()`

```php
productReferencesManagementGetAll($storefront_id, $product_reference, $product_specification_id, $product_id, $product_link_id, $skip, $take, $sorting, $search, $sku, $tags, $custom_fields, $tenant_id): \Aurigma\BackOffice\Model\PagedOfProductReferenceDto
```

Returns all storefront product references relevant to the specified query parameters.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

// Configure OAuth2 access token for authorization: OAuth2ClientCredentials
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure OAuth2 access token for authorization: OAuth2Implicit
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure API key authorization: Bearer
$config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Aurigma\BackOffice\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new Aurigma\BackOffice\Api\ProductReferencesManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$storefront_id = 56; // int | Storefront identifier.
$product_reference = 'product_reference_example'; // string | Product reference filter.  Product reference is an external reference to Customer's Canvas product, e.g online store product identifier.
$product_specification_id = 56; // int | Customer's Canvas product specification filter.
$product_id = 56; // int | Customer's Canvas product filter.
$product_link_id = 56; // int | Customer's Canvas product link filter.
$skip = 56; // int | Defines page start offset from beginning of sorted result list.
$take = 56; // int | Defines page length (how many consequent items of sorted result list should be taken).
$sorting = 'sorting_example'; // string | Defines sorting order of result list e.g.: \"Title ASC, LastModified DESC\".
$search = 'search_example'; // string | Search string for partial match.
$sku = 'sku_example'; // string | SKU filter.
$tags = array('tags_example'); // string[] | List of tags that product should have.
$custom_fields = 'custom_fields_example'; // string | Serialized custom fields dictionary filter. For example: {\"public\":\"true\",\"name\":\"my item\"}.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->productReferencesManagementGetAll($storefront_id, $product_reference, $product_specification_id, $product_id, $product_link_id, $skip, $take, $sorting, $search, $sku, $tags, $custom_fields, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductReferencesManagementApi->productReferencesManagementGetAll: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **storefront_id** | **int**| Storefront identifier. | |
| **product_reference** | **string**| Product reference filter.  Product reference is an external reference to Customer&#39;s Canvas product, e.g online store product identifier. | [optional] |
| **product_specification_id** | **int**| Customer&#39;s Canvas product specification filter. | [optional] |
| **product_id** | **int**| Customer&#39;s Canvas product filter. | [optional] |
| **product_link_id** | **int**| Customer&#39;s Canvas product link filter. | [optional] |
| **skip** | **int**| Defines page start offset from beginning of sorted result list. | [optional] |
| **take** | **int**| Defines page length (how many consequent items of sorted result list should be taken). | [optional] |
| **sorting** | **string**| Defines sorting order of result list e.g.: \&quot;Title ASC, LastModified DESC\&quot;. | [optional] |
| **search** | **string**| Search string for partial match. | [optional] |
| **sku** | **string**| SKU filter. | [optional] |
| **tags** | [**string[]**](../Model/string.md)| List of tags that product should have. | [optional] |
| **custom_fields** | **string**| Serialized custom fields dictionary filter. For example: {\&quot;public\&quot;:\&quot;true\&quot;,\&quot;name\&quot;:\&quot;my item\&quot;}. | [optional] |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\PagedOfProductReferenceDto**](../Model/PagedOfProductReferenceDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
