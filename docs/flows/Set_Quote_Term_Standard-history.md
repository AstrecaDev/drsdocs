# Set_Quote_Term_Standard history

<!-- This page has been generated to be viewed with mkdocs-material, you can not view it just as markdown . Activate tab plugin following the doc at https://squidfunk.github.io/mkdocs-material/reference/content-tabs/ -->

=== "Jan 17, 2024 (Initial)"

    _Jan 17, 2024, by Astreva Dev in commit Taken Backup of Changes Pushed to UAT_

    
    ## Flow Diagram [(_View History_)](Set_Quote_Term_Standard-history.md)
    
    ```mermaid
    %% If you read this, your Markdown visualizer does not handle MermaidJS syntax.
    %% - If you are in VsCode, install extension `Markdown Preview Mermaid Support` at https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid
    %% - If you are using sfdx-hardis, try to define env variable `MERMAID_MODES=cli,docker` ,then run again the command to regenerate markdown with SVG images.
    %% - If you are within mkdocs-material, define mermaid plugin in `mkdocs.yml` as described in https://squidfunk.github.io/mkdocs-material/extensions/mermaid/
    %% - At last resort, you can copy-paste this MermaidJS code in https://mermaid.live/ to see the Flow Diagram
    
    flowchart TB
    START(["START<br/><b>AutoLaunched Flow</b></br>Type: <b> Record After Save</b>"]):::startClass
    click START "#general-information" "3003025343"
    
    Set_Standard[\"🟰 <em></em><br/>Set Standard"/]:::assignments
    click Set_Standard "#set_standard" "2622611227"
    
    Uncheck_Standard[\"🟰 <em></em><br/>Uncheck Standard"/]:::assignments
    click Uncheck_Standard "#uncheck_standard" "3925085773"
    
    Is_Quote_Term_Standard{"🔀 <em></em><br/>Is Quote Term Standard"}:::decisions
    click Is_Quote_Term_Standard "#is_quote_term_standard" "1309259019"
    
    Update_Quote_Term[("🛠️ <em></em><br/>Update Quote Term")]:::recordUpdates
    click Update_Quote_Term "#update_quote_term" "103487514"
    
    Set_Standard --> Update_Quote_Term
    Uncheck_Standard --> Update_Quote_Term
    Is_Quote_Term_Standard --> |"Standard"| Set_Standard
    Is_Quote_Term_Standard --> |"Not Standard"| Uncheck_Standard
    Update_Quote_Term --> END_Update_Quote_Term
    START -->  Is_Quote_Term_Standard
    END_Update_Quote_Term(( END )):::endClass
    
    
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
    |Object|Quote_Term__c|
    |Process Type| Auto Launched Flow|
    |Trigger Type| Record After Save|
    |Record Trigger Type| Create And Update|
    |Label|Set Quote Term Standard|
    |Status|Active|
    |Interview Label|Set Quote Term Standard {!$Flow.CurrentDateTime}|
    | Builder Type (PM)|LightningFlowBuilder|
    | Canvas Mode (PM)|AUTO_LAYOUT_CANVAS|
    | Origin Builder Type (PM)|LightningFlowBuilder|
    |Connector|[Is_Quote_Term_Standard](#is_quote_term_standard)|
    |Next Node|[Is_Quote_Term_Standard](#is_quote_term_standard)|
    
    
    ## Flow Nodes Details
    
    ### Set_Standard
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Assignment|
    |Label|Set Standard|
    |Connector|[Update_Quote_Term](#update_quote_term)|
    
    
    #### Assignments
    
    |Assign To Reference|Operator|Value|
    |:-- |:--:|:--: |
    |$Record.Standard__c| Assign|✅|
    
    
    
    
    ### Uncheck_Standard
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Assignment|
    |Label|Uncheck Standard|
    |Connector|[Update_Quote_Term](#update_quote_term)|
    
    
    #### Assignments
    
    |Assign To Reference|Operator|Value|
    |:-- |:--:|:--: |
    |$Record.Standard__c| Assign|⬜|
    
    
    
    
    ### Is_Quote_Term_Standard
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Decision|
    |Label|Is Quote Term Standard|
    |Default Connector|[Uncheck_Standard](#uncheck_standard)|
    |Default Connector Label|Not Standard|
    
    
    #### Rule Standard (Standard)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Set_Standard](#set_standard)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |1|$Record.Quote_Term__c| Equal To|$Record.Term__r.Term__c|
    
    
    
    
    ### Update_Quote_Term
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Label|Update Quote Term|
    |Input Reference|$Record|
    
    
    
    
    
    
    ___
    
    _Documentation generated from branch main by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_

