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

# updateordernumber Class

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
public with sharing class updateordernumber {
  public static void updateordernumber(List<Quotelineitem> inputqliList) {
    // Convert Trigger.new to a list of Quotelineitems
    List<Quotelineitem> qliList = (List<Quotelineitem>) inputqliList;

    // Initialize a map to store Quotelineitems based on their product families
    Map<String, List<Quotelineitem>> qliMap = new Map<String, List<Quotelineitem>>();

    // Initialize a map to keep track of the count of base unit Quotelineitems per family
    Map<String, Integer> baseUnitQliMap = new Map<String, Integer>();

    // Iterate through each Quotelineitem in the list
    for (Quotelineitem qli : qliList) {
      // Check if the Quotelineitem belongs to the 'Base Unit' family and is standalone
      if (qli.Product2.Family == 'Base Unit' && qli.Standalone__c == true) {
        // If standalone base unit, initialize the maps with 'Base Unit' as the key
        qliMap.put('Base Unit', new List<Quotelineitem>());
        baseUnitQliMap.put('Base Unit', 0);
      } else if (
        qli.Product2.Family == 'Base Unit' &&
        qli.Standalone__c == false
      ) {
        // If base unit but not standalone
        String key = qli.Base_Unit_Family__r.Name;
        if (baseUnitQliMap.containsKey(key)) {
          // Add to existing list and update count
          qliMap.get(key).add(qli);
          baseUnitQliMap.put(key, baseUnitQliMap.get(key) + 1);
        } else {
          // If family key doesn't exist, create a new list and update count
          List<Quotelineitem> valueList = new List<Quotelineitem>();
          valueList.add(qli);
          baseUnitQliMap.put(key, 1);
          qliMap.put(key, valueList);
        }
      } else if (qli.Product2.Family != 'Base Unit') {
        // If not a base unit, directly add to map using family as key
        qliMap.put(qli.Product2.Family, new List<Quotelineitem>());
        qliMap.get(qli.Product2.Family).add(qli);
      }
    }

    // Sort Quotelineitems based on their family and set the sort order
    if (!qliMap.isEmpty()) {
      Integer i = 0;
      for (String family : qliMap.keySet()) {
        for (Quotelineitem qli : qliMap.get(family)) {
          if (family == 'Base Unit') {
            // Set sort order with a different increment for base units
            qli.Sort_Order__c = i * 0.1;
            i++;
          } else {
            // Set sort order with regular increment for other families
            qli.Sort_Order__c = i;
            i++;
          }
        }
      }
    }
  }
}

