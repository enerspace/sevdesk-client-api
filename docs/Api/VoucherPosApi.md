# Swagger\Client\VoucherPosApi

All URIs are relative to *https://my.sevdesk.de/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addVoucherPos**](VoucherPosApi.md#addVoucherPos) | **POST** /VoucherPos | Create a new voucher position
[**deleteVoucherPos**](VoucherPosApi.md#deleteVoucherPos) | **DELETE** /VoucherPos/{id} | Delete an existing voucher position
[**getVoucherPositions**](VoucherPosApi.md#getVoucherPositions) | **GET** /VoucherPos | Get an overview of all voucher positions
[**updateVoucherPos**](VoucherPosApi.md#updateVoucherPos) | **PUT** /VoucherPos/{id} | Update an existing voucher position
[**voucherPosGetAdditionalInformation**](VoucherPosApi.md#voucherPosGetAdditionalInformation) | **GET** /VoucherPos/{id}/getAdditionalInfo | Get additional information about the asset which is connected to a specified voucher position
[**voucherPosGetAssetInstance**](VoucherPosApi.md#voucherPosGetAssetInstance) | **GET** /VoucherPos/{id}/getAssetInstance | Get the asset which is connected to a specified voucher position


# **addVoucherPos**
> \Swagger\Client\Model\ModelVoucherPos addVoucherPos($body)

Create a new voucher position

Calls VoucherPos.php to create a voucher position

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('token', 'Bearer');

$apiInstance = new Swagger\Client\Api\VoucherPosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = "\"voucher[id]=&voucher[objectName]=Voucher&taxRate=&sum=&accountingType[id]=&accountingType[objectName]=AccountingType&isAsset=\""; // string | To create a voucher position, simply enter desired values after parameter= and remove the quotation marks.

try {
    $result = $apiInstance->addVoucherPos($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoucherPosApi->addVoucherPos: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **string**| To create a voucher position, simply enter desired values after parameter&#x3D; and remove the quotation marks. |

### Return type

[**\Swagger\Client\Model\ModelVoucherPos**](../Model/ModelVoucherPos.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteVoucherPos**
> deleteVoucherPos($id)

Delete an existing voucher position

Calls the delete() function in VoucherPos.php to delete a voucher position

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('token', 'Bearer');

$apiInstance = new Swagger\Client\Api\VoucherPosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Id of voucher position you want to delete

try {
    $apiInstance->deleteVoucherPos($id);
} catch (Exception $e) {
    echo 'Exception when calling VoucherPosApi->deleteVoucherPos: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Id of voucher position you want to delete |

### Return type

void (empty response body)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getVoucherPositions**
> \Swagger\Client\Model\ModelVoucherPos getVoucherPositions($limit, $offset, $embed)

Get an overview of all voucher positions

Calls VoucherPos.php to get necessary variables.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('token', 'Bearer');

$apiInstance = new Swagger\Client\Api\VoucherPosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 100; // int | Limits the number of entries returned. Default is 100
$offset = 0; // int | Set the index where the returned voucher positions start. Default is 0
$embed = array("embed_example"); // string[] | Get some additional information. Embed can handle multiple values, they must be separated by comma. Default ``.

try {
    $result = $apiInstance->getVoucherPositions($limit, $offset, $embed);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoucherPosApi->getVoucherPositions: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| Limits the number of entries returned. Default is 100 | [optional] [default to 100]
 **offset** | **int**| Set the index where the returned voucher positions start. Default is 0 | [optional] [default to 0]
 **embed** | [**string[]**](../Model/string.md)| Get some additional information. Embed can handle multiple values, they must be separated by comma. Default &#x60;&#x60;. | [optional]

### Return type

[**\Swagger\Client\Model\ModelVoucherPos**](../Model/ModelVoucherPos.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateVoucherPos**
> \Swagger\Client\Model\ModelVoucherPos updateVoucherPos($id, $body)

Update an existing voucher position

Calls VoucherPos.php to update an existing voucher position

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('token', 'Bearer');

$apiInstance = new Swagger\Client\Api\VoucherPosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Id of the voucher position you want to update
$body = "body_example"; // string | Parameters which need to be updated. Please refer to the description from create voucher position.    Enter the parameters according to the syntax: parameter1=&parameter2= and remove the quotation marks

try {
    $result = $apiInstance->updateVoucherPos($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoucherPosApi->updateVoucherPos: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Id of the voucher position you want to update |
 **body** | **string**| Parameters which need to be updated. Please refer to the description from create voucher position.    Enter the parameters according to the syntax: parameter1&#x3D;&amp;parameter2&#x3D; and remove the quotation marks | [optional]

### Return type

[**\Swagger\Client\Model\ModelVoucherPos**](../Model/ModelVoucherPos.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **voucherPosGetAdditionalInformation**
> voucherPosGetAdditionalInformation($id)

Get additional information about the asset which is connected to a specified voucher position

Calls getAdditionalInformation() in VoucherPos.php to get additional information about the asset which is connected to the specified voucher position

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('token', 'Bearer');

$apiInstance = new Swagger\Client\Api\VoucherPosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Id of the voucher position of which you want to get additional information about the connected asset

try {
    $apiInstance->voucherPosGetAdditionalInformation($id);
} catch (Exception $e) {
    echo 'Exception when calling VoucherPosApi->voucherPosGetAdditionalInformation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Id of the voucher position of which you want to get additional information about the connected asset |

### Return type

void (empty response body)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **voucherPosGetAssetInstance**
> \Swagger\Client\Model\ModelAsset voucherPosGetAssetInstance($id)

Get the asset which is connected to a specified voucher position

Calls getAssetInstance() in VoucherPos.php to get the asset which is connected to the specified voucher position

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('token', 'Bearer');

$apiInstance = new Swagger\Client\Api\VoucherPosApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Id of the voucher position of which you want to get the connected asset

try {
    $result = $apiInstance->voucherPosGetAssetInstance($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoucherPosApi->voucherPosGetAssetInstance: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Id of the voucher position of which you want to get the connected asset |

### Return type

[**\Swagger\Client\Model\ModelAsset**](../Model/ModelAsset.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

