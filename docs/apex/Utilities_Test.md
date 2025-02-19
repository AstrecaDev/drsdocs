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

# Utilities_Test Class

`ISTEST`

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class Utilities_Test {
    @isTest
    private static void getInstance(){
        String instance = '';
        Organization o = [SELECT OrganizationType, InstanceName FROM Organization limit 1];
        String orgType = o.OrganizationType;
        String insName = o.InstanceName;

        //Set this header to test it
        ApexPages.currentPage().getHeaders().put('Host', insName+'.visual.force.com');

        if(orgType == 'Developer Edition'){
            List<String> parts = ApexPages.currentPage().getHeaders().get('Host').split('\\.');
            instance = parts[parts.size() - 4] + '.';
        }

        System.assertEquals(instance, Utilities.getInstance());
    }
    @isTest
    private static void getSubdomainPrefix(){
        //This will always be empty unless it's sandbox
        System.assertEquals('', Utilities.getSubdomainPrefix());
    }

}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class Utilities_Test {
    @isTest
    private static void getInstance(){
        String instance = '';
        Organization o = [SELECT OrganizationType, InstanceName FROM Organization limit 1];
        String orgType = o.OrganizationType;
        String insName = o.InstanceName;

        //Set this header to test it
        ApexPages.currentPage().getHeaders().put('Host', insName+'.visual.force.com');

        if(orgType == 'Developer Edition'){
            List<String> parts = ApexPages.currentPage().getHeaders().get('Host').split('\\.');
            instance = parts[parts.size() - 4] + '.';
        }

        System.assertEquals(instance, Utilities.getInstance());
    }
    @isTest
    private static void getSubdomainPrefix(){
        //This will always be empty unless it's sandbox
        System.assertEquals('', Utilities.getSubdomainPrefix());
    }

}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class Utilities_Test {
    @isTest
    private static void getInstance(){
        String instance = '';
        Organization o = [SELECT OrganizationType, InstanceName FROM Organization limit 1];
        String orgType = o.OrganizationType;
        String insName = o.InstanceName;

        //Set this header to test it
        ApexPages.currentPage().getHeaders().put('Host', insName+'.visual.force.com');

        if(orgType == 'Developer Edition'){
            List<String> parts = ApexPages.currentPage().getHeaders().get('Host').split('\\.');
            instance = parts[parts.size() - 4] + '.';
        }

        System.assertEquals(instance, Utilities.getInstance());
    }
    @isTest
    private static void getSubdomainPrefix(){
        //This will always be empty unless it's sandbox
        System.assertEquals('', Utilities.getSubdomainPrefix());
    }

}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class Utilities_Test {
    @isTest
    private static void getInstance(){
        String instance = '';
        Organization o = [SELECT OrganizationType, InstanceName FROM Organization limit 1];
        String orgType = o.OrganizationType;
        String insName = o.InstanceName;

        //Set this header to test it
        ApexPages.currentPage().getHeaders().put('Host', insName+'.visual.force.com');

        if(orgType == 'Developer Edition'){
            List<String> parts = ApexPages.currentPage().getHeaders().get('Host').split('\\.');
            instance = parts[parts.size() - 4] + '.';
        }

        System.assertEquals(instance, Utilities.getInstance());
    }
    @isTest
    private static void getSubdomainPrefix(){
        //This will always be empty unless it's sandbox
        System.assertEquals('', Utilities.getSubdomainPrefix());
    }

}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class Utilities_Test {
    @isTest
    private static void getInstance(){
        String instance = '';
        Organization o = [SELECT OrganizationType, InstanceName FROM Organization limit 1];
        String orgType = o.OrganizationType;
        String insName = o.InstanceName;

        //Set this header to test it
        ApexPages.currentPage().getHeaders().put('Host', insName+'.visual.force.com');

        if(orgType == 'Developer Edition'){
            List<String> parts = ApexPages.currentPage().getHeaders().get('Host').split('\\.');
            instance = parts[parts.size() - 4] + '.';
        }

        System.assertEquals(instance, Utilities.getInstance());
    }
    @isTest
    private static void getSubdomainPrefix(){
        //This will always be empty unless it's sandbox
        System.assertEquals('', Utilities.getSubdomainPrefix());
    }

}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class Utilities_Test {
    @isTest
    private static void getInstance(){
        String instance = '';
        Organization o = [SELECT OrganizationType, InstanceName FROM Organization limit 1];
        String orgType = o.OrganizationType;
        String insName = o.InstanceName;

        //Set this header to test it
        ApexPages.currentPage().getHeaders().put('Host', insName+'.visual.force.com');

        if(orgType == 'Developer Edition'){
            List<String> parts = ApexPages.currentPage().getHeaders().get('Host').split('\\.');
            instance = parts[parts.size() - 4] + '.';
        }

        System.assertEquals(instance, Utilities.getInstance());
    }
    @isTest
    private static void getSubdomainPrefix(){
        //This will always be empty unless it's sandbox
        System.assertEquals('', Utilities.getSubdomainPrefix());
    }

}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class Utilities_Test {
    @isTest
    private static void getInstance(){
        String instance = '';
        Organization o = [SELECT OrganizationType, InstanceName FROM Organization limit 1];
        String orgType = o.OrganizationType;
        String insName = o.InstanceName;

        //Set this header to test it
        ApexPages.currentPage().getHeaders().put('Host', insName+'.visual.force.com');

        if(orgType == 'Developer Edition'){
            List<String> parts = ApexPages.currentPage().getHeaders().get('Host').split('\\.');
            instance = parts[parts.size() - 4] + '.';
        }

        System.assertEquals(instance, Utilities.getInstance());
    }
    @isTest
    private static void getSubdomainPrefix(){
        //This will always be empty unless it's sandbox
        System.assertEquals('', Utilities.getSubdomainPrefix());
    }

}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class Utilities_Test {
    @isTest
    private static void getInstance(){
        String instance = '';
        Organization o = [SELECT OrganizationType, InstanceName FROM Organization limit 1];
        String orgType = o.OrganizationType;
        String insName = o.InstanceName;

        //Set this header to test it
        ApexPages.currentPage().getHeaders().put('Host', insName+'.visual.force.com');

        if(orgType == 'Developer Edition'){
            List<String> parts = ApexPages.currentPage().getHeaders().get('Host').split('\\.');
            instance = parts[parts.size() - 4] + '.';
        }

        System.assertEquals(instance, Utilities.getInstance());
    }
    @isTest
    private static void getSubdomainPrefix(){
        //This will always be empty unless it's sandbox
        System.assertEquals('', Utilities.getSubdomainPrefix());
    }

}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class Utilities_Test {
  @isTest
  private static void getInstance() {
    String instance = '';
    Organization o = [
      SELECT OrganizationType, InstanceName
      FROM Organization
      LIMIT 1
    ];
    String orgType = o.OrganizationType;
    String insName = o.InstanceName;

    //Set this header to test it
    ApexPages.currentPage()
      .getHeaders()
      .put('Host', insName + '.visual.force.com');

    if (orgType == 'Developer Edition') {
      List<String> parts = ApexPages.currentPage()
        .getHeaders()
        .get('Host')
        .split('\\.');
      instance = parts[parts.size() - 4] + '.';
    }

    System.assertEquals(instance, Utilities.getInstance());
  }
  @isTest
  private static void getSubdomainPrefix() {
    //This will always be empty unless it's sandbox
    System.assertEquals('', Utilities.getSubdomainPrefix());
  }
}

```

## Methods
### `getInstance()`

`ISTEST`

#### Signature
```apex
private static void getInstance()
```

#### Return Type
**void**

---

### `getSubdomainPrefix()`

`ISTEST`

#### Signature
```apex
private static void getSubdomainPrefix()
```

#### Return Type
**void**