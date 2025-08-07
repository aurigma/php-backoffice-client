# Aurigma\BackOffice\StorefrontsManagementApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**storefrontsManagementCreateBigCommerceStorefront()**](StorefrontsManagementApi.md#storefrontsManagementCreateBigCommerceStorefront) | **POST** /api/backoffice/v1/storefronts/bigcommerce | Creates new BigCommerce storefront. |
| [**storefrontsManagementCreateCustomStorefront()**](StorefrontsManagementApi.md#storefrontsManagementCreateCustomStorefront) | **POST** /api/backoffice/v1/storefronts/custom | Creates new custom storefront. |
| [**storefrontsManagementCreateMagentoStorefront()**](StorefrontsManagementApi.md#storefrontsManagementCreateMagentoStorefront) | **POST** /api/backoffice/v1/storefronts/magento | Creates new Magento storefront. |
| [**storefrontsManagementCreateNopCommerceStorefront()**](StorefrontsManagementApi.md#storefrontsManagementCreateNopCommerceStorefront) | **POST** /api/backoffice/v1/storefronts/nopcommerce | Creates new NopCommerce storefront. |
| [**storefrontsManagementCreateWooCommerceStorefront()**](StorefrontsManagementApi.md#storefrontsManagementCreateWooCommerceStorefront) | **POST** /api/backoffice/v1/storefronts/woocommerce | Creates new WooCommerce storefront. |
| [**storefrontsManagementDelete()**](StorefrontsManagementApi.md#storefrontsManagementDelete) | **DELETE** /api/backoffice/v1/storefronts/{id} | Deletes an existing storefront by its identifier. |
| [**storefrontsManagementGet()**](StorefrontsManagementApi.md#storefrontsManagementGet) | **GET** /api/backoffice/v1/storefronts/{id} | Returns a storefront by identifier. |
| [**storefrontsManagementGetAll()**](StorefrontsManagementApi.md#storefrontsManagementGetAll) | **GET** /api/backoffice/v1/storefronts | Returns all storefronts, relevant to the specified query parameters. |
| [**storefrontsManagementGetBigCommerceStorefront()**](StorefrontsManagementApi.md#storefrontsManagementGetBigCommerceStorefront) | **GET** /api/backoffice/v1/storefronts/bigcommerce/{id} | Returns extended information about BigCommerce storefront. |
| [**storefrontsManagementGetCustomStorefront()**](StorefrontsManagementApi.md#storefrontsManagementGetCustomStorefront) | **GET** /api/backoffice/v1/storefronts/custom/{id} | Returns extended information about custom storefront. |
| [**storefrontsManagementGetMagentoStorefront()**](StorefrontsManagementApi.md#storefrontsManagementGetMagentoStorefront) | **GET** /api/backoffice/v1/storefronts/magento/{id} | Returns extended information about Magento storefront. |
| [**storefrontsManagementGetNopCommerceStorefront()**](StorefrontsManagementApi.md#storefrontsManagementGetNopCommerceStorefront) | **GET** /api/backoffice/v1/storefronts/nopcommerce/{id} | Returns extended information about NopCommerce storefront. |
| [**storefrontsManagementGetWooCommerceStorefront()**](StorefrontsManagementApi.md#storefrontsManagementGetWooCommerceStorefront) | **GET** /api/backoffice/v1/storefronts/woocommerce/{id} | Returns extended information about WooCommerce storefront. |


## `storefrontsManagementCreateBigCommerceStorefront()`

```php
storefrontsManagementCreateBigCommerceStorefront($tenant_id, $create_big_commerce_storefront_dto): \Aurigma\BackOffice\Model\BigCommerceStorefrontDto
```

Creates new BigCommerce storefront.

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


$apiInstance = new Aurigma\BackOffice\Api\StorefrontsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenant_id = 56; // int | Tenant identifier.
$create_big_commerce_storefront_dto = new \Aurigma\BackOffice\Model\CreateBigCommerceStorefrontDto(); // \Aurigma\BackOffice\Model\CreateBigCommerceStorefrontDto | BigCommerce storefront creation model.

try {
    $result = $apiInstance->storefrontsManagementCreateBigCommerceStorefront($tenant_id, $create_big_commerce_storefront_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontsManagementApi->storefrontsManagementCreateBigCommerceStorefront: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **create_big_commerce_storefront_dto** | [**\Aurigma\BackOffice\Model\CreateBigCommerceStorefrontDto**](../Model/CreateBigCommerceStorefrontDto.md)| BigCommerce storefront creation model. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\BigCommerceStorefrontDto**](../Model/BigCommerceStorefrontDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storefrontsManagementCreateCustomStorefront()`

```php
storefrontsManagementCreateCustomStorefront($tenant_id, $create_custom_storefront_dto): \Aurigma\BackOffice\Model\CustomStorefrontDto
```

Creates new custom storefront.

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


$apiInstance = new Aurigma\BackOffice\Api\StorefrontsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenant_id = 56; // int | Tenant identifier.
$create_custom_storefront_dto = new \Aurigma\BackOffice\Model\CreateCustomStorefrontDto(); // \Aurigma\BackOffice\Model\CreateCustomStorefrontDto | Custom storefront creation model.

try {
    $result = $apiInstance->storefrontsManagementCreateCustomStorefront($tenant_id, $create_custom_storefront_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontsManagementApi->storefrontsManagementCreateCustomStorefront: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **create_custom_storefront_dto** | [**\Aurigma\BackOffice\Model\CreateCustomStorefrontDto**](../Model/CreateCustomStorefrontDto.md)| Custom storefront creation model. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\CustomStorefrontDto**](../Model/CustomStorefrontDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storefrontsManagementCreateMagentoStorefront()`

```php
storefrontsManagementCreateMagentoStorefront($tenant_id, $create_magento_storefront_dto): \Aurigma\BackOffice\Model\MagentoStorefrontDto
```

Creates new Magento storefront.

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


$apiInstance = new Aurigma\BackOffice\Api\StorefrontsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenant_id = 56; // int | Tenant identifier.
$create_magento_storefront_dto = new \Aurigma\BackOffice\Model\CreateMagentoStorefrontDto(); // \Aurigma\BackOffice\Model\CreateMagentoStorefrontDto | Magento storefront creation model.

try {
    $result = $apiInstance->storefrontsManagementCreateMagentoStorefront($tenant_id, $create_magento_storefront_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontsManagementApi->storefrontsManagementCreateMagentoStorefront: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **create_magento_storefront_dto** | [**\Aurigma\BackOffice\Model\CreateMagentoStorefrontDto**](../Model/CreateMagentoStorefrontDto.md)| Magento storefront creation model. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\MagentoStorefrontDto**](../Model/MagentoStorefrontDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storefrontsManagementCreateNopCommerceStorefront()`

```php
storefrontsManagementCreateNopCommerceStorefront($tenant_id, $create_nop_commerce_storefront_dto): \Aurigma\BackOffice\Model\NopCommerceStorefrontDto
```

Creates new NopCommerce storefront.

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


$apiInstance = new Aurigma\BackOffice\Api\StorefrontsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenant_id = 56; // int | Tenant identifier.
$create_nop_commerce_storefront_dto = new \Aurigma\BackOffice\Model\CreateNopCommerceStorefrontDto(); // \Aurigma\BackOffice\Model\CreateNopCommerceStorefrontDto | NopCommerce storefront creation model.

try {
    $result = $apiInstance->storefrontsManagementCreateNopCommerceStorefront($tenant_id, $create_nop_commerce_storefront_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontsManagementApi->storefrontsManagementCreateNopCommerceStorefront: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **create_nop_commerce_storefront_dto** | [**\Aurigma\BackOffice\Model\CreateNopCommerceStorefrontDto**](../Model/CreateNopCommerceStorefrontDto.md)| NopCommerce storefront creation model. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\NopCommerceStorefrontDto**](../Model/NopCommerceStorefrontDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storefrontsManagementCreateWooCommerceStorefront()`

```php
storefrontsManagementCreateWooCommerceStorefront($tenant_id, $create_woo_commerce_storefront_dto): \Aurigma\BackOffice\Model\WooCommerceStorefrontDto
```

Creates new WooCommerce storefront.

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


$apiInstance = new Aurigma\BackOffice\Api\StorefrontsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenant_id = 56; // int | Tenant identifier.
$create_woo_commerce_storefront_dto = new \Aurigma\BackOffice\Model\CreateWooCommerceStorefrontDto(); // \Aurigma\BackOffice\Model\CreateWooCommerceStorefrontDto | WooCommerce storefront creation model.

try {
    $result = $apiInstance->storefrontsManagementCreateWooCommerceStorefront($tenant_id, $create_woo_commerce_storefront_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontsManagementApi->storefrontsManagementCreateWooCommerceStorefront: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenant_id** | **int**| Tenant identifier. | [optional] |
| **create_woo_commerce_storefront_dto** | [**\Aurigma\BackOffice\Model\CreateWooCommerceStorefrontDto**](../Model/CreateWooCommerceStorefrontDto.md)| WooCommerce storefront creation model. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\WooCommerceStorefrontDto**](../Model/WooCommerceStorefrontDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storefrontsManagementDelete()`

```php
storefrontsManagementDelete($id, $tenant_id): \Aurigma\BackOffice\Model\StorefrontDto
```

Deletes an existing storefront by its identifier.

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


$apiInstance = new Aurigma\BackOffice\Api\StorefrontsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Storefront identifier.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->storefrontsManagementDelete($id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontsManagementApi->storefrontsManagementDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Storefront identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\StorefrontDto**](../Model/StorefrontDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storefrontsManagementGet()`

```php
storefrontsManagementGet($id, $tenant_id): \Aurigma\BackOffice\Model\StorefrontDto
```

Returns a storefront by identifier.

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


$apiInstance = new Aurigma\BackOffice\Api\StorefrontsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Storefront identifier.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->storefrontsManagementGet($id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontsManagementApi->storefrontsManagementGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Storefront identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\StorefrontDto**](../Model/StorefrontDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storefrontsManagementGetAll()`

```php
storefrontsManagementGetAll($types, $skip, $take, $sorting, $search, $tenant_id): \Aurigma\BackOffice\Model\PagedOfStorefrontDto
```

Returns all storefronts, relevant to the specified query parameters.

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


$apiInstance = new Aurigma\BackOffice\Api\StorefrontsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$types = array(new \Aurigma\BackOffice\Model\\Aurigma\BackOffice\Model\StorefrontType()); // \Aurigma\BackOffice\Model\StorefrontType[] | Storefront type filter.
$skip = 56; // int | Defines page start offset from beginning of sorted result list.
$take = 56; // int | Defines page length (how many consequent items of sorted result list should be taken).
$sorting = 'sorting_example'; // string | Defines sorting order of result list e.g.: \"Title ASC, LastModified DESC\".
$search = 'search_example'; // string | Search string for partial match.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->storefrontsManagementGetAll($types, $skip, $take, $sorting, $search, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontsManagementApi->storefrontsManagementGetAll: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **types** | [**\Aurigma\BackOffice\Model\StorefrontType[]**](../Model/\Aurigma\BackOffice\Model\StorefrontType.md)| Storefront type filter. | [optional] |
| **skip** | **int**| Defines page start offset from beginning of sorted result list. | [optional] |
| **take** | **int**| Defines page length (how many consequent items of sorted result list should be taken). | [optional] |
| **sorting** | **string**| Defines sorting order of result list e.g.: \&quot;Title ASC, LastModified DESC\&quot;. | [optional] |
| **search** | **string**| Search string for partial match. | [optional] |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\PagedOfStorefrontDto**](../Model/PagedOfStorefrontDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storefrontsManagementGetBigCommerceStorefront()`

```php
storefrontsManagementGetBigCommerceStorefront($id, $tenant_id): \Aurigma\BackOffice\Model\MagentoStorefrontDto
```

Returns extended information about BigCommerce storefront.

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


$apiInstance = new Aurigma\BackOffice\Api\StorefrontsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Storefront identifier.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->storefrontsManagementGetBigCommerceStorefront($id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontsManagementApi->storefrontsManagementGetBigCommerceStorefront: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Storefront identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\MagentoStorefrontDto**](../Model/MagentoStorefrontDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storefrontsManagementGetCustomStorefront()`

```php
storefrontsManagementGetCustomStorefront($id, $tenant_id): \Aurigma\BackOffice\Model\CustomStorefrontDto
```

Returns extended information about custom storefront.

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


$apiInstance = new Aurigma\BackOffice\Api\StorefrontsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Storefront identifier.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->storefrontsManagementGetCustomStorefront($id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontsManagementApi->storefrontsManagementGetCustomStorefront: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Storefront identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\CustomStorefrontDto**](../Model/CustomStorefrontDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storefrontsManagementGetMagentoStorefront()`

```php
storefrontsManagementGetMagentoStorefront($id, $tenant_id): \Aurigma\BackOffice\Model\MagentoStorefrontDto
```

Returns extended information about Magento storefront.

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


$apiInstance = new Aurigma\BackOffice\Api\StorefrontsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Storefront identifier.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->storefrontsManagementGetMagentoStorefront($id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontsManagementApi->storefrontsManagementGetMagentoStorefront: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Storefront identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\MagentoStorefrontDto**](../Model/MagentoStorefrontDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storefrontsManagementGetNopCommerceStorefront()`

```php
storefrontsManagementGetNopCommerceStorefront($id, $tenant_id): \Aurigma\BackOffice\Model\NopCommerceStorefrontDto
```

Returns extended information about NopCommerce storefront.

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


$apiInstance = new Aurigma\BackOffice\Api\StorefrontsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Storefront identifier.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->storefrontsManagementGetNopCommerceStorefront($id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontsManagementApi->storefrontsManagementGetNopCommerceStorefront: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Storefront identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\NopCommerceStorefrontDto**](../Model/NopCommerceStorefrontDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `storefrontsManagementGetWooCommerceStorefront()`

```php
storefrontsManagementGetWooCommerceStorefront($id, $tenant_id): \Aurigma\BackOffice\Model\WooCommerceStorefrontDto
```

Returns extended information about WooCommerce storefront.

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


$apiInstance = new Aurigma\BackOffice\Api\StorefrontsManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Storefront identifier.
$tenant_id = 56; // int | Tenant identifier.

try {
    $result = $apiInstance->storefrontsManagementGetWooCommerceStorefront($id, $tenant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorefrontsManagementApi->storefrontsManagementGetWooCommerceStorefront: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Storefront identifier. | |
| **tenant_id** | **int**| Tenant identifier. | [optional] |

### Return type

[**\Aurigma\BackOffice\Model\WooCommerceStorefrontDto**](../Model/WooCommerceStorefrontDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey), [OAuth2ClientCredentials](../../README.md#OAuth2ClientCredentials), [OAuth2Implicit](../../README.md#OAuth2Implicit), [Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
