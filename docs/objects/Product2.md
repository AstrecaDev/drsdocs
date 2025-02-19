## Product2

<!-- Object description -->

## Fields

| Name      | Label | Type | Description |
| :-------- | :---- | :--: | :---------- | 
| Conga_Definition_Trigger__c | Conga Definition Trigger | Text | <!-- --> |
| Description |  |  | <!-- --> |
| DisplayUrl |  |  | <!-- --> |
| ExternalDataSourceId |  | Lookup | <!-- --> |
| ExternalId |  |  | <!-- --> |
| Family |  | Picklist | <!-- --> |
| IsActive |  |  | <!-- --> |
| IsSerialized |  |  | <!-- --> |
| Module__c | Module | Checkbox | <!-- --> |
| Name |  |  | <!-- --> |
| Product_Description_Rich__c | Product Description | Html | <!-- --> |
| Product_Marketing_Description__c | Product Marketing Description | Html | <!-- --> |
| Product_Specifications__c | Product Specifications | Html | <!-- --> |
| ProductCode |  |  | <!-- --> |
| QuantityUnitOfMeasure |  | Picklist | <!-- --> |
| StockKeepingUnit |  |  | <!-- --> |
| TransferRecordMode |  |  | <!-- --> |
| Type__c | Type | Picklist | <!-- --> |
| Wavelength__c | Wavelength | Number | Wavelength of the Product Laser |


## Related Flows

| Object | Name      | Type | Description |
| :----  | :-------- | :--: | :---------- | 
| Product2 | [Product_Update_Flow](../flows/Product_Update_Flow.md) |  Record After Save | Added Fault Path & Detailed Description in Each Node |


## Related Apex Classes

| Apex Class | Type |
| :----      | :--: | 
| [DeleteQuoteLineItemsTest](../apex/DeleteQuoteLineItemsTest.md) | Test |
| [GetoliTest](../apex/GetoliTest.md) | Test |
| [GetqlinesTest](../apex/GetqlinesTest.md) | Test |
| [OppLineItemControllerTest](../apex/OppLineItemControllerTest.md) | Test |
| [ProductWavelengthUpdater](../apex/ProductWavelengthUpdater.md) | Class |
| [ProductWavelengthUpdaterTest](../apex/ProductWavelengthUpdaterTest.md) | Test |
| [QliExtensionTest](../apex/QliExtensionTest.md) | Test |
| [QuoteLineItemControllerTest](../apex/QuoteLineItemControllerTest.md) | Test |
| [QuoteLineItemsExtensionTest](../apex/QuoteLineItemsExtensionTest.md) | Test |
| [updateordernumber](../apex/updateordernumber.md) | Class |




_Documentation generated with [sfdx-hardis](https://sfdx-hardis.cloudity.com)_
