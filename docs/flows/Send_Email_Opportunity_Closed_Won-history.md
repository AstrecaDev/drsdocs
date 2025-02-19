# Send_Email_Opportunity_Closed_Won history

<!-- This page has been generated to be viewed with mkdocs-material, you can not view it just as markdown . Activate tab plugin following the doc at https://squidfunk.github.io/mkdocs-material/reference/content-tabs/ -->

=== "Feb 4, 2025 (Initial)"

    _Feb 4, 2025, by Astreva Dev in commit Update documentation and flow metadata; enhance links and formatting for clarity_

    
    ## Flow Diagram [(_View History_)](Send_Email_Opportunity_Closed_Won-history.md)
    
    ```mermaid
    %% If you read this, your Markdown visualizer does not handle MermaidJS syntax.
    %% - If you are in VsCode, install extension `Markdown Preview Mermaid Support` at https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid
    %% - If you are using sfdx-hardis, try to define env variable `MERMAID_MODES=cli,docker` ,then run again the command to regenerate markdown with SVG images.
    %% - If you are within mkdocs-material, define mermaid plugin in `mkdocs.yml` as described in https://squidfunk.github.io/mkdocs-material/extensions/mermaid/
    %% - At last resort, you can copy-paste this MermaidJS code in https://mermaid.live/ to see the Flow Diagram
    
    flowchart TB
    START(["START<br/><b>AutoLaunched Flow</b></br>Type: <b> Record After Save</b>"]):::startClass
    click START "#general-information" "1800984453"
    
    Send_Email_to_Primary_Contact("📧 <em></em><br/>Send Email to Primary Contact"):::actionCalls
    click Send_Email_to_Primary_Contact "#send_email_to_primary_contact" "480228537"
    
    Get_Email_Template[("🔍 <em></em><br/>Get Email Template")]:::recordLookups
    click Get_Email_Template "#get_email_template" "2885240406"
    
    Send_Email_to_Primary_Contact --> END_Send_Email_to_Primary_Contact
    Get_Email_Template --> Send_Email_to_Primary_Contact
    START --> |"Send Email after opp is Won"| Get_Email_Template
    END_Send_Email_to_Primary_Contact(( END )):::endClass
    
    
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
    |Object|Opportunity|
    |Process Type| Auto Launched Flow|
    |Trigger Type| Record After Save|
    |Record Trigger Type| Update|
    |Label|Send Email Opportunity = Closed Won|
    |Status|Active|
    |Does Require Record Changed To Meet Criteria|✅|
    |Description|This flow is used to send an email after 3 weeks to the Primary Contact when the Opportunity is Closed Won + added one min delay for testing|
    |Environments|Default|
    |Interview Label|Send Email Opportunity = Closed Won {!$Flow.CurrentDateTime}|
    | Builder Type (PM)|LightningFlowBuilder|
    | Canvas Mode (PM)|FREE_FORM_CANVAS|
    | Origin Builder Type (PM)|LightningFlowBuilder|
    
    
    #### Scheduled Paths
    
    |Label|Name|Offset Number|Offset Unit|Record Field|Time Source|Connector|
    |:-- |:-- |:-- |:-- |:-- |:-- |:--  |
    |Send Email after opp is Won|Send_Email_after_opp_is_Won|21|Days|<!-- -->|RecordTriggerEvent|[Get_Email_Template](#get_email_template)|
    
    
    #### Filters (logic: **and**)
    
    |Filter Id|Field|Operator|Value|
    |:-- |:-- |:--:|:--: |
    |1|StageName| Equal To|Closed Won|
    |2|Primary_Contact__c| Is Null|<!-- -->|
    
    
    ## Flow Nodes Details
    
    ### Send_Email_to_Primary_Contact
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Action Call|
    |Label|Send Email to Primary Contact|
    |Action Type|Email Simple|
    |Action Name|emailSimple|
    |Flow Transaction Model|CurrentTransaction|
    |Name Segment|emailSimple|
    |Related Record Id (input)|$Record.Id|
    |Recipient Id (input)|$Record.Primary_Contact__r.Id|
    |Log Email On Send (input)|✅|
    |Email Template Id (input)|Get_Email_Template.Id|
    
    
    ### Get_Email_Template
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Lookup|
    |Object|EmailTemplate|
    |Label|Get Email Template|
    |Assign Null Values If No Records Found|⬜|
    |Get First Record Only|✅|
    |Store Output Automatically|✅|
    |Connector|[Send_Email_to_Primary_Contact](#send_email_to_primary_contact)|
    
    
    #### Filters (logic: **and**)
    
    |Filter Id|Field|Operator|Value|
    |:-- |:-- |:--:|:--: |
    |1|DeveloperName| Equal To|Closed_Won_Email_HTML|
    
    
    
    
    
    
    
    
    ___
    
    _Documentation generated from branch main by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_

