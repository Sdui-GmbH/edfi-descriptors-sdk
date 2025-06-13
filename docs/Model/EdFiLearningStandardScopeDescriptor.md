# # EdFiLearningStandardScopeDescriptor

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional]
**code_value** | **string** | A code or abbreviation that is used to refer to the descriptor. |
**namespace** | **string** | A globally unique namespace that identifies this descriptor set. Author is strongly encouraged to use the Universal Resource Identifier (http, ftp, file, etc.) for the source of the descriptor definition. Best practice is for this source to be the descriptor file itself, so that it can be machine-readable and be fetched in real-time, if necessary. |
**description** | **string** | The description of the descriptor. | [optional]
**effective_begin_date** | **\DateTime** | The beginning date of the period when the descriptor is in effect. If omitted, the default is immediate effectiveness. | [optional]
**effective_end_date** | **\DateTime** | The end date of the period when the descriptor is in effect. | [optional]
**short_description** | **string** | A shortened description for the descriptor. |
**_etag** | **string** | A unique system-generated value that identifies the version of the resource. | [optional]
**_last_modified_date** | **\DateTime** | The date and time the resource was last modified. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
