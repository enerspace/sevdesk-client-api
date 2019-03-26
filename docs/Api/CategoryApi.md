# Swagger\Client\CategoryApi

All URIs are relative to *https://my.sevdesk.de/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addCategory**](CategoryApi.md#addCategory) | **POST** /Category | Create a new category
[**deleteCategory**](CategoryApi.md#deleteCategory) | **DELETE** /Category/{id} | Delete an existing category
[**getCategories**](CategoryApi.md#getCategories) | **GET** /Category | Get an overview of all categories
[**updateCategory**](CategoryApi.md#updateCategory) | **PUT** /Category/{id} | Update a existing category


# **addCategory**
> \Swagger\Client\Model\ModelCategory addCategory($body)

Create a new category

Calls Category.php

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('token', 'Bearer');

$apiInstance = new Swagger\Client\Api\CategoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = "\"name=&objectType=&priority=100\""; // string | To create a category, simply enter desired values after parameter= and remove the quotation marks.

try {
    $result = $apiInstance->addCategory($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CategoryApi->addCategory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **string**| To create a category, simply enter desired values after parameter&#x3D; and remove the quotation marks. |

### Return type

[**\Swagger\Client\Model\ModelCategory**](../Model/ModelCategory.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteCategory**
> deleteCategory($id)

Delete an existing category

Calls the delete() function in Category.php

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('token', 'Bearer');

$apiInstance = new Swagger\Client\Api\CategoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | id of category you want to delete

try {
    $apiInstance->deleteCategory($id);
} catch (Exception $e) {
    echo 'Exception when calling CategoryApi->deleteCategory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| id of category you want to delete |

### Return type

void (empty response body)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCategories**
> \Swagger\Client\Model\ModelCategory getCategories($limit, $offset)

Get an overview of all categories

Calls Category.php to get necessary variables.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('token', 'Bearer');

$apiInstance = new Swagger\Client\Api\CategoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 100; // int | Limits the number of entries returned. Default is 100
$offset = 0; // int | Set the index where the returned categories start. Default is 0

try {
    $result = $apiInstance->getCategories($limit, $offset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CategoryApi->getCategories: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| Limits the number of entries returned. Default is 100 | [optional] [default to 100]
 **offset** | **int**| Set the index where the returned categories start. Default is 0 | [optional] [default to 0]

### Return type

[**\Swagger\Client\Model\ModelCategory**](../Model/ModelCategory.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateCategory**
> \Swagger\Client\Model\ModelCategory updateCategory($id, $body)

Update a existing category

Calls Category.php

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('token', 'Bearer');

$apiInstance = new Swagger\Client\Api\CategoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | id of category you want to update
$body = "body_example"; // string | Parameters which need to be updated. Please refer to the description from create discount.    Enter the parameters according to the syntax: parameter1=&parameter2=

try {
    $result = $apiInstance->updateCategory($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CategoryApi->updateCategory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| id of category you want to update |
 **body** | **string**| Parameters which need to be updated. Please refer to the description from create discount.    Enter the parameters according to the syntax: parameter1&#x3D;&amp;parameter2&#x3D; | [optional]

### Return type

[**\Swagger\Client\Model\ModelCategory**](../Model/ModelCategory.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

