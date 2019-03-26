# Swagger\Client\CurrencyExchangeRateApi

All URIs are relative to *https://my.sevdesk.de/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getCurrencyExchangeRates**](CurrencyExchangeRateApi.md#getCurrencyExchangeRates) | **GET** /CurrencyExchangeRate | Get an overview of all currency exchange rates


# **getCurrencyExchangeRates**
> \Swagger\Client\Model\ModelCurrencyExchangeRate getCurrencyExchangeRates($limit, $offset)

Get an overview of all currency exchange rates

Calls CurrencyExchangeRate.php to get necessary variables

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('token', 'Bearer');

$apiInstance = new Swagger\Client\Api\CurrencyExchangeRateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 1000; // int | Limits the number of entries returned. Default is 1000.    Be aware that there are over 100000 entries in the database for currency exchange rate, so using a limit higher than 1000 with offset=0 is not recommended!    However you can set the offset appropriately so you minimize the amount of returned exchange rates and keep loading time to a low.
$offset = 0; // int | Set the index where the returned currency exchange rates start. Default is 0

try {
    $result = $apiInstance->getCurrencyExchangeRates($limit, $offset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CurrencyExchangeRateApi->getCurrencyExchangeRates: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| Limits the number of entries returned. Default is 1000.    Be aware that there are over 100000 entries in the database for currency exchange rate, so using a limit higher than 1000 with offset&#x3D;0 is not recommended!    However you can set the offset appropriately so you minimize the amount of returned exchange rates and keep loading time to a low. | [optional] [default to 1000]
 **offset** | **int**| Set the index where the returned currency exchange rates start. Default is 0 | [optional] [default to 0]

### Return type

[**\Swagger\Client\Model\ModelCurrencyExchangeRate**](../Model/ModelCurrencyExchangeRate.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

