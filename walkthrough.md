1. You can install the bindings via [Composer](http://getcomposer.org/). Run the following command:

```json
composer require passbase/passbase-php
```

2. You can now use the Passbase SDK by requiring the `autoload.php` file

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure the SDK with your API Secret access key
$config = Passbase\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', '{{YOUR_SECRET_API_KEY}}');

$apiInstance = new Passbase\api\ProjectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getSettings();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProjectApi->getSettings: ', $e->getMessage(), PHP_EOL;
}
?>
```
