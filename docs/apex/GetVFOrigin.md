---
hide:
  - path
---

---
hide:
  - path
---

---
hide:
  - path
---

---
hide:
  - path
---

---
hide:
  - path
---

---
hide:
  - path
---

---
hide:
  - path
---

---
hide:
  - path
---

---
hide:
  - path
---

# GetVFOrigin Class

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
public with sharing class GetVFOrigin {
    @AuraEnabled(cacheable=true)
    public static string getVFOrigin() {
      string vfOrigin = '';
    string baseURL = URL.getOrgDomainUrl().toExternalForm(); // Expected Format = https://domain.my.salesforce.com
 
    // Expected Format for DE, Sandbox & Production ORgs = https://domain--c.vf.force.com
    vfOrigin = baseURL.split('.my.')[0] + '.my.salesforce.com--c.' + 'vf.force.com';
 
   // Please note the DOMAIN mismatch error in your console logs , if any. 
   // Earlier it used to end with  --c.visualforce.com
   // Now, it is found to work successfully when ended with --c.vf.force.com
 
 
    /* ********* Below Odd Discrepancy was found while implementing this in a Trailhead Playground ***********
    Organization oOrg = [SELECT InstanceName, IsSandbox, OrganizationType FROM Organization LIMIT 1];
    if(oOrg.OrganizationType == 'Developer Edition'){
      // Expected Format for Trailhead Playground DE Org = https://domain--c.ap4.visual.force.com
      vfOrigin = baseURL.split('.my.')[0]+'--c.'+oOrg.InstanceName.toLowercase()+'.visual.force.com';
 
    } else {
      // Expected Format for personal DE, Sandbox & Production Orgs = https://domain--c.visualforce.com
      vfOrigin = baseURL.split('.my.')[0]+'--c.'+'visualforce.com';
    }  */
 
    return vfOrigin;
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
public with sharing class GetVFOrigin {
    @AuraEnabled(cacheable=true)
    public static string getVFOrigin() {
      string vfOrigin = '';
    string baseURL = URL.getOrgDomainUrl().toExternalForm(); // Expected Format = https://domain.my.salesforce.com
 
    // Expected Format for DE, Sandbox & Production ORgs = https://domain--c.vf.force.com
    vfOrigin = baseURL.split('.my.')[0] + '.my.salesforce.com--c.' + 'vf.force.com';
 
   // Please note the DOMAIN mismatch error in your console logs , if any. 
   // Earlier it used to end with  --c.visualforce.com
   // Now, it is found to work successfully when ended with --c.vf.force.com
 
 
    /* ********* Below Odd Discrepancy was found while implementing this in a Trailhead Playground ***********
    Organization oOrg = [SELECT InstanceName, IsSandbox, OrganizationType FROM Organization LIMIT 1];
    if(oOrg.OrganizationType == 'Developer Edition'){
      // Expected Format for Trailhead Playground DE Org = https://domain--c.ap4.visual.force.com
      vfOrigin = baseURL.split('.my.')[0]+'--c.'+oOrg.InstanceName.toLowercase()+'.visual.force.com';
 
    } else {
      // Expected Format for personal DE, Sandbox & Production Orgs = https://domain--c.visualforce.com
      vfOrigin = baseURL.split('.my.')[0]+'--c.'+'visualforce.com';
    }  */
 
    return vfOrigin;
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
public with sharing class GetVFOrigin {
    @AuraEnabled(cacheable=true)
    public static string getVFOrigin() {
      string vfOrigin = '';
    string baseURL = URL.getOrgDomainUrl().toExternalForm(); // Expected Format = https://domain.my.salesforce.com
 
    // Expected Format for DE, Sandbox & Production ORgs = https://domain--c.vf.force.com
    vfOrigin = baseURL.split('.my.')[0] + '.my.salesforce.com--c.' + 'vf.force.com';
 
   // Please note the DOMAIN mismatch error in your console logs , if any. 
   // Earlier it used to end with  --c.visualforce.com
   // Now, it is found to work successfully when ended with --c.vf.force.com
 
 
    /* ********* Below Odd Discrepancy was found while implementing this in a Trailhead Playground ***********
    Organization oOrg = [SELECT InstanceName, IsSandbox, OrganizationType FROM Organization LIMIT 1];
    if(oOrg.OrganizationType == 'Developer Edition'){
      // Expected Format for Trailhead Playground DE Org = https://domain--c.ap4.visual.force.com
      vfOrigin = baseURL.split('.my.')[0]+'--c.'+oOrg.InstanceName.toLowercase()+'.visual.force.com';
 
    } else {
      // Expected Format for personal DE, Sandbox & Production Orgs = https://domain--c.visualforce.com
      vfOrigin = baseURL.split('.my.')[0]+'--c.'+'visualforce.com';
    }  */
 
    return vfOrigin;
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
public with sharing class GetVFOrigin {
    @AuraEnabled(cacheable=true)
    public static string getVFOrigin() {
      string vfOrigin = '';
    string baseURL = URL.getOrgDomainUrl().toExternalForm(); // Expected Format = https://domain.my.salesforce.com
 
    // Expected Format for DE, Sandbox & Production ORgs = https://domain--c.vf.force.com
    vfOrigin = baseURL.split('.my.')[0] + '.my.salesforce.com--c.' + 'vf.force.com';
 
   // Please note the DOMAIN mismatch error in your console logs , if any. 
   // Earlier it used to end with  --c.visualforce.com
   // Now, it is found to work successfully when ended with --c.vf.force.com
 
 
    /* ********* Below Odd Discrepancy was found while implementing this in a Trailhead Playground ***********
    Organization oOrg = [SELECT InstanceName, IsSandbox, OrganizationType FROM Organization LIMIT 1];
    if(oOrg.OrganizationType == 'Developer Edition'){
      // Expected Format for Trailhead Playground DE Org = https://domain--c.ap4.visual.force.com
      vfOrigin = baseURL.split('.my.')[0]+'--c.'+oOrg.InstanceName.toLowercase()+'.visual.force.com';
 
    } else {
      // Expected Format for personal DE, Sandbox & Production Orgs = https://domain--c.visualforce.com
      vfOrigin = baseURL.split('.my.')[0]+'--c.'+'visualforce.com';
    }  */
 
    return vfOrigin;
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
public with sharing class GetVFOrigin {
    @AuraEnabled(cacheable=true)
    public static string getVFOrigin() {
      string vfOrigin = '';
    string baseURL = URL.getOrgDomainUrl().toExternalForm(); // Expected Format = https://domain.my.salesforce.com
 
    // Expected Format for DE, Sandbox & Production ORgs = https://domain--c.vf.force.com
    vfOrigin = baseURL.split('.my.')[0] + '.my.salesforce.com--c.' + 'vf.force.com';
 
   // Please note the DOMAIN mismatch error in your console logs , if any. 
   // Earlier it used to end with  --c.visualforce.com
   // Now, it is found to work successfully when ended with --c.vf.force.com
 
 
    /* ********* Below Odd Discrepancy was found while implementing this in a Trailhead Playground ***********
    Organization oOrg = [SELECT InstanceName, IsSandbox, OrganizationType FROM Organization LIMIT 1];
    if(oOrg.OrganizationType == 'Developer Edition'){
      // Expected Format for Trailhead Playground DE Org = https://domain--c.ap4.visual.force.com
      vfOrigin = baseURL.split('.my.')[0]+'--c.'+oOrg.InstanceName.toLowercase()+'.visual.force.com';
 
    } else {
      // Expected Format for personal DE, Sandbox & Production Orgs = https://domain--c.visualforce.com
      vfOrigin = baseURL.split('.my.')[0]+'--c.'+'visualforce.com';
    }  */
 
    return vfOrigin;
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
public with sharing class GetVFOrigin {
    @AuraEnabled(cacheable=true)
    public static string getVFOrigin() {
      string vfOrigin = '';
    string baseURL = URL.getOrgDomainUrl().toExternalForm(); // Expected Format = https://domain.my.salesforce.com
 
    // Expected Format for DE, Sandbox & Production ORgs = https://domain--c.vf.force.com
    vfOrigin = baseURL.split('.my.')[0] + '.my.salesforce.com--c.' + 'vf.force.com';
 
   // Please note the DOMAIN mismatch error in your console logs , if any. 
   // Earlier it used to end with  --c.visualforce.com
   // Now, it is found to work successfully when ended with --c.vf.force.com
 
 
    /* ********* Below Odd Discrepancy was found while implementing this in a Trailhead Playground ***********
    Organization oOrg = [SELECT InstanceName, IsSandbox, OrganizationType FROM Organization LIMIT 1];
    if(oOrg.OrganizationType == 'Developer Edition'){
      // Expected Format for Trailhead Playground DE Org = https://domain--c.ap4.visual.force.com
      vfOrigin = baseURL.split('.my.')[0]+'--c.'+oOrg.InstanceName.toLowercase()+'.visual.force.com';
 
    } else {
      // Expected Format for personal DE, Sandbox & Production Orgs = https://domain--c.visualforce.com
      vfOrigin = baseURL.split('.my.')[0]+'--c.'+'visualforce.com';
    }  */
 
    return vfOrigin;
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
public with sharing class GetVFOrigin {
    @AuraEnabled(cacheable=true)
    public static string getVFOrigin() {
      string vfOrigin = '';
    string baseURL = URL.getOrgDomainUrl().toExternalForm(); // Expected Format = https://domain.my.salesforce.com
 
    // Expected Format for DE, Sandbox & Production ORgs = https://domain--c.vf.force.com
    vfOrigin = baseURL.split('.my.')[0] + '.my.salesforce.com--c.' + 'vf.force.com';
 
   // Please note the DOMAIN mismatch error in your console logs , if any. 
   // Earlier it used to end with  --c.visualforce.com
   // Now, it is found to work successfully when ended with --c.vf.force.com
 
 
    /* ********* Below Odd Discrepancy was found while implementing this in a Trailhead Playground ***********
    Organization oOrg = [SELECT InstanceName, IsSandbox, OrganizationType FROM Organization LIMIT 1];
    if(oOrg.OrganizationType == 'Developer Edition'){
      // Expected Format for Trailhead Playground DE Org = https://domain--c.ap4.visual.force.com
      vfOrigin = baseURL.split('.my.')[0]+'--c.'+oOrg.InstanceName.toLowercase()+'.visual.force.com';
 
    } else {
      // Expected Format for personal DE, Sandbox & Production Orgs = https://domain--c.visualforce.com
      vfOrigin = baseURL.split('.my.')[0]+'--c.'+'visualforce.com';
    }  */
 
    return vfOrigin;
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
public with sharing class GetVFOrigin {
    @AuraEnabled(cacheable=true)
    public static string getVFOrigin() {
      string vfOrigin = '';
    string baseURL = URL.getOrgDomainUrl().toExternalForm(); // Expected Format = https://domain.my.salesforce.com
 
    // Expected Format for DE, Sandbox & Production ORgs = https://domain--c.vf.force.com
    vfOrigin = baseURL.split('.my.')[0] + '.my.salesforce.com--c.' + 'vf.force.com';
 
   // Please note the DOMAIN mismatch error in your console logs , if any. 
   // Earlier it used to end with  --c.visualforce.com
   // Now, it is found to work successfully when ended with --c.vf.force.com
 
 
    /* ********* Below Odd Discrepancy was found while implementing this in a Trailhead Playground ***********
    Organization oOrg = [SELECT InstanceName, IsSandbox, OrganizationType FROM Organization LIMIT 1];
    if(oOrg.OrganizationType == 'Developer Edition'){
      // Expected Format for Trailhead Playground DE Org = https://domain--c.ap4.visual.force.com
      vfOrigin = baseURL.split('.my.')[0]+'--c.'+oOrg.InstanceName.toLowercase()+'.visual.force.com';
 
    } else {
      // Expected Format for personal DE, Sandbox & Production Orgs = https://domain--c.visualforce.com
      vfOrigin = baseURL.split('.my.')[0]+'--c.'+'visualforce.com';
    }  */
 
    return vfOrigin;
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
public with sharing class GetVFOrigin {
  @AuraEnabled(cacheable=true)
  public static string getVFOrigin() {
    string vfOrigin = '';
    string baseURL = URL.getOrgDomainUrl().toExternalForm(); // Expected Format = https://domain.my.salesforce.com

    // Expected Format for DE, Sandbox & Production ORgs = https://domain--c.vf.force.com
    vfOrigin =
      baseURL.split('.my.')[0] +
      '.my.salesforce.com--c.' +
      'vf.force.com';

    // Please note the DOMAIN mismatch error in your console logs , if any.
    // Earlier it used to end with  --c.visualforce.com
    // Now, it is found to work successfully when ended with --c.vf.force.com

    /* ********* Below Odd Discrepancy was found while implementing this in a Trailhead Playground ***********
    Organization oOrg = [SELECT InstanceName, IsSandbox, OrganizationType FROM Organization LIMIT 1];
    if(oOrg.OrganizationType == 'Developer Edition'){
      // Expected Format for Trailhead Playground DE Org = https://domain--c.ap4.visual.force.com
      vfOrigin = baseURL.split('.my.')[0]+'--c.'+oOrg.InstanceName.toLowercase()+'.visual.force.com';
 
    } else {
      // Expected Format for personal DE, Sandbox & Production Orgs = https://domain--c.visualforce.com
      vfOrigin = baseURL.split('.my.')[0]+'--c.'+'visualforce.com';
    }  */

    return vfOrigin;
  }
}

```

## Methods
### `getVFOrigin()`

`AURAENABLED`

#### Signature
```apex
public static string getVFOrigin()
```

#### Return Type
**string**