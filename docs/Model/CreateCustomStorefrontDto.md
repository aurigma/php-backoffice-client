# # CreateCustomStorefrontDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Storefront name. |
**processing_pipelines_trigger_project_status** | **int** | Status of project that should become a trigger to start project items processing automatically. | [optional]
**post_processing_pipeline_id** | **int** | Identifier of pipeline that should be used for post-processing for projects when all project items are processed. | [optional]
**api_key_header_name** | **string** | Name of header that will be used to provide API key to target storefront system. | [optional]
**api_key** | **string** | API key for target storefront system. | [optional]
**shop_urls** | **string[]** | List of storefront shops URLs. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
