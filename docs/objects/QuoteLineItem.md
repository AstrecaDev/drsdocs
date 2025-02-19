## QuoteLineItem

<!-- Object description -->

## Fields

| Name      | Label | Type | Description |
| :-------- | :---- | :--: | :---------- | 
| Commission__c | Commission | Currency | <!-- --> |
| Commission_Total__c | Commission Total | Currency | <!-- --> |
| Description |  |  | <!-- --> |
| Discount |  |  | <!-- --> |
| Discount_Amount__c | Discount Amount | Currency | <!-- --> |
| End_User_Sales_Price__c | International MSRP Sales Price | Currency | <!-- --> |
| ISP__c | International Transfer Price | Currency | <!-- --> |
| Item_Number__c | Item Number | Text | <!-- --> |
| LineNumber |  |  | <!-- --> |
| ListPrice |  |  | <!-- --> |
| Module__c | Module | Checkbox | <!-- --> |
| MSRP__c | International MSRP | Currency | <!-- --> |
| MSRP_Total__c | Extended International MSRP Price | Currency | <!-- --> |
| Optional__c | Optional | Checkbox | <!-- --> |
| order_number__c | Order Number | Number | Order Number to define the sort order on Quote Doc |
| Original_Commission__c | Original Commission | Currency | <!-- --> |
| Original_List_Price__c | Standard Price | Currency | <!-- --> |
| PriceBook__c | PriceBook | Text | <!-- --> |
| Product_Description_Rich__c | Product Description | Html | <!-- --> |
| Product_Marketing_Description__c | Product Marketing Description | Html | <!-- --> |
| Product_Specifications__c | Product Specifications | Html | <!-- --> |
| Product2Id |  | Lookup | <!-- --> |
| ProductCode |  |  | <!-- --> |
| Quantity |  |  | <!-- --> |
| QuoteId |  | MasterDetail | <!-- --> |
| ServiceDate |  |  | <!-- --> |
| Sort_Order__c | Sort Order | Number | <!-- --> |
| Subtotal |  |  | <!-- --> |
| Total_Discount__c | Total Discount | Currency | <!-- --> |
| Total_End_User_Price__c | International MSRP Total | Currency | <!-- --> |
| Total_List_Price__c | Total Sales Price | Currency | <!-- --> |
| Total_User_Discount__c | Total International MSRP Discount | Currency | <!-- --> |
| TotalPrice |  |  | <!-- --> |
| Transfer_Discount_Percent__c | Discount (%) | Percent | <!-- --> |
| UnitPrice |  |  | <!-- --> |
| User_Discount__c | Unit International MSRP Discount Amount | Currency | <!-- --> |
| User_Discount_Percent__c | International MSRP Discount (%) | Percent | <!-- --> |

## Validation Rules

| Rule      | Active | Description | Formula |
| :-------- | :---- | :---------- | :------ |
| Component_Product_Validation | Yes | This validation rule is created by Astreca team to enter correct order number on quoteline | `AND(
OR(
ISPICKVAL(Product2.Type__c, "Upgrade"),
ISPICKVAL(Product2.Type__c, "Warranty"),
ISPICKVAL(Product2.Type__c, "Discount"),
ISPICKVAL(Product2.Type__c, "Promotion"),
ISPICKVAL(Product2.Type__c, "Module"),
ISPICKVAL(Product2.Type__c, "Options")
),
MOD(order_number__c, 1) = 0,

NOT(ISBLANK(order_number__c))
)` |
| Qunatity_should_not_in_Decimal | Yes | This validation rule is created by Astreca team to enter integer quantity | `AND(
NOT(ISBLANK(Quantity)),
MOD(Quantity, 1) <> 0
)` |
| Standalone_not_contain_decimal | Yes | This validation rule is created by Astreca team to enter integer number for standalone type | `AND(
OR(
ISPICKVAL(Product2.Type__c, "Standalone"),
ISPICKVAL(Product2.Type__c, "Base Unit")
),
NOT(ISBLANK(order_number__c )),
MOD(order_number__c , 1) <> 0
)` |


## Related Flows

| Object | Name      | Type | Description |
| :----  | :-------- | :--: | :---------- | 
| Product2 | [Product_Update_Flow](../flows/Product_Update_Flow.md) |  Record After Save | Added Fault Path & Detailed Description in Each Node |
| QuoteLineItem | [Quote_Line_Create_Before_Save](../flows/Quote_Line_Create_Before_Save.md) |  Record Before Save | Added custom metadata to update the default order number on quote line item when it's get created from Opportunity. |
| QuoteLineItem | [Quote_Line_Create_or_Update_After_Save](../flows/Quote_Line_Create_or_Update_After_Save.md) |  Record After Save | This flow is updated to adjust the condition so that when Optional__c  prior value is true & updated to false & Discount_Amount__c is equal to Original_List_Price__c then Discount_Amount__c  should be 0 |


## Related Apex Classes

| Apex Class | Type |
| :----      | :--: | 
| [DeleteQuoteLineItemsTest](../apex/DeleteQuoteLineItemsTest.md) | Test |
| [GetqlinesTest](../apex/GetqlinesTest.md) | Test |
| [QliExtensionTest](../apex/QliExtensionTest.md) | Test |
| [QuoteLineItemControllerTest](../apex/QuoteLineItemControllerTest.md) | Test |
| [QuoteLineItemsExtensionTest](../apex/QuoteLineItemsExtensionTest.md) | Test |




_Documentation generated with [sfdx-hardis](https://sfdx-hardis.cloudity.com)_
