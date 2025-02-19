# Product_Update_Flow history

<!-- This page has been generated to be viewed with mkdocs-material, you can not view it just as markdown . Activate tab plugin following the doc at https://squidfunk.github.io/mkdocs-material/reference/content-tabs/ -->

=== "Feb 19, 2025"

    _Feb 19, 2025, by Astreva Dev in commit Update documentation to hide paths in various Apex classes and enhance test coverage for ReportFinderUtil, GetVFOriginTest, QuoteTriggerTest, TestTermBothTrigger, Utilities_Test, and ProductWavelengthUpdaterTest classes_

    
    ## Flow Diagram
    
    ```mermaid
    %% If you read this, your Markdown visualizer does not handle MermaidJS syntax.
    %% - If you are in VsCode, install extension `Markdown Preview Mermaid Support` at https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid
    %% - If you are using sfdx-hardis, try to define env variable `MERMAID_MODES=cli,docker` ,then run again the command to regenerate markdown with SVG images.
    %% - If you are within mkdocs-material, define mermaid plugin in `mkdocs.yml` as described in https://squidfunk.github.io/mkdocs-material/extensions/mermaid/
    %% - At last resort, you can copy-paste this MermaidJS code in https://mermaid.live/ to see the Flow Diagram
    
    flowchart TB
    START(["<b>START<br/><b>AutoLaunched Flow</b></br>Type: <b> Record After Save</b></b>"]):::startClassChanged
    
    
    click START "#general-information" "3147909353"
    
    
    Add_QuoteId_to_the_Quoteidlist[\"🟰 <em></em><br/>Add QuoteId to the Quoteidlist"/]:::assignments
    click Add_QuoteId_to_the_Quoteidlist "#add_quoteid_to_the_quoteidlist" "1866064868"
    
    Error_in_Retrieving_Qli("🚫 <em></em><br/>Error in Retrieving Qli"):::customErrors
    click Error_in_Retrieving_Qli "#error_in_retrieving_qli" "337066739"
    
    
    Error_in_Updating_Flow("<b>🚫 <em></em><br/>Error in Updating Flow</b>"):::customErrorsAdded
    click Error_in_Updating_Flow "#error_in_updating_flow" "3669331069"
    
    Error_while_updating_Quote("<b>🚫 <em></em><br/>Error while updating Quote</b>"):::customErrorsAdded
    click Error_while_updating_Quote "#error_while_updating_quote" "2327222034"
    
    
    Iterate_over_Qli{{"🔁 <em></em><br/>Iterate over Qli"}}:::loops
    click Iterate_over_Qli "#iterate_over_qli" "3860701936"
    
    Get_Qli[("<b>🔍 <em></em><br/>Get Qli</b>")]:::recordLookupsChanged
    
    
    click Get_Qli "#get_qli" "3536360511"
    
    
    Update_QLIs[("<b>🛠️ <em></em><br/>Update QLIs</b>")]:::recordUpdatesChanged
    
    
    click Update_QLIs "#update_qlis" "1564738783"
    
    
    
    Update_Quote[("<b>🛠️ <em></em><br/>Update Quote</b>")]:::recordUpdatesAdded
    click Update_Quote "#update_quote" "2470212501"
    
    
    Add_QuoteId_to_the_Quoteidlist --> Iterate_over_Qli
    Error_in_Retrieving_Qli --> END_Error_in_Retrieving_Qli
    
    Error_in_Updating_Flow ==> END_Error_in_Updating_Flow
    Error_while_updating_Quote ==> END_Error_while_updating_Quote
    
    Iterate_over_Qli --> |"For Each"|Add_QuoteId_to_the_Quoteidlist
    Iterate_over_Qli ---> |"After Last"|Update_QLIs
    Get_Qli --> Iterate_over_Qli
    Get_Qli -. Fault .->Error_in_Retrieving_Qli
    
    Update_QLIs -.-> END_Update_QLIs
    
    Update_QLIs ==> Update_Quote
    Update_QLIs -. 🟩Fault .->Error_in_Updating_Flow
    Update_Quote ==> END_Update_Quote
    Update_Quote -. 🟩Fault .->Error_while_updating_Quote
    
    START -->  Get_Qli
    END_Error_in_Retrieving_Qli(( END )):::endClass
    
    END_Update_QLIs(( END )):::endClassRemoved
    
    END_Error_in_Updating_Flow(( END )):::endClassAdded
    END_Error_while_updating_Quote(( END )):::endClassAdded
    END_Update_Quote(( END )):::endClassAdded
    
    
    
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
      
    linkStyle 2,3,9,10,11,12 stroke:#00ff00,stroke-width:4px,color:green;
    linkStyle 8 stroke:#ff0000,stroke-width:4px,color:red;
    ```
    
    <!-- Flow description -->
    
    ## General Information
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Object|Product2|
    |Process Type| Auto Launched Flow|
    |Trigger Type| Record After Save|
    |Record Trigger Type| Update|
    |Label|Product Update Flow|
    |Status|Active|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Description</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Added Fault Path & Detailed Description in Each Node</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Description</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Added Update Quote fields Specs Updated & status . Also added fault path for all the dml , filter Quote status as Invalid</b></span>|
    |Environments|Default|
    |Interview Label|Product Update Flow {!$Flow.CurrentDateTime}|
    | Builder Type (PM)|LightningFlowBuilder|
    | Canvas Mode (PM)|AUTO_LAYOUT_CANVAS|
    | Origin Builder Type (PM)|LightningFlowBuilder|
    |Connector|[Get_Qli](#get_qli)|
    |Next Node|[Get_Qli](#get_qli)|
    
    
    ## Variables
    
    |Name|Data Type|Is Collection|Is Input|Is Output|Object Type|Description|
    |:-- |:--:|:--:|:--:|:--:|:--:|:--  |
    |Invalid|Boolean|⬜|⬜|⬜|<!-- -->|<!-- -->|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>QLIList</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>SObject</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>QuoteLineItem</i></span>|<span style="background-color: #ff7f7f; color: black;"><i><!-- --></i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>QLIList</b></span>|<span style="background-color: #a6e22e; color: black;"><b>SObject</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|<span style="background-color: #a6e22e; color: black;"><b>QuoteLineItem</b></span>|<span style="background-color: #a6e22e; color: black;"><b>This is collection variable which holds all the QLI records for further dml operation</b></span>|
    |Quoteidlist|String|✅|✅|✅|<!-- -->|This contains all the  ids of the Quotes whose QLI  are related to the triggering Product Record|
    |QuoteLine|SObject|⬜|⬜|⬜|QuoteLineItem|<!-- -->|
    
    
    ## Flow Nodes Details
    
    ### 🟩Error_in_Updating_Flow
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Type</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Custom Error</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Error in Updating Flow</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Custom Error Messages</b></span>|<span style="background-color: #a6e22e; color: black;"><b>errorMessage: '{!$Flow.FaultMessage}'<br/>isFieldError: false<br/></b></span>|
    
    
    ### 🟩Error_while_updating_Quote
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Type</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Custom Error</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Error while updating Quote</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Custom Error Messages</b></span>|<span style="background-color: #a6e22e; color: black;"><b>errorMessage: '{!$Flow.FaultMessage}'<br/>isFieldError: false<br/></b></span>|
    
    
    
    ### Get_Qli
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Lookup|
    |Object|QuoteLineItem|
    |Label|Get Qli|
    |Description|In this We are fetching all the Qli related to the Triggering records which will be used for Subsequent operations|
    |Assign Null Values If No Records Found|⬜|
    |Fault Connector|[Error_in_Retrieving_Qli](#error_in_retrieving_qli)|
    |Get First Record Only|⬜|
    |Sort Field|QuoteId|
    |Sort Order|Asc|
    |Store Output Automatically|✅|
    |Connector|[Iterate_over_Qli](#iterate_over_qli)|
    
    
    #### Filters (logic: **and**)
    
    |Filter Id|Field|Operator|Value|
    |:-- |:-- |:--:|:--: |
    |1|Product2Id| Equal To|$Record.Id|
    |2|Quote_Status__c| Not Equal To|Quote Approved|
    |3|Quote_Status__c| Not Equal To|Purchasing|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>4</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Quote_Status__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Not Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Invalid</b></span>|
    
    
    
    
    
    ### Update_QLIs
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Label|Update QLIs|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Description</b></span>|<span style="background-color: #a6e22e; color: black;"><b>In this we are updating Invalid checkbox on the QLI who are related to the triggering Product record as true</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Fault Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Error_in_Updating_Flow](#error_in_updating_flow)</b></span>|
    |Input Reference|QLIList|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Update_Quote](#update_quote)</b></span>|
    
    
    
    
    ### 🟩Update_Quote
    
    
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Type</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Record Update</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Object</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Quote</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Update Quote</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Description</b></span>|<span style="background-color: #a6e22e; color: black;"><b>In this we are updating specs updated checkbox to true & the status as Invalid on the Quote</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Fault Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Error_while_updating_Quote](#error_while_updating_quote)</b></span>|
    
    
    
    
    #### 🟩Filters (logic: **and**)
    
    
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Filter Id</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Field</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Operator</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Value</b></span>|
    |:-- |:-- |:--:|:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Id</b></span>|<span style="background-color: #a6e22e; color: black;"><b> In</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Quoteidlist</b></span>|
    
    
    
    
    #### 🟩Input Assignments
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Field</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Value</b></span>|
    |:-- |:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Status</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Invalid</b></span>|
    
    
    
    
    
    
    
    
    
    ___
    
    _Documentation generated from branch main by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_

=== "Feb 18, 2025"

    _Feb 18, 2025, by Astreva Dev in commit Refactor Product Update Flow to improve quote line handling; update assignment logic, add filters for quote status, and enhance variable definitions for clarity_

    
    ## Flow Diagram
    
    ```mermaid
    %% If you read this, your Markdown visualizer does not handle MermaidJS syntax.
    %% - If you are in VsCode, install extension `Markdown Preview Mermaid Support` at https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid
    %% - If you are using sfdx-hardis, try to define env variable `MERMAID_MODES=cli,docker` ,then run again the command to regenerate markdown with SVG images.
    %% - If you are within mkdocs-material, define mermaid plugin in `mkdocs.yml` as described in https://squidfunk.github.io/mkdocs-material/extensions/mermaid/
    %% - At last resort, you can copy-paste this MermaidJS code in https://mermaid.live/ to see the Flow Diagram
    
    flowchart TB
    START(["START<br/><b>AutoLaunched Flow</b></br>Type: <b> Record After Save</b>"]):::startClass
    click START "#general-information" "3606985215"
    
    Add_QuoteId_to_the_Quoteidlist[\"<b>🟰 <em></em><br/>Add QuoteId to the Quoteidlist</b>"/]:::assignmentsChanged
    
    
    click Add_QuoteId_to_the_Quoteidlist "#add_quoteid_to_the_quoteidlist" "1866064868"
    
    
    Error_in_Retrieving_Qli("🚫 <em></em><br/>Error in Retrieving Qli"):::customErrors
    click Error_in_Retrieving_Qli "#error_in_retrieving_qli" "337066739"
    
    
    Error_While_Updating_the_Quotes("<i>🚫 <em></em><br/>Error While Updating the Quotes</i>"):::customErrorsRemoved
    click Error_While_Updating_the_Quotes "#error_while_updating_the_quotes" "25437798"
    
    
    Iterate_over_Qli{{"<b>🔁 <em></em><br/>Iterate over Qli</b>"}}:::loopsChanged
    
    
    click Iterate_over_Qli "#iterate_over_qli" "3860701936"
    
    
    Get_Qli[("<b>🔍 <em></em><br/>Get Qli</b>")]:::recordLookupsChanged
    
    
    click Get_Qli "#get_qli" "848727240"
    
    
    
    Update_Quotes[("<i>🛠️ <em></em><br/>Update Quotes</i>")]:::recordUpdatesRemoved
    click Update_Quotes "#update_quotes" "1352445001"
    
    Update_QLIs[("<b>🛠️ <em></em><br/>Update QLIs</b>")]:::recordUpdatesAdded
    click Update_QLIs "#update_qlis" "318572132"
    
    
    Add_QuoteId_to_the_Quoteidlist --> Iterate_over_Qli
    Error_in_Retrieving_Qli --> END_Error_in_Retrieving_Qli
    
    Error_While_Updating_the_Quotes -.-> END_Error_While_Updating_the_Quotes
    
    Iterate_over_Qli --> |"For Each"|Add_QuoteId_to_the_Quoteidlist
    
    Iterate_over_Qli -.-> |"🟥<i>After Last</i>"|Update_Quotes
    
    Iterate_over_Qli ===> |"🟩<b>After Last</b>"|Update_QLIs
    
    Get_Qli --> Iterate_over_Qli
    Get_Qli -. Fault .->Error_in_Retrieving_Qli
    
    Update_Quotes -.-> END_Update_Quotes
    Update_Quotes -. 🟥Fault .->Error_While_Updating_the_Quotes
    
    Update_QLIs ==> END_Update_QLIs
    
    START -->  Get_Qli
    END_Error_in_Retrieving_Qli(( END )):::endClass
    
    END_Error_While_Updating_the_Quotes(( END )):::endClassRemoved
    END_Update_Quotes(( END )):::endClassRemoved
    
    END_Update_QLIs(( END )):::endClassAdded
    
    
    
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
      
    linkStyle 5,10 stroke:#00ff00,stroke-width:4px,color:green;
    linkStyle 2,4,8,9 stroke:#ff0000,stroke-width:4px,color:red;
    ```
    
    <!-- Flow description -->
    
    ## Variables
    
    |Name|Data Type|Is Collection|Is Input|Is Output|Object Type|Description|
    |:-- |:--:|:--:|:--:|:--:|:--:|:--  |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Invalid</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Boolean</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>QLIList</b></span>|<span style="background-color: #a6e22e; color: black;"><b>SObject</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|<span style="background-color: #a6e22e; color: black;"><b>QuoteLineItem</b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |Quoteidlist|String|✅|✅|✅|<!-- -->|This contains all the  ids of the Quotes whose QLI  are related to the triggering Product Record|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>QuoteLine</b></span>|<span style="background-color: #a6e22e; color: black;"><b>SObject</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|<span style="background-color: #a6e22e; color: black;"><b>QuoteLineItem</b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    
    
    
    ## Flow Nodes Details
    
    ### Add_QuoteId_to_the_Quoteidlist
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Assignment|
    |Label|Add QuoteId to the Quoteidlist|
    |Description|In this We store all the Quote ids in collection variable in order to Update it later|
    |Connector|[Iterate_over_Qli](#iterate_over_qli)|
    
    
    #### Assignments
    
    |Assign To Reference|Operator|Value|
    |:-- |:--:|:--: |
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Quoteidlist</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Add</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Iterate_over_Qli.QuoteId</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>QuoteLine</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Assign</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Iterate_over_Qli](#iterate_over_qli)</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>QuoteLine.Invalid__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Assign</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>QLIList</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Add</b></span>|<span style="background-color: #a6e22e; color: black;"><b>QuoteLine</b></span>|
    
    
    
    
    
    ### 🟥Error_While_Updating_the_Quotes
    
    |🟥<span style="background-color: #ff7f7f; color: black;"><i><!-- --></i></span>|<span style="background-color: #ff7f7f; color: black;"><i><!-- --></i></span>|
    |:---|:---|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Type</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Custom Error</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Label</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Error While Updating the Quotes</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Custom Error Messages</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>errorMessage: '{!$Flow.FaultMessage}'<br/>isFieldError: false<br/></i></span>|
    
    
    
    ### Iterate_over_Qli
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Loop|
    |Label|Iterate over Qli|
    |Description|In this we are Iterating over Qli in order to get the QuoteIDs inside the collection variable for subsequent Update Operation|
    |Collection Reference|[Get_Qli](#get_qli)|
    |Iteration Order|Asc|
    |Next Value Connector|[Add_QuoteId_to_the_Quoteidlist](#add_quoteid_to_the_quoteidlist)|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>No More Values Connector</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>[Update_Quotes](#update_quotes)</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>No More Values Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Update_QLIs](#update_qlis)</b></span>|
    
    
    
    ### Get_Qli
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Lookup|
    |Object|QuoteLineItem|
    |Label|Get Qli|
    |Description|In this We are fetching all the Qli related to the Triggering records which will be used for Subsequent operations|
    |Assign Null Values If No Records Found|⬜|
    |Fault Connector|[Error_in_Retrieving_Qli](#error_in_retrieving_qli)|
    |Get First Record Only|⬜|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Sort Field</b></span>|<span style="background-color: #a6e22e; color: black;"><b>QuoteId</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Sort Order</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Asc</b></span>|
    |Store Output Automatically|✅|
    |Connector|[Iterate_over_Qli](#iterate_over_qli)|
    
    
    #### Filters (logic: **and**)
    
    |Filter Id|Field|Operator|Value|
    |:-- |:-- |:--:|:--: |
    |1|Product2Id| Equal To|$Record.Id|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>2</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Quote_Status__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Not Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Quote Approved</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>3</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Quote_Status__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Not Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Purchasing</b></span>|
    
    
    
    
    
    
    ### 🟥Update_Quotes
    
    ### 🟩Update_QLIs
    
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Object</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Quote</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Label</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Update Quotes</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Description</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Update the flag on Quotes to True in order to invalidate it</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Fault Connector</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>[Error_While_Updating_the_Quotes](#error_while_updating_the_quotes)</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Update QLIs</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Input Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>QLIList</b></span>|
    
    
    
    
    #### 🟥Filters (logic: **and**)
    
    
    
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Filter Id</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Field</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Operator</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Value</i></span>|
    |:-- |:-- |:--:|:--: |
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>1</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Id</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> In</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Quoteidlist</i></span>|
    
    
    
    
    
    
    #### 🟥Input Assignments
    
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Field</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Value</i></span>|
    |:-- |:--: |
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Specs_Updated__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    
    
    
    
    
    
    
    
    
    ___
    
    _Documentation generated from branch main by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_

=== "Feb 4, 2025 (Initial)"

    _Feb 4, 2025, by Astreva Dev in commit Update documentation and flow metadata; enhance links and formatting for clarity_

    
    ## Flow Diagram [(_View History_)](Product_Update_Flow-history.md)
    
    ```mermaid
    %% If you read this, your Markdown visualizer does not handle MermaidJS syntax.
    %% - If you are in VsCode, install extension `Markdown Preview Mermaid Support` at https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid
    %% - If you are using sfdx-hardis, try to define env variable `MERMAID_MODES=cli,docker` ,then run again the command to regenerate markdown with SVG images.
    %% - If you are within mkdocs-material, define mermaid plugin in `mkdocs.yml` as described in https://squidfunk.github.io/mkdocs-material/extensions/mermaid/
    %% - At last resort, you can copy-paste this MermaidJS code in https://mermaid.live/ to see the Flow Diagram
    
    flowchart TB
    START(["START<br/><b>AutoLaunched Flow</b></br>Type: <b> Record After Save</b>"]):::startClass
    click START "#general-information" "3606985215"
    
    Add_QuoteId_to_the_Quoteidlist[\"🟰 <em></em><br/>Add QuoteId to the Quoteidlist"/]:::assignments
    click Add_QuoteId_to_the_Quoteidlist "#add_quoteid_to_the_quoteidlist" "1954194491"
    
    Error_in_Retrieving_Qli("🚫 <em></em><br/>Error in Retrieving Qli"):::customErrors
    click Error_in_Retrieving_Qli "#error_in_retrieving_qli" "337066739"
    
    Error_While_Updating_the_Quotes("🚫 <em></em><br/>Error While Updating the Quotes"):::customErrors
    click Error_While_Updating_the_Quotes "#error_while_updating_the_quotes" "25437798"
    
    Iterate_over_Qli{{"🔁 <em></em><br/>Iterate over Qli"}}:::loops
    click Iterate_over_Qli "#iterate_over_qli" "2787915841"
    
    Get_Qli[("🔍 <em></em><br/>Get Qli")]:::recordLookups
    click Get_Qli "#get_qli" "3877506192"
    
    Update_Quotes[("🛠️ <em></em><br/>Update Quotes")]:::recordUpdates
    click Update_Quotes "#update_quotes" "1352445001"
    
    Add_QuoteId_to_the_Quoteidlist --> Iterate_over_Qli
    Error_in_Retrieving_Qli --> END_Error_in_Retrieving_Qli
    Error_While_Updating_the_Quotes --> END_Error_While_Updating_the_Quotes
    Iterate_over_Qli --> |"For Each"|Add_QuoteId_to_the_Quoteidlist
    Iterate_over_Qli ---> |"After Last"|Update_Quotes
    Get_Qli --> Iterate_over_Qli
    Get_Qli -. Fault .->Error_in_Retrieving_Qli
    Update_Quotes --> END_Update_Quotes
    Update_Quotes -. Fault .->Error_While_Updating_the_Quotes
    START -->  Get_Qli
    END_Error_in_Retrieving_Qli(( END )):::endClass
    END_Error_While_Updating_the_Quotes(( END )):::endClass
    END_Update_Quotes(( END )):::endClass
    
    
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
    |Object|Product2|
    |Process Type| Auto Launched Flow|
    |Trigger Type| Record After Save|
    |Record Trigger Type| Update|
    |Label|Product Update Flow|
    |Status|Active|
    |Description|Added Fault Path & Detailed Description in Each Node|
    |Environments|Default|
    |Interview Label|Product Update Flow {!$Flow.CurrentDateTime}|
    | Builder Type (PM)|LightningFlowBuilder|
    | Canvas Mode (PM)|AUTO_LAYOUT_CANVAS|
    | Origin Builder Type (PM)|LightningFlowBuilder|
    |Connector|[Get_Qli](#get_qli)|
    |Next Node|[Get_Qli](#get_qli)|
    
    
    ## Variables
    
    |Name|Data Type|Is Collection|Is Input|Is Output|Object Type|Description|
    |:-- |:--:|:--:|:--:|:--:|:--:|:--  |
    |Quoteidlist|String|✅|✅|✅|<!-- -->|This contains all the  ids of the Quotes whose QLI  are related to the triggering Product Record|
    
    
    ## Flow Nodes Details
    
    ### Add_QuoteId_to_the_Quoteidlist
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Assignment|
    |Label|Add QuoteId to the Quoteidlist|
    |Description|In this We store all the Quote ids in collection variable in order to Update it later|
    |Connector|[Iterate_over_Qli](#iterate_over_qli)|
    
    
    #### Assignments
    
    |Assign To Reference|Operator|Value|
    |:-- |:--:|:--: |
    |Quoteidlist| Add|Iterate_over_Qli.QuoteId|
    
    
    
    
    ### Error_in_Retrieving_Qli
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Custom Error|
    |Label|Error in Retrieving Qli|
    |Custom Error Messages|errorMessage: '{!$Flow.FaultMessage}'<br/>isFieldError: false<br/>|
    
    
    ### Error_While_Updating_the_Quotes
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Custom Error|
    |Label|Error While Updating the Quotes|
    |Custom Error Messages|errorMessage: '{!$Flow.FaultMessage}'<br/>isFieldError: false<br/>|
    
    
    ### Iterate_over_Qli
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Loop|
    |Label|Iterate over Qli|
    |Description|In this we are Iterating over Qli in order to get the QuoteIDs inside the collection variable for subsequent Update Operation|
    |Collection Reference|[Get_Qli](#get_qli)|
    |Iteration Order|Asc|
    |Next Value Connector|[Add_QuoteId_to_the_Quoteidlist](#add_quoteid_to_the_quoteidlist)|
    |No More Values Connector|[Update_Quotes](#update_quotes)|
    
    
    ### Get_Qli
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Lookup|
    |Object|QuoteLineItem|
    |Label|Get Qli|
    |Description|In this We are fetching all the Qli related to the Triggering records which will be used for Subsequent operations|
    |Assign Null Values If No Records Found|⬜|
    |Fault Connector|[Error_in_Retrieving_Qli](#error_in_retrieving_qli)|
    |Get First Record Only|⬜|
    |Store Output Automatically|✅|
    |Connector|[Iterate_over_Qli](#iterate_over_qli)|
    
    
    #### Filters (logic: **and**)
    
    |Filter Id|Field|Operator|Value|
    |:-- |:-- |:--:|:--: |
    |1|Product2Id| Equal To|$Record.Id|
    
    
    
    
    ### Update_Quotes
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Object|Quote|
    |Label|Update Quotes|
    |Description|Update the flag on Quotes to True in order to invalidate it|
    |Fault Connector|[Error_While_Updating_the_Quotes](#error_while_updating_the_quotes)|
    
    
    #### Filters (logic: **and**)
    
    |Filter Id|Field|Operator|Value|
    |:-- |:-- |:--:|:--: |
    |1|Id| In|Quoteidlist|
    
    
    
    
    #### Input Assignments
    
    |Field|Value|
    |:-- |:--: |
    |Specs_Updated__c|✅|
    
    
    
    
    
    
    
    
    ___
    
    _Documentation generated from branch main by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_

