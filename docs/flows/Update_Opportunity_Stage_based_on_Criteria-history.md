# Update_Opportunity_Stage_based_on_Criteria history

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
    
    
    click START "#general-information" "3231658401"
    
    
    
    Edit_Custom_Error_Message("<i>🚫 <em></em><br/>Edit Custom Error Message</i>"):::customErrorsRemoved
    click Edit_Custom_Error_Message "#edit_custom_error_message" "1095227459"
    
    Check_Closed_Lost_OR_Qualification_Open{"<b>🔀 <em></em><br/>Check Closed Lost OR Qualification Open</b>"}:::decisionsAdded
    click Check_Closed_Lost_OR_Qualification_Open "#check_closed_lost_or_qualification_open" "145491887"
    
    
    Check_lost_reason_check{"🔀 <em></em><br/>Check lost reason check"}:::decisions
    click Check_lost_reason_check "#check_lost_reason_check" "4211295357"
    
    
    Check_Qualification_Open{"<b>🔀 <em></em><br/>Check Qualification Open</b>"}:::decisionsAdded
    click Check_Qualification_Open "#check_qualification_open" "1025165503"
    
    
    Check_Stages{"<b>🔀 <em></em><br/>Check for Stages</b>"}:::decisionsChanged
    
    
    click Check_Stages "#check_stages" "1781644690"
    
    
    
    Is_record_type_is_Commercial{"<i>🔀 <em></em><br/>Is record type is Commercial</i>"}:::decisionsRemoved
    click Is_record_type_is_Commercial "#is_record_type_is_commercial" "2036744810"
    
    Check_stages_for_OPT_out_stage{"<b>🔀 <em></em><br/>Check stages for OPT out stage</b>"}:::decisionsAdded
    click Check_stages_for_OPT_out_stage "#check_stages_for_opt_out_stage" "2143286211"
    
    
    
    Get_Record_Type[("<i>🔍 <em></em><br/>Get Record Type</i>")]:::recordLookupsRemoved
    click Get_Record_Type "#get_record_type" "2937391985"
    
    Is_Record_Type_is_Commercial{"<b>🔀 <em></em><br/>Is Record Type is Commercial</b>"}:::decisionsAdded
    click Is_Record_Type_is_Commercial "#is_record_type_is_commercial" "2626656005"
    
    
    
    Opt_Out_stage_Check{"<b>🔀 <em></em><br/>Opt Out stage Check</b>"}:::decisionsAdded
    click Opt_Out_stage_Check "#opt_out_stage_check" "1651747938"
    
    Get_Record_Id[("<b>🔍 <em></em><br/>Get Record Id</b>")]:::recordLookupsAdded
    click Get_Record_Id "#get_record_id" "3327078178"
    
    
    Contacted_by_Purchasing[("🛠️ <em></em><br/>Contacted by Purchasing")]:::recordUpdates
    click Contacted_by_Purchasing "#contacted_by_purchasing" "1564523026"
    
    Need_By_Date_Known[("🛠️ <em></em><br/>Need By Date Known")]:::recordUpdates
    click Need_By_Date_Known "#need_by_date_known" "2994484318"
    
    Order_Sent_Quoted_to_Purchasing[("🛠️ <em></em><br/>Order Sent/Quoted to Purchasing")]:::recordUpdates
    click Order_Sent_Quoted_to_Purchasing "#order_sent_quoted_to_purchasing" "4212543125"
    
    Update_Opportunity_Stage_Decision_Maker_Confirmed[("🛠️ <em></em><br/>Update Opportunity Stage Decision Maker Confirmed")]:::recordUpdates
    click Update_Opportunity_Stage_Decision_Maker_Confirmed "#update_opportunity_stage_decision_maker_confirmed" "2990577729"
    
    Update_Product_Fit_Confirm_Confirm[("🛠️ <em></em><br/>Update Product Fit Confirm Confirm")]:::recordUpdates
    click Update_Product_Fit_Confirm_Confirm "#update_product_fit_confirm_confirm" "1902452237"
    
    
    Update_Qualification_Open[("<b>🛠️ <em></em><br/>Update Qualification Open</b>")]:::recordUpdatesAdded
    click Update_Qualification_Open "#update_qualification_open" "105523667"
    
    
    Update_Stage_to_Application_Fit_Confirmed[("<b>🛠️ <em></em><br/>Update Stage to Application Fit Confirmed</b>")]:::recordUpdatesChanged
    click Update_Stage_to_Application_Fit_Confirmed "#update_stage_to_application_fit_confirmed" "3429755109"
    
    
    Update_Stage_to_Application_Fit_Confirmed_OptOut[("<b>🛠️ <em></em><br/>Update Stage to Application Fit Confirmed</b>")]:::recordUpdatesAdded
    click Update_Stage_to_Application_Fit_Confirmed_OptOut "#update_stage_to_application_fit_confirmed_optout" "2140366214"
    
    
    Update_stage_to_Budget_Fit_Confirmed[("🛠️ <em></em><br/>Update stage to Budget Fit Confirmed")]:::recordUpdates
    click Update_stage_to_Budget_Fit_Confirmed "#update_stage_to_budget_fit_confirmed" "1893901757"
    
    Update_stage_to_closed_lost[("🛠️ <em></em><br/>Update stage to closed lost")]:::recordUpdates
    click Update_stage_to_closed_lost "#update_stage_to_closed_lost" "1405627287"
    
    
    Update_Stage_to_Closed_Won[("<b>🛠️ <em></em><br/>Update Stage to Closed Won</b>")]:::recordUpdatesAdded
    click Update_Stage_to_Closed_Won "#update_stage_to_closed_won" "2405043518"
    
    
    Update_Stage_to_Contact_Approval[("<b>🛠️ <em></em><br/>Update Stage to Contact Approval</b>")]:::recordUpdatesChanged
    
    
    click Update_Stage_to_Contact_Approval "#update_stage_to_contact_approval" "95911793"
    
    
    
    Update_stage_to_Contacted_by_Purchasing1[("<b>🛠️ <em></em><br/>Update stage to Contacted by Purchasing</b>")]:::recordUpdatesAdded
    click Update_stage_to_Contacted_by_Purchasing1 "#update_stage_to_contacted_by_purchasing1" "2641641505"
    
    Update_stage_to_Contract_Approval1[("<b>🛠️ <em></em><br/>Update stage to Contract Approval</b>")]:::recordUpdatesAdded
    click Update_stage_to_Contract_Approval1 "#update_stage_to_contract_approval1" "650282925"
    
    
    Update_Stage_to_Funded[("🛠️ <em></em><br/>Update Stage to Funded")]:::recordUpdates
    click Update_Stage_to_Funded "#update_stage_to_funded" "306446618"
    
    
    Edit_Custom_Error_Message -.-> Check_lost_reason_check
    
    Update_Stage_to_funded_in_OPT_stage[("<b>🛠️ <em></em><br/>Update Stage to funded in OPT stage</b>")]:::recordUpdatesAdded
    click Update_Stage_to_funded_in_OPT_stage "#update_stage_to_funded_in_opt_stage" "3139017682"
    
    Update_Stage_to_Need_by_Date_known1[("<b>🛠️ <em></em><br/>Update Stage to Need by Date known</b>")]:::recordUpdatesAdded
    click Update_Stage_to_Need_by_Date_known1 "#update_stage_to_need_by_date_known1" "1358509797"
    
    Update_stage_to_Order_Sent_Quoted_to_Purchasing1[("<b>🛠️ <em></em><br/>Update stage to Order Sent/Quoted to Purchasing</b>")]:::recordUpdatesAdded
    click Update_stage_to_Order_Sent_Quoted_to_Purchasing1 "#update_stage_to_order_sent_quoted_to_purchasing1" "3483833861"
    
    Check_Closed_Lost_OR_Qualification_Open ==> |"🟩<b>Check for closed won checkbox is true</b>"| Update_Stage_to_Closed_Won
    Check_Closed_Lost_OR_Qualification_Open ==> |"🟩<b>Check Lost Reason & Notes(Post Morterm)</b>"| Update_stage_to_closed_lost
    Check_Closed_Lost_OR_Qualification_Open ==> |"🟩<b>Default Outcome</b>"| Update_Qualification_Open
    
    Check_lost_reason_check --> |"Lost Reason not null"| Update_stage_to_closed_lost
    Check_lost_reason_check --> |"Default Outcome"| END_Check_lost_reason_check
    
    Check_Stages -.-> |"🟥<i>Closed Lost Check</i>"| Edit_Custom_Error_Message
    
    Check_Qualification_Open ==> |"🟩<b>Some fields not present</b>"| Check_Closed_Lost_OR_Qualification_Open
    Check_Qualification_Open ==> |"🟩<b>Default</b>"| Opt_Out_stage_Check
    Check_Stages ==> |"🟩<b>Check for closed won is true</b>"| Update_Stage_to_Closed_Won
    Check_Stages ==> |"🟩<b>Closed Lost Check</b>"| Check_lost_reason_check
    Check_Stages ==> |"🟩<b>Closed Won Stage</b>"| Update_Stage_to_Closed_Won
    
    Check_Stages --> |"Contact Approval"| Update_Stage_to_Contact_Approval
    Check_Stages --> |"Contacted by Purchasing Stage"| Contacted_by_Purchasing
    Check_Stages --> |"Order Sent/Quoted to Purchasing Stage"| Order_Sent_Quoted_to_Purchasing
    Check_Stages --> |"Need By Date Known Stage"| Need_By_Date_Known
    Check_Stages --> |"Funded Stage"| Update_Stage_to_Funded
    Check_Stages --> |"Application Fit Confirmed Stage"| Update_Stage_to_Application_Fit_Confirmed
    Check_Stages --> |"Budget Fit Confirmed Stage"| Update_stage_to_Budget_Fit_Confirmed
    Check_Stages --> |"Decision Maker Confirmed Stage"| Update_Opportunity_Stage_Decision_Maker_Confirmed
    Check_Stages --> |"Product Fit Confirmed Stage"| Update_Product_Fit_Confirm_Confirm
    Check_Stages --> |"Default Outcome"| END_Check_Stages
    
    Is_record_type_is_Commercial -.-> |"🟥<i>Commercial</i>"| Check_Stages
    Is_record_type_is_Commercial -.-> |"🟥<i>Defense</i>"| END_Is_record_type_is_Commercial
    Get_Record_Type -.-> Is_record_type_is_Commercial
    
    Check_stages_for_OPT_out_stage ==> |"🟩<b>Budget fit to Application fit</b>"| Update_Stage_to_Application_Fit_Confirmed_OptOut
    Check_stages_for_OPT_out_stage ==> |"🟩<b>Application to Funded</b>"| Update_Stage_to_funded_in_OPT_stage
    Check_stages_for_OPT_out_stage ==> |"🟩<b>Funded to Need by date</b>"| Update_Stage_to_Need_by_Date_known1
    Check_stages_for_OPT_out_stage ==> |"🟩<b>Need by date to Order Sent/Quoted to Purchasing</b>"| Update_stage_to_Order_Sent_Quoted_to_Purchasing1
    Check_stages_for_OPT_out_stage ==> |"🟩<b>Order Sent/Quoted to Purchasing to Contacted by Purchasing</b>"| Update_stage_to_Contacted_by_Purchasing1
    Check_stages_for_OPT_out_stage ==> |"🟩<b>Contacted by Purchasing to Contract Approval</b>"| Update_stage_to_Contract_Approval1
    Check_stages_for_OPT_out_stage ==> |"🟩<b>Default Outcome</b>"| END_Check_stages_for_OPT_out_stage
    Is_Record_Type_is_Commercial ==> |"🟩<b>Record Type is Commercial</b>"| Check_Qualification_Open
    Is_Record_Type_is_Commercial ==> |"🟩<b>Record Type is not Commercial</b>"| END_Is_Record_Type_is_Commercial
    Opt_Out_stage_Check ==> |"🟩<b>Opt stage = false</b>"| Check_Stages
    Opt_Out_stage_Check ==> |"🟩<b>Default Outcome</b>"| Check_stages_for_OPT_out_stage
    Get_Record_Id ==> Is_Record_Type_is_Commercial
    
    Contacted_by_Purchasing --> END_Contacted_by_Purchasing
    Need_By_Date_Known --> END_Need_By_Date_Known
    Order_Sent_Quoted_to_Purchasing --> END_Order_Sent_Quoted_to_Purchasing
    Update_Opportunity_Stage_Decision_Maker_Confirmed --> END_Update_Opportunity_Stage_Decision_Maker_Confirmed
    Update_Product_Fit_Confirm_Confirm --> END_Update_Product_Fit_Confirm_Confirm
    
    Update_Qualification_Open ==> END_Update_Qualification_Open
    
    Update_Stage_to_Application_Fit_Confirmed --> END_Update_Stage_to_Application_Fit_Confirmed
    
    Update_Stage_to_Application_Fit_Confirmed_OptOut ==> END_Update_Stage_to_Application_Fit_Confirmed_OptOut
    
    Update_stage_to_Budget_Fit_Confirmed --> END_Update_stage_to_Budget_Fit_Confirmed
    Update_stage_to_closed_lost --> END_Update_stage_to_closed_lost
    
    Update_Stage_to_Closed_Won ==> END_Update_Stage_to_Closed_Won
    
    Update_Stage_to_Contact_Approval --> END_Update_Stage_to_Contact_Approval
    
    Update_stage_to_Contacted_by_Purchasing1 ==> END_Update_stage_to_Contacted_by_Purchasing1
    Update_stage_to_Contract_Approval1 ==> END_Update_stage_to_Contract_Approval1
    
    Update_Stage_to_Funded --> END_Update_Stage_to_Funded
    
    START -.->  Get_Record_Type
    
    Update_Stage_to_funded_in_OPT_stage ==> END_Update_Stage_to_funded_in_OPT_stage
    Update_Stage_to_Need_by_Date_known1 ==> END_Update_Stage_to_Need_by_Date_known1
    Update_stage_to_Order_Sent_Quoted_to_Purchasing1 ==> END_Update_stage_to_Order_Sent_Quoted_to_Purchasing1
    START ==>  Get_Record_Id
    
    END_Check_lost_reason_check(( END )):::endClass
    END_Check_Stages(( END )):::endClass
    
    END_Is_record_type_is_Commercial(( END )):::endClassRemoved
    
    END_Check_stages_for_OPT_out_stage(( END )):::endClassAdded
    END_Is_Record_Type_is_Commercial(( END )):::endClassAdded
    
    END_Contacted_by_Purchasing(( END )):::endClass
    END_Need_By_Date_Known(( END )):::endClass
    END_Order_Sent_Quoted_to_Purchasing(( END )):::endClass
    END_Update_Opportunity_Stage_Decision_Maker_Confirmed(( END )):::endClass
    END_Update_Product_Fit_Confirm_Confirm(( END )):::endClass
    
    END_Update_Qualification_Open(( END )):::endClassAdded
    
    END_Update_Stage_to_Application_Fit_Confirmed(( END )):::endClass
    
    END_Update_Stage_to_Application_Fit_Confirmed_OptOut(( END )):::endClassAdded
    
    END_Update_stage_to_Budget_Fit_Confirmed(( END )):::endClass
    END_Update_stage_to_closed_lost(( END )):::endClass
    
    END_Update_Stage_to_Closed_Won(( END )):::endClassAdded
    
    END_Update_Stage_to_Contact_Approval(( END )):::endClass
    
    END_Update_stage_to_Contacted_by_Purchasing1(( END )):::endClassAdded
    END_Update_stage_to_Contract_Approval1(( END )):::endClassAdded
    
    END_Update_Stage_to_Funded(( END )):::endClass
    
    END_Update_Stage_to_funded_in_OPT_stage(( END )):::endClassAdded
    END_Update_Stage_to_Need_by_Date_known1(( END )):::endClassAdded
    END_Update_stage_to_Order_Sent_Quoted_to_Purchasing1(( END )):::endClassAdded
    
    
    
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
      
    linkStyle 1,2,3,7,8,9,10,11,25,26,27,28,29,30,31,32,33,34,35,36,42,44,47,49,50,53,54,55,56 stroke:#00ff00,stroke-width:4px,color:green;
    linkStyle 0,6,22,23,24,52 stroke:#ff0000,stroke-width:4px,color:red;
    ```
    
    <!-- Flow description -->
    
    ## General Information
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Object|Opportunity|
    |Process Type| Auto Launched Flow|
    |Trigger Type| Record After Save|
    |Record Trigger Type| Create And Update|
    |Label|Update Opportunity Stage based on Criteria|
    |Status|Active|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Description</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>This flow is checking required fields before update Stage on Opportunity + added closed won check in start</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Description</b></span>|<span style="background-color: #a6e22e; color: black;"><b>This flow is checking required fields before update Stage on Opportunity + Update Closed Lost or Qualification Open + updated 17 May 24 + Added condition for For Closed won checkbox v2</b></span>|
    |Environments|Default|
    |Interview Label|Update Opportunity Stage based on Criteria {!$Flow.CurrentDateTime}|
    | Builder Type (PM)|LightningFlowBuilder|
    | Canvas Mode (PM)|FREE_FORM_CANVAS|
    | Origin Builder Type (PM)|LightningFlowBuilder|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Connector</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>[Get_Record_Type](#get_record_type)</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Next Node</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>[Get_Record_Type](#get_record_type)</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Get_Record_Id](#get_record_id)</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Next Node</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Get_Record_Id](#get_record_id)</b></span>|
    
    
    
    
    #### 🟥Filters (logic: **and**)
    
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Filter Id</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Field</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Operator</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Value</i></span>|
    |:-- |:-- |:--:|:--: |
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>1</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>StageName</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Not Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Closed Won</i></span>|
    
    
    
    ## Flow Nodes Details
    
    
    ### 🟥Edit_Custom_Error_Message
    
    ### 🟩Check_Closed_Lost_OR_Qualification_Open
    
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Type</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Custom Error</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Label</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Edit Custom Error Message</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Description</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Custom Error Message</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Custom Error Messages</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>errorMessage: Please Select<br/>fieldSelection: Lost_Reason__c<br/>isFieldError: true<br/></i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Connector</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>[Check_lost_reason_check](#check_lost_reason_check)</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Type</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Decision</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Check Closed Lost OR Qualification Open</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Default Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Update_Qualification_Open](#update_qualification_open)</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Default Connector Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Default Outcome</b></span>|
    
    
    
    
    #### 🟩Rule Check_for_closed_won_checkbox_is_true (Check for closed won checkbox is true)
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Update_Stage_to_Closed_Won](#update_stage_to_closed_won)</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Logic</b></span>|<span style="background-color: #a6e22e; color: black;"><b>and</b></span>|
    
    
    
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Id</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Left Value Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Operator</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Right Value</b></span>|
    |:-- |:-- |:--:|:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.For_Closed_Won__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    
    
    
    
    #### 🟩Rule Check_Lost_Reason_Notes_Post_Morterm (Check Lost Reason & Notes(Post Morterm))
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Update_stage_to_closed_lost](#update_stage_to_closed_lost)</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Logic</b></span>|<span style="background-color: #a6e22e; color: black;"><b>and</b></span>|
    
    
    
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Id</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Left Value Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Operator</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Right Value</b></span>|
    |:-- |:-- |:--:|:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Lost_Reason__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Is Null</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>2</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Notes_Post_Mortem__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    
    
    
    
    
    ### 🟩Check_Qualification_Open
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Type</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Decision</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Check Qualification Open</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Description</b></span>|<span style="background-color: #a6e22e; color: black;"><b>This is use to set up qualification open stage</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Default Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Opt_Out_stage_Check](#opt_out_stage_check)</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Default Connector Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Default</b></span>|
    
    
    #### 🟩Rule Some_fields_not_present (Some fields not present)
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Check_Closed_Lost_OR_Qualification_Open](#check_closed_lost_or_qualification_open)</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Logic</b></span>|<span style="background-color: #a6e22e; color: black;"><b>or</b></span>|
    
    
    
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Id</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Left Value Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Operator</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Right Value</b></span>|
    |:-- |:-- |:--:|:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Name</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Is Null</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>2</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Account.Name</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Is Null</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>3</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.LOB__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Is Null</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>4</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Market_Segment__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Is Null</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    
    
    
    
    
    ### Check_Stages
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Decision|
    |Label|Check for Stages|
    |Default Connector Label|Default Outcome|
    
    
    
    #### 🟩Rule Check_for_closed_won_is_true (Check for closed won is true)
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Update_Stage_to_Closed_Won](#update_stage_to_closed_won)</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Logic</b></span>|<span style="background-color: #a6e22e; color: black;"><b>and</b></span>|
    
    
    
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Id</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Left Value Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Operator</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Right Value</b></span>|
    |:-- |:-- |:--:|:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.For_Closed_Won__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    
    
    
    
    
    #### Rule Closed_Lost_Check_1 (Closed Lost Check)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Connector</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>[Edit_Custom_Error_Message](#edit_custom_error_message)</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Check_lost_reason_check](#check_lost_reason_check)</b></span>|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |1|$Record.Notes_Post_Mortem__c| Equal To|✅|
    
    
    
    
    
    #### 🟩Rule Closed_Won_Stage (Closed Won Stage)
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Update_Stage_to_Closed_Won](#update_stage_to_closed_won)</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Logic</b></span>|<span style="background-color: #a6e22e; color: black;"><b>and</b></span>|
    
    
    
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Id</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Left Value Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Operator</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Right Value</b></span>|
    |:-- |:-- |:--:|:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Visual_Compliance__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>2</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Notes_Attachments_Add_Visual_Complia__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>3</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Notes_Attachments_Add_EUS__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>4</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Asset__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Is Null</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>5</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Sales_Order__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Is Null</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>6</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Purchase_Order__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Is Null</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>7</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Notes_Attachments_Approved_Contract__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    
    
    
    
    
    #### Rule Contact_Approval (Contact Approval)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Update_Stage_to_Contact_Approval](#update_stage_to_contact_approval)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>1</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.LeadSource</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>2</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Market_Segment__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>3</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.LOB__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>4</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.AccountId</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>5</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Name</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>6</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.HasOpportunityLineItem</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>7</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.TotalOpportunityQuantity</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>8</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Has_Contact_Role_as_DM__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>9</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Has_Notes_Attachment__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>10</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Application__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>11</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Amount</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>12</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Budget_Quote__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>13</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Funding_Date__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>14</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Funding_Source__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>15</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Requested_Ship_date__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>16</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Quote_Sent_Check__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>17</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Contact_Role_EDM__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Contact_Role_EDM__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    
    
    
    
    
    #### Rule Contacted_by_Purchasing_Stage (Contacted by Purchasing Stage)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Contacted_by_Purchasing](#contacted_by_purchasing)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>1</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.LeadSource</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>2</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Market_Segment__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>3</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.LOB__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>4</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.AccountId</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>5</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Name</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>6</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.HasOpportunityLineItem</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>7</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.TotalOpportunityQuantity</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>8</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Has_Contact_Role_as_DM__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>9</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Has_Notes_Attachment__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>10</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Application__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>11</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Amount</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>12</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Budget_Quote__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>13</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Funding_Date__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>14</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Funding_Source__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>15</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Requested_Ship_date__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>16</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Quote_Sent_Check__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Quote_Sent_Check__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    
    
    
    
    
    #### Rule Order_Sent_Quoted_to_Purchasing_Stage (Order Sent/Quoted to Purchasing Stage)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Order_Sent_Quoted_to_Purchasing](#order_sent_quoted_to_purchasing)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>1</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.LeadSource</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>2</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Market_Segment__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>3</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.LOB__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>4</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.AccountId</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>5</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Name</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>6</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.HasOpportunityLineItem</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>7</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.TotalOpportunityQuantity</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>8</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Has_Contact_Role_as_DM__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>9</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Has_Notes_Attachment__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>10</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Application__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>11</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Amount</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>12</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Budget_Quote__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>13</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Funding_Date__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>14</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Funding_Source__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>15</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Requested_Ship_date__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Requested_Ship_date__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Is Null</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|
    
    
    
    
    
    #### Rule Need_By_Date_Known_Stage (Need By Date Known Stage)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Need_By_Date_Known](#need_by_date_known)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>1</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.LeadSource</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>2</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Market_Segment__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>3</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.LOB__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>4</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.AccountId</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>5</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Name</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>6</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.HasOpportunityLineItem</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>7</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.TotalOpportunityQuantity</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>8</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Has_Contact_Role_as_DM__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>9</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Has_Notes_Attachment__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>10</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Application__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>11</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Amount</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>12</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Budget_Quote__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>13</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Funding_Date__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>14</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Funding_Source__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Funding_Date__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Is Null</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>2</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Funding_Source__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Is Null</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|
    
    
    
    
    
    #### Rule Funded_Stage (Funded Stage)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Update_Stage_to_Funded](#update_stage_to_funded)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>1</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.LeadSource</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>2</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Market_Segment__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>3</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.LOB__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>4</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.AccountId</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>5</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Name</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>6</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.HasOpportunityLineItem</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>7</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.TotalOpportunityQuantity</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>8</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Has_Contact_Role_as_DM__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>9</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Has_Notes_Attachment__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>10</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Application__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>11</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Amount</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>12</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Budget_Quote__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Has_Notes_Attachment__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>2</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Application__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Is Null</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|
    
    
    
    
    
    #### Rule Application_Fit_Confirmed_Stage (Application Fit Confirmed Stage)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Update_Stage_to_Application_Fit_Confirmed](#update_stage_to_application_fit_confirmed)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>1</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.LeadSource</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>2</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Market_Segment__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>3</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.LOB__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>4</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.AccountId</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>5</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Name</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>6</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.HasOpportunityLineItem</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>7</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.TotalOpportunityQuantity</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>8</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Has_Contact_Role_as_DM__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>9</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Amount</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>10</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Budget_Quote__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Budget_Quote__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    
    
    
    
    
    #### Rule Budget_Fit_Confirmed_Stage (Budget Fit Confirmed Stage)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Update_stage_to_Budget_Fit_Confirmed](#update_stage_to_budget_fit_confirmed)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>1</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.LeadSource</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>2</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Market_Segment__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>3</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.LOB__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>4</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.AccountId</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>5</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Name</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>6</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.HasOpportunityLineItem</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>7</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.TotalOpportunityQuantity</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>8</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Has_Contact_Role_as_DM__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>✅</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Has_Contact_Role_as_DM__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    
    
    
    
    
    #### Rule Decision_Maker_Confirmed_Stage (Decision Maker Confirmed Stage)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Update_Opportunity_Stage_Decision_Maker_Confirmed](#update_opportunity_stage_decision_maker_confirmed)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |1|$Record.TotalOpportunityQuantity| Is Null|⬜|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>2</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Name</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>3</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.AccountId</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>4</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.LOB__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>5</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.Market_Segment__c</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>6</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.LeadSource</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>2</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.HasOpportunityLineItem</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    
    
    
    
    
    ### 🟥Is_record_type_is_Commercial
    
    ### 🟩Check_stages_for_OPT_out_stage
    
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Decision|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Label</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Is record type is Commercial</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Default Connector Label</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Defense</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Check stages for OPT out stage</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Default Connector Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Default Outcome</b></span>|
    
    
    
    
    #### 🟥Rule Commercial (Commercial)
    
    #### 🟩Rule budget_fit_to_Application_fit (Budget fit to Application fit)
    
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Update_Stage_to_Application_Fit_Confirmed_OptOut](#update_stage_to_application_fit_confirmed_optout)</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Logic</b></span>|<span style="background-color: #a6e22e; color: black;"><b>and</b></span>|
    
    
    
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Id</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Left Value Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Operator</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Right Value</b></span>|
    |:-- |:-- |:--:|:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.StageName</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Budget Fit Confirmed</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>2</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Opt_Out_Stage__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    
    
    
    
    #### 🟩Rule Application_to_Funded (Application to Funded)
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Update_Stage_to_funded_in_OPT_stage](#update_stage_to_funded_in_opt_stage)</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Logic</b></span>|<span style="background-color: #a6e22e; color: black;"><b>and</b></span>|
    
    
    
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Id</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Left Value Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Operator</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Right Value</b></span>|
    |:-- |:-- |:--:|:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.StageName</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Application Fit Confirmed</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>2</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Opt_Out_Stage__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    
    
    
    
    #### 🟩Rule Funded_to_Need_by_date (Funded to Need by date)
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Update_Stage_to_Need_by_Date_known1](#update_stage_to_need_by_date_known1)</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Logic</b></span>|<span style="background-color: #a6e22e; color: black;"><b>and</b></span>|
    
    
    
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Id</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Left Value Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Operator</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Right Value</b></span>|
    |:-- |:-- |:--:|:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.StageName</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Funded</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>2</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Opt_Out_Stage__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    
    
    
    
    #### 🟩Rule Need_by_date_to_Order_Sent_Quoted_to_Purchasing (Need by date to Order Sent/Quoted to Purchasing)
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Update_stage_to_Order_Sent_Quoted_to_Purchasing1](#update_stage_to_order_sent_quoted_to_purchasing1)</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Logic</b></span>|<span style="background-color: #a6e22e; color: black;"><b>and</b></span>|
    
    
    
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Id</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Left Value Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Operator</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Right Value</b></span>|
    |:-- |:-- |:--:|:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.StageName</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Need By Date Known</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>2</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Opt_Out_Stage__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    
    
    
    
    #### 🟩Rule Order_Sent_Quoted_to_Purchasing_to_Contacted_by_Purchasing (Order Sent/Quoted to Purchasing to Contacted by Purchasing)
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Update_stage_to_Contacted_by_Purchasing1](#update_stage_to_contacted_by_purchasing1)</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Logic</b></span>|<span style="background-color: #a6e22e; color: black;"><b>and</b></span>|
    
    
    
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Id</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Left Value Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Operator</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Right Value</b></span>|
    |:-- |:-- |:--:|:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.StageName</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Order Sent/Quoted to Purchasing</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>2</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Opt_Out_Stage__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    
    
    
    
    #### 🟩Rule Contacted_by_Purchasing_to_Contract_Approval (Contacted by Purchasing to Contract Approval)
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Update_stage_to_Contract_Approval1](#update_stage_to_contract_approval1)</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Logic</b></span>|<span style="background-color: #a6e22e; color: black;"><b>and</b></span>|
    
    
    
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Id</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Left Value Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Operator</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Right Value</b></span>|
    |:-- |:-- |:--:|:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.StageName</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Contacted by Purchasing</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>2</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Opt_Out_Stage__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>✅</b></span>|
    
    
    
    
    ### 🟩Is_Record_Type_is_Commercial
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Type</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Decision</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Is Record Type is Commercial</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Default Connector Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Record Type is not Commercial</b></span>|
    
    
    #### 🟩Rule Record_Type_is_Commercial (Record Type is Commercial)
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Check_Qualification_Open](#check_qualification_open)</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Logic</b></span>|<span style="background-color: #a6e22e; color: black;"><b>and</b></span>|
    
    
    
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Condition Id</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Left Value Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Operator</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Right Value</b></span>|
    |:-- |:-- |:--:|:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Get_Record_Id.Id</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Is Null</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>2</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.RecordTypeId</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Get_Record_Id.Id</b></span>|
    
    
    
    
    ### 🟩Opt_Out_stage_Check
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Type</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Decision</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Opt Out stage Check</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Default Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Check_stages_for_OPT_out_stage](#check_stages_for_opt_out_stage)</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Default Connector Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Default Outcome</b></span>|
    
    
    #### 🟩Rule Opt_stage_false (Opt stage = false)
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |Connector|[Check_Stages](#check_stages)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>1</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Get_Record_Type.Id</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Is Null</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>⬜</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>2</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>$Record.RecordTypeId</i></span>|<span style="background-color: #ff7f7f; color: black;"><i> Equal To</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Get_Record_Type.Id</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>1</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record.Opt_Out_Stage__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b> Equal To</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|
    
    
    
    
    
    
    ### 🟥Get_Record_Type
    
    ### 🟩Get_Record_Id
    
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Lookup|
    |Object|RecordType|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Label</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Get Record Type</i></span>|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Description</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Get record types present on Opportunity object</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Get Record Id</b></span>|
    |Assign Null Values If No Records Found|⬜|
    |Get First Record Only|✅|
    |Store Output Automatically|✅|
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>Connector</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>[Is_record_type_is_Commercial](#is_record_type_is_commercial)</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Connector</b></span>|<span style="background-color: #a6e22e; color: black;"><b>[Is_Record_Type_is_Commercial](#is_record_type_is_commercial)</b></span>|
    
    
    
    ### 🟩Update_Qualification_Open
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Type</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Record Update</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Update Qualification Open</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Description</b></span>|<span style="background-color: #a6e22e; color: black;"><b>This is use to update stage as qualification open</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Input Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record</b></span>|
    
    
    #### 🟩Input Assignments
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Field</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Value</b></span>|
    |:-- |:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>StageName</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Qualification (Open)</b></span>|
    
    
    
    
    
    ### 🟩Update_Stage_to_Application_Fit_Confirmed_OptOut
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Type</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Record Update</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Update Stage to Application Fit Confirmed</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Input Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record</b></span>|
    
    
    #### 🟩Input Assignments
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Field</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Value</b></span>|
    |:-- |:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Opt_Out_Stage__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>StageName</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Application Fit Confirmed</b></span>|
    
    
    
    
    
    ### 🟩Update_Stage_to_Closed_Won
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Type</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Record Update</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Update Stage to Closed Won</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Input Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record</b></span>|
    
    
    #### 🟩Input Assignments
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Field</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Value</b></span>|
    |:-- |:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>StageName</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Closed Won</b></span>|
    
    
    
    
    
    ### Update_Stage_to_Contact_Approval
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Label|Update Stage to Contact Approval|
    |Input Reference|$Record|
    
    
    #### Input Assignments
    
    |Field|Value|
    |:-- |:--: |
    |🟥<span style="background-color: #ff7f7f; color: black;"><i>StageName</i></span>|<span style="background-color: #ff7f7f; color: black;"><i>Contact Approval</i></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>StageName</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Contract Approval</b></span>|
    
    
    
    
    
    
    ### 🟩Update_stage_to_Contacted_by_Purchasing1
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Type</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Record Update</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Update stage to Contacted by Purchasing</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Input Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record</b></span>|
    
    
    #### 🟩Input Assignments
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Field</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Value</b></span>|
    |:-- |:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Opt_Out_Stage__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>StageName</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Contacted by Purchasing</b></span>|
    
    
    
    
    ### 🟩Update_stage_to_Contract_Approval1
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Type</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Record Update</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Update stage to Contract Approval</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Input Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record</b></span>|
    
    
    #### 🟩Input Assignments
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Field</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Value</b></span>|
    |:-- |:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Opt_Out_Stage__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>StageName</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Contract Approval</b></span>|
    
    
    
    
    
    ### 🟩Update_Stage_to_funded_in_OPT_stage
    
    
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Type</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Record Update</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Update Stage to funded in OPT stage</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Input Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record</b></span>|
    
    
    
    
    #### 🟩Input Assignments
    
    
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Field</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Value</b></span>|
    |:-- |:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Opt_Out_Stage__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>StageName</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Funded</b></span>|
    
    
    
    
    ### 🟩Update_Stage_to_Need_by_Date_known1
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Type</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Record Update</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Update Stage to Need by Date known</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Input Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record</b></span>|
    
    
    #### 🟩Input Assignments
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Field</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Value</b></span>|
    |:-- |:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Opt_Out_Stage__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>StageName</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Need By Date Known</b></span>|
    
    
    
    
    ### 🟩Update_stage_to_Order_Sent_Quoted_to_Purchasing1
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|<span style="background-color: #a6e22e; color: black;"><b><!-- --></b></span>|
    |:---|:---|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Type</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Record Update</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Label</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Update stage to Order Sent/Quoted to Purchasing</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Input Reference</b></span>|<span style="background-color: #a6e22e; color: black;"><b>$Record</b></span>|
    
    
    #### 🟩Input Assignments
    
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Field</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Value</b></span>|
    |:-- |:--: |
    |🟩<span style="background-color: #a6e22e; color: black;"><b>Opt_Out_Stage__c</b></span>|<span style="background-color: #a6e22e; color: black;"><b>⬜</b></span>|
    |🟩<span style="background-color: #a6e22e; color: black;"><b>StageName</b></span>|<span style="background-color: #a6e22e; color: black;"><b>Order Sent/Quoted to Purchasing</b></span>|
    
    
    
    
    
    
    
    
    
    ___
    
    _Documentation generated from branch main by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_

=== "Jan 17, 2024 (Initial)"

    _Jan 17, 2024, by Astreva Dev in commit Taken Backup of Changes Pushed to UAT_

    
    ## Flow Diagram [(_View History_)](Update_Opportunity_Stage_based_on_Criteria-history.md)
    
    ```mermaid
    %% If you read this, your Markdown visualizer does not handle MermaidJS syntax.
    %% - If you are in VsCode, install extension `Markdown Preview Mermaid Support` at https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid
    %% - If you are using sfdx-hardis, try to define env variable `MERMAID_MODES=cli,docker` ,then run again the command to regenerate markdown with SVG images.
    %% - If you are within mkdocs-material, define mermaid plugin in `mkdocs.yml` as described in https://squidfunk.github.io/mkdocs-material/extensions/mermaid/
    %% - At last resort, you can copy-paste this MermaidJS code in https://mermaid.live/ to see the Flow Diagram
    
    flowchart TB
    START(["START<br/><b>AutoLaunched Flow</b></br>Type: <b> Record After Save</b>"]):::startClass
    click START "#general-information" "2910597281"
    
    Edit_Custom_Error_Message("🚫 <em></em><br/>Edit Custom Error Message"):::customErrors
    click Edit_Custom_Error_Message "#edit_custom_error_message" "1095227459"
    
    Check_lost_reason_check{"🔀 <em></em><br/>Check lost reason check"}:::decisions
    click Check_lost_reason_check "#check_lost_reason_check" "4211295357"
    
    Check_Stages{"🔀 <em></em><br/>Check for Stages"}:::decisions
    click Check_Stages "#check_stages" "1628196555"
    
    Is_record_type_is_Commercial{"🔀 <em></em><br/>Is record type is Commercial"}:::decisions
    click Is_record_type_is_Commercial "#is_record_type_is_commercial" "2036744810"
    
    Get_Record_Type[("🔍 <em></em><br/>Get Record Type")]:::recordLookups
    click Get_Record_Type "#get_record_type" "2937391985"
    
    Contacted_by_Purchasing[("🛠️ <em></em><br/>Contacted by Purchasing")]:::recordUpdates
    click Contacted_by_Purchasing "#contacted_by_purchasing" "1564523026"
    
    Need_By_Date_Known[("🛠️ <em></em><br/>Need By Date Known")]:::recordUpdates
    click Need_By_Date_Known "#need_by_date_known" "2994484318"
    
    Order_Sent_Quoted_to_Purchasing[("🛠️ <em></em><br/>Order Sent/Quoted to Purchasing")]:::recordUpdates
    click Order_Sent_Quoted_to_Purchasing "#order_sent_quoted_to_purchasing" "4212543125"
    
    Update_Opportunity_Stage_Decision_Maker_Confirmed[("🛠️ <em></em><br/>Update Opportunity Stage Decision Maker Confirmed")]:::recordUpdates
    click Update_Opportunity_Stage_Decision_Maker_Confirmed "#update_opportunity_stage_decision_maker_confirmed" "2990577729"
    
    Update_Product_Fit_Confirm_Confirm[("🛠️ <em></em><br/>Update Product Fit Confirm Confirm")]:::recordUpdates
    click Update_Product_Fit_Confirm_Confirm "#update_product_fit_confirm_confirm" "1902452237"
    
    Update_Stage_to_Application_Fit_Confirmed[("🛠️ <em></em><br/>Update Stage to Application Fit Confirmed")]:::recordUpdates
    click Update_Stage_to_Application_Fit_Confirmed "#update_stage_to_application_fit_confirmed" "3429755109"
    
    Update_stage_to_Budget_Fit_Confirmed[("🛠️ <em></em><br/>Update stage to Budget Fit Confirmed")]:::recordUpdates
    click Update_stage_to_Budget_Fit_Confirmed "#update_stage_to_budget_fit_confirmed" "1893901757"
    
    Update_stage_to_closed_lost[("🛠️ <em></em><br/>Update stage to closed lost")]:::recordUpdates
    click Update_stage_to_closed_lost "#update_stage_to_closed_lost" "1405627287"
    
    Update_Stage_to_Contact_Approval[("🛠️ <em></em><br/>Update Stage to Contact Approval")]:::recordUpdates
    click Update_Stage_to_Contact_Approval "#update_stage_to_contact_approval" "2039889160"
    
    Update_Stage_to_Funded[("🛠️ <em></em><br/>Update Stage to Funded")]:::recordUpdates
    click Update_Stage_to_Funded "#update_stage_to_funded" "306446618"
    
    Edit_Custom_Error_Message --> Check_lost_reason_check
    Check_lost_reason_check --> |"Lost Reason not null"| Update_stage_to_closed_lost
    Check_lost_reason_check --> |"Default Outcome"| END_Check_lost_reason_check
    Check_Stages --> |"Closed Lost Check"| Edit_Custom_Error_Message
    Check_Stages --> |"Contact Approval"| Update_Stage_to_Contact_Approval
    Check_Stages --> |"Contacted by Purchasing Stage"| Contacted_by_Purchasing
    Check_Stages --> |"Order Sent/Quoted to Purchasing Stage"| Order_Sent_Quoted_to_Purchasing
    Check_Stages --> |"Need By Date Known Stage"| Need_By_Date_Known
    Check_Stages --> |"Funded Stage"| Update_Stage_to_Funded
    Check_Stages --> |"Application Fit Confirmed Stage"| Update_Stage_to_Application_Fit_Confirmed
    Check_Stages --> |"Budget Fit Confirmed Stage"| Update_stage_to_Budget_Fit_Confirmed
    Check_Stages --> |"Decision Maker Confirmed Stage"| Update_Opportunity_Stage_Decision_Maker_Confirmed
    Check_Stages --> |"Product Fit Confirmed Stage"| Update_Product_Fit_Confirm_Confirm
    Check_Stages --> |"Default Outcome"| END_Check_Stages
    Is_record_type_is_Commercial --> |"Commercial"| Check_Stages
    Is_record_type_is_Commercial --> |"Defense"| END_Is_record_type_is_Commercial
    Get_Record_Type --> Is_record_type_is_Commercial
    Contacted_by_Purchasing --> END_Contacted_by_Purchasing
    Need_By_Date_Known --> END_Need_By_Date_Known
    Order_Sent_Quoted_to_Purchasing --> END_Order_Sent_Quoted_to_Purchasing
    Update_Opportunity_Stage_Decision_Maker_Confirmed --> END_Update_Opportunity_Stage_Decision_Maker_Confirmed
    Update_Product_Fit_Confirm_Confirm --> END_Update_Product_Fit_Confirm_Confirm
    Update_Stage_to_Application_Fit_Confirmed --> END_Update_Stage_to_Application_Fit_Confirmed
    Update_stage_to_Budget_Fit_Confirmed --> END_Update_stage_to_Budget_Fit_Confirmed
    Update_stage_to_closed_lost --> END_Update_stage_to_closed_lost
    Update_Stage_to_Contact_Approval --> END_Update_Stage_to_Contact_Approval
    Update_Stage_to_Funded --> END_Update_Stage_to_Funded
    START -->  Get_Record_Type
    END_Check_lost_reason_check(( END )):::endClass
    END_Check_Stages(( END )):::endClass
    END_Is_record_type_is_Commercial(( END )):::endClass
    END_Contacted_by_Purchasing(( END )):::endClass
    END_Need_By_Date_Known(( END )):::endClass
    END_Order_Sent_Quoted_to_Purchasing(( END )):::endClass
    END_Update_Opportunity_Stage_Decision_Maker_Confirmed(( END )):::endClass
    END_Update_Product_Fit_Confirm_Confirm(( END )):::endClass
    END_Update_Stage_to_Application_Fit_Confirmed(( END )):::endClass
    END_Update_stage_to_Budget_Fit_Confirmed(( END )):::endClass
    END_Update_stage_to_closed_lost(( END )):::endClass
    END_Update_Stage_to_Contact_Approval(( END )):::endClass
    END_Update_Stage_to_Funded(( END )):::endClass
    
    
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
    |Record Trigger Type| Create And Update|
    |Label|Update Opportunity Stage based on Criteria|
    |Status|Active|
    |Description|This flow is checking required fields before update Stage on Opportunity + added closed won check in start|
    |Environments|Default|
    |Interview Label|Update Opportunity Stage based on Criteria {!$Flow.CurrentDateTime}|
    | Builder Type (PM)|LightningFlowBuilder|
    | Canvas Mode (PM)|FREE_FORM_CANVAS|
    | Origin Builder Type (PM)|LightningFlowBuilder|
    |Connector|[Get_Record_Type](#get_record_type)|
    |Next Node|[Get_Record_Type](#get_record_type)|
    
    
    #### Filters (logic: **and**)
    
    |Filter Id|Field|Operator|Value|
    |:-- |:-- |:--:|:--: |
    |1|StageName| Not Equal To|Closed Won|
    
    
    ## Variables
    
    |Name|Data Type|Is Collection|Is Input|Is Output|Object Type|Description|
    |:-- |:--:|:--:|:--:|:--:|:--:|:--  |
    |ProductFitConfirmedCheckVar|Boolean|⬜|✅|✅|<!-- -->|<!-- -->|
    |QualificationCheck|Boolean|⬜|✅|✅|<!-- -->|<!-- -->|
    |recordTypeDeveloperName|String|⬜|✅|✅|<!-- -->|<!-- -->|
    
    
    ## Flow Nodes Details
    
    ### Edit_Custom_Error_Message
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Custom Error|
    |Label|Edit Custom Error Message|
    |Description|Custom Error Message|
    |Custom Error Messages|errorMessage: Please Select<br/>fieldSelection: Lost_Reason__c<br/>isFieldError: true<br/>|
    |Connector|[Check_lost_reason_check](#check_lost_reason_check)|
    
    
    ### Check_lost_reason_check
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Decision|
    |Label|Check lost reason check|
    |Default Connector Label|Default Outcome|
    
    
    #### Rule Lost_Reason_not_null (Lost Reason not null)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Update_stage_to_closed_lost](#update_stage_to_closed_lost)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |1|$Record.Lost_Reason__c| Is Null|⬜|
    
    
    
    
    ### Check_Stages
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Decision|
    |Label|Check for Stages|
    |Default Connector Label|Default Outcome|
    
    
    #### Rule Closed_Lost_Check_1 (Closed Lost Check)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Edit_Custom_Error_Message](#edit_custom_error_message)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |1|$Record.Notes_Post_Mortem__c| Equal To|✅|
    
    
    
    
    #### Rule Contact_Approval (Contact Approval)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Update_Stage_to_Contact_Approval](#update_stage_to_contact_approval)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |1|$Record.LeadSource| Is Null|⬜|
    |2|$Record.Market_Segment__c| Is Null|⬜|
    |3|$Record.LOB__c| Is Null|⬜|
    |4|$Record.AccountId| Is Null|⬜|
    |5|$Record.Name| Is Null|⬜|
    |6|$Record.HasOpportunityLineItem| Equal To|✅|
    |7|$Record.TotalOpportunityQuantity| Is Null|⬜|
    |8|$Record.Has_Contact_Role_as_DM__c| Equal To|✅|
    |9|$Record.Has_Notes_Attachment__c| Equal To|✅|
    |10|$Record.Application__c| Is Null|⬜|
    |11|$Record.Amount| Is Null|⬜|
    |12|$Record.Budget_Quote__c| Equal To|✅|
    |13|$Record.Funding_Date__c| Is Null|⬜|
    |14|$Record.Funding_Source__c| Is Null|⬜|
    |15|$Record.Requested_Ship_date__c| Is Null|⬜|
    |16|$Record.Quote_Sent_Check__c| Equal To|✅|
    |17|$Record.Contact_Role_EDM__c| Equal To|✅|
    
    
    
    
    #### Rule Contacted_by_Purchasing_Stage (Contacted by Purchasing Stage)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Contacted_by_Purchasing](#contacted_by_purchasing)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |1|$Record.LeadSource| Is Null|⬜|
    |2|$Record.Market_Segment__c| Is Null|⬜|
    |3|$Record.LOB__c| Is Null|⬜|
    |4|$Record.AccountId| Is Null|⬜|
    |5|$Record.Name| Is Null|⬜|
    |6|$Record.HasOpportunityLineItem| Equal To|✅|
    |7|$Record.TotalOpportunityQuantity| Is Null|⬜|
    |8|$Record.Has_Contact_Role_as_DM__c| Equal To|✅|
    |9|$Record.Has_Notes_Attachment__c| Equal To|✅|
    |10|$Record.Application__c| Is Null|⬜|
    |11|$Record.Amount| Is Null|⬜|
    |12|$Record.Budget_Quote__c| Equal To|✅|
    |13|$Record.Funding_Date__c| Is Null|⬜|
    |14|$Record.Funding_Source__c| Is Null|⬜|
    |15|$Record.Requested_Ship_date__c| Is Null|⬜|
    |16|$Record.Quote_Sent_Check__c| Equal To|✅|
    
    
    
    
    #### Rule Order_Sent_Quoted_to_Purchasing_Stage (Order Sent/Quoted to Purchasing Stage)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Order_Sent_Quoted_to_Purchasing](#order_sent_quoted_to_purchasing)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |1|$Record.LeadSource| Is Null|⬜|
    |2|$Record.Market_Segment__c| Is Null|⬜|
    |3|$Record.LOB__c| Is Null|⬜|
    |4|$Record.AccountId| Is Null|⬜|
    |5|$Record.Name| Is Null|⬜|
    |6|$Record.HasOpportunityLineItem| Equal To|✅|
    |7|$Record.TotalOpportunityQuantity| Is Null|⬜|
    |8|$Record.Has_Contact_Role_as_DM__c| Equal To|✅|
    |9|$Record.Has_Notes_Attachment__c| Equal To|✅|
    |10|$Record.Application__c| Is Null|⬜|
    |11|$Record.Amount| Is Null|⬜|
    |12|$Record.Budget_Quote__c| Equal To|✅|
    |13|$Record.Funding_Date__c| Is Null|⬜|
    |14|$Record.Funding_Source__c| Is Null|⬜|
    |15|$Record.Requested_Ship_date__c| Is Null|⬜|
    
    
    
    
    #### Rule Need_By_Date_Known_Stage (Need By Date Known Stage)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Need_By_Date_Known](#need_by_date_known)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |1|$Record.LeadSource| Is Null|⬜|
    |2|$Record.Market_Segment__c| Is Null|⬜|
    |3|$Record.LOB__c| Is Null|⬜|
    |4|$Record.AccountId| Is Null|⬜|
    |5|$Record.Name| Is Null|⬜|
    |6|$Record.HasOpportunityLineItem| Equal To|✅|
    |7|$Record.TotalOpportunityQuantity| Is Null|⬜|
    |8|$Record.Has_Contact_Role_as_DM__c| Equal To|✅|
    |9|$Record.Has_Notes_Attachment__c| Equal To|✅|
    |10|$Record.Application__c| Is Null|⬜|
    |11|$Record.Amount| Is Null|⬜|
    |12|$Record.Budget_Quote__c| Equal To|✅|
    |13|$Record.Funding_Date__c| Is Null|⬜|
    |14|$Record.Funding_Source__c| Is Null|⬜|
    
    
    
    
    #### Rule Funded_Stage (Funded Stage)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Update_Stage_to_Funded](#update_stage_to_funded)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |1|$Record.LeadSource| Is Null|⬜|
    |2|$Record.Market_Segment__c| Is Null|⬜|
    |3|$Record.LOB__c| Is Null|⬜|
    |4|$Record.AccountId| Is Null|⬜|
    |5|$Record.Name| Is Null|⬜|
    |6|$Record.HasOpportunityLineItem| Equal To|✅|
    |7|$Record.TotalOpportunityQuantity| Is Null|⬜|
    |8|$Record.Has_Contact_Role_as_DM__c| Equal To|✅|
    |9|$Record.Has_Notes_Attachment__c| Equal To|✅|
    |10|$Record.Application__c| Is Null|⬜|
    |11|$Record.Amount| Is Null|⬜|
    |12|$Record.Budget_Quote__c| Equal To|✅|
    
    
    
    
    #### Rule Application_Fit_Confirmed_Stage (Application Fit Confirmed Stage)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Update_Stage_to_Application_Fit_Confirmed](#update_stage_to_application_fit_confirmed)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |1|$Record.LeadSource| Is Null|⬜|
    |2|$Record.Market_Segment__c| Is Null|⬜|
    |3|$Record.LOB__c| Is Null|⬜|
    |4|$Record.AccountId| Is Null|⬜|
    |5|$Record.Name| Is Null|⬜|
    |6|$Record.HasOpportunityLineItem| Equal To|✅|
    |7|$Record.TotalOpportunityQuantity| Is Null|⬜|
    |8|$Record.Has_Contact_Role_as_DM__c| Equal To|✅|
    |9|$Record.Amount| Is Null|⬜|
    |10|$Record.Budget_Quote__c| Equal To|✅|
    
    
    
    
    #### Rule Budget_Fit_Confirmed_Stage (Budget Fit Confirmed Stage)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Update_stage_to_Budget_Fit_Confirmed](#update_stage_to_budget_fit_confirmed)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |1|$Record.LeadSource| Is Null|⬜|
    |2|$Record.Market_Segment__c| Is Null|⬜|
    |3|$Record.LOB__c| Is Null|⬜|
    |4|$Record.AccountId| Is Null|⬜|
    |5|$Record.Name| Is Null|⬜|
    |6|$Record.HasOpportunityLineItem| Equal To|✅|
    |7|$Record.TotalOpportunityQuantity| Is Null|⬜|
    |8|$Record.Has_Contact_Role_as_DM__c| Equal To|✅|
    
    
    
    
    #### Rule Decision_Maker_Confirmed_Stage (Decision Maker Confirmed Stage)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Update_Opportunity_Stage_Decision_Maker_Confirmed](#update_opportunity_stage_decision_maker_confirmed)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |1|$Record.TotalOpportunityQuantity| Is Null|⬜|
    |2|$Record.Name| Is Null|⬜|
    |3|$Record.AccountId| Is Null|⬜|
    |4|$Record.LOB__c| Is Null|⬜|
    |5|$Record.Market_Segment__c| Is Null|⬜|
    |6|$Record.LeadSource| Is Null|⬜|
    
    
    
    
    #### Rule Product_Fit_Confirmed_Stage (Product Fit Confirmed Stage)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Update_Product_Fit_Confirm_Confirm](#update_product_fit_confirm_confirm)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |1|$Record.Name| Is Null|⬜|
    |2|$Record.Account.Name| Is Null|⬜|
    |3|$Record.LOB__c| Is Null|⬜|
    |4|$Record.Market_Segment__c| Is Null|⬜|
    |5|$Record.LeadSource| Is Null|⬜|
    
    
    
    
    ### Is_record_type_is_Commercial
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Decision|
    |Label|Is record type is Commercial|
    |Default Connector Label|Defense|
    
    
    #### Rule Commercial (Commercial)
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Connector|[Check_Stages](#check_stages)|
    |Condition Logic|and|
    
    
    
    
    |Condition Id|Left Value Reference|Operator|Right Value|
    |:-- |:-- |:--:|:--: |
    |1|Get_Record_Type.Id| Is Null|⬜|
    |2|$Record.RecordTypeId| Equal To|Get_Record_Type.Id|
    
    
    
    
    ### Get_Record_Type
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Lookup|
    |Object|RecordType|
    |Label|Get Record Type|
    |Description|Get record types present on Opportunity object|
    |Assign Null Values If No Records Found|⬜|
    |Get First Record Only|✅|
    |Store Output Automatically|✅|
    |Connector|[Is_record_type_is_Commercial](#is_record_type_is_commercial)|
    
    
    #### Filters (logic: **and**)
    
    |Filter Id|Field|Operator|Value|
    |:-- |:-- |:--:|:--: |
    |1|DeveloperName| Equal To|Commercial|
    |2|SobjectType| Equal To|Opportunity|
    
    
    
    
    ### Contacted_by_Purchasing
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Label|Contacted by Purchasing|
    |Input Reference|$Record|
    
    
    #### Input Assignments
    
    |Field|Value|
    |:-- |:--: |
    |StageName|Contacted by Purchasing|
    
    
    
    
    ### Need_By_Date_Known
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Label|Need By Date Known|
    |Input Reference|$Record|
    
    
    #### Input Assignments
    
    |Field|Value|
    |:-- |:--: |
    |StageName|Need By Date Known|
    
    
    
    
    ### Order_Sent_Quoted_to_Purchasing
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Label|Order Sent/Quoted to Purchasing|
    |Input Reference|$Record|
    
    
    #### Input Assignments
    
    |Field|Value|
    |:-- |:--: |
    |StageName|Order Sent/Quoted to Purchasing|
    
    
    
    
    ### Update_Opportunity_Stage_Decision_Maker_Confirmed
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Label|Update Opportunity Stage Decision Maker Confirmed|
    |Input Reference|$Record|
    
    
    #### Input Assignments
    
    |Field|Value|
    |:-- |:--: |
    |StageName|Decision Maker Confirmed|
    
    
    
    
    ### Update_Product_Fit_Confirm_Confirm
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Label|Update Product Fit Confirm Confirm|
    |Input Reference|$Record|
    
    
    #### Input Assignments
    
    |Field|Value|
    |:-- |:--: |
    |StageName|Product Fit Confirmed|
    
    
    
    
    ### Update_Stage_to_Application_Fit_Confirmed
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Label|Update Stage to Application Fit Confirmed|
    |Input Reference|$Record|
    
    
    #### Input Assignments
    
    |Field|Value|
    |:-- |:--: |
    |StageName|Application Fit Confirmed|
    
    
    
    
    ### Update_stage_to_Budget_Fit_Confirmed
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Label|Update stage to Budget Fit Confirmed|
    |Input Reference|$Record|
    
    
    #### Input Assignments
    
    |Field|Value|
    |:-- |:--: |
    |StageName|Budget Fit Confirmed|
    
    
    
    
    ### Update_stage_to_closed_lost
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Label|Update stage to closed lost|
    |Input Reference|$Record|
    
    
    #### Input Assignments
    
    |Field|Value|
    |:-- |:--: |
    |StageName|Closed Lost|
    
    
    
    
    ### Update_Stage_to_Contact_Approval
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Label|Update Stage to Contact Approval|
    |Input Reference|$Record|
    
    
    #### Input Assignments
    
    |Field|Value|
    |:-- |:--: |
    |StageName|Contact Approval|
    
    
    
    
    ### Update_Stage_to_Funded
    
    |<!-- -->|<!-- -->|
    |:---|:---|
    |Type|Record Update|
    |Label|Update Stage to Funded|
    |Input Reference|$Record|
    
    
    #### Input Assignments
    
    |Field|Value|
    |:-- |:--: |
    |StageName|Funded|
    
    
    
    
    
    
    
    
    ___
    
    _Documentation generated from branch main by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_

