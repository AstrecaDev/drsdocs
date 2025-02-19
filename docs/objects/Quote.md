## Quote

<!-- Object description -->

## Fields

| Name      | Label | Type | Description |
| :-------- | :---- | :--: | :---------- | 
| Account_Name_Case__c | Account Name | Text | <!-- --> |
| AccountId |  | Lookup | <!-- --> |
| AdditionalAddress |  |  | <!-- --> |
| AdditionalName |  |  | <!-- --> |
| Bill_To_Contact__c | Bill To Contact | Text | <!-- --> |
| BillingAddress |  |  | <!-- --> |
| BillingName |  |  | <!-- --> |
| Case__c | Case | Lookup | This look up field is created by Astreca |
| ContactId |  | Lookup | <!-- --> |
| ContractId |  | Lookup | <!-- --> |
| Description |  |  | <!-- --> |
| Discount |  |  | <!-- --> |
| Discount_Total__c | Standard Discount Total | Summary | <!-- --> |
| Email |  |  | <!-- --> |
| ExpirationDate |  |  | <!-- --> |
| Fax |  |  | <!-- --> |
| GrandTotal |  |  | <!-- --> |
| IsSyncing |  |  | <!-- --> |
| LineItemCount |  |  | <!-- --> |
| Name |  |  | <!-- --> |
| OpportunityId |  | MasterDetail | <!-- --> |
| Orchastrate_Status__c | Orchestrate Status | Picklist | <!-- --> |
| OwnerId |  | Lookup | <!-- --> |
| Payment_Terms__c | Payment Terms | Picklist | <!-- --> |
| Phone |  |  | <!-- --> |
| PriceBook__c | PriceBook | Text | <!-- --> |
| Process_Instance__c | Process Instance | Lookup | <!-- --> |
| Quote_Grand_Total__c | Quote Grand Total | Currency | <!-- --> |
| QuoteAccountId |  | Lookup | <!-- --> |
| QuoteToAddress |  |  | <!-- --> |
| QuoteToName |  |  | <!-- --> |
| RelatedWorkId |  | Lookup | <!-- --> |
| Repair_Fee__c | Repair Fee | Currency | <!-- --> |
| Ship_To_Contact__c | Ship To Contact | Text | <!-- --> |
| ShippingAddress |  |  | <!-- --> |
| ShippingHandling |  |  | <!-- --> |
| ShippingName |  |  | <!-- --> |
| Status |  | Picklist | <!-- --> |
| Subtotal |  |  | <!-- --> |
| Subtotal_Custom__c | Subtotal | Currency | This is used with the Quote Lines customization to bring the Subtotal to the right amount. |
| Tax |  |  | <!-- --> |
| Tax_Percent__c | Tax Percent | Percent | <!-- --> |
| Tax_Percent_Amount__c | Tax Percent Amount | Currency | <!-- --> |
| TotalPrice |  |  | <!-- --> |
| Type__c | Type | Picklist | <!-- --> |
| User_Discount_Total__c | MSRP Discount Total | Summary | <!-- --> |


## Related Flows

| Object | Name      | Type | Description |
| :----  | :-------- | :--: | :---------- | 
| Product2 | [Product_Update_Flow](../flows/Product_Update_Flow.md) |  Record After Save | Added Fault Path & Detailed Description in Each Node |
| Quote | [Auto_Populate_Opportunity_and_Contact_Info_to_Quote](../flows/Auto_Populate_Opportunity_and_Contact_Info_to_Quote.md) |  Record After Save | This flow will fire on Quote Creation and Updation ,It will update Contact on quote from Opportunity Contact Role if Role is Decision Maker and Type = Sales// Added Email ,Bill & ship to Contact,Phone & Fax on 4th April |
| Quote | [Quote_Create_or_Update_Before_Save](../flows/Quote_Create_or_Update_Before_Save.md) |  Record Before Save | <!-- --> |
| Quote | [Update_Expiration_Date_on_Quote](../flows/Update_Expiration_Date_on_Quote.md) |  Record Before Save | This flow is used to update expiration date depending on created date on Quote object. |
| Quote | [Update_Opportunity_based_on_Quote_Status](../flows/Update_Opportunity_based_on_Quote_Status.md) |  Record After Save | This flow is used to update Opportunity checkbox based on Quote Status |
| QuoteLineItem | [Quote_Line_Create_Before_Save](../flows/Quote_Line_Create_Before_Save.md) |  Record Before Save | Added custom metadata to update the default order number on quote line item when it's get created from Opportunity. |
| QuoteLineItem | [Quote_Line_Create_or_Update_After_Save](../flows/Quote_Line_Create_or_Update_After_Save.md) |  Record After Save | This flow is updated to adjust the condition so that when Optional__c  prior value is true & updated to false & Discount_Amount__c is equal to Original_List_Price__c then Discount_Amount__c  should be 0 |


## Related Apex Classes

| Apex Class | Type |
| :----      | :--: | 
| [DeleteQuoteLineItemsTest](../apex/DeleteQuoteLineItemsTest.md) | Test |
| [GetqlinesTest](../apex/GetqlinesTest.md) | Test |
| [OppLineItemControllerTest](../apex/OppLineItemControllerTest.md) | Test |
| [QliExtensionTest](../apex/QliExtensionTest.md) | Test |
| [QuoteLineItemControllerTest](../apex/QuoteLineItemControllerTest.md) | Test |
| [QuoteLineItemsExtensionTest](../apex/QuoteLineItemsExtensionTest.md) | Test |
| [QuoteTriggerTest](../apex/QuoteTriggerTest.md) | Test |
| [ReusableLookupController](../apex/ReusableLookupController.md) | Lightning Controller |
| [SavedocclassTest](../apex/SavedocclassTest.md) | Test |
| [updateordernumber](../apex/updateordernumber.md) | Class |


## Related Lightning Pages

| Lightning Page | Type |
| :----      | :--: | 
| [Opportunity_Record_Page2](../pages/Opportunity_Record_Page2.md) |  Record Page |
| [Quote_Record_Page](../pages/Quote_Record_Page.md) |  Record Page |


_Documentation generated with [sfdx-hardis](https://sfdx-hardis.cloudity.com)_
