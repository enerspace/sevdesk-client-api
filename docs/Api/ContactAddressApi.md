# Swagger\Client\ContactAddressApi

All URIs are relative to *https://my.sevdesk.de/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addContactAddress**](ContactAddressApi.md#addContactAddress) | **POST** /ContactAddress | Create a new contact address
[**deleteContactAddress**](ContactAddressApi.md#deleteContactAddress) | **DELETE** /ContactAddress/{id} | Delete an existing contact address
[**getContactAddresses**](ContactAddressApi.md#getContactAddresses) | **GET** /ContactAddress | Get an overview of all contact addresses
[**updateContactAddress**](ContactAddressApi.md#updateContactAddress) | **PUT** /ContactAddress/{id} | Update an existing contact address


# **addContactAddress**
> \Swagger\Client\Model\ModelContactAddress addContactAddress($body)

Create a new contact address

Calls ContactAddress.php

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ContactAddressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = "\"contact[id]=&contact[objectName]=Contact&country[id]=&country[objectName]=StaticCountry&street=&zip=&city=\""; // string | To create a contact address, simply enter desired values after parameter= and remove the quotation marks

try {
    $result = $apiInstance->addContactAddress($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactAddressApi->addContactAddress: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **string**| To create a contact address, simply enter desired values after parameter&#x3D; and remove the quotation marks |

### Return type

[**\Swagger\Client\Model\ModelContactAddress**](../Model/ModelContactAddress.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteContactAddress**
> deleteContactAddress($id)

Delete an existing contact address

Calls the delete() function in ContactAddress.php

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ContactAddressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | id of contact address you want to delete

try {
    $apiInstance->deleteContactAddress($id);
} catch (Exception $e) {
    echo 'Exception when calling ContactAddressApi->deleteContactAddress: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| id of contact address you want to delete |

### Return type

void (empty response body)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getContactAddresses**
> \Swagger\Client\Model\ModelContactAddress getContactAddresses($limit, $offset, $embed)

Get an overview of all contact addresses

Calls ContactAddress.php to get necessary variables

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ContactAddressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 100; // int | Limits the number of entries returned. Default is 100
$offset = 0; // int | Set the index where the returned contacts start. Default is 0
$embed = array("embed_example"); // string[] | Get some additional information. Embed can handle multiple values, they must be separated by comma. Default ``.

try {
    $result = $apiInstance->getContactAddresses($limit, $offset, $embed);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactAddressApi->getContactAddresses: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| Limits the number of entries returned. Default is 100 | [optional] [default to 100]
 **offset** | **int**| Set the index where the returned contacts start. Default is 0 | [optional] [default to 0]
 **embed** | [**string[]**](../Model/string.md)| Get some additional information. Embed can handle multiple values, they must be separated by comma. Default &#x60;&#x60;. | [optional]

### Return type

[**\Swagger\Client\Model\ModelContactAddress**](../Model/ModelContactAddress.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateContactAddress**
> \Swagger\Client\Model\ModelContactAddress updateContactAddress($id, $body)

Update an existing contact address

Calls ContactAddress.php

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('token', 'Bearer');

$apiInstance = new Swagger\Client\Api\ContactAddressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | id of contact address you want to update
$body = "body_example"; // string | Parameters which need to be updated. Please refer to the description from create contact address.    Enter the parameters according to the syntax: parameter1=&parameter2=

try {
    $result = $apiInstance->updateContactAddress($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactAddressApi->updateContactAddress: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| id of contact address you want to update |
 **body** | **string**| Parameters which need to be updated. Please refer to the description from create contact address.    Enter the parameters according to the syntax: parameter1&#x3D;&amp;parameter2&#x3D; | [optional]

### Return type

[**\Swagger\Client\Model\ModelContactAddress**](../Model/ModelContactAddress.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

