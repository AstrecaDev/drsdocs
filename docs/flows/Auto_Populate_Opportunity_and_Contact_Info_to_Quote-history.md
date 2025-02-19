# Auto_Populate_Opportunity_and_Contact_Info_to_Quote history

<!-- This page has been generated to be viewed with mkdocs-material, you can not view it just as markdown . Activate tab plugin following the doc at https://squidfunk.github.io/mkdocs-material/reference/content-tabs/ -->

=== "Feb 4, 2025"

    _Feb 4, 2025, by Astreva Dev in commit Update documentation and flow metadata; enhance links and formatting for clarity_

    
    ## Flow Diagram
    
    ```mermaid
    %% If you read this, your Markdown visualizer does not handle MermaidJS syntax.
    %% - If you are in VsCode, install extension `Markdown Preview Mermaid Support` at https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid
    %% - If you are using sfdx-hardis, try to define env variable `MERMAID_MODES=cli,docker` ,then run again the command to regenerate markdown with SVG images.
    %% - If you are within mkdocs-material, define mermaid plugin in `mkdocs.yml` as described in https://squidfunk.github.io/mkdocs-material/extensions/mermaid/
    %% - At last resort, you can copy-paste this MermaidJS code in https://mermaid.live/ to see the Flow Diagram
    
    flowchart TB
    START(["<b>START<br/><b>AutoLaunched Flow</b></br>Type: <b> Record After Save</b></b>"]):::startClassChanged
    
    
    click START "#general-information" "3351202257"
    
    
    Contact_Role_of_Opportunity{"🔀 <em></em><br/>Contact Role of Opportunity"}:::decisions
    click Contact_Role_of_Opportunity "#contact_role_of_opportunity" "2221579896"
    
    
    Get_Contact_Record_related_to_Opportunity_Contact_Role[("<b>🔍 <em></em><br/>Get Contact Record related to Opportunity Contact Role</b>")]:::recordLookupsAdded
    click Get_Contact_Record_related_to_Opportunity_Contact_Role "#get_contact_record_related_to_opportunity_contact_role" "3768477982"
    
    
    Get_Opportunity_Contact_Role[("<b>🔍 <em></em><br/>Get Opportunity Contact Role</b>")]:::recordLookupsChanged
    
    
    click Get_Opportunity_Contact_Role "#get_opportunity_contact_role" "2187321246"
    
    
    Update_Quote_which_is_triggering[("<b>🛠️ <em></em><br/>Update Quote which is triggering</b>")]:::recordUpdatesChanged
    
    
    click Update_Quote_which_is_triggering "#update_quote_which_is_triggering" "1919738406"
    
    
    Update_Type_Sales[("🛠️ <em></em><br/>Update Type = Sales")]:::recordUpdates
    click Update_Type_Sales "#update_type_sales" "4112617503"
    
    Contact_Role_of_Opportunity --> |"Contact Role is not Blank"| Update_Quote_which_is_triggering
    Contact_Role_of_Opportunity --> |"Default Outcome"| END_Contact_Role_of_Opportunity
    
    Get_Opportunity_Contact_Role -.-> Contact_Role_of_Opportunity
    
    Get_Contact_Record_related_to_Opportunity_Contact_Role ==> Contact_Role_of_Opportunity
    Get_Opportunity_Contact_Role ==> Get_Contact_Record_related_to_Opportunity_Contact_Role
    
    Update_Quote_which_is_triggering --> END_Update_Quote_which_is_triggering
    Update_Type_Sales --> Get_Opportunity_Contact_Role
    START -->  Update_Type_Sales
    END_Contact_Role_of_Opportunity(( END )):::endClass
    END_Update_Quote_which_is_triggering(( END )):::endClass
    
    
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
      
    linkStyle 3,4 stroke:#00ff00,stroke-width:4px,color:green;
    linkStyle 2 stroke:#ff0000,stroke-width:4px,color:red;
    ```
    
    <!-- Flow description -->
    
    ## General Information
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Object|Quote|
    |Process Type| Auto Launched Flow|
    |Trigger Type| Record After Save|
    |Record Trigger Type| Create And Update|
    |Label|Auto Populate Opportunity and Contact Info to Quote|
    |Status|Active|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Description</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>This flow will fire on Quote Creation and Updation ,It will update Contact on quote from Opportunity Contact Role if Role is Decision Maker and Type = Sales</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Description</b></span>|<span style="background-color: #a6e22e; color: black;"><b>This flow will fire on Quote Creation and Updation ,It will update Contact on quote from Opportunity Contact Role if Role is Decision Maker and Type = Sales// Added Email ,Bill & ship to Contact,Phone & Fax on 4th April</b></span>|
    |Environments|Default|
    |Interview Label|Auto Populate Opportunity and Contact Info to Quote {!$Flow.CurrentDateTime}|
    | Builder Type (PM)|LightningFlowBuilder|
    | Canvas Mode (PM)|FREE_FORM_CANVAS|
    | Origin Builder Type (PM)|LightningFlowBuilder|
    |Connector|[Update_Type_Sales](#update_type_sales)|
    |Next Node|[Update_Type_Sales](#update_type_sales)|
    
    
    ## Flow Nodes Details
    
    ### 🟩Get_Contact_Record_related_to_Opportunity_Contact_Role
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Type</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Record Lookup</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Object</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Contact</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Get Contact Record related to Opportunity Contact Role</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Description</b></span>|<span style="background-color: #a6e22e; color: black;"><b>This get element is used to fetch contactID</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Assign Null Values If No Records Found</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Get First Record Only</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Store Output Automatically</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Contact_Role_of_Opportunity](#contact_role_of_opportunity)</b></span>|
    
    
    #### 🟩Filters (logic: **and**)
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Filter Id</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Field</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Operator</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Value</b></span>|
    |:-- |:-- |:--:|:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Id</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Get_Opportunity_Contact_Role.ContactId</b></span>|
    
    
    
    
    
    ### Get_Opportunity_Contact_Role
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Lookup|
    |Object|OpportunityContactRole|
    |Label|Get Opportunity Contact Role|
    |Description|This element is used to get opportunity Contact Role|
    |Assign Null Values If No Records Found|⬜|
    |Get First Record Only|✅|
    |Store Output Automatically|✅|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Connector</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>[Contact_Role_of_Opportunity](#contact_role_of_opportunity)</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Get_Contact_Record_related_to_Opportunity_Contact_Role](#get_contact_record_related_to_opportunity_contact_role)</b></span>|
    
    
    
    ### Update_Quote_which_is_triggering
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Label|Update Quote which is triggering|
    |Description|This|
    |Input Reference|$Record|
    
    
    #### Input Assignments
    
    |Field|Value|
    |:-- |:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Bill_To_Contact__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Get_Contact_Record_related_to_Opportunity_Contact_Role.Name</b></span>|
    |ContactId|Get_Opportunity_Contact_Role.ContactId|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Email</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Get_Contact_Record_related_to_Opportunity_Contact_Role.Email</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Fax</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Get_Contact_Record_related_to_Opportunity_Contact_Role.Fax</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Phone</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Get_Contact_Record_related_to_Opportunity_Contact_Role.Phone</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Ship_To_Contact__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Get_Contact_Record_related_to_Opportunity_Contact_Role.Name</b></span>|
    
    
    
    
    
    ___
    
    _Documentation generated from branch main by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_

=== "Jan 17, 2024 (Initial)"

    _Jan 17, 2024, by Astreva Dev in commit Taken Backup of Changes Pushed to UAT_

    
    ## Flow Diagram [(_View History_)](Auto_Populate_Opportunity_and_Contact_Info_to_Quote-history.md)
    
    ```mermaid
    %% If you read this, your Markdown visualizer does not handle MermaidJS syntax.
    %% - If you are in VsCode, install extension `Markdown Preview Mermaid Support` at https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid
    %% - If you are using sfdx-hardis, try to define env variable `MERMAID_MODES=cli,docker` ,then run again the command to regenerate markdown with SVG images.
    %% - If you are within mkdocs-material, define mermaid plugin in `mkdocs.yml` as described in https://squidfunk.github.io/mkdocs-material/extensions/mermaid/
    %% - At last resort, you can copy-paste this MermaidJS code in https://mermaid.live/ to see the Flow Diagram
    
    flowchart TB
    START(["START<br/><b>AutoLaunched Flow</b></br>Type: <b> Record After Save</b>"]):::startClass
    click START "#general-information" "1665027337"
    
    Contact_Role_of_Opportunity{"🔀 <em></em><br/>Contact Role of Opportunity"}:::decisions
    click Contact_Role_of_Opportunity "#contact_role_of_opportunity" "2221579896"
    
    Get_Opportunity_Contact_Role[("🔍 <em></em><br/>Get Opportunity Contact Role")]:::recordLookups
    click Get_Opportunity_Contact_Role "#get_opportunity_contact_role" "4030563442"
    
    Update_Quote_which_is_triggering[("🛠️ <em></em><br/>Update Quote which is triggering")]:::recordUpdates
    click Update_Quote_which_is_triggering "#update_quote_which_is_triggering" "19104854"
    
    Update_Type_Sales[("🛠️ <em></em><br/>Update Type = Sales")]:::recordUpdates
    click Update_Type_Sales "#update_type_sales" "4112617503"
    
    Contact_Role_of_Opportunity --> |"Contact Role is not Blank"| Update_Quote_which_is_triggering
    Contact_Role_of_Opportunity --> |"Default Outcome"| END_Contact_Role_of_Opportunity
    Get_Opportunity_Contact_Role --> Contact_Role_of_Opportunity
    Update_Quote_which_is_triggering --> END_Update_Quote_which_is_triggering
    Update_Type_Sales --> Get_Opportunity_Contact_Role
    START -->  Update_Type_Sales
    END_Contact_Role_of_Opportunity(( END )):::endClass
    END_Update_Quote_which_is_triggering(( END )):::endClass
    
    
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
    |Label|Auto Populate Opportunity and Contact Info to Quote|
    |Status|Active|
    |Description|This flow will fire on Quote Creation and Updation ,It will update Contact on quote from Opportunity Contact Role if Role is Decision Maker and Type = Sales|
    |Environments|Default|
    |Interview Label|Auto Populate Opportunity and Contact Info to Quote {!$Flow.CurrentDateTime}|
    | Builder Type (PM)|LightningFlowBuilder|
    | Canvas Mode (PM)|FREE_FORM_CANVAS|
    | Origin Builder Type (PM)|LightningFlowBuilder|
    |Connector|[Update_Type_Sales](#update_type_sales)|
    |Next Node|[Update_Type_Sales](#update_type_sales)|
    
    
    #### Filters (logic: **and**)
    
    |Filter Id|Field|Operator|Value|
    |:-- |:-- |:--:|:--: |
    |1|OpportunityId| Is Null|<!-- -->|
    
    
    ## Variables
    
    |Name|Data Type|Is Collection|Is Input|Is Output|Object Type|Description|
    |:-- |:--:|:--:|:--:|:--:|:--:|:--  |
    |OpportunityIdVar|SObject|⬜|⬜|⬜|Opportunity|<!-- -->|
    
    
    ## Flow Nodes Details
    
    ### Contact_Role_of_Opportunity
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Decision|
    |Label|Contact Role of Opportunity|
    |Default Connector Label|Default Outcome|
    
    
    #### Rule Contact_Role_is_not_Blank (Contact Role is not Blank)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Update_Quote_which_is_triggering](#update_quote_which_is_triggering)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |1|Get_Opportunity_Contact_Role.ContactId| Is Null|⬜|
    |2|Get_Opportunity_Contact_Role.Role| Equal To|Decision Maker|
    |3|$Record.ContactId| Is Null|✅|
    
    
    
    
    ### Get_Opportunity_Contact_Role
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Lookup|
    |Object|OpportunityContactRole|
    |Label|Get Opportunity Contact Role|
    |Description|This element is used to get opportunity Contact Role|
    |Assign Null Values If No Records Found|⬜|
    |Get First Record Only|✅|
    |Store Output Automatically|✅|
    |Connector|[Contact_Role_of_Opportunity](#contact_role_of_opportunity)|
    
    
    #### Filters (logic: **and**)
    
    |Filter Id|Field|Operator|Value|
    |:-- |:-- |:--:|:--: |
    |1|OpportunityId| Is Null|<!-- -->|
    |2|OpportunityId| Equal To|$Record.Opportunity.Id|
    |3|Role| Equal To|Decision Maker|
    
    
    
    
    ### Update_Quote_which_is_triggering
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Label|Update Quote which is triggering|
    |Description|This|
    |Input Reference|$Record|
    
    
    #### Input Assignments
    
    |Field|Value|
    |:-- |:--: |
    |ContactId|Get_Opportunity_Contact_Role.ContactId|
    
    
    
    
    ### Update_Type_Sales
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Label|Update Type = Sales|
    |Input Reference|$Record|
    |Connector|[Get_Opportunity_Contact_Role](#get_opportunity_contact_role)|
    
    
    #### Filters (logic: **or**)
    
    |Filter Id|Field|Operator|Value|
    |:-- |:-- |:--:|:--: |
    |1|Type__c| Not Equal To|Sales|
    |2|Type__c| Is Null|<!-- -->|
    
    
    
    
    #### Input Assignments
    
    |Field|Value|
    |:-- |:--: |
    |Type__c|Sales|
    
    
    
    
    
    
    
    
    ___
    
    _Documentation generated from branch main by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_