```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
public with sharing class updateordernumber {
  public static void updateordernumber(List<Quotelineitem> inputqliList) {
    // Convert Trigger.new to a list of Quotelineitems
    List<Quotelineitem> qliList = (List<Quotelineitem>) inputqliList;

    // Initialize a map to store Quotelineitems based on their product families
    Map<String, List<Quotelineitem>> qliMap = new Map<String, List<Quotelineitem>>();

    // Initialize a map to keep track of the count of base unit Quotelineitems per family
    Map<String, Integer> baseUnitQliMap = new Map<String, Integer>();

    // Iterate through each Quotelineitem in the list
    for (Quotelineitem qli : qliList) {
      // Check if the Quotelineitem belongs to the 'Base Unit' family and is standalone
      if (qli.Product2.Family == 'Base Unit' && qli.Standalone__c == true) {
        // If standalone base unit, initialize the maps with 'Base Unit' as the key
        qliMap.put('Base Unit', new List<Quotelineitem>());
        baseUnitQliMap.put('Base Unit', 0);
      } else if (
        qli.Product2.Family == 'Base Unit' &&
        qli.Standalone__c == false
      ) {
        // If base unit but not standalone
        String key = qli.Base_Unit_Family__r.Name;
        if (baseUnitQliMap.containsKey(key)) {
          // Add to existing list and update count
          qliMap.get(key).add(qli);
          baseUnitQliMap.put(key, baseUnitQliMap.get(key) + 1);
        } else {
          // If family key doesn't exist, create a new list and update count
          List<Quotelineitem> valueList = new List<Quotelineitem>();
          valueList.add(qli);
          baseUnitQliMap.put(key, 1);
          qliMap.put(key, valueList);
        }
      } else if (qli.Product2.Family != 'Base Unit') {
        // If not a base unit, directly add to map using family as key
        qliMap.put(qli.Product2.Family, new List<Quotelineitem>());
        qliMap.get(qli.Product2.Family).add(qli);
      }
    }

    // Sort Quotelineitems based on their family and set the sort order
    if (!qliMap.isEmpty()) {
      Integer i = 0;
      for (String family : qliMap.keySet()) {
        for (Quotelineitem qli : qliMap.get(family)) {
          if (family == 'Base Unit') {
            // Set sort order with a different increment for base units
            qli.Sort_Order__c = i * 0.1;
            i++;
          } else {
            // Set sort order with regular increment for other families
            qli.Sort_Order__c = i;
            i++;
          }
        }
      }
    }
  }
}

```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
public with sharing class updateordernumber {
  public static void updateordernumber(List<Quotelineitem> inputqliList) {
    // Convert Trigger.new to a list of Quotelineitems
    List<Quotelineitem> qliList = (List<Quotelineitem>) inputqliList;

    // Initialize a map to store Quotelineitems based on their product families
    Map<String, List<Quotelineitem>> qliMap = new Map<String, List<Quotelineitem>>();

    // Initialize a map to keep track of the count of base unit Quotelineitems per family
    Map<String, Integer> baseUnitQliMap = new Map<String, Integer>();

    // Iterate through each Quotelineitem in the list
    for (Quotelineitem qli : qliList) {
      // Check if the Quotelineitem belongs to the 'Base Unit' family and is standalone
      if (qli.Product2.Family == 'Base Unit' && qli.Standalone__c == true) {
        // If standalone base unit, initialize the maps with 'Base Unit' as the key
        qliMap.put('Base Unit', new List<Quotelineitem>());
        baseUnitQliMap.put('Base Unit', 0);
      } else if (
        qli.Product2.Family == 'Base Unit' &&
        qli.Standalone__c == false
      ) {
        // If base unit but not standalone
        String key = qli.Base_Unit_Family__r.Name;
        if (baseUnitQliMap.containsKey(key)) {
          // Add to existing list and update count
          qliMap.get(key).add(qli);
          baseUnitQliMap.put(key, baseUnitQliMap.get(key) + 1);
        } else {
          // If family key doesn't exist, create a new list and update count
          List<Quotelineitem> valueList = new List<Quotelineitem>();
          valueList.add(qli);
          baseUnitQliMap.put(key, 1);
          qliMap.put(key, valueList);
        }
      } else if (qli.Product2.Family != 'Base Unit') {
        // If not a base unit, directly add to map using family as key
        qliMap.put(qli.Product2.Family, new List<Quotelineitem>());
        qliMap.get(qli.Product2.Family).add(qli);
      }
    }

    // Sort Quotelineitems based on their family and set the sort order
    if (!qliMap.isEmpty()) {
      Integer i = 0;
      for (String family : qliMap.keySet()) {
        for (Quotelineitem qli : qliMap.get(family)) {
          if (family == 'Base Unit') {
            // Set sort order with a different increment for base units
            qli.Sort_Order__c = i * 0.1;
            i++;
          } else {
            // Set sort order with regular increment for other families
            qli.Sort_Order__c = i;
            i++;
          }
        }
      }
    }
  }
}

