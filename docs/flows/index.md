---
hide:
  - path
---

## Flows

| Object | Name      | Type | Description |
| :----  | :-------- | :--: | :---------- | 
| 💻 | [New_Quote](New_Quote.md) [🕒](New_Quote-history.md) |  Screen Flow | This is used for a new quote button and will set default fields. |
| 💻 | [customer_satisfaction](customer_satisfaction.md) [🕒](customer_satisfaction-history.md) |  Survey | <!-- --> |
| 💻 | [net_promoter_score](net_promoter_score.md) [🕒](net_promoter_score-history.md) |  Survey | <!-- --> |
| Case | [Customer_Survey_Email](Customer_Survey_Email.md) [🕒](Customer_Survey_Email-history.md) |  Record After Save | <!-- --> |
| Lead | [Contacted_Leads](Contacted_Leads.md) [🕒](Contacted_Leads-history.md) |  Workflow | <!-- --> |
| Lead | [MQL_to_SQL_Assignment](MQL_to_SQL_Assignment.md) [🕒](MQL_to_SQL_Assignment-history.md) |  Record After Save | <!-- --> |
| Opportunity | [Send_Email_Opportunity_Closed_Won](Send_Email_Opportunity_Closed_Won.md) [🕒](Send_Email_Opportunity_Closed_Won-history.md) |  Record After Save | This flow is used to send an email after 3 weeks to the Primary Contact when the Opportunity is Closed Won + added one min delay for testing |
| Opportunity | [Update_Lost_Reason_and_Post_Mortem_to_Blank](Update_Lost_Reason_and_Post_Mortem_to_Blank.md) [🕒](Update_Lost_Reason_and_Post_Mortem_to_Blank-history.md) |  Record Before Save | <!-- --> |
| Opportunity | [Update_Opportunity_Stage_based_on_Criteria](Update_Opportunity_Stage_based_on_Criteria.md) [🕒](Update_Opportunity_Stage_based_on_Criteria-history.md) |  Record After Save | This flow is checking required fields before update Stage on Opportunity + Update Closed Lost or Qualification Open + updated 17 May 24 + Added condition for For Closed won checkbox v2 |
| OpportunityContactRole | [Delete_Opp_Primary_Contact](Delete_Opp_Primary_Contact.md) [🕒](Delete_Opp_Primary_Contact-history.md) |  Record Before Delete | This flow will clear the PrimaryContactName__c & Primary_Contact__c fields when Associated Contact role is deleted |
| OpportunityContactRole | [Update_Has_Contact_Role_on_Opp](Update_Has_Contact_Role_on_Opp.md) [🕒](Update_Has_Contact_Role_on_Opp-history.md) |  Record After Save | <!-- --> |
| OpportunityContactRole | [Update_Opp_Primary_Contact](Update_Opp_Primary_Contact.md) [🕒](Update_Opp_Primary_Contact-history.md) |  Record After Save | In this version PrimaryContactName__c  field is updated with Primary Contact's Name to make Opportunity searchable in Global Search. With added fault path |
| Product2 | [Product_Update_Flow](Product_Update_Flow.md) [🕒](Product_Update_Flow-history.md) |  Record After Save | Added Update Quote fields Specs Updated & status . Also added fault path for all the dml , filter Quote status as Invalid |
| Quote | [Auto_Populate_Opportunity_and_Contact_Info_to_Quote](Auto_Populate_Opportunity_and_Contact_Info_to_Quote.md) [🕒](Auto_Populate_Opportunity_and_Contact_Info_to_Quote-history.md) |  Record After Save | This flow will fire on Quote Creation and Updation ,It will update Contact on quote from Opportunity Contact Role if Role is Decision Maker and Type = Sales// Added Email ,Bill & ship to Contact,Phone & Fax on 4th April |
| Quote | [Quote_Create_or_Update_Before_Save](Quote_Create_or_Update_Before_Save.md) [🕒](Quote_Create_or_Update_Before_Save-history.md) |  Record Before Save | <!-- --> |
| Quote | [Update_Expiration_Date_on_Quote](Update_Expiration_Date_on_Quote.md) [🕒](Update_Expiration_Date_on_Quote-history.md) |  Record Before Save | This flow is used to update expiration date depending on created date on Quote object. |
| Quote | [Update_Opportunity_based_on_Quote_Status](Update_Opportunity_based_on_Quote_Status.md) [🕒](Update_Opportunity_based_on_Quote_Status-history.md) |  Record After Save | This flow is used to update Opportunity checkbox based on Quote Status |
| QuoteLineItem | [Quote_Line_Create_Before_Save](Quote_Line_Create_Before_Save.md) [🕒](Quote_Line_Create_Before_Save-history.md) |  Record Before Save | Added custom metadata to update the default order number on quote line item when it's get created from Opportunity. |
| QuoteLineItem | [Quote_Line_Create_or_Update_After_Save](Quote_Line_Create_or_Update_After_Save.md) [🕒](Quote_Line_Create_or_Update_After_Save-history.md) |  Record After Save | This flow is updated to adjust the condition so that when Optional__c  prior value is true & updated to false & Discount_Amount__c is equal to Original_List_Price__c then Discount_Amount__c  should be 0 |
| Quote_Term__c | [Set_Quote_Term_After_Save](Set_Quote_Term_After_Save.md) [🕒](Set_Quote_Term_After_Save-history.md) |  Record Before Save | <!-- --> |
| Quote_Term__c | [Set_Quote_Term_Standard](Set_Quote_Term_Standard.md) [🕒](Set_Quote_Term_Standard-history.md) |  Record After Save | <!-- --> |

_Documentation generated from branch main with [sfdx-hardis](https://sfdx-hardis.cloudity.com) by [Cloudity](https://cloudity.com) command [`sf hardis:doc:project2markdown`](https://sfdx-hardis.cloudity.com/hardis/doc/project2markdown/)_
