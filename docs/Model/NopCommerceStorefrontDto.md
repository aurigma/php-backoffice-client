# # NopCommerceStorefrontDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**settings** | [**\Aurigma\BackOffice\Model\NopCommerceSettingsDto**](NopCommerceSettingsDto.md) |  | [optional]
**id** | **int** | Storefront identifier. | [optional]
**tenant_id** | **int** | Tenant identifier. | [optional]
**name** | **string** | Storefront name. | [optional]
**processing_pipelines_trigger_project_status** | **int** | Status of project that should become a trigger to start project items processing automatically. | [optional]
**post_processing_pipeline_id** | **int** | Identifier of pipeline that should be used for post-processing for projects when all project items are processed. | [optional]
**type** | [**\Aurigma\BackOffice\Model\StorefrontType**](StorefrontType.md) |  | [optional]
**created** | **\DateTime** | Storefront entity creation date and time. | [optional]
**shop_urls** | **string[]** | Connected shops URLs. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
