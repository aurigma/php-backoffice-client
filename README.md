# Aurigma Customer's Canvas SDK - BackOffice API Client
======================================================

This module is a PHP API client for BackOffice API service which is a part of [**Customer's Canvas**](https://customerscanvas.com) web-to-print system. It is supposed that you are familiar with its services and understand how to use its APIs. To learn more about Customer's Canvas and its services, refer the [Getting Started section of its documentation](https://customerscanvas.com/dev/getting-started/intro.html).

## Pre-requisites

To be able to use this package, you need to meet the following requirements: 

* You must have an account at Customer's Canvas.

For other platforms, see the [Backend services](https://customerscanvas.com/dev/getting-started/about-backend-services.html) article in Customer's Canvas documentation. 


## Installation

```
composer require aurigma/php-backoffice-client
```

### Requirements

PHP 7.4 and later.
Should also work with PHP 8.0.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');




$apiInstance = new Aurigma\BackOffice\Api\BuildInfoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->buildInfoGetInfo();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BuildInfoApi->buildInfoGetInfo: ', $e->getMessage(), PHP_EOL;
}

```

## Author

Aurigma Inc <info@aurigma.com> (https://customerscanvas.com)

## API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*BuildInfoApi* | [**buildInfoGetInfo**](docs/Api/BuildInfoApi.md#buildinfogetinfo) | **GET** /api/backoffice/v1/info | Returns assembly build info.
*BuildInfoApi* | [**buildInfoHeadInfo**](docs/Api/BuildInfoApi.md#buildinfoheadinfo) | **HEAD** /api/backoffice/v1/info | Returns assembly build info.
*ProductReferencesManagementApi* | [**productReferencesManagementCreate**](docs/Api/ProductReferencesManagementApi.md#productreferencesmanagementcreate) | **POST** /api/backoffice/v1/product-references | Creates a new storefront product reference.
*ProductReferencesManagementApi* | [**productReferencesManagementDelete**](docs/Api/ProductReferencesManagementApi.md#productreferencesmanagementdelete) | **DELETE** /api/backoffice/v1/product-references/{reference} | Deletes the storefront product reference.
*ProductReferencesManagementApi* | [**productReferencesManagementGet**](docs/Api/ProductReferencesManagementApi.md#productreferencesmanagementget) | **GET** /api/backoffice/v1/product-references/{reference} | Returns a storefront product reference.
*ProductReferencesManagementApi* | [**productReferencesManagementGetAll**](docs/Api/ProductReferencesManagementApi.md#productreferencesmanagementgetall) | **GET** /api/backoffice/v1/product-references | Returns all storefront product references relevant to the specified query parameters.
*ProductsManagementApi* | [**productsManagementCreateDesignsConnections**](docs/Api/ProductsManagementApi.md#productsmanagementcreatedesignsconnections) | **POST** /api/backoffice/v1/products/{id}/design-connections | Creates new designs connections for a specified product.
*ProductsManagementApi* | [**productsManagementCreateDocumentsConnections**](docs/Api/ProductsManagementApi.md#productsmanagementcreatedocumentsconnections) | **POST** /api/backoffice/v1/products/{id}/document-connections | Creates new documents connections for a specified product.
*ProductsManagementApi* | [**productsManagementCreateMockupsConnections**](docs/Api/ProductsManagementApi.md#productsmanagementcreatemockupsconnections) | **POST** /api/backoffice/v1/products/{id}/mockup-connections | Creates new mockups connections for a specified product.
*ProductsManagementApi* | [**productsManagementCreateProduct**](docs/Api/ProductsManagementApi.md#productsmanagementcreateproduct) | **POST** /api/backoffice/v1/products | Creates a new product and returns its description.
*ProductsManagementApi* | [**productsManagementDeleteProduct**](docs/Api/ProductsManagementApi.md#productsmanagementdeleteproduct) | **DELETE** /api/backoffice/v1/products/{id} | Deletes a product by its identifier.
*ProductsManagementApi* | [**productsManagementGetAllProducts**](docs/Api/ProductsManagementApi.md#productsmanagementgetallproducts) | **GET** /api/backoffice/v1/products | Returns all products, relevant to the specified query parameters.
*ProductsManagementApi* | [**productsManagementGetAvailablePersonalizationWorkflows**](docs/Api/ProductsManagementApi.md#productsmanagementgetavailablepersonalizationworkflows) | **GET** /api/backoffice/v1/products/available-workflows | Returns all available product personalization workflows.
*ProductsManagementApi* | [**productsManagementGetAvailableProcessingPipelines**](docs/Api/ProductsManagementApi.md#productsmanagementgetavailableprocessingpipelines) | **GET** /api/backoffice/v1/products/available-pipelines | Returns all available product processing pipelines.
*ProductsManagementApi* | [**productsManagementGetProduct**](docs/Api/ProductsManagementApi.md#productsmanagementgetproduct) | **GET** /api/backoffice/v1/products/{id} | Returns a product by its identifier.
*ProductsManagementApi* | [**productsManagementGetProductOptions**](docs/Api/ProductsManagementApi.md#productsmanagementgetproductoptions) | **GET** /api/backoffice/v1/products/{id}/options | Returns a list of product options.
*ProductsManagementApi* | [**productsManagementGetProductVariant**](docs/Api/ProductsManagementApi.md#productsmanagementgetproductvariant) | **GET** /api/backoffice/v1/products/{id}/variants/{productVariantId} | Returns a product variant.
*ProductsManagementApi* | [**productsManagementGetProductVariantDesigns**](docs/Api/ProductsManagementApi.md#productsmanagementgetproductvariantdesigns) | **GET** /api/backoffice/v1/products/{id}/variant-designs | Returns a list of product variant designs.
*ProductsManagementApi* | [**productsManagementGetProductVariantDocuments**](docs/Api/ProductsManagementApi.md#productsmanagementgetproductvariantdocuments) | **GET** /api/backoffice/v1/products/{id}/variant-documents | Returns a list of product variant documents.
*ProductsManagementApi* | [**productsManagementGetProductVariantMockups**](docs/Api/ProductsManagementApi.md#productsmanagementgetproductvariantmockups) | **GET** /api/backoffice/v1/products/{id}/variant-mockups | Returns a list of product variant mockups.
*ProductsManagementApi* | [**productsManagementGetProductVariants**](docs/Api/ProductsManagementApi.md#productsmanagementgetproductvariants) | **GET** /api/backoffice/v1/products/{id}/variants | Returns a list of product variants.
*ProductsManagementApi* | [**productsManagementImportProducts**](docs/Api/ProductsManagementApi.md#productsmanagementimportproducts) | **POST** /api/backoffice/v1/products/import | Imports products from a specific CSV file and returns a list of imported products descriptions.
*ProductsManagementApi* | [**productsManagementRemoveDesignsConnections**](docs/Api/ProductsManagementApi.md#productsmanagementremovedesignsconnections) | **DELETE** /api/backoffice/v1/products/{id}/design-connections | Removes designs connections for a specified product.
*ProductsManagementApi* | [**productsManagementRemoveDocumentsConnections**](docs/Api/ProductsManagementApi.md#productsmanagementremovedocumentsconnections) | **DELETE** /api/backoffice/v1/products/{id}/document-connections | Removes documents connections for a specified product.
*ProductsManagementApi* | [**productsManagementRemoveMockupsConnections**](docs/Api/ProductsManagementApi.md#productsmanagementremovemockupsconnections) | **DELETE** /api/backoffice/v1/products/{id}/mockup-connections | Removes mockups connections for a specified product.
*ProductsManagementApi* | [**productsManagementSetProductVariantAvailability**](docs/Api/ProductsManagementApi.md#productsmanagementsetproductvariantavailability) | **POST** /api/backoffice/v1/products/{id}/set-variant-availability | Set product variants availability. Variants identifiers will be changed.
*ProductsManagementApi* | [**productsManagementSetProductVariantPrice**](docs/Api/ProductsManagementApi.md#productsmanagementsetproductvariantprice) | **POST** /api/backoffice/v1/products/{id}/set-variant-price | Set product variants price. Variants identifiers will be changed.
*ProductsManagementApi* | [**productsManagementSetProductVariantSku**](docs/Api/ProductsManagementApi.md#productsmanagementsetproductvariantsku) | **POST** /api/backoffice/v1/products/{id}/set-variant-sku | Set product variants SKU. Variants identifiers will be changed.
*StorefrontsManagementApi* | [**storefrontsManagementCreateBigCommerceStorefront**](docs/Api/StorefrontsManagementApi.md#storefrontsmanagementcreatebigcommercestorefront) | **POST** /api/backoffice/v1/storefronts/bigcommerce | Creates new BigCommerce storefront.
*StorefrontsManagementApi* | [**storefrontsManagementCreateCustomStorefront**](docs/Api/StorefrontsManagementApi.md#storefrontsmanagementcreatecustomstorefront) | **POST** /api/backoffice/v1/storefronts/custom | Creates new custom storefront.
*StorefrontsManagementApi* | [**storefrontsManagementCreateMagentoStorefront**](docs/Api/StorefrontsManagementApi.md#storefrontsmanagementcreatemagentostorefront) | **POST** /api/backoffice/v1/storefronts/magento | Creates new Magento storefront.
*StorefrontsManagementApi* | [**storefrontsManagementCreateNopCommerceStorefront**](docs/Api/StorefrontsManagementApi.md#storefrontsmanagementcreatenopcommercestorefront) | **POST** /api/backoffice/v1/storefronts/nopcommerce | Creates new NopCommerce storefront.
*StorefrontsManagementApi* | [**storefrontsManagementCreateWooCommerceStorefront**](docs/Api/StorefrontsManagementApi.md#storefrontsmanagementcreatewoocommercestorefront) | **POST** /api/backoffice/v1/storefronts/woocommerce | Creates new WooCommerce storefront.
*StorefrontsManagementApi* | [**storefrontsManagementDelete**](docs/Api/StorefrontsManagementApi.md#storefrontsmanagementdelete) | **DELETE** /api/backoffice/v1/storefronts/{id} | Deletes an existing storefront by its identifier.
*StorefrontsManagementApi* | [**storefrontsManagementGet**](docs/Api/StorefrontsManagementApi.md#storefrontsmanagementget) | **GET** /api/backoffice/v1/storefronts/{id} | Returns a storefront by identifier.
*StorefrontsManagementApi* | [**storefrontsManagementGetAll**](docs/Api/StorefrontsManagementApi.md#storefrontsmanagementgetall) | **GET** /api/backoffice/v1/storefronts | Returns all storefronts, relevant to the specified query parameters.
*StorefrontsManagementApi* | [**storefrontsManagementGetBigCommerceStorefront**](docs/Api/StorefrontsManagementApi.md#storefrontsmanagementgetbigcommercestorefront) | **GET** /api/backoffice/v1/storefronts/bigcommerce/{id} | Returns extended information about BigCommerce storefront.
*StorefrontsManagementApi* | [**storefrontsManagementGetCustomStorefront**](docs/Api/StorefrontsManagementApi.md#storefrontsmanagementgetcustomstorefront) | **GET** /api/backoffice/v1/storefronts/custom/{id} | Returns extended information about custom storefront.
*StorefrontsManagementApi* | [**storefrontsManagementGetMagentoStorefront**](docs/Api/StorefrontsManagementApi.md#storefrontsmanagementgetmagentostorefront) | **GET** /api/backoffice/v1/storefronts/magento/{id} | Returns extended information about Magento storefront.
*StorefrontsManagementApi* | [**storefrontsManagementGetNopCommerceStorefront**](docs/Api/StorefrontsManagementApi.md#storefrontsmanagementgetnopcommercestorefront) | **GET** /api/backoffice/v1/storefronts/nopcommerce/{id} | Returns extended information about NopCommerce storefront.
*StorefrontsManagementApi* | [**storefrontsManagementGetWooCommerceStorefront**](docs/Api/StorefrontsManagementApi.md#storefrontsmanagementgetwoocommercestorefront) | **GET** /api/backoffice/v1/storefronts/woocommerce/{id} | Returns extended information about WooCommerce storefront.
*UsersManagementApi* | [**usersManagementCreate**](docs/Api/UsersManagementApi.md#usersmanagementcreate) | **POST** /api/backoffice/v1/users | Creates a new tenant user.
*UsersManagementApi* | [**usersManagementDelete**](docs/Api/UsersManagementApi.md#usersmanagementdelete) | **DELETE** /api/backoffice/v1/users/{id} | Deletes an existing tenant user.
*UsersManagementApi* | [**usersManagementGet**](docs/Api/UsersManagementApi.md#usersmanagementget) | **GET** /api/backoffice/v1/users/{id} | Returns a tenant user by user identifier.
*UsersManagementApi* | [**usersManagementGetAll**](docs/Api/UsersManagementApi.md#usersmanagementgetall) | **GET** /api/backoffice/v1/users | Returns a tenant users list.
*UsersManagementApi* | [**usersManagementGetAllRoles**](docs/Api/UsersManagementApi.md#usersmanagementgetallroles) | **GET** /api/backoffice/v1/users/roles | Returns all tenant user roles, relevant to the specified query parameters.

## Models

- [AppearanceDataDto](docs/Model/AppearanceDataDto.md)
- [AppearanceDataItemDto](docs/Model/AppearanceDataItemDto.md)
- [AppearanceDataType](docs/Model/AppearanceDataType.md)
- [BigCommerceSettingsDto](docs/Model/BigCommerceSettingsDto.md)
- [BigCommerceStorefrontDto](docs/Model/BigCommerceStorefrontDto.md)
- [BuildInfoModel](docs/Model/BuildInfoModel.md)
- [ConflictType](docs/Model/ConflictType.md)
- [CreateBigCommerceStorefrontDto](docs/Model/CreateBigCommerceStorefrontDto.md)
- [CreateCustomStorefrontDto](docs/Model/CreateCustomStorefrontDto.md)
- [CreateMagentoStorefrontDto](docs/Model/CreateMagentoStorefrontDto.md)
- [CreateNopCommerceStorefrontDto](docs/Model/CreateNopCommerceStorefrontDto.md)
- [CreateProductDesignConnectionsDto](docs/Model/CreateProductDesignConnectionsDto.md)
- [CreateProductDocumentConnectionsDto](docs/Model/CreateProductDocumentConnectionsDto.md)
- [CreateProductDto](docs/Model/CreateProductDto.md)
- [CreateProductMockupConnectionsDto](docs/Model/CreateProductMockupConnectionsDto.md)
- [CreateProductOptionDto](docs/Model/CreateProductOptionDto.md)
- [CreateProductOptionValueDto](docs/Model/CreateProductOptionValueDto.md)
- [CreateProductReferenceDto](docs/Model/CreateProductReferenceDto.md)
- [CreateTenantUserDto](docs/Model/CreateTenantUserDto.md)
- [CreateWooCommerceStorefrontDto](docs/Model/CreateWooCommerceStorefrontDto.md)
- [CustomStorefrontDto](docs/Model/CustomStorefrontDto.md)
- [GeneralConflictDto](docs/Model/GeneralConflictDto.md)
- [ImageInfo](docs/Model/ImageInfo.md)
- [MagentoSettingsDto](docs/Model/MagentoSettingsDto.md)
- [MagentoStorefrontDto](docs/Model/MagentoStorefrontDto.md)
- [MicrosoftAspNetCoreMvcProblemDetails](docs/Model/MicrosoftAspNetCoreMvcProblemDetails.md)
- [NopCommerceSettingsDto](docs/Model/NopCommerceSettingsDto.md)
- [NopCommerceStorefrontDto](docs/Model/NopCommerceStorefrontDto.md)
- [OptionType](docs/Model/OptionType.md)
- [PagedOfPersonalizationWorkflowDto](docs/Model/PagedOfPersonalizationWorkflowDto.md)
- [PagedOfProcessingPipelineDto](docs/Model/PagedOfProcessingPipelineDto.md)
- [PagedOfProductDto](docs/Model/PagedOfProductDto.md)
- [PagedOfProductOptionDto](docs/Model/PagedOfProductOptionDto.md)
- [PagedOfProductReferenceDto](docs/Model/PagedOfProductReferenceDto.md)
- [PagedOfProductVariantDesignDto](docs/Model/PagedOfProductVariantDesignDto.md)
- [PagedOfProductVariantDocumentDto](docs/Model/PagedOfProductVariantDocumentDto.md)
- [PagedOfProductVariantDto](docs/Model/PagedOfProductVariantDto.md)
- [PagedOfProductVariantMockupDto](docs/Model/PagedOfProductVariantMockupDto.md)
- [PagedOfStorefrontDto](docs/Model/PagedOfStorefrontDto.md)
- [PagedOfTenantUserDto](docs/Model/PagedOfTenantUserDto.md)
- [PagedOfTenantUserRoleDto](docs/Model/PagedOfTenantUserRoleDto.md)
- [PersonalizationWorkflowDto](docs/Model/PersonalizationWorkflowDto.md)
- [ProcessingPipelineDto](docs/Model/ProcessingPipelineDto.md)
- [ProductAssetConnectionOptionsDto](docs/Model/ProductAssetConnectionOptionsDto.md)
- [ProductDesignConnectionDto](docs/Model/ProductDesignConnectionDto.md)
- [ProductDocumentConnectionDto](docs/Model/ProductDocumentConnectionDto.md)
- [ProductDto](docs/Model/ProductDto.md)
- [ProductMockupConnectionDto](docs/Model/ProductMockupConnectionDto.md)
- [ProductMockupType](docs/Model/ProductMockupType.md)
- [ProductOptionDto](docs/Model/ProductOptionDto.md)
- [ProductOptionValueDto](docs/Model/ProductOptionValueDto.md)
- [ProductReferenceCreationConflictDto](docs/Model/ProductReferenceCreationConflictDto.md)
- [ProductReferenceDto](docs/Model/ProductReferenceDto.md)
- [ProductReferenceInfo](docs/Model/ProductReferenceInfo.md)
- [ProductReferenceType](docs/Model/ProductReferenceType.md)
- [ProductVariantAvailabilityDto](docs/Model/ProductVariantAvailabilityDto.md)
- [ProductVariantDesignDto](docs/Model/ProductVariantDesignDto.md)
- [ProductVariantDocumentDto](docs/Model/ProductVariantDocumentDto.md)
- [ProductVariantDto](docs/Model/ProductVariantDto.md)
- [ProductVariantMockupDto](docs/Model/ProductVariantMockupDto.md)
- [ProductVariantMockupType](docs/Model/ProductVariantMockupType.md)
- [ProductVariantOptionDto](docs/Model/ProductVariantOptionDto.md)
- [ProductVariantPriceDto](docs/Model/ProductVariantPriceDto.md)
- [ProductVariantResourceDto](docs/Model/ProductVariantResourceDto.md)
- [ProductVariantResourcePreview](docs/Model/ProductVariantResourcePreview.md)
- [ProductVariantResourceType](docs/Model/ProductVariantResourceType.md)
- [ProductVariantSkuDto](docs/Model/ProductVariantSkuDto.md)
- [RemoveProductAssetConnectionDto](docs/Model/RemoveProductAssetConnectionDto.md)
- [RemoveProductDesignConnectionsDto](docs/Model/RemoveProductDesignConnectionsDto.md)
- [RemoveProductDocumentConnectionsDto](docs/Model/RemoveProductDocumentConnectionsDto.md)
- [RemoveProductMockupConnectionsDto](docs/Model/RemoveProductMockupConnectionsDto.md)
- [SetProductVariantAvailabilityDto](docs/Model/SetProductVariantAvailabilityDto.md)
- [SetProductVariantPriceDto](docs/Model/SetProductVariantPriceDto.md)
- [SetProductVariantSkuDto](docs/Model/SetProductVariantSkuDto.md)
- [SimpleOptionValue](docs/Model/SimpleOptionValue.md)
- [StorefrontDto](docs/Model/StorefrontDto.md)
- [StorefrontType](docs/Model/StorefrontType.md)
- [SurfaceUsageType](docs/Model/SurfaceUsageType.md)
- [TenantUserDto](docs/Model/TenantUserDto.md)
- [TenantUserRoleDto](docs/Model/TenantUserRoleDto.md)
- [WooCommerceSettingsDto](docs/Model/WooCommerceSettingsDto.md)
- [WooCommerceStorefrontDto](docs/Model/WooCommerceStorefrontDto.md)
- [WorkflowType](docs/Model/WorkflowType.md)

## Authorization

Authentication schemes defined for the API:
### ApiKey

- **Type**: API key
- **API key parameter name**: X-API-Key
- **Location**: HTTP header


### Bearer

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header


### OAuth2ClientCredentials

- **Type**: `OAuth`
- **Flow**: `application`
- **Authorization URL**: ``
- **Scopes**: N/A

### OAuth2Implicit

- **Type**: `OAuth`
- **Flow**: `implicit`
- **Authorization URL**: `https://localhost:44378/connect/authorize`
- **Scopes**: 
    - **Projects_full**: Manipulate projects
    - **Projects_read**: Read projects
    - **Templates_full**: Manipulate products
    - **Templates_read**: Read products
    - **Storefronts_full**: Manipulate products
    - **Storefronts_read**: Read products
    - **StorefrontUsers_full**: Manipulate storefront users
    - **StorefrontUsers_read**: Read storefront users
    - **TenantUsers_full**: Manipulate storefront users
    - **TenantUsers_read**: Read storefront users

### oauth2-code

- **Type**: `OAuth`
- **Flow**: `accessCode`
- **Authorization URL**: `https://localhost:44378/connect/authorize`
- **Scopes**: 
    - **Projects_full**: Manipulate projects
    - **Projects_read**: Read projects
    - **Templates_full**: Manipulate products
    - **Templates_read**: Read products
    - **Storefronts_full**: Manipulate products
    - **Storefronts_read**: Read products
    - **StorefrontUsers_full**: Manipulate storefront users
    - **StorefrontUsers_read**: Read storefront users
    - **TenantUsers_full**: Manipulate storefront users
    - **TenantUsers_read**: Read storefront users
