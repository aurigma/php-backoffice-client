# # ProductMockupConnectionDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mockup_id** | **string** | Mockup identifier. | [optional]
**options** | [**\Aurigma\BackOffice\Model\ProductAssetConnectionOptionsDto[]**](ProductAssetConnectionOptionsDto.md) | Connection options. Set empty if mockup should be available for all product variants. | [optional]
**mockup_types** | [**\Aurigma\BackOffice\Model\ProductMockupType[]**](ProductMockupType.md) | Product mockup types. Single mockup may be used as editor, preview and thumbnail mockup at the same time. | [optional]
**surfaces** | **string** | Product mockup target surfaces. Comma-separated surface indexes (\&quot;1,2,3\&quot;) or &#x60;all&#x60; value may be set. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
