# Aurigma\BackOffice\ProductsManagementApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**productsManagementCreateDesignsConnections()**](ProductsManagementApi.md#productsManagementCreateDesignsConnections) | **POST** /api/backoffice/v1/products/{id}/design-connections | Creates new designs connections for a specified product. |
| [**productsManagementCreateDocumentsConnections()**](ProductsManagementApi.md#productsManagementCreateDocumentsConnections) | **POST** /api/backoffice/v1/products/{id}/document-connections | Creates new documents connections for a specified product. |
| [**productsManagementCreateMockupsConnections()**](ProductsManagementApi.md#productsManagementCreateMockupsConnections) | **POST** /api/backoffice/v1/products/{id}/mockup-connections | Creates new mockups connections for a specified product. |
| [**productsManagementCreateProduct()**](ProductsManagementApi.md#productsManagementCreateProduct) | **POST** /api/backoffice/v1/products | Creates a new product and returns its description. |
| [**productsManagementDeleteProduct()**](ProductsManagementApi.md#productsManagementDeleteProduct) | **DELETE** /api/backoffice/v1/products/{id} | Deletes a product by its identifier. |
| [**productsManagementGetAllProducts()**](ProductsManagementApi.md#productsManagementGetAllProducts) | **GET** /api/backoffice/v1/products | Returns all products, relevant to the specified query parameters. |
| [**productsManagementGetAvailablePersonalizationWorkflows()**](ProductsManagementApi.md#productsManagementGetAvailablePersonalizationWorkflows) | **GET** /api/backoffice/v1/products/available-workflows | Returns all available product personalization workflows. |
| [**productsManagementGetAvailableProcessingPipelines()**](ProductsManagementApi.md#productsManagementGetAvailableProcessingPipelines) | **GET** /api/backoffice/v1/products/available-pipelines | Returns all available product processing pipelines. |
| [**productsManagementGetProduct()**](ProductsManagementApi.md#productsManagementGetProduct) | **GET** /api/backoffice/v1/products/{id} | Returns a product by its identifier. |
| [**productsManagementGetProductOptions()**](ProductsManagementApi.md#productsManagementGetProductOptions) | **GET** /api/backoffice/v1/products/{id}/options | Returns a list of product options. |
| [**productsManagementGetProductVariant()**](ProductsManagementApi.md#productsManagementGetProductVariant) | **GET** /api/backoffice/v1/products/{id}/variants/{productVariantId} | Returns a product variant. |
| [**productsManagementGetProductVariantDesigns()**](ProductsManagementApi.md#productsManagementGetProductVariantDesigns) | **GET** /api/backoffice/v1/products/{id}/variant-designs | Returns a list of product variant designs. |
| [**productsManagementGetProductVariantDocuments()**](ProductsManagementApi.md#productsManagementGetProductVariantDocuments) | **GET** /api/backoffice/v1/products/{id}/variant-documents | Returns a list of product variant documents. |
| [**productsManagementGetProductVariantMockups()**](ProductsManagementApi.md#productsManagementGetProductVariantMockups) | **GET** /api/backoffice/v1/products/{id}/variant-mockups | Returns a list of product variant mockups. |
| [**productsManagementGetProductVariants()**](ProductsManagementApi.md#productsManagementGetProductVariants) | **GET** /api/backoffice/v1/products/{id}/variants | Returns a list of product variants. |
| [**productsManagementImportProducts()**](ProductsManagementApi.md#productsManagementImportProducts) | **POST** /api/backoffice/v1/products/import | Imports products from a specific CSV file and returns a list of imported products descriptions. |
| [**productsManagementRemoveDesignsConnections()**](ProductsManagementApi.md#productsManagementRemoveDesignsConnections) | **DELETE** /api/backoffice/v1/products/{id}/design-connections | Removes designs connections for a specified product. |
| [**productsManagementRemoveDocumentsConnections()**](ProductsManagementApi.md#productsManagementRemoveDocumentsConnections) | **DELETE** /api/backoffice/v1/products/{id}/document-connections | Removes documents connections for a specified product. |
| [**productsManagementRemoveMockupsConnections()**](ProductsManagementApi.md#productsManagementRemoveMockupsConnections) | **DELETE** /api/backoffice/v1/products/{id}/mockup-connections | Removes mockups connections for a specified product. |
| [**productsManagementSetProductVariantAvailability()**](ProductsManagementApi.md#productsManagementSetProductVariantAvailability) | **POST** /api/backoffice/v1/products/{id}/set-variant-availability | Set product variants availability. Variants identifiers will be changed. |
| [**productsManagementSetProductVariantPrice()**](ProductsManagementApi.md#productsManagementSetProductVariantPrice) | **POST** /api/backoffice/v1/products/{id}/set-variant-price | Set product variants price. Variants identifiers will be changed. |
| [**productsManagementSetProductVariantSku()**](ProductsManagementApi.md#productsManagementSetProductVariantSku) | **POST** /api/backoffice/v1/products/{id}/set-variant-sku | Set product variants SKU. Variants identifiers will be changed. |


## `productsManagementCreateDesignsConnections()`

```php
productsManagementCreateDesignsConnections($id, $tenant_id, $create_product_design_connections_dto)
```

Creates new designs connections for a specified product.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Product identifier.
$tenant_id = 56; // int | Tenant identifier.
$create_product_design_connections_dto = new \Aurigma\BackOffice\Model\CreateProductDesignConnectionsDto(); // \Aurigma\BackOffice\Model\CreateProductDesignConnectionsDto | Product designs connections creation parameters.

try {
    $apiInstance->productsManagementCreateDesignsConnections($id, $tenant_id, $create_product_design_connections_dto);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementCreateDesignsConnections: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Product identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **create_product_design_connections_dto** | [**\Aurigma\BackOffice\Model\CreateProductDesignConnectionsDto**](../Model/CreateProductDesignConnectionsDto.md)| Product designs connections creation parameters. | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementCreateDocumentsConnections()`

```php
productsManagementCreateDocumentsConnections($id, $tenant_id, $create_product_document_connections_dto)
```

Creates new documents connections for a specified product.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Product identifier.
$tenant_id = 56; // int | Tenant identifier.
$create_product_document_connections_dto = new \Aurigma\BackOffice\Model\CreateProductDocumentConnectionsDto(); // \Aurigma\BackOffice\Model\CreateProductDocumentConnectionsDto | Product documents connections creation parameters.

try {
    $apiInstance->productsManagementCreateDocumentsConnections($id, $tenant_id, $create_product_document_connections_dto);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementCreateDocumentsConnections: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Product identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **create_product_document_connections_dto** | [**\Aurigma\BackOffice\Model\CreateProductDocumentConnectionsDto**](../Model/CreateProductDocumentConnectionsDto.md)| Product documents connections creation parameters. | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementCreateMockupsConnections()`

```php
productsManagementCreateMockupsConnections($id, $tenant_id, $create_product_mockup_connections_dto)
```

Creates new mockups connections for a specified product.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Product identifier.
$tenant_id = 56; // int | Tenant identifier.
$create_product_mockup_connections_dto = new \Aurigma\BackOffice\Model\CreateProductMockupConnectionsDto(); // \Aurigma\BackOffice\Model\CreateProductMockupConnectionsDto | Product mockups connections creation parameters.

try {
    $apiInstance->productsManagementCreateMockupsConnections($id, $tenant_id, $create_product_mockup_connections_dto);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementCreateMockupsConnections: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Product identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **create_product_mockup_connections_dto** | [**\Aurigma\BackOffice\Model\CreateProductMockupConnectionsDto**](../Model/CreateProductMockupConnectionsDto.md)| Product mockups connections creation parameters. | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementCreateProduct()`

```php
productsManagementCreateProduct($tenant_id, $create_product_dto): \Aurigma\BackOffice\Model\ProductDto
```

Creates a new product and returns its description.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenant_id = 56; // int | Tenant identifier.
$create_product_dto = new \Aurigma\BackOffice\Model\CreateProductDto(); // \Aurigma\BackOffice\Model\CreateProductDto

try {
    $result = $apiInstance->productsManagementCreateProduct($tenant_id, $create_product_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementCreateProduct: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **create_product_dto** | [**\Aurigma\BackOffice\Model\CreateProductDto**](../Model/CreateProductDto.md)|  | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\ProductDto**](../Model/ProductDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementDeleteProduct()`

```php
productsManagementDeleteProduct($id, $tenant_id)
```

Deletes a product by its identifier.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Product identifier.
$tenant_id = 56; // int | Tenant identifier.

try {
    $apiInstance->productsManagementDeleteProduct($id, $tenant_id);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementDeleteProduct: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Product identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementGetAllProducts()`

```php
productsManagementGetAllProducts($skip, $take, $sorting, $search, $sku, $tags, $custom_fields, $tenant_id): \Aurigma\BackOffice\Model\PagedOfProductDto
```

Returns all products, relevant to the specified query parameters.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$skip = 56; // int | Defines page start offset from beginning of sorted result list.
$take = 56; // int | Defines page length (how many consequent items of sorted result list should be taken).
$sorting = 'sorting_example'; // string | Defines sorting order of result list e.g.: \"Title ASC, LastModified DESC\".
$search = 'search_example'; // string | Search string for partial match.
$sku = 'sku_example'; // string | SKU of linked ecommerce product.
$tags = array('tags_example'); // string[] | List of tags that product should have.
$custom_fields = 'custom_fields_example'; // string | Serialized custom fields dictionary filter. For example: {\"public\":\"true\",\"name\":\"my item\"}.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->productsManagementGetAllProducts($skip, $take, $sorting, $search, $sku, $tags, $custom_fields, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementGetAllProducts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **skip** | **int**| Defines page start offset from beginning of sorted result list. | [optional] |
| **take** | **int**| Defines page length (how many consequent items of sorted result list should be taken). | [optional] |
| **sorting** | **string**| Defines sorting order of result list e.g.: \&quot;Title ASC, LastModified DESC\&quot;. | [optional] |
| **search** | **string**| Search string for partial match. | [optional] |
| **sku** | **string**| SKU of linked ecommerce product. | [optional] |
| **tags** | [**string[]**](../Model/string.md)| List of tags that product should have. | [optional] |
| **custom_fields** | **string**| Serialized custom fields dictionary filter. For example: {\&quot;public\&quot;:\&quot;true\&quot;,\&quot;name\&quot;:\&quot;my item\&quot;}. | [optional] |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\PagedOfProductDto**](../Model/PagedOfProductDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementGetAvailablePersonalizationWorkflows()`

```php
productsManagementGetAvailablePersonalizationWorkflows($skip, $take, $search, $tenant_id): \Aurigma\BackOffice\Model\PagedOfPersonalizationWorkflowDto
```

Returns all available product personalization workflows.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$skip = 56; // int | Defines page start offset from beginning of sorted result list.
$take = 56; // int | Defines page length (how many consequent items of sorted result list should be taken).
$search = 'search_example'; // string | Search string for partial by personalization workflow name.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->productsManagementGetAvailablePersonalizationWorkflows($skip, $take, $search, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementGetAvailablePersonalizationWorkflows: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **skip** | **int**| Defines page start offset from beginning of sorted result list. | [optional] |
| **take** | **int**| Defines page length (how many consequent items of sorted result list should be taken). | [optional] |
| **search** | **string**| Search string for partial by personalization workflow name. | [optional] |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\PagedOfPersonalizationWorkflowDto**](../Model/PagedOfPersonalizationWorkflowDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementGetAvailableProcessingPipelines()`

```php
productsManagementGetAvailableProcessingPipelines($skip, $take, $search, $tenant_id): \Aurigma\BackOffice\Model\PagedOfProcessingPipelineDto
```

Returns all available product processing pipelines.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$skip = 56; // int | Defines page start offset from beginning of sorted result list.
$take = 56; // int | Defines page length (how many consequent items of sorted result list should be taken).
$search = 'search_example'; // string | Search string for partial by processing pipeline name.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->productsManagementGetAvailableProcessingPipelines($skip, $take, $search, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementGetAvailableProcessingPipelines: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **skip** | **int**| Defines page start offset from beginning of sorted result list. | [optional] |
| **take** | **int**| Defines page length (how many consequent items of sorted result list should be taken). | [optional] |
| **search** | **string**| Search string for partial by processing pipeline name. | [optional] |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\PagedOfProcessingPipelineDto**](../Model/PagedOfProcessingPipelineDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementGetProduct()`

```php
productsManagementGetProduct($id, $product_version_id, $tenant_id): \Aurigma\BackOffice\Model\ProductDto
```

Returns a product by its identifier.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Product identifier.
$product_version_id = 56; // int | Product version identifier.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->productsManagementGetProduct($id, $product_version_id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementGetProduct: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Product identifier. | |
| **product_version_id** | **int**| Product version identifier. | [optional] |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\ProductDto**](../Model/ProductDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementGetProductOptions()`

```php
productsManagementGetProductOptions($id, $product_version_id, $tenant_id): \Aurigma\BackOffice\Model\PagedOfProductOptionDto
```

Returns a list of product options.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Product identifier.
$product_version_id = 56; // int | Product version identifier.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->productsManagementGetProductOptions($id, $product_version_id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementGetProductOptions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Product identifier. | |
| **product_version_id** | **int**| Product version identifier. | [optional] |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\PagedOfProductOptionDto**](../Model/PagedOfProductOptionDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementGetProductVariant()`

```php
productsManagementGetProductVariant($id, $product_variant_id, $product_version_id, $tenant_id): \Aurigma\BackOffice\Model\ProductVariantDto
```

Returns a product variant.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Product identifier.
$product_variant_id = 56; // int | Product variant identifier.
$product_version_id = 56; // int | Product version identifier.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->productsManagementGetProductVariant($id, $product_variant_id, $product_version_id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementGetProductVariant: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Product identifier. | |
| **product_variant_id** | **int**| Product variant identifier. | |
| **product_version_id** | **int**| Product version identifier. | [optional] |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\ProductVariantDto**](../Model/ProductVariantDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementGetProductVariantDesigns()`

```php
productsManagementGetProductVariantDesigns($id, $product_version_id, $product_variant_id, $search, $design_custom_fields, $design_path, $skip, $take, $options, $product_filter_id, $take_available_only, $sku, $tenant_id): \Aurigma\BackOffice\Model\PagedOfProductVariantDesignDto
```

Returns a list of product variant designs.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Product identifier.
$product_version_id = 56; // int | Product version identifier.
$product_variant_id = 56; // int | Product variant identifier.
$search = 'search_example'; // string | Search string for design name partial match.
$design_custom_fields = 'design_custom_fields_example'; // string | Custom attributes dictionary filter for designs. For example: {\"public\":\"true\",\"name\":\"my item\"}
$design_path = 'design_path_example'; // string | Path filter for designs. Subfolders included by default.
$skip = 56; // int | Defines page start offset from beginning of sorted result list.
$take = 56; // int | Defines page length (how many consequent items of sorted result list should be taken).
$options = 'options_example'; // string | Defines options filter e.g.: \"{ \"opt1_id\": \"opt1_val1_id, opt1_val2_id\", \"opt2_id\": \"opt2_val1_id\" }\".
$product_filter_id = 56; // int | Defines special filter based on product filter with specified identifier.
$take_available_only = True; // bool | Defines special filter for available product variants.
$sku = 'sku_example'; // string | SKU of linked ecommerce product.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->productsManagementGetProductVariantDesigns($id, $product_version_id, $product_variant_id, $search, $design_custom_fields, $design_path, $skip, $take, $options, $product_filter_id, $take_available_only, $sku, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementGetProductVariantDesigns: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Product identifier. | |
| **product_version_id** | **int**| Product version identifier. | [optional] |
| **product_variant_id** | **int**| Product variant identifier. | [optional] |
| **search** | **string**| Search string for design name partial match. | [optional] |
| **design_custom_fields** | **string**| Custom attributes dictionary filter for designs. For example: {\&quot;public\&quot;:\&quot;true\&quot;,\&quot;name\&quot;:\&quot;my item\&quot;} | [optional] |
| **design_path** | **string**| Path filter for designs. Subfolders included by default. | [optional] |
| **skip** | **int**| Defines page start offset from beginning of sorted result list. | [optional] |
| **take** | **int**| Defines page length (how many consequent items of sorted result list should be taken). | [optional] |
| **options** | **string**| Defines options filter e.g.: \&quot;{ \&quot;opt1_id\&quot;: \&quot;opt1_val1_id, opt1_val2_id\&quot;, \&quot;opt2_id\&quot;: \&quot;opt2_val1_id\&quot; }\&quot;. | [optional] |
| **product_filter_id** | **int**| Defines special filter based on product filter with specified identifier. | [optional] |
| **take_available_only** | **bool**| Defines special filter for available product variants. | [optional] |
| **sku** | **string**| SKU of linked ecommerce product. | [optional] |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\PagedOfProductVariantDesignDto**](../Model/PagedOfProductVariantDesignDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementGetProductVariantDocuments()`

```php
productsManagementGetProductVariantDocuments($id, $product_version_id, $product_variant_id, $search, $document_custom_fields, $document_path, $skip, $take, $options, $product_filter_id, $take_available_only, $sku, $tenant_id): \Aurigma\BackOffice\Model\PagedOfProductVariantDocumentDto
```

Returns a list of product variant documents.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Product identifier.
$product_version_id = 56; // int | Product version identifier.
$product_variant_id = 56; // int | Product variant identifier.
$search = 'search_example'; // string | Search string for document name partial match.
$document_custom_fields = 'document_custom_fields_example'; // string | Custom attributes dictionary filter for documents. For example: {\"public\":\"true\",\"name\":\"my item\"}
$document_path = 'document_path_example'; // string | Path filter for documents. Subfolders included by default.
$skip = 56; // int | Defines page start offset from beginning of sorted result list.
$take = 56; // int | Defines page length (how many consequent items of sorted result list should be taken).
$options = 'options_example'; // string | Defines options filter e.g.: \"{ \"opt1_id\": \"opt1_val1_id, opt1_val2_id\", \"opt2_id\": \"opt2_val1_id\" }\".
$product_filter_id = 56; // int | Defines special filter based on product filter with specified identifier.
$take_available_only = True; // bool | Defines special filter for available product variants.
$sku = 'sku_example'; // string | SKU of linked ecommerce product.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->productsManagementGetProductVariantDocuments($id, $product_version_id, $product_variant_id, $search, $document_custom_fields, $document_path, $skip, $take, $options, $product_filter_id, $take_available_only, $sku, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementGetProductVariantDocuments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Product identifier. | |
| **product_version_id** | **int**| Product version identifier. | [optional] |
| **product_variant_id** | **int**| Product variant identifier. | [optional] |
| **search** | **string**| Search string for document name partial match. | [optional] |
| **document_custom_fields** | **string**| Custom attributes dictionary filter for documents. For example: {\&quot;public\&quot;:\&quot;true\&quot;,\&quot;name\&quot;:\&quot;my item\&quot;} | [optional] |
| **document_path** | **string**| Path filter for documents. Subfolders included by default. | [optional] |
| **skip** | **int**| Defines page start offset from beginning of sorted result list. | [optional] |
| **take** | **int**| Defines page length (how many consequent items of sorted result list should be taken). | [optional] |
| **options** | **string**| Defines options filter e.g.: \&quot;{ \&quot;opt1_id\&quot;: \&quot;opt1_val1_id, opt1_val2_id\&quot;, \&quot;opt2_id\&quot;: \&quot;opt2_val1_id\&quot; }\&quot;. | [optional] |
| **product_filter_id** | **int**| Defines special filter based on product filter with specified identifier. | [optional] |
| **take_available_only** | **bool**| Defines special filter for available product variants. | [optional] |
| **sku** | **string**| SKU of linked ecommerce product. | [optional] |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\PagedOfProductVariantDocumentDto**](../Model/PagedOfProductVariantDocumentDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementGetProductVariantMockups()`

```php
productsManagementGetProductVariantMockups($id, $product_version_id, $product_variant_id, $search, $mockup_custom_fields, $mockup_path, $skip, $take, $options, $product_filter_id, $take_available_only, $sku, $tenant_id): \Aurigma\BackOffice\Model\PagedOfProductVariantMockupDto
```

Returns a list of product variant mockups.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Product identifier.
$product_version_id = 56; // int | Product version identifier.
$product_variant_id = 56; // int | Product variant identifier.
$search = 'search_example'; // string | Search string for design name partial match.
$mockup_custom_fields = 'mockup_custom_fields_example'; // string | Custom attributes dictionary filter for mockups. For example: {\"public\":\"true\",\"name\":\"my item\"}
$mockup_path = 'mockup_path_example'; // string | Path filter for mockups. Subfolders included by default.
$skip = 56; // int | Defines page start offset from beginning of sorted result list.
$take = 56; // int | Defines page length (how many consequent items of sorted result list should be taken).
$options = 'options_example'; // string | Defines options filter e.g.: \"{ \"opt1_id\": \"opt1_val1_id, opt1_val2_id\", \"opt2_id\": \"opt2_val1_id\" }\".
$product_filter_id = 56; // int | Defines special filter based on product filter with specified identifier.
$take_available_only = True; // bool | Defines special filter for available product variants.
$sku = 'sku_example'; // string | SKU of linked ecommerce product.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->productsManagementGetProductVariantMockups($id, $product_version_id, $product_variant_id, $search, $mockup_custom_fields, $mockup_path, $skip, $take, $options, $product_filter_id, $take_available_only, $sku, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementGetProductVariantMockups: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Product identifier. | |
| **product_version_id** | **int**| Product version identifier. | [optional] |
| **product_variant_id** | **int**| Product variant identifier. | [optional] |
| **search** | **string**| Search string for design name partial match. | [optional] |
| **mockup_custom_fields** | **string**| Custom attributes dictionary filter for mockups. For example: {\&quot;public\&quot;:\&quot;true\&quot;,\&quot;name\&quot;:\&quot;my item\&quot;} | [optional] |
| **mockup_path** | **string**| Path filter for mockups. Subfolders included by default. | [optional] |
| **skip** | **int**| Defines page start offset from beginning of sorted result list. | [optional] |
| **take** | **int**| Defines page length (how many consequent items of sorted result list should be taken). | [optional] |
| **options** | **string**| Defines options filter e.g.: \&quot;{ \&quot;opt1_id\&quot;: \&quot;opt1_val1_id, opt1_val2_id\&quot;, \&quot;opt2_id\&quot;: \&quot;opt2_val1_id\&quot; }\&quot;. | [optional] |
| **product_filter_id** | **int**| Defines special filter based on product filter with specified identifier. | [optional] |
| **take_available_only** | **bool**| Defines special filter for available product variants. | [optional] |
| **sku** | **string**| SKU of linked ecommerce product. | [optional] |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\PagedOfProductVariantMockupDto**](../Model/PagedOfProductVariantMockupDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementGetProductVariants()`

```php
productsManagementGetProductVariants($id, $product_version_id, $skip, $take, $options, $product_filter_id, $take_available_only, $sku, $tenant_id): \Aurigma\BackOffice\Model\PagedOfProductVariantDto
```

Returns a list of product variants.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Product identifier.
$product_version_id = 56; // int | Product version identifier.
$skip = 56; // int | Defines page start offset from beginning of sorted result list.
$take = 56; // int | Defines page length (how many consequent items of sorted result list should be taken).
$options = 'options_example'; // string | Defines options filter e.g.: \"{ \"opt1_id\": \"opt1_val1_id, opt1_val2_id\", \"opt2_id\": \"opt2_val1_id\" }\".
$product_filter_id = 56; // int | Defines special filter based on product filter with specified identifier.
$take_available_only = True; // bool | Defines special filter for available product variants.
$sku = 'sku_example'; // string | SKU of linked ecommerce product.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->productsManagementGetProductVariants($id, $product_version_id, $skip, $take, $options, $product_filter_id, $take_available_only, $sku, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementGetProductVariants: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Product identifier. | |
| **product_version_id** | **int**| Product version identifier. | [optional] |
| **skip** | **int**| Defines page start offset from beginning of sorted result list. | [optional] |
| **take** | **int**| Defines page length (how many consequent items of sorted result list should be taken). | [optional] |
| **options** | **string**| Defines options filter e.g.: \&quot;{ \&quot;opt1_id\&quot;: \&quot;opt1_val1_id, opt1_val2_id\&quot;, \&quot;opt2_id\&quot;: \&quot;opt2_val1_id\&quot; }\&quot;. | [optional] |
| **product_filter_id** | **int**| Defines special filter based on product filter with specified identifier. | [optional] |
| **take_available_only** | **bool**| Defines special filter for available product variants. | [optional] |
| **sku** | **string**| SKU of linked ecommerce product. | [optional] |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\PagedOfProductVariantDto**](../Model/PagedOfProductVariantDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementImportProducts()`

```php
productsManagementImportProducts($tenant_id, $file): \Aurigma\BackOffice\Model\PagedOfProductDto
```

Imports products from a specific CSV file and returns a list of imported products descriptions.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenant_id = 56; // int | Tenant identifier.
$file = "/path/to/file.txt"; // \SplFileObject | CSV file with products data.

try {
    $result = $apiInstance->productsManagementImportProducts($tenant_id, $file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementImportProducts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **file** | **\SplFileObject****\SplFileObject**| CSV file with products data. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\PagedOfProductDto**](../Model/PagedOfProductDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementRemoveDesignsConnections()`

```php
productsManagementRemoveDesignsConnections($id, $tenant_id, $remove_product_design_connections_dto)
```

Removes designs connections for a specified product.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Product identifier.
$tenant_id = 56; // int | Tenant identifier.
$remove_product_design_connections_dto = new \Aurigma\BackOffice\Model\RemoveProductDesignConnectionsDto(); // \Aurigma\BackOffice\Model\RemoveProductDesignConnectionsDto | Product designs connections creation parameters.

try {
    $apiInstance->productsManagementRemoveDesignsConnections($id, $tenant_id, $remove_product_design_connections_dto);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementRemoveDesignsConnections: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Product identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **remove_product_design_connections_dto** | [**\Aurigma\BackOffice\Model\RemoveProductDesignConnectionsDto**](../Model/RemoveProductDesignConnectionsDto.md)| Product designs connections creation parameters. | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementRemoveDocumentsConnections()`

```php
productsManagementRemoveDocumentsConnections($id, $tenant_id, $remove_product_document_connections_dto)
```

Removes documents connections for a specified product.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Product identifier.
$tenant_id = 56; // int | Tenant identifier.
$remove_product_document_connections_dto = new \Aurigma\BackOffice\Model\RemoveProductDocumentConnectionsDto(); // \Aurigma\BackOffice\Model\RemoveProductDocumentConnectionsDto | Product documents connections creation parameters.

try {
    $apiInstance->productsManagementRemoveDocumentsConnections($id, $tenant_id, $remove_product_document_connections_dto);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementRemoveDocumentsConnections: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Product identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **remove_product_document_connections_dto** | [**\Aurigma\BackOffice\Model\RemoveProductDocumentConnectionsDto**](../Model/RemoveProductDocumentConnectionsDto.md)| Product documents connections creation parameters. | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementRemoveMockupsConnections()`

```php
productsManagementRemoveMockupsConnections($id, $tenant_id, $remove_product_mockup_connections_dto)
```

Removes mockups connections for a specified product.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Product identifier.
$tenant_id = 56; // int | Tenant identifier.
$remove_product_mockup_connections_dto = new \Aurigma\BackOffice\Model\RemoveProductMockupConnectionsDto(); // \Aurigma\BackOffice\Model\RemoveProductMockupConnectionsDto | Product mockups connections creation parameters.

try {
    $apiInstance->productsManagementRemoveMockupsConnections($id, $tenant_id, $remove_product_mockup_connections_dto);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementRemoveMockupsConnections: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Product identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **remove_product_mockup_connections_dto** | [**\Aurigma\BackOffice\Model\RemoveProductMockupConnectionsDto**](../Model/RemoveProductMockupConnectionsDto.md)| Product mockups connections creation parameters. | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementSetProductVariantAvailability()`

```php
productsManagementSetProductVariantAvailability($id, $tenant_id, $set_product_variant_availability_dto)
```

Set product variants availability. Variants identifiers will be changed.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Product identifier.
$tenant_id = 56; // int | Tenant identifier.
$set_product_variant_availability_dto = new \Aurigma\BackOffice\Model\SetProductVariantAvailabilityDto(); // \Aurigma\BackOffice\Model\SetProductVariantAvailabilityDto | Set product variants availability operation parameters.

try {
    $apiInstance->productsManagementSetProductVariantAvailability($id, $tenant_id, $set_product_variant_availability_dto);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementSetProductVariantAvailability: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Product identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **set_product_variant_availability_dto** | [**\Aurigma\BackOffice\Model\SetProductVariantAvailabilityDto**](../Model/SetProductVariantAvailabilityDto.md)| Set product variants availability operation parameters. | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementSetProductVariantPrice()`

```php
productsManagementSetProductVariantPrice($id, $tenant_id, $set_product_variant_price_dto)
```

Set product variants price. Variants identifiers will be changed.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Product identifier.
$tenant_id = 56; // int | Tenant identifier.
$set_product_variant_price_dto = new \Aurigma\BackOffice\Model\SetProductVariantPriceDto(); // \Aurigma\BackOffice\Model\SetProductVariantPriceDto | Set product variants price operation parameters.

try {
    $apiInstance->productsManagementSetProductVariantPrice($id, $tenant_id, $set_product_variant_price_dto);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementSetProductVariantPrice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Product identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **set_product_variant_price_dto** | [**\Aurigma\BackOffice\Model\SetProductVariantPriceDto**](../Model/SetProductVariantPriceDto.md)| Set product variants price operation parameters. | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productsManagementSetProductVariantSku()`

```php
productsManagementSetProductVariantSku($id, $tenant_id, $set_product_variant_sku_dto)
```

Set product variants SKU. Variants identifiers will be changed.

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


$apiInstance = new Aurigma\BackOffice\Api\ProductsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Product identifier.
$tenant_id = 56; // int | Tenant identifier.
$set_product_variant_sku_dto = new \Aurigma\BackOffice\Model\SetProductVariantSkuDto(); // \Aurigma\BackOffice\Model\SetProductVariantSkuDto | Set product variants SKU operation parameters.

try {
    $apiInstance->productsManagementSetProductVariantSku($id, $tenant_id, $set_product_variant_sku_dto);
} catch (Exception $e) {
    echo 'Exception when calling ProductsManagementApi->productsManagementSetProductVariantSku: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Product identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **set_product_variant_sku_dto** | [**\Aurigma\BackOffice\Model\SetProductVariantSkuDto**](../Model/SetProductVariantSkuDto.md)| Set product variants SKU operation parameters. | [optional] |

### Return type

void (empty response body)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