```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
public with sharing class updateordernumber {
  public static void updateordernumber(List<Quotelineitem> inputqliList) {
    // Convert Trigger.new to a list of Quotelineitems
    List<Quotelineitem> qliList = (List<Quotelineitem>) inputqliList;

    // Initialize a map to store Quotelineitems based on their product families
    Map<String, List<Quotelineitem>> qliMap = new Map<String, List<Quotelineitem>>();

    // Initialize a map to keep track of the count of base unit Quotelineitems per family
    Map<String, Integer> baseUnitQliMap = new Map<String, Integer>();

    // Iterate through each Quotelineitem in the list
    for (Quotelineitem qli : qliList) {
      // Check if the Quotelineitem belongs to the 'Base Unit' family and is standalone
      if (qli.Product2.Family == 'Base Unit' && qli.Standalone__c == true) {
        // If standalone base unit, initialize the maps with 'Base Unit' as the key
        qliMap.put('Base Unit', new List<Quotelineitem>());
        baseUnitQliMap.put('Base Unit', 0);
      } else if (
        qli.Product2.Family == 'Base Unit' &&
        qli.Standalone__c == false
      ) {
        // If base unit but not standalone
        String key = qli.Base_Unit_Family__r.Name;
        if (baseUnitQliMap.containsKey(key)) {
          // Add to existing list and update count
          qliMap.get(key).add(qli);
          baseUnitQliMap.put(key, baseUnitQliMap.get(key) + 1);
        } else {
          // If family key doesn't exist, create a new list and update count
          List<Quotelineitem> valueList = new List<Quotelineitem>();
          valueList.add(qli);
          baseUnitQliMap.put(key, 1);
          qliMap.put(key, valueList);
        }
      } else if (qli.Product2.Family != 'Base Unit') {
        // If not a base unit, directly add to map using family as key
        qliMap.put(qli.Product2.Family, new List<Quotelineitem>());
        qliMap.get(qli.Product2.Family).add(qli);
      }
    }

    // Sort Quotelineitems based on their family and set the sort order
    if (!qliMap.isEmpty()) {
      Integer i = 0;
      for (String family : qliMap.keySet()) {
        for (Quotelineitem qli : qliMap.get(family)) {
          if (family == 'Base Unit') {
            // Set sort order with a different increment for base units
            qli.Sort_Order__c = i * 0.1;
            i++;
          } else {
            // Set sort order with regular increment for other families
            qli.Sort_Order__c = i;
            i++;
          }
        }
      }
    }
  }
}

```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
public with sharing class updateordernumber {
  public static void updateordernumber(List<Quotelineitem> inputqliList) {
    // Convert Trigger.new to a list of Quotelineitems
    List<Quotelineitem> qliList = (List<Quotelineitem>) inputqliList;

    // Initialize a map to store Quotelineitems based on their product families
    Map<String, List<Quotelineitem>> qliMap = new Map<String, List<Quotelineitem>>();

    // Initialize a map to keep track of the count of base unit Quotelineitems per family
    Map<String, Integer> baseUnitQliMap = new Map<String, Integer>();

    // Iterate through each Quotelineitem in the list
    for (Quotelineitem qli : qliList) {
      // Check if the Quotelineitem belongs to the 'Base Unit' family and is standalone
      if (qli.Product2.Family == 'Base Unit' && qli.Standalone__c == true) {
        // If standalone base unit, initialize the maps with 'Base Unit' as the key
        qliMap.put('Base Unit', new List<Quotelineitem>());
        baseUnitQliMap.put('Base Unit', 0);
      } else if (
        qli.Product2.Family == 'Base Unit' &&
        qli.Standalone__c == false
      ) {
        // If base unit but not standalone
        String key = qli.Base_Unit_Family__r.Name;
        if (baseUnitQliMap.containsKey(key)) {
          // Add to existing list and update count
          qliMap.get(key).add(qli);
          baseUnitQliMap.put(key, baseUnitQliMap.get(key) + 1);
        } else {
          // If family key doesn't exist, create a new list and update count
          List<Quotelineitem> valueList = new List<Quotelineitem>();
          valueList.add(qli);
          baseUnitQliMap.put(key, 1);
          qliMap.put(key, valueList);
        }
      } else if (qli.Product2.Family != 'Base Unit') {
        // If not a base unit, directly add to map using family as key
        qliMap.put(qli.Product2.Family, new List<Quotelineitem>());
        qliMap.get(qli.Product2.Family).add(qli);
      }
    }

    // Sort Quotelineitems based on their family and set the sort order
    if (!qliMap.isEmpty()) {
      Integer i = 0;
      for (String family : qliMap.keySet()) {
        for (Quotelineitem qli : qliMap.get(family)) {
          if (family == 'Base Unit') {
            // Set sort order with a different increment for base units
            qli.Sort_Order__c = i * 0.1;
            i++;
          } else {
            // Set sort order with regular increment for other families
            qli.Sort_Order__c = i;
            i++;
          }
        }
      }
    }
  }
}

