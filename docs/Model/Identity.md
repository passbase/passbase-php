# # Identity

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique ID of the identity | [optional]
**status** | **string** | Current state of the identity in Passbase&#39;s systems | [optional]
**owner** | [**\Passbase\models\IdentityOwner**](.md) |  | [optional]
**score** | **double** | Float between 0 and 1 representing our confidence that this identity is valid. 0 meaning we couldn&#39;t verify any of the information provided with accuracy, and 1 absolute confidence. | [optional]
**created** | **int** | Unix-timestamp of when the identity was created | [optional]
**updated** | **int** | Unix-timestamp of when the identity was updated | [optional]
**resources** | [**\Passbase\models\IdentityResource[]**](IdentityResource.md) | resources attached to a verification | [optional]
**metadata** | **object** | Customer defined arbitrary payload initially passed through the client-sdk | [optional]
**watchlist** | [**\Passbase\models\WatchlistResponse**](.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
