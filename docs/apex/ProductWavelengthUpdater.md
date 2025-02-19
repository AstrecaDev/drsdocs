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

# ProductWavelengthUpdater Class

This class updates the Wavelength__c field for Product2 records 
based on a numeric value found in the product name before the micrometer symbol (µm).

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
/**
 * @description This class updates the Wavelength__c field for Product2 records
 *              based on a numeric value found in the product name before the micrometer symbol (µm).
 */
public with sharing class ProductWavelengthUpdater {
    
    /**
     * @description Fetches Product2 records, extracts numeric wavelength values from their names 
     *              using regex, and updates the Wavelength__c field accordingly.
     * @notes       - The regex pattern captures numbers before the "µm" symbol.
     *              - It sets the extracted value in Wavelength__c field.
     *             - It uses bulk update to avoid multiple DML statements in loop.
     */
    public static void updateWavelengthFromProductName() {
        // Query for products with non-null names
        List<Product2> products = [SELECT Id, Name, Wavelength__c FROM Product2 WHERE Name != null WITH USER_MODE];
        List<Product2> productsToUpdate = new List<Product2>();

        // Regular expression to match a number before the micrometer symbol (µm)
        Pattern pattern = Pattern.compile('(\\d+(?:\\.\\d+)?)\\s*µm');

        for (Product2 product : products) {
            if (product.Name != null) {
                Matcher matcher = pattern.matcher(product.Name);

                if (matcher.find()) {
                    // Extract the numeric portion from the product name
                    String numberStr = matcher.group(1);
                    Decimal extractedNumber = Decimal.valueOf(numberStr);

                    // Update the Wavelength__c field
                   
                        product.Wavelength__c = extractedNumber;
                  
                    // Add the product to the list for bulk update
                    productsToUpdate.add(product);
                }
            }
        }

        // Bulk update to avoid multiple DML statements in loop
        if (!productsToUpdate.isEmpty()) {
            try {
                 Database.update(productsToUpdate, false,AccessLevel.User_mode);
            } catch (DmlException e) {
                System.debug('Error updating products: ' + e.getMessage());
            }
        }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
/**
 * @description This class updates the Wavelength__c field for Product2 records
 *              based on a numeric value found in the product name before the micrometer symbol (µm).
 */
public with sharing class ProductWavelengthUpdater {
    
    /**
     * @description Fetches Product2 records, extracts numeric wavelength values from their names 
     *              using regex, and updates the Wavelength__c field accordingly.
     * @notes       - The regex pattern captures numbers before the "µm" symbol.
     *              - It sets the extracted value in Wavelength__c field.
     *             - It uses bulk update to avoid multiple DML statements in loop.
     */
    public static void updateWavelengthFromProductName() {
        // Query for products with non-null names
        List<Product2> products = [SELECT Id, Name, Wavelength__c FROM Product2 WHERE Name != null WITH USER_MODE];
        List<Product2> productsToUpdate = new List<Product2>();

        // Regular expression to match a number before the micrometer symbol (µm)
        Pattern pattern = Pattern.compile('(\\d+(?:\\.\\d+)?)\\s*µm');

        for (Product2 product : products) {
            if (product.Name != null) {
                Matcher matcher = pattern.matcher(product.Name);

                if (matcher.find()) {
                    // Extract the numeric portion from the product name
                    String numberStr = matcher.group(1);
                    Decimal extractedNumber = Decimal.valueOf(numberStr);

                    // Update the Wavelength__c field
                   
                        product.Wavelength__c = extractedNumber;
                  
                    // Add the product to the list for bulk update
                    productsToUpdate.add(product);
                }
            }
        }

        // Bulk update to avoid multiple DML statements in loop
        if (!productsToUpdate.isEmpty()) {
            try {
                 Database.update(productsToUpdate, false,AccessLevel.User_mode);
            } catch (DmlException e) {
                System.debug('Error updating products: ' + e.getMessage());
            }
        }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
/**
 * @description This class updates the Wavelength__c field for Product2 records
 *              based on a numeric value found in the product name before the micrometer symbol (µm).
 */
public with sharing class ProductWavelengthUpdater {
    
    /**
     * @description Fetches Product2 records, extracts numeric wavelength values from their names 
     *              using regex, and updates the Wavelength__c field accordingly.
     * @notes       - The regex pattern captures numbers before the "µm" symbol.
     *              - It sets the extracted value in Wavelength__c field.
     *             - It uses bulk update to avoid multiple DML statements in loop.
     */
    public static void updateWavelengthFromProductName() {
        // Query for products with non-null names
        List<Product2> products = [SELECT Id, Name, Wavelength__c FROM Product2 WHERE Name != null WITH USER_MODE];
        List<Product2> productsToUpdate = new List<Product2>();

        // Regular expression to match a number before the micrometer symbol (µm)
        Pattern pattern = Pattern.compile('(\\d+(?:\\.\\d+)?)\\s*µm');

        for (Product2 product : products) {
            if (product.Name != null) {
                Matcher matcher = pattern.matcher(product.Name);

                if (matcher.find()) {
                    // Extract the numeric portion from the product name
                    String numberStr = matcher.group(1);
                    Decimal extractedNumber = Decimal.valueOf(numberStr);

                    // Update the Wavelength__c field
                   
                        product.Wavelength__c = extractedNumber;
                  
                    // Add the product to the list for bulk update
                    productsToUpdate.add(product);
                }
            }
        }

        // Bulk update to avoid multiple DML statements in loop
        if (!productsToUpdate.isEmpty()) {
            try {
                 Database.update(productsToUpdate, false,AccessLevel.User_mode);
            } catch (DmlException e) {
                System.debug('Error updating products: ' + e.getMessage());
            }
        }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
/**
 * @description This class updates the Wavelength__c field for Product2 records
 *              based on a numeric value found in the product name before the micrometer symbol (µm).
 */
public with sharing class ProductWavelengthUpdater {
    
    /**
     * @description Fetches Product2 records, extracts numeric wavelength values from their names 
     *              using regex, and updates the Wavelength__c field accordingly.
     * @notes       - The regex pattern captures numbers before the "µm" symbol.
     *              - It sets the extracted value in Wavelength__c field.
     *             - It uses bulk update to avoid multiple DML statements in loop.
     */
    public static void updateWavelengthFromProductName() {
        // Query for products with non-null names
        List<Product2> products = [SELECT Id, Name, Wavelength__c FROM Product2 WHERE Name != null WITH USER_MODE];
        List<Product2> productsToUpdate = new List<Product2>();

        // Regular expression to match a number before the micrometer symbol (µm)
        Pattern pattern = Pattern.compile('(\\d+(?:\\.\\d+)?)\\s*µm');

        for (Product2 product : products) {
            if (product.Name != null) {
                Matcher matcher = pattern.matcher(product.Name);

                if (matcher.find()) {
                    // Extract the numeric portion from the product name
                    String numberStr = matcher.group(1);
                    Decimal extractedNumber = Decimal.valueOf(numberStr);

                    // Update the Wavelength__c field
                   
                        product.Wavelength__c = extractedNumber;
                  
                    // Add the product to the list for bulk update
                    productsToUpdate.add(product);
                }
            }
        }

        // Bulk update to avoid multiple DML statements in loop
        if (!productsToUpdate.isEmpty()) {
            try {
                 Database.update(productsToUpdate, false,AccessLevel.User_mode);
            } catch (DmlException e) {
                System.debug('Error updating products: ' + e.getMessage());
            }
        }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
/**
 * @description This class updates the Wavelength__c field for Product2 records
 *              based on a numeric value found in the product name before the micrometer symbol (µm).
 */
public with sharing class ProductWavelengthUpdater {
    
    /**
     * @description Fetches Product2 records, extracts numeric wavelength values from their names 
     *              using regex, and updates the Wavelength__c field accordingly.
     * @notes       - The regex pattern captures numbers before the "µm" symbol.
     *              - It sets the extracted value in Wavelength__c field.
     *             - It uses bulk update to avoid multiple DML statements in loop.
     */
    public static void updateWavelengthFromProductName() {
        // Query for products with non-null names
        List<Product2> products = [SELECT Id, Name, Wavelength__c FROM Product2 WHERE Name != null WITH USER_MODE];
        List<Product2> productsToUpdate = new List<Product2>();

        // Regular expression to match a number before the micrometer symbol (µm)
        Pattern pattern = Pattern.compile('(\\d+(?:\\.\\d+)?)\\s*µm');

        for (Product2 product : products) {
            if (product.Name != null) {
                Matcher matcher = pattern.matcher(product.Name);

                if (matcher.find()) {
                    // Extract the numeric portion from the product name
                    String numberStr = matcher.group(1);
                    Decimal extractedNumber = Decimal.valueOf(numberStr);

                    // Update the Wavelength__c field
                   
                        product.Wavelength__c = extractedNumber;
                  
                    // Add the product to the list for bulk update
                    productsToUpdate.add(product);
                }
            }
        }

        // Bulk update to avoid multiple DML statements in loop
        if (!productsToUpdate.isEmpty()) {
            try {
                 Database.update(productsToUpdate, false,AccessLevel.User_mode);
            } catch (DmlException e) {
                System.debug('Error updating products: ' + e.getMessage());
            }
        }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
/**
 * @description This class updates the Wavelength__c field for Product2 records
 *              based on a numeric value found in the product name before the micrometer symbol (µm).
 */
public with sharing class ProductWavelengthUpdater {
    
    /**
     * @description Fetches Product2 records, extracts numeric wavelength values from their names 
     *              using regex, and updates the Wavelength__c field accordingly.
     * @notes       - The regex pattern captures numbers before the "µm" symbol.
     *              - It sets the extracted value in Wavelength__c field.
     *             - It uses bulk update to avoid multiple DML statements in loop.
     */
    public static void updateWavelengthFromProductName() {
        // Query for products with non-null names
        List<Product2> products = [SELECT Id, Name, Wavelength__c FROM Product2 WHERE Name != null WITH USER_MODE];
        List<Product2> productsToUpdate = new List<Product2>();

        // Regular expression to match a number before the micrometer symbol (µm)
        Pattern pattern = Pattern.compile('(\\d+(?:\\.\\d+)?)\\s*µm');

        for (Product2 product : products) {
            if (product.Name != null) {
                Matcher matcher = pattern.matcher(product.Name);

                if (matcher.find()) {
                    // Extract the numeric portion from the product name
                    String numberStr = matcher.group(1);
                    Decimal extractedNumber = Decimal.valueOf(numberStr);

                    // Update the Wavelength__c field
                   
                        product.Wavelength__c = extractedNumber;
                  
                    // Add the product to the list for bulk update
                    productsToUpdate.add(product);
                }
            }
        }

        // Bulk update to avoid multiple DML statements in loop
        if (!productsToUpdate.isEmpty()) {
            try {
                 Database.update(productsToUpdate, false,AccessLevel.User_mode);
            } catch (DmlException e) {
                System.debug('Error updating products: ' + e.getMessage());
            }
        }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
/**
 * @description This class updates the Wavelength__c field for Product2 records
 *              based on a numeric value found in the product name before the micrometer symbol (µm).
 */
public with sharing class ProductWavelengthUpdater {
    
    /**
     * @description Fetches Product2 records, extracts numeric wavelength values from their names 
     *              using regex, and updates the Wavelength__c field accordingly.
     * @notes       - The regex pattern captures numbers before the "µm" symbol.
     *              - It sets the extracted value in Wavelength__c field.
     *             - It uses bulk update to avoid multiple DML statements in loop.
     */
    public static void updateWavelengthFromProductName() {
        // Query for products with non-null names
        List<Product2> products = [SELECT Id, Name, Wavelength__c FROM Product2 WHERE Name != null WITH USER_MODE];
        List<Product2> productsToUpdate = new List<Product2>();

        // Regular expression to match a number before the micrometer symbol (µm)
        Pattern pattern = Pattern.compile('(\\d+(?:\\.\\d+)?)\\s*µm');

        for (Product2 product : products) {
            if (product.Name != null) {
                Matcher matcher = pattern.matcher(product.Name);

                if (matcher.find()) {
                    // Extract the numeric portion from the product name
                    String numberStr = matcher.group(1);
                    Decimal extractedNumber = Decimal.valueOf(numberStr);

                    // Update the Wavelength__c field
                   
                        product.Wavelength__c = extractedNumber;
                  
                    // Add the product to the list for bulk update
                    productsToUpdate.add(product);
                }
            }
        }

        // Bulk update to avoid multiple DML statements in loop
        if (!productsToUpdate.isEmpty()) {
            try {
                 Database.update(productsToUpdate, false,AccessLevel.User_mode);
            } catch (DmlException e) {
                System.debug('Error updating products: ' + e.getMessage());
            }
        }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
/**
 * @description This class updates the Wavelength__c field for Product2 records
 *              based on a numeric value found in the product name before the micrometer symbol (µm).
 */
public with sharing class ProductWavelengthUpdater {
    
    /**
     * @description Fetches Product2 records, extracts numeric wavelength values from their names 
     *              using regex, and updates the Wavelength__c field accordingly.
     * @notes       - The regex pattern captures numbers before the "µm" symbol.
     *              - It sets the extracted value in Wavelength__c field.
     *             - It uses bulk update to avoid multiple DML statements in loop.
     */
    public static void updateWavelengthFromProductName() {
        // Query for products with non-null names
        List<Product2> products = [SELECT Id, Name, Wavelength__c FROM Product2 WHERE Name != null WITH USER_MODE];
        List<Product2> productsToUpdate = new List<Product2>();

        // Regular expression to match a number before the micrometer symbol (µm)
        Pattern pattern = Pattern.compile('(\\d+(?:\\.\\d+)?)\\s*µm');

        for (Product2 product : products) {
            if (product.Name != null) {
                Matcher matcher = pattern.matcher(product.Name);

                if (matcher.find()) {
                    // Extract the numeric portion from the product name
                    String numberStr = matcher.group(1);
                    Decimal extractedNumber = Decimal.valueOf(numberStr);

                    // Update the Wavelength__c field
                   
                        product.Wavelength__c = extractedNumber;
                  
                    // Add the product to the list for bulk update
                    productsToUpdate.add(product);
                }
            }
        }

        // Bulk update to avoid multiple DML statements in loop
        if (!productsToUpdate.isEmpty()) {
            try {
                 Database.update(productsToUpdate, false,AccessLevel.User_mode);
            } catch (DmlException e) {
                System.debug('Error updating products: ' + e.getMessage());
            }
        }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
/**
 * @description This class updates the Wavelength__c field for Product2 records
 *              based on a numeric value found in the product name before the micrometer symbol (µm).
 */
public with sharing class ProductWavelengthUpdater {
  /**
   * @description Fetches Product2 records, extracts numeric wavelength values from their names
   *              using regex, and updates the Wavelength__c field accordingly.
   * @notes       - The regex pattern captures numbers before the "µm" symbol.
   *              - It sets the extracted value in Wavelength__c field.
   *             - It uses bulk update to avoid multiple DML statements in loop.
   */
  public static void updateWavelengthFromProductName() {
    // Query for products with non-null names
    List<Product2> products = [
      SELECT Id, Name, Wavelength__c
      FROM Product2
      WHERE Name != NULL
      WITH USER_MODE
    ];
    List<Product2> productsToUpdate = new List<Product2>();

    // Regular expression to match a number before the micrometer symbol (µm)
    Pattern pattern = Pattern.compile('(\\d+(?:\\.\\d+)?)\\s*µm');

    for (Product2 product : products) {
      if (product.Name != null) {
        Matcher matcher = pattern.matcher(product.Name);

        if (matcher.find()) {
          // Extract the numeric portion from the product name
          String numberStr = matcher.group(1);
          Decimal extractedNumber = Decimal.valueOf(numberStr);

          // Update the Wavelength__c field

          product.Wavelength__c = extractedNumber;

          // Add the product to the list for bulk update
          productsToUpdate.add(product);
        }
      }
    }

    // Bulk update to avoid multiple DML statements in loop
    if (!productsToUpdate.isEmpty()) {
      try {
        Database.update(productsToUpdate, false, AccessLevel.User_mode);
      } catch (DmlException e) {
        System.debug('Error updating products: ' + e.getMessage());
      }
    }
  }
}

```

## Methods
### `updateWavelengthFromProductName()`

Fetches Product2 records, extracts numeric wavelength values from their names 
using regex, and updates the Wavelength__c field accordingly.

**Notes** 

- The regex pattern captures numbers before the &quot;µm&quot; symbol. 
- It sets the extracted value in Wavelength__c field. 
- It uses bulk update to avoid multiple DML statements in loop.

#### Signature
```apex
public static void updateWavelengthFromProductName()
```

#### Return Type
**void**