![banner](https://passbase-sdk-banner.netlify.app/php.png)

# Passbase PHP SDK

<span class=\"subtext\">
Welcome to the Passbase Verifications API docs. This documentation will
help you understand our models and the Verification API with its endpoints.
Based on this you can build your own system (i.e. verification) and hook it
up to Passbase.

In case of feedback or questions you can reach us under this email address: [developer@passbase.com](mailto:developer@passbase.com).
</span>

A User submits a video selfie and valid identifying __Resources__ during a
__Verification__ guided by the Passbase client-side integration. Once all
the necessary __Resources__ are submitted, __Data points__ are extracted,
digitized, and authenticated. These Data points then becomes part of the
User's __Identity__. The User then consents to share __Resources__ and/or
__Data points__ from their Identity with you. This information is passed
to you and can be used to make decisions about a User (e.g. activate account).
This table below explains our terminology further.

| Term                                    | Description |
|-----------------------------------------|-------------|
| [Identity](#tag/identity_model)         | A set of Data points and Resources related to and owned by one single User. This data can be accessed by you through a Verification. |
| Data points                             | Any data about a User extracted from a Resource (E.g. Passport Number, or Age). |
| [Resource](#tag/resource_model)         | A source document used to generate the Data points for a User (E.g. Passport). |
| [User](#tag/user_model)                 | The owner of an email address associated with an Identity. |
| Verification                            | A transaction through which a User consents to share Data points with you. If the Data points you request are not already available in the User's Identity, the Passbase client will ask the User to submit the necessary Resource required to extract them. |
| Re-authentication (login)               | A transaction through which a User can certify the ownership of Personal data previously shared through an Authentication. |


# Authentication

<span class=\"subtext\">
There are two forms of authentication for the API:
<br/>&bull; API Key
<br/>&bull; Bearer JWT Token

</span>



## Installation & Usage

### Requirements

PHP 7.2 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/passbase/passbase-php.git"
    }
  ],
  "require": {
    "passbase/passbase-php": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/passbase/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure API key authorization: SecretApiKey
$config = Passbase\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Passbase\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');


$apiInstance = new Passbase\Api\IdentityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Unique ID of the identity to return

try {
    $result = $apiInstance->getIdentityById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IdentityApi->getIdentityById: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://api.passbase.com/verification/v2*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*IdentityApi* | [**getIdentityById**](docs/Api/IdentityApi.md#getidentitybyid) | **GET** /identities/{id} | Get identity
*IdentityApi* | [**getIdentityResourceById**](docs/Api/IdentityApi.md#getidentityresourcebyid) | **GET** /identity/{id}/resources/{resource_id} | Get resource
*IdentityApi* | [**getIdentityResourceFileById**](docs/Api/IdentityApi.md#getidentityresourcefilebyid) | **GET** /identity/{id}/resources/{resource_id}/resource_files/{resource_file_id} | Get resource file
*IdentityApi* | [**listIdentities**](docs/Api/IdentityApi.md#listidentities) | **GET** /identities | List identities
*IdentityApi* | [**listIdentityResources**](docs/Api/IdentityApi.md#listidentityresources) | **GET** /identity/{id}/resources | List resources
*ProjectApi* | [**getSettings**](docs/Api/ProjectApi.md#getsettings) | **GET** /settings | Get project settings

## Models

- [Cursor](docs/Model/Cursor.md)
- [Identity](docs/Model/Identity.md)
- [IdentityOwner](docs/Model/IdentityOwner.md)
- [IdentityResource](docs/Model/IdentityResource.md)
- [PaginatedIdentities](docs/Model/PaginatedIdentities.md)
- [PaginatedResources](docs/Model/PaginatedResources.md)
- [ProjectSettings](docs/Model/ProjectSettings.md)
- [ProjectSettingsCustomizations](docs/Model/ProjectSettingsCustomizations.md)
- [ProjectSettingsVerificationSteps](docs/Model/ProjectSettingsVerificationSteps.md)
- [Resource](docs/Model/Resource.md)
- [ResourceFile](docs/Model/ResourceFile.md)
- [ResourceInput](docs/Model/ResourceInput.md)
- [User](docs/Model/User.md)
- [WatchlistResponse](docs/Model/WatchlistResponse.md)

## Authorization

### IdentityAccessToken

- **Type**: Bearer authentication (JWT)


### PublishableApiKey

- **Type**: API key
- **API key parameter name**: X-API-KEY
- **Location**: HTTP header



### SecretApiKey

- **Type**: API key
- **API key parameter name**: X-API-KEY
- **Location**: HTTP header


## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.0.0`
    - Package version: `1.2.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
