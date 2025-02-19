# Quote_Line_Create_or_Update_After_Save history

<!-- This page has been generated to be viewed with mkdocs-material, you can not view it just as markdown . Activate tab plugin following the doc at https://squidfunk.github.io/mkdocs-material/reference/content-tabs/ -->

=== "Aug 8, 2024"

    _Aug 8, 2024, by Astreva Dev in commit Changed the code for Deployment_

    
    ## Flow Diagram
    
    ```mermaid
    %% If you read this, your Markdown visualizer does not handle MermaidJS syntax.
    %% - If you are in VsCode, install extension `Markdown Preview Mermaid Support` at https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid
    %% - If you are using sfdx-hardis, try to define env variable `MERMAID_MODES=cli,docker` ,then run again the command to regenerate markdown with SVG images.
    %% - If you are within mkdocs-material, define mermaid plugin in `mkdocs.yml` as described in https://squidfunk.github.io/mkdocs-material/extensions/mermaid/
    %% - At last resort, you can copy-paste this MermaidJS code in https://mermaid.live/ to see the Flow Diagram
    
    flowchart TB
    START(["<b>START<br/><b>AutoLaunched Flow</b></br>Type: <b> Record After Save</b></b>"]):::startClassChanged
    
    
    click START "#general-information" "4102135194"
    
    
    Set_Quote_Line_Fields[\"🟰 <em></em><br/>Set Quote Line Fields"/]:::assignments
    click Set_Quote_Line_Fields "#set_quote_line_fields" "4182342871"
    
    Opportunity_Product{"🔀 <em></em><br/>Opportunity Product?"}:::decisions
    click Opportunity_Product "#opportunity_product" "3895732036"
    
    Update_Opportunity_Product[("🛠️ <em></em><br/>Update Opportunity Product")]:::recordUpdates
    click Update_Opportunity_Product "#update_opportunity_product" "4259590008"
    
    Update_Quote_Line_Item[("🛠️ <em></em><br/>Update Quote Line Item")]:::recordUpdates
    click Update_Quote_Line_Item "#update_quote_line_item" "58141146"
    
    Set_Quote_Line_Fields --> Update_Quote_Line_Item
    Opportunity_Product --> |"Yes"| Update_Opportunity_Product
    Opportunity_Product --> |"No"| END_Opportunity_Product
    Update_Opportunity_Product --> END_Update_Opportunity_Product
    Update_Quote_Line_Item --> Opportunity_Product
    START -->  Set_Quote_Line_Fields
    END_Opportunity_Product(( END )):::endClass
    END_Update_Opportunity_Product(( END )):::endClass
    
    
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
    
    
    
    classDef actionCallsAdded fill:green,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef assignmentsAdded fill:green,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef collectionProcessorsAdded fill:green,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef customErrorsAdded fill:green,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef decisionsAdded fill:green,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef loopsAdded fill:green,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef recordCreatesAdded fill:green,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef recordDeletesAdded fill:green,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef recordLookupsAdded fill:green,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef recordUpdatesAdded fill:green,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef screensAdded fill:green,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef subflowsAdded fill:green,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef startClassAdded fill:green,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    
    classDef actionCallsRemoved fill:red,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef assignmentsRemoved fill:red,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef collectionProcessorsRemoved fill:red,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef customErrorsRemoved fill:red,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef decisionsRemoved fill:red,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef loopsRemoved fill:red,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef recordCreatesRemoved fill:red,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef recordDeletesRemoved fill:red,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef recordLookupsRemoved fill:red,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef recordUpdatesRemoved fill:red,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef screensRemoved fill:red,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef subflowsRemoved fill:red,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef startClassRemoved fill:red,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    
    classDef actionCallsChanged fill:orange,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef assignmentsChanged fill:orange,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef collectionProcessorsChanged fill:orange,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef customErrorsChanged fill:orange,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef decisionsChanged fill:orange,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef loopsChanged fill:orange,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef recordCreatesChanged fill:orange,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef recordDeletesChanged fill:orange,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef recordLookupsChanged fill:orange,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef recordUpdatesChanged fill:orange,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef screensChanged fill:orange,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef subflowsChanged fill:orange,color:white,stroke-width:4px,text-decoration:none,max-height:100px
    classDef startClassChanged fill:orange,color:white,stroke-width:4px,text-decoration:none,max-height:100px
      
    ```
    
    <!-- Flow description -->
    
    ## General Information
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Object|QuoteLineItem|
    |Process Type| Auto Launched Flow|
    |Trigger Type| Record After Save|
    |Record Trigger Type| Create And Update|
    |Label|Quote Line - Create or Update - After Save|
    |Status|Active|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Description</b></span>|<span style="background-color: #a6e22e; color: black;"><b>This flow is updated to adjust the condition so that when Optional__c  prior value is true & updated to false & Discount_Amount__c is equal to Original_List_Price__c then Discount_Amount__c  should be 0</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Environments</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Default</b></span>|
    |Interview Label|Quote Line - Create or Update - After Save {!$Flow.CurrentDateTime}|
    | Builder Type (PM)|LightningFlowBuilder|
    | Canvas Mode (PM)|FREE_FORM_CANVAS|
    | Origin Builder Type (PM)|LightningFlowBuilder|
    |Connector|[Set_Quote_Line_Fields](#set_quote_line_fields)|
    |Next Node|[Set_Quote_Line_Fields](#set_quote_line_fields)|
    
    
    ## Formulas
    
    |Name|Data Type|Expression|Description|
    |:-- |:--:|:-- |:--  |
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>discount</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Number</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>IF({!$Record.Optional__c}, {!$Record.Original_List_Price__c} ,IF(!ISBLANK({!$Record.Discount_Amount__c}) </i></span>|<span style="background-color: #ff7f7f; color: black;"><i> {!$Record.Discount_Amount__c}>0,{!$Record.Discount_Amount__c},0))</i></span>|<span style="background-color: #ff7f7f; color: black;"><i><!-- --></i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>discount</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Number</b></span>|<span style="background-color: #a6e22e; color: black;"><b>IF(<br/>    {!$Record.Optional__c}, <br/>    {!$Record.Original_List_Price__c}, <br/>    IF(<br/>        AND(<br/>            PRIORVALUE({!$Record.Optional__c}),<br/>            {!$Record.Discount_Amount__c} = {!$Record.Original_List_Price__c}<br/>        ), <br/>        0, <br/>        IF(<br/>            !ISBLANK({!$Record.Discount_Amount__c}) </b></span>|<span style="background-color: #a6e22e; color: black;"><b> {!$Record.Discount_Amount__c} > 0, <br/>            {!$Record.Discount_Amount__c}, <br/>            0<br/>        )<br/>    )<br/>)</b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |unitPrice|Currency|{!$Record.Original_List_Price__c} - {!discount}|<!-- -->|
    
    
    ___
    
    _Documentation generated from branch main by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_

=== "Jan 17, 2024 (Initial)"

    _Jan 17, 2024, by Astreva Dev in commit Taken Backup of Changes Pushed to UAT_

    
    ## Flow Diagram [(_View History_)](Quote_Line_Create_or_Update_After_Save-history.md)
    
    ```mermaid
    %% If you read this, your Markdown visualizer does not handle MermaidJS syntax.
    %% - If you are in VsCode, install extension `Markdown Preview Mermaid Support` at https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid
    %% - If you are using sfdx-hardis, try to define env variable `MERMAID_MODES=cli,docker` ,then run again the command to regenerate markdown with SVG images.
    %% - If you are within mkdocs-material, define mermaid plugin in `mkdocs.yml` as described in https://squidfunk.github.io/mkdocs-material/extensions/mermaid/
    %% - At last resort, you can copy-paste this MermaidJS code in https://mermaid.live/ to see the Flow Diagram
    
    flowchart TB
    START(["START<br/><b>AutoLaunched Flow</b></br>Type: <b> Record After Save</b>"]):::startClass
    click START "#general-information" "1630024433"
    
    Set_Quote_Line_Fields[\"🟰 <em></em><br/>Set Quote Line Fields"/]:::assignments
    click Set_Quote_Line_Fields "#set_quote_line_fields" "4182342871"
    
    Opportunity_Product{"🔀 <em></em><br/>Opportunity Product?"}:::decisions
    click Opportunity_Product "#opportunity_product" "3895732036"
    
    Update_Opportunity_Product[("🛠️ <em></em><br/>Update Opportunity Product")]:::recordUpdates
    click Update_Opportunity_Product "#update_opportunity_product" "4259590008"
    
    Update_Quote_Line_Item[("🛠️ <em></em><br/>Update Quote Line Item")]:::recordUpdates
    click Update_Quote_Line_Item "#update_quote_line_item" "58141146"
    
    Set_Quote_Line_Fields --> Update_Quote_Line_Item
    Opportunity_Product --> |"Yes"| Update_Opportunity_Product
    Opportunity_Product --> |"No"| END_Opportunity_Product
    Update_Opportunity_Product --> END_Update_Opportunity_Product
    Update_Quote_Line_Item --> Opportunity_Product
    START -->  Set_Quote_Line_Fields
    END_Opportunity_Product(( END )):::endClass
    END_Update_Opportunity_Product(( END )):::endClass
    
    
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
    |Object|QuoteLineItem|
    |Process Type| Auto Launched Flow|
    |Trigger Type| Record After Save|
    |Record Trigger Type| Create And Update|
    |Label|Quote Line - Create or Update - After Save|
    |Status|Active|
    |Interview Label|Quote Line - Create or Update - After Save {!$Flow.CurrentDateTime}|
    | Builder Type (PM)|LightningFlowBuilder|
    | Canvas Mode (PM)|FREE_FORM_CANVAS|
    | Origin Builder Type (PM)|LightningFlowBuilder|
    |Connector|[Set_Quote_Line_Fields](#set_quote_line_fields)|
    |Next Node|[Set_Quote_Line_Fields](#set_quote_line_fields)|
    
    
    ## Formulas
    
    |Name|Data Type|Expression|Description|
    |:-- |:--:|:-- |:--  |
    |discount|Number|IF({!$Record.Optional__c}, {!$Record.Original_List_Price__c} ,IF(!ISBLANK({!$Record.Discount_Amount__c}) || {!$Record.Discount_Amount__c}>0,{!$Record.Discount_Amount__c},0))|<!-- -->|
    |unitPrice|Currency|{!$Record.Original_List_Price__c} - {!discount}|<!-- -->|
    
    
    ## Flow Nodes Details
    
    ### Set_Quote_Line_Fields
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Assignment|
    |Label|Set Quote Line Fields|
    |Connector|[Update_Quote_Line_Item](#update_quote_line_item)|
    
    
    #### Assignments
    
    |Assign To Reference|Operator|Value|
    |:-- |:--:|:--: |
    |$Record.Discount_Amount__c| Assign|discount|
    |$Record.UnitPrice| Assign|unitPrice|
    
    
    
    
    ### Opportunity_Product
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Decision|
    |Label|Opportunity Product?|
    |Default Connector Label|No|
    
    
    #### Rule Yes (Yes)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Update_Opportunity_Product](#update_opportunity_product)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |1|$Record.OpportunityLineItemId| Is Null|⬜|
    
    
    
    
    ### Update_Opportunity_Product
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Object|OpportunityLineItem|
    |Label|Update Opportunity Product|
    
    
    #### Filters (logic: **and**)
    
    |Filter Id|Field|Operator|Value|
    |:-- |:-- |:--:|:--: |
    |1|Id| Equal To|$Record.OpportunityLineItemId|
    
    
    
    
    #### Input Assignments
    
    |Field|Value|
    |:-- |:--: |
    |Optional__c|$Record.Optional__c|
    
    
    
    
    ### Update_Quote_Line_Item
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Label|Update Quote Line Item|
    |Input Reference|$Record|
    |Connector|[Opportunity_Product](#opportunity_product)|
    
    
    
    
    
    
    ___
    
    _Documentation generated from branch main by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_

