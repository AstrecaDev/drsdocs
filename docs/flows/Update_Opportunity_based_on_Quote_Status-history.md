# Update_Opportunity_based_on_Quote_Status history

<!-- This page has been generated to be viewed with mkdocs-material, you can not view it just as markdown . Activate tab plugin following the doc at https://squidfunk.github.io/mkdocs-material/reference/content-tabs/ -->

=== "Jan 17, 2024 (Initial)"

    _Jan 17, 2024, by Astreva Dev in commit Taken Backup of Changes Pushed to UAT_

    
    ## Flow Diagram [(_View History_)](Update_Opportunity_based_on_Quote_Status-history.md)
    
    ```mermaid
    %% If you read this, your Markdown visualizer does not handle MermaidJS syntax.
    %% - If you are in VsCode, install extension `Markdown Preview Mermaid Support` at https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid
    %% - If you are using sfdx-hardis, try to define env variable `MERMAID_MODES=cli,docker` ,then run again the command to regenerate markdown with SVG images.
    %% - If you are within mkdocs-material, define mermaid plugin in `mkdocs.yml` as described in https://squidfunk.github.io/mkdocs-material/extensions/mermaid/
    %% - At last resort, you can copy-paste this MermaidJS code in https://mermaid.live/ to see the Flow Diagram
    
    flowchart TB
    START(["START<br/><b>AutoLaunched Flow</b></br>Type: <b> Record After Save</b>"]):::startClass
    click START "#general-information" "2069192970"
    
    Check_for_different_Status{"🔀 <em></em><br/>Check for different Status"}:::decisions
    click Check_for_different_Status "#check_for_different_status" "288784867"
    
    Update_related_opportunity_Checkbox[("🛠️ <em></em><br/>Update related opportunity Checkbox")]:::recordUpdates
    click Update_related_opportunity_Checkbox "#update_related_opportunity_checkbox" "2137570785"
    
    Update_Related_Opportunity_Quote_Sent_Checkbox[("🛠️ <em></em><br/>Update Related Opportunity Quote Sent Checkbox")]:::recordUpdates
    click Update_Related_Opportunity_Quote_Sent_Checkbox "#update_related_opportunity_quote_sent_checkbox" "295710788"
    
    Check_for_different_Status --> |"Budgetary Quote Sent"| Update_related_opportunity_Checkbox
    Check_for_different_Status --> |"Quote Sent Check"| Update_Related_Opportunity_Quote_Sent_Checkbox
    Check_for_different_Status --> |"Default Outcome"| END_Check_for_different_Status
    Update_related_opportunity_Checkbox --> END_Update_related_opportunity_Checkbox
    Update_Related_Opportunity_Quote_Sent_Checkbox --> END_Update_Related_Opportunity_Quote_Sent_Checkbox
    START -->  Check_for_different_Status
    END_Check_for_different_Status(( END )):::endClass
    END_Update_related_opportunity_Checkbox(( END )):::endClass
    END_Update_Related_Opportunity_Quote_Sent_Checkbox(( END )):::endClass
    
    
    classDef actionCalls fill:#D4E4FC,color:black,text-decoration:none,max-height:100px
    classDef assignments fill:#FBEED7,color:black,text-decoration:none,max-height:100px
    classDef collectionProcessors fill:#F0E3FA,color:black,text-decoration:none,max-height:100px
    classDef customErrors fill:#FFE9E9,color:black,text-decoration:none,max-height:100px
    classDef decisions fill:#FDEAF6,color:black,text-decoration:none,max-height:100px
    classDef loops fill:#FDEAF6,color:black,text-decoration:none,max-height:100px
    classDef recordCreates fill:#FFF8C9,color:black,text-decoration:none,max-height:100px
    classDef recordDeletes fill:#FFF8C9,color:black,text-decoration:none,max-height:100px
    classDef recordLookups fill:#EDEAFF,color:black,text-decoration:none,max-height:100px
    classDef recordUpdates fill:#FFF8C9,color:black,text-decoration:none,max-height:100px
    classDef screens fill:#DFF6FF,color:black,text-decoration:none,max-height:100px
    classDef subflows fill:#D4E4FC,color:black,text-decoration:none,max-height:100px
    classDef startClass fill:#D9F2E6,color:black,text-decoration:none,max-height:100px
    classDef endClass fill:#F9BABA,color:black,text-decoration:none,max-height:100px
    
    
    ```
    
    <!-- Flow description -->
    
    ## General Information
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Object|Quote|
    |Process Type| Auto Launched Flow|
    |Trigger Type| Record After Save|
    |Record Trigger Type| Create And Update|
    |Label|Update Opportunity based on Quote Status|
    |Status|Active|
    |Description|This flow is used to update Opportunity checkbox based on Quote Status|
    |Environments|Default|
    |Interview Label|Update Opportunity based on Quote Status {!$Flow.CurrentDateTime}|
    | Builder Type (PM)|LightningFlowBuilder|
    | Canvas Mode (PM)|FREE_FORM_CANVAS|
    | Origin Builder Type (PM)|LightningFlowBuilder|
    |Connector|[Check_for_different_Status](#check_for_different_status)|
    |Next Node|[Check_for_different_Status](#check_for_different_status)|
    
    
    #### Filters (logic: **1 AND (2 OR 3)**)
    
    |Filter Id|Field|Operator|Value|
    |:-- |:-- |:--:|:--: |
    |1|OpportunityId| Is Null|<!-- -->|
    |2|Status| Equal To|Quote Sent|
    |3|Status| Equal To|Budgetary Quote Sent|
    
    
    ## Flow Nodes Details
    
    ### Check_for_different_Status
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Decision|
    |Label|Check for different Status|
    |Description|check status = Budgetary Quote Sent or Quote Sent|
    |Default Connector Label|Default Outcome|
    
    
    #### Rule Budgetary_Quote_Sent (Budgetary Quote Sent)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Update_related_opportunity_Checkbox](#update_related_opportunity_checkbox)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |1|$Record.Status| Equal To|Budgetary Quote Sent|
    
    
    
    
    #### Rule Quote_Sent_Check (Quote Sent Check)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Update_Related_Opportunity_Quote_Sent_Checkbox](#update_related_opportunity_quote_sent_checkbox)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |1|$Record.Status| Equal To|Quote Sent|
    
    
    
    
    ### Update_related_opportunity_Checkbox
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Object|Opportunity|
    |Label|Update related opportunity Checkbox|
    
    
    #### Filters (logic: **and**)
    
    |Filter Id|Field|Operator|Value|
    |:-- |:-- |:--:|:--: |
    |1|Id| Equal To|$Record.OpportunityId|
    
    
    
    
    #### Input Assignments
    
    |Field|Value|
    |:-- |:--: |
    |Budget_Quote__c|✅|
    
    
    
    
    ### Update_Related_Opportunity_Quote_Sent_Checkbox
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Object|Opportunity|
    |Label|Update Related Opportunity Quote Sent Checkbox|
    
    
    #### Filters (logic: **and**)
    
    |Filter Id|Field|Operator|Value|
    |:-- |:-- |:--:|:--: |
    |1|Id| Equal To|$Record.OpportunityId|
    
    
    
    
    #### Input Assignments
    
    |Field|Value|
    |:-- |:--: |
    |Quote_Sent_Check__c|✅|
    
    
    
    
    
    
    
    
    ___
    
    _Documentation generated from branch main by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_