```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
public with sharing class updateordernumber {
  public static void updateordernumber(List<Quotelineitem> inputqliList) {
    // Convert Trigger.new to a list of Quotelineitems
    List<Quotelineitem> qliList = (List<Quotelineitem>) inputqliList;

    // Initialize a map to store Quotelineitems based on their product families
    Map<String, List<Quotelineitem>> qliMap = new Map<String, List<Quotelineitem>>();

    // Initialize a map to keep track of the count of base unit Quotelineitems per family
    Map<String, Integer> baseUnitQliMap = new Map<String, Integer>();

    // Iterate through each Quotelineitem in the list
    for (Quotelineitem qli : qliList) {
      // Check if the Quotelineitem belongs to the 'Base Unit' family and is standalone
      if (qli.Product2.Family == 'Base Unit' && qli.Standalone__c == true) {
        // If standalone base unit, initialize the maps with 'Base Unit' as the key
        qliMap.put('Base Unit', new List<Quotelineitem>());
        baseUnitQliMap.put('Base Unit', 0);
      } else if (
        qli.Product2.Family == 'Base Unit' &&
        qli.Standalone__c == false
      ) {
        // If base unit but not standalone
        String key = qli.Base_Unit_Family__r.Name;
        if (baseUnitQliMap.containsKey(key)) {
          // Add to existing list and update count
          qliMap.get(key).add(qli);
          baseUnitQliMap.put(key, baseUnitQliMap.get(key) + 1);
        } else {
          // If family key doesn't exist, create a new list and update count
          List<Quotelineitem> valueList = new List<Quotelineitem>();
          valueList.add(qli);
          baseUnitQliMap.put(key, 1);
          qliMap.put(key, valueList);
        }
      } else if (qli.Product2.Family != 'Base Unit') {
        // If not a base unit, directly add to map using family as key
        qliMap.put(qli.Product2.Family, new List<Quotelineitem>());
        qliMap.get(qli.Product2.Family).add(qli);
      }
    }

    // Sort Quotelineitems based on their family and set the sort order
    if (!qliMap.isEmpty()) {
      Integer i = 0;
      for (String family : qliMap.keySet()) {
        for (Quotelineitem qli : qliMap.get(family)) {
          if (family == 'Base Unit') {
            // Set sort order with a different increment for base units
            qli.Sort_Order__c = i * 0.1;
            i++;
          } else {
            // Set sort order with regular increment for other families
            qli.Sort_Order__c = i;
            i++;
          }
        }
      }
    }
  }
}

```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
public with sharing class updateordernumber {
  public static void updateordernumber(List<Quotelineitem> inputqliList) {
    // Convert Trigger.new to a list of Quotelineitems
    List<Quotelineitem> qliList = (List<Quotelineitem>) inputqliList;

    // Initialize a map to store Quotelineitems based on their product families
    Map<String, List<Quotelineitem>> qliMap = new Map<String, List<Quotelineitem>>();

    // Initialize a map to keep track of the count of base unit Quotelineitems per family
    Map<String, Integer> baseUnitQliMap = new Map<String, Integer>();

    // Iterate through each Quotelineitem in the list
    for (Quotelineitem qli : qliList) {
      // Check if the Quotelineitem belongs to the 'Base Unit' family and is standalone
      if (qli.Product2.Family == 'Base Unit' && qli.Standalone__c == true) {
        // If standalone base unit, initialize the maps with 'Base Unit' as the key
        qliMap.put('Base Unit', new List<Quotelineitem>());
        baseUnitQliMap.put('Base Unit', 0);
      } else if (
        qli.Product2.Family == 'Base Unit' &&
        qli.Standalone__c == false
      ) {
        // If base unit but not standalone
        String key = qli.Base_Unit_Family__r.Name;
        if (baseUnitQliMap.containsKey(key)) {
          // Add to existing list and update count
          qliMap.get(key).add(qli);
          baseUnitQliMap.put(key, baseUnitQliMap.get(key) + 1);
        } else {
          // If family key doesn't exist, create a new list and update count
          List<Quotelineitem> valueList = new List<Quotelineitem>();
          valueList.add(qli);
          baseUnitQliMap.put(key, 1);
          qliMap.put(key, valueList);
        }
      } else if (qli.Product2.Family != 'Base Unit') {
        // If not a base unit, directly add to map using family as key
        qliMap.put(qli.Product2.Family, new List<Quotelineitem>());
        qliMap.get(qli.Product2.Family).add(qli);
      }
    }

    // Sort Quotelineitems based on their family and set the sort order
    if (!qliMap.isEmpty()) {
      Integer i = 0;
      for (String family : qliMap.keySet()) {
        for (Quotelineitem qli : qliMap.get(family)) {
          if (family == 'Base Unit') {
            // Set sort order with a different increment for base units
            qli.Sort_Order__c = i * 0.1;
            i++;
          } else {
            // Set sort order with regular increment for other families
            qli.Sort_Order__c = i;
            i++;
          }
        }
      }
    }
  }
}

