# # ProjectSettings

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique ID of the project | [optional]
**slug** | **string** | Slugs are meant to be a way to verify people just with the link | [optional]
**environment** | **string** |  | [optional]
**organization** | **string** | Name of the organization that owns this project | [optional]
**customizations** | [**\Passbase\models\ProjectSettingsCustomizations**](ProjectSettingsCustomizations.md) |  | [optional]
**verification_steps** | [**\Passbase\models\ProjectSettingsVerificationSteps[]**](ProjectSettingsVerificationSteps.md) | List of the steps through which the user must go through to complete their verification | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
