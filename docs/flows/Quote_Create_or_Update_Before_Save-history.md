# Quote_Create_or_Update_Before_Save history

<!-- This page has been generated to be viewed with mkdocs-material, you can not view it just as markdown . Activate tab plugin following the doc at https://squidfunk.github.io/mkdocs-material/reference/content-tabs/ -->

=== "Jan 17, 2024 (Initial)"

    _Jan 17, 2024, by Astreva Dev in commit Taken Backup of Changes Pushed to UAT_

    
    ## Flow Diagram [(_View History_)](Quote_Create_or_Update_Before_Save-history.md)
    
    ```mermaid
    %% If you read this, your Markdown visualizer does not handle MermaidJS syntax.
    %% - If you are in VsCode, install extension `Markdown Preview Mermaid Support` at https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid
    %% - If you are using sfdx-hardis, try to define env variable `MERMAID_MODES=cli,docker` ,then run again the command to regenerate markdown with SVG images.
    %% - If you are within mkdocs-material, define mermaid plugin in `mkdocs.yml` as described in https://squidfunk.github.io/mkdocs-material/extensions/mermaid/
    %% - At last resort, you can copy-paste this MermaidJS code in https://mermaid.live/ to see the Flow Diagram
    
    flowchart TB
    START(["START<br/><b>AutoLaunched Flow</b></br>Type: <b> Record Before Save</b>"]):::startClass
    click START "#general-information" "3976593862"
    
    Assign_Values[\"🟰 <em></em><br/>Assign Values"/]:::assignments
    click Assign_Values "#assign_values" "268277274"
    
    Assign_Values --> END_Assign_Values
    START -->  Assign_Values
    END_Assign_Values(( END )):::endClass
    
    
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
    |Trigger Type| Record Before Save|
    |Record Trigger Type| Create And Update|
    |Label|Quote - Create or Update - Before Save|
    |Status|Active|
    |Interview Label|Quote - Create or Update - Before Save {!$Flow.CurrentDateTime}|
    | Builder Type (PM)|LightningFlowBuilder|
    | Canvas Mode (PM)|AUTO_LAYOUT_CANVAS|
    | Origin Builder Type (PM)|LightningFlowBuilder|
    |Connector|[Assign_Values](#assign_values)|
    |Next Node|[Assign_Values](#assign_values)|
    
    
    ## Formulas
    
    |Name|Data Type|Expression|Description|
    |:-- |:--:|:-- |:--  |
    |shipping|Number|IF(ISBLANK({!$Record.ShippingHandling}) || TEXT({!$Record.ShippingHandling}) = "",0,{!$Record.ShippingHandling})|<!-- -->|
    |tax|Number|IF(ISBLANK({!$Record.Tax}) || TEXT({!$Record.Tax}) = "",0,{!$Record.Tax})|<!-- -->|
    
    
    ## Flow Nodes Details
    
    ### Assign_Values
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Assignment|
    |Label|Assign Values|
    
    
    #### Assignments
    
    |Assign To Reference|Operator|Value|
    |:-- |:--:|:--: |
    |$Record.Tax| Assign|tax|
    |$Record.ShippingHandling| Assign|shipping|
    
    
    
    
    
    
    
    
    ___
    
    _Documentation generated from branch main by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_

