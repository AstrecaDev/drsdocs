## SFDX Project CI/CD configuration

| Sfdx-hardis Parameter | Value | Description & doc link |
| :--------- | :---- | :---------- |
| Install Packages During Check Deploy | ⬜ | [Install 1GP & 2GP packages during deployment check CI/CD job](https://sfdx-hardis.cloudity.com/hardis/project/deploy/smart/#packages-installation) |
| Use Delta Deployment | ⬜ | [Deploys only updated metadatas , only when a MR/PR is from a minor branch to a major branch](https://sfdx-hardis.cloudity.com/salesforce-ci-cd-config-delta-deployment/#delta-mode) |
| Use Smart Deployment Tests | ⬜ | [Skip Apex test cases if delta metadatas can not impact them, only when a MR/PR is from a minor branch to a major branch](https://sfdx-hardis.cloudity.com/hardis/project/deploy/smart/#smart-deployments-tests) |

___

## Package XML files

| Package name | Description |
| :----------- | :---------- |
| [Package folder: force-app](force-app-package.xml.md) (397) | Package.xml generated from content of SFDX package force-app (folder force-app) |

___

## Apex Classes

| Apex Class | Type |
| :----      | :--: | 
| [DeleteQuoteLineItemsTest](apex/DeleteQuoteLineItemsTest.md) | Test |
| [GetVFOrigin](apex/GetVFOrigin.md) | Lightning Controller |
| [GetVFOriginTest](apex/GetVFOriginTest.md) | Test |
| [GetoliTest](apex/GetoliTest.md) | Test |
| [GetqlinesTest](apex/GetqlinesTest.md) | Test |
| [NavigationMenuItemsController](apex/NavigationMenuItemsController.md) | Lightning Controller |
| [OppLineItemControllerTest](apex/OppLineItemControllerTest.md) | Test |
| [ProductWavelengthUpdater](apex/ProductWavelengthUpdater.md) | Class |
| [ProductWavelengthUpdaterTest](apex/ProductWavelengthUpdaterTest.md) | Test |
| [QliExtensionTest](apex/QliExtensionTest.md) | Test |
| [QuoteLineItemControllerTest](apex/QuoteLineItemControllerTest.md) | Test |
| [QuoteLineItemsExtensionTest](apex/QuoteLineItemsExtensionTest.md) | Test |
| [QuoteTriggerTest](apex/QuoteTriggerTest.md) | Test |
| [ReportFinderUtil](apex/ReportFinderUtil.md) | Class |
| [ReusableLookupController](apex/ReusableLookupController.md) | Lightning Controller |
| [SavedocclassTest](apex/SavedocclassTest.md) | Test |
| [TestTermBothTrigger](apex/TestTermBothTrigger.md) | Test |
| [Utilities](apex/Utilities.md) | Class |
| [Utilities_Test](apex/Utilities_Test.md) | Test |
| [updateordernumber](apex/updateordernumber.md) | Class |

## Flows

| Object | Name      | Type | Description |
| :----  | :-------- | :--: | :---------- | 
| 💻 | [New_Quote](flows/New_Quote.md) |  Screen Flow | This is used for a new quote button and will set default fields. |
| 💻 | [customer_satisfaction](flows/customer_satisfaction.md) |  Survey | <!-- --> |
| 💻 | [net_promoter_score](flows/net_promoter_score.md) |  Survey | <!-- --> |
| Case | [Customer_Survey_Email](flows/Customer_Survey_Email.md) |  Record After Save | <!-- --> |
| Lead | [Contacted_Leads](flows/Contacted_Leads.md) |  Workflow | <!-- --> |
| Lead | [MQL_to_SQL_Assignment](flows/MQL_to_SQL_Assignment.md) |  Record After Save | <!-- --> |
| Opportunity | [Send_Email_Opportunity_Closed_Won](flows/Send_Email_Opportunity_Closed_Won.md) |  Record After Save | This flow is used to send an email after 3 weeks to the Primary Contact when the Opportunity is Closed Won + added one min delay for testing |
| Opportunity | [Update_Lost_Reason_and_Post_Mortem_to_Blank](flows/Update_Lost_Reason_and_Post_Mortem_to_Blank.md) |  Record Before Save | <!-- --> |
| Opportunity | [Update_Opportunity_Stage_based_on_Criteria](flows/Update_Opportunity_Stage_based_on_Criteria.md) |  Record After Save | This flow is checking required fields before update Stage on Opportunity + Update Closed Lost or Qualification Open + updated 17 May 24 + Added condition for For Closed won checkbox v2 |
| OpportunityContactRole | [Delete_Opp_Primary_Contact](flows/Delete_Opp_Primary_Contact.md) |  Record Before Delete | This flow will clear the PrimaryContactName__c & Primary_Contact__c fields when Associated Contact role is deleted |
| OpportunityContactRole | [Update_Has_Contact_Role_on_Opp](flows/Update_Has_Contact_Role_on_Opp.md) |  Record After Save | <!-- --> |
| OpportunityContactRole | [Update_Opp_Primary_Contact](flows/Update_Opp_Primary_Contact.md) |  Record After Save | In this version PrimaryContactName__c  field is updated with Primary Contact's Name to make Opportunity searchable in Global Search. With added fault path |
| Product2 | [Product_Update_Flow](flows/Product_Update_Flow.md) |  Record After Save | Added Fault Path & Detailed Description in Each Node |
| Quote | [Auto_Populate_Opportunity_and_Contact_Info_to_Quote](flows/Auto_Populate_Opportunity_and_Contact_Info_to_Quote.md) |  Record After Save | This flow will fire on Quote Creation and Updation ,It will update Contact on quote from Opportunity Contact Role if Role is Decision Maker and Type = Sales// Added Email ,Bill & ship to Contact,Phone & Fax on 4th April |
| Quote | [Quote_Create_or_Update_Before_Save](flows/Quote_Create_or_Update_Before_Save.md) |  Record Before Save | <!-- --> |
| Quote | [Update_Expiration_Date_on_Quote](flows/Update_Expiration_Date_on_Quote.md) |  Record Before Save | This flow is used to update expiration date depending on created date on Quote object. |
| Quote | [Update_Opportunity_based_on_Quote_Status](flows/Update_Opportunity_based_on_Quote_Status.md) |  Record After Save | This flow is used to update Opportunity checkbox based on Quote Status |
| QuoteLineItem | [Quote_Line_Create_Before_Save](flows/Quote_Line_Create_Before_Save.md) |  Record Before Save | Added custom metadata to update the default order number on quote line item when it's get created from Opportunity. |
| QuoteLineItem | [Quote_Line_Create_or_Update_After_Save](flows/Quote_Line_Create_or_Update_After_Save.md) |  Record After Save | This flow is updated to adjust the condition so that when Optional__c  prior value is true & updated to false & Discount_Amount__c is equal to Original_List_Price__c then Discount_Amount__c  should be 0 |
| Quote_Term__c | [Set_Quote_Term_After_Save](flows/Set_Quote_Term_After_Save.md) |  Record Before Save | <!-- --> |
| Quote_Term__c | [Set_Quote_Term_Standard](flows/Set_Quote_Term_Standard.md) |  Record After Save | <!-- --> |

___

## Lightning Pages

| Lightning Page | Type |
| :----      | :--: | 
| [Opportunity_Record_Page2](pages/Opportunity_Record_Page2.md) |  Record Page |
| [Quote_Record_Page](pages/Quote_Record_Page.md) |  Record Page |

## Objects

| Name      | Label | Description |
| :-------- | :---- | :---------- | 
| [Account](objects/Account.md) |  | <!-- --> |
| [Address](objects/Address.md) |  | <!-- --> |
| [Opportunity](objects/Opportunity.md) |  | <!-- --> |
| [Product2](objects/Product2.md) |  | <!-- --> |
| [Quote](objects/Quote.md) |  | <!-- --> |
| [QuoteLineItem](objects/QuoteLineItem.md) |  | <!-- --> |
| [Quote_Term_Event__e](objects/Quote_Term_Event__e.md) | Quote_Term_Event | <!-- --> |
| [qliordermapping__mdt](objects/qliordermapping__mdt.md) | qliordermapping | QLI order number data to populate default values in QLI Order number Field |

___


## Doc HTML Pages

To read the documentation as HTML pages, run the following code (you need [**Python**](https://www.python.org/downloads/) on your computer)

```python
pip install mkdocs-material mkdocs-exclude-search mdx_truly_sane_lists || python -m pip install mkdocs-material mkdocs-exclude-search mdx_truly_sane_lists || py -m pip install mkdocs-material mkdocs-exclude-search mdx_truly_sane_lists
mkdocs serve -v || python -m mkdocs serve -v || py -m mkdocs serve -v
```

To just generate HTML pages that you can host anywhere, run `mkdocs build || python -m mkdocs build || py -m mkdocs build`


_Documentation generated from branch main with [sfdx-hardis](https://sfdx-hardis.cloudity.com) by [Cloudity](https://cloudity.com) command [`sf hardis:doc:project2markdown`](https://sfdx-hardis.cloudity.com/hardis/doc/project2markdown/)_
