# ModelVatReport

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**create** | [**\DateTime**](\DateTime.md) | date the vat report was created | [optional] 
**update** | [**\DateTime**](\DateTime.md) | date the vat report was last updated | [optional] 
**sev_client** | **object** | sevClient is the unique id every customer has and is used in nearly all operations | [optional] 
**country** | [**\Swagger\Client\Model\ModelStaticCountry**](ModelStaticCountry.md) | StaticCountry of the vat report | [optional] 
**report_date** | [**\DateTime**](\DateTime.md) | date of the vat report | [optional] 
**reporting_year** | **string** | year which is reported | [optional] 
**reporting_period** | **string** | period which is reported | [optional] 
**reporting_period_code** | **string** |  | [optional] 
**reporting_values** | **string** |  | [optional] 
**test_case** | **bool** |  | [optional] 
**actual_taxation** | **bool** | define if you want to report the main income method or the profit and loss | [optional] 
**corrected** | **bool** |  | [optional] 
**result_finance_authority** | **string** |  | [optional] 
**finance_authority_ticket_number** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