```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
public with sharing class updateordernumber {
  public static void updateordernumber(List<Quotelineitem> inputqliList) {
    // Convert Trigger.new to a list of Quotelineitems
    List<Quotelineitem> qliList = (List<Quotelineitem>) inputqliList;

    // Initialize a map to store Quotelineitems based on their product families
    Map<String, List<Quotelineitem>> qliMap = new Map<String, List<Quotelineitem>>();

    // Initialize a map to keep track of the count of base unit Quotelineitems per family
    Map<String, Integer> baseUnitQliMap = new Map<String, Integer>();

    // Iterate through each Quotelineitem in the list
    for (Quotelineitem qli : qliList) {
      // Check if the Quotelineitem belongs to the 'Base Unit' family and is standalone
      if (qli.Product2.Family == 'Base Unit' && qli.Standalone__c == true) {
        // If standalone base unit, initialize the maps with 'Base Unit' as the key
        qliMap.put('Base Unit', new List<Quotelineitem>());
        baseUnitQliMap.put('Base Unit', 0);
      } else if (
        qli.Product2.Family == 'Base Unit' &&
        qli.Standalone__c == false
      ) {
        // If base unit but not standalone
        String key = qli.Base_Unit_Family__r.Name;
        if (baseUnitQliMap.containsKey(key)) {
          // Add to existing list and update count
          qliMap.get(key).add(qli);
          baseUnitQliMap.put(key, baseUnitQliMap.get(key) + 1);
        } else {
          // If family key doesn't exist, create a new list and update count
          List<Quotelineitem> valueList = new List<Quotelineitem>();
          valueList.add(qli);
          baseUnitQliMap.put(key, 1);
          qliMap.put(key, valueList);
        }
      } else if (qli.Product2.Family != 'Base Unit') {
        // If not a base unit, directly add to map using family as key
        qliMap.put(qli.Product2.Family, new List<Quotelineitem>());
        qliMap.get(qli.Product2.Family).add(qli);
      }
    }

    // Sort Quotelineitems based on their family and set the sort order
    if (!qliMap.isEmpty()) {
      Integer i = 0;
      for (String family : qliMap.keySet()) {
        for (Quotelineitem qli : qliMap.get(family)) {
          if (family == 'Base Unit') {
            // Set sort order with a different increment for base units
            qli.Sort_Order__c = i * 0.1;
            i++;
          } else {
            // Set sort order with regular increment for other families
            qli.Sort_Order__c = i;
            i++;
          }
        }
      }
    }
  }
}

```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
public with sharing class updateordernumber {
  public static void updateordernumber(List<Quotelineitem> inputqliList) {
    // Convert Trigger.new to a list of Quotelineitems
    List<Quotelineitem> qliList = (List<Quotelineitem>) inputqliList;

    // Initialize a map to store Quotelineitems based on their product families
    Map<String, List<Quotelineitem>> qliMap = new Map<String, List<Quotelineitem>>();

    // Initialize a map to keep track of the count of base unit Quotelineitems per family
    Map<String, Integer> baseUnitQliMap = new Map<String, Integer>();

    // Iterate through each Quotelineitem in the list
    for (Quotelineitem qli : qliList) {
      // Check if the Quotelineitem belongs to the 'Base Unit' family and is standalone
      if (qli.Product2.Family == 'Base Unit' && qli.Standalone__c == true) {
        // If standalone base unit, initialize the maps with 'Base Unit' as the key
        qliMap.put('Base Unit', new List<Quotelineitem>());
        baseUnitQliMap.put('Base Unit', 0);
      } else if (
        qli.Product2.Family == 'Base Unit' &&
        qli.Standalone__c == false
      ) {
        // If base unit but not standalone
        String key = qli.Base_Unit_Family__r.Name;
        if (baseUnitQliMap.containsKey(key)) {
          // Add to existing list and update count
          qliMap.get(key).add(qli);
          baseUnitQliMap.put(key, baseUnitQliMap.get(key) + 1);
        } else {
          // If family key doesn't exist, create a new list and update count
          List<Quotelineitem> valueList = new List<Quotelineitem>();
          valueList.add(qli);
          baseUnitQliMap.put(key, 1);
          qliMap.put(key, valueList);
        }
      } else if (qli.Product2.Family != 'Base Unit') {
        // If not a base unit, directly add to map using family as key
        qliMap.put(qli.Product2.Family, new List<Quotelineitem>());
        qliMap.get(qli.Product2.Family).add(qli);
      }
    }

    // Sort Quotelineitems based on their family and set the sort order
    if (!qliMap.isEmpty()) {
      Integer i = 0;
      for (String family : qliMap.keySet()) {
        for (Quotelineitem qli : qliMap.get(family)) {
          if (family == 'Base Unit') {
            // Set sort order with a different increment for base units
            qli.Sort_Order__c = i * 0.1;
            i++;
          } else {
            // Set sort order with regular increment for other families
            qli.Sort_Order__c = i;
            i++;
          }
        }
      }
    }
  }
}

```

## Methods
### `updateordernumber(inputqliList)`

#### Signature
```apex
public static void updateordernumber(List<Quotelineitem> inputqliList)
```

#### Parameters
| Name | Type | Description |
|------|------|-------------|
| inputqliList | List&lt;Quotelineitem&gt; |  |

#### Return Type
**void**