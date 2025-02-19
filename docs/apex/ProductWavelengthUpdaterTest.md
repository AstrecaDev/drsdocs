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

# ProductWavelengthUpdaterTest Class

`ISTEST`

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class ProductWavelengthUpdaterTest {
    @testSetup
    static void setupTestData() {
        List<Product2> products = new List<Product2>{
            new Product2(Name = 'Laser 1550 µm', Wavelength__c = null),
            new Product2(Name = 'LED 650 µm', Wavelength__c = 100),
            new Product2(Name = 'Fiber 850 µm', Wavelength__c = null),
            new Product2(Name = 'No Wavelength Product', Wavelength__c = null)
        };
        insert products;
    }

    @isTest
    static void testUpdateWavelengthFromProductName() {
        // Run the method
        Test.startTest();
        ProductWavelengthUpdater.updateWavelengthFromProductName();
        Test.stopTest();

        // Query updated products
        List<Product2> updatedProducts = [SELECT Id, Name, Wavelength__c FROM Product2];
        Map<String, Decimal> expectedValues = new Map<String, Decimal>{
            'Laser 1550 µm' => 1550.000,
            'LED 650 µm' => 650.000, // 100 existing + 650 extracted
            'Fiber 850 µm' => 850.000,
            'No Wavelength Product' => null
        };

        // Validate results
        for (Product2 product : updatedProducts) {
            if (expectedValues.containsKey(product.Name)) {
                System.assertEquals(expectedValues.get(product.Name), product.Wavelength__c,
                    'Wavelength value mismatch for product: ' + product.Name);
            }
        }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class ProductWavelengthUpdaterTest {
    @testSetup
    static void setupTestData() {
        List<Product2> products = new List<Product2>{
            new Product2(Name = 'Laser 1550 µm', Wavelength__c = null),
            new Product2(Name = 'LED 650 µm', Wavelength__c = 100),
            new Product2(Name = 'Fiber 850 µm', Wavelength__c = null),
            new Product2(Name = 'No Wavelength Product', Wavelength__c = null)
        };
        insert products;
    }

    @isTest
    static void testUpdateWavelengthFromProductName() {
        // Run the method
        Test.startTest();
        ProductWavelengthUpdater.updateWavelengthFromProductName();
        Test.stopTest();

        // Query updated products
        List<Product2> updatedProducts = [SELECT Id, Name, Wavelength__c FROM Product2];
        Map<String, Decimal> expectedValues = new Map<String, Decimal>{
            'Laser 1550 µm' => 1550.000,
            'LED 650 µm' => 650.000, // 100 existing + 650 extracted
            'Fiber 850 µm' => 850.000,
            'No Wavelength Product' => null
        };

        // Validate results
        for (Product2 product : updatedProducts) {
            if (expectedValues.containsKey(product.Name)) {
                System.assertEquals(expectedValues.get(product.Name), product.Wavelength__c,
                    'Wavelength value mismatch for product: ' + product.Name);
            }
        }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class ProductWavelengthUpdaterTest {
    @testSetup
    static void setupTestData() {
        List<Product2> products = new List<Product2>{
            new Product2(Name = 'Laser 1550 µm', Wavelength__c = null),
            new Product2(Name = 'LED 650 µm', Wavelength__c = 100),
            new Product2(Name = 'Fiber 850 µm', Wavelength__c = null),
            new Product2(Name = 'No Wavelength Product', Wavelength__c = null)
        };
        insert products;
    }

    @isTest
    static void testUpdateWavelengthFromProductName() {
        // Run the method
        Test.startTest();
        ProductWavelengthUpdater.updateWavelengthFromProductName();
        Test.stopTest();

        // Query updated products
        List<Product2> updatedProducts = [SELECT Id, Name, Wavelength__c FROM Product2];
        Map<String, Decimal> expectedValues = new Map<String, Decimal>{
            'Laser 1550 µm' => 1550.000,
            'LED 650 µm' => 650.000, // 100 existing + 650 extracted
            'Fiber 850 µm' => 850.000,
            'No Wavelength Product' => null
        };

        // Validate results
        for (Product2 product : updatedProducts) {
            if (expectedValues.containsKey(product.Name)) {
                System.assertEquals(expectedValues.get(product.Name), product.Wavelength__c,
                    'Wavelength value mismatch for product: ' + product.Name);
            }
        }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class ProductWavelengthUpdaterTest {
    @testSetup
    static void setupTestData() {
        List<Product2> products = new List<Product2>{
            new Product2(Name = 'Laser 1550 µm', Wavelength__c = null),
            new Product2(Name = 'LED 650 µm', Wavelength__c = 100),
            new Product2(Name = 'Fiber 850 µm', Wavelength__c = null),
            new Product2(Name = 'No Wavelength Product', Wavelength__c = null)
        };
        insert products;
    }

    @isTest
    static void testUpdateWavelengthFromProductName() {
        // Run the method
        Test.startTest();
        ProductWavelengthUpdater.updateWavelengthFromProductName();
        Test.stopTest();

        // Query updated products
        List<Product2> updatedProducts = [SELECT Id, Name, Wavelength__c FROM Product2];
        Map<String, Decimal> expectedValues = new Map<String, Decimal>{
            'Laser 1550 µm' => 1550.000,
            'LED 650 µm' => 650.000, // 100 existing + 650 extracted
            'Fiber 850 µm' => 850.000,
            'No Wavelength Product' => null
        };

        // Validate results
        for (Product2 product : updatedProducts) {
            if (expectedValues.containsKey(product.Name)) {
                System.assertEquals(expectedValues.get(product.Name), product.Wavelength__c,
                    'Wavelength value mismatch for product: ' + product.Name);
            }
        }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class ProductWavelengthUpdaterTest {
    @testSetup
    static void setupTestData() {
        List<Product2> products = new List<Product2>{
            new Product2(Name = 'Laser 1550 µm', Wavelength__c = null),
            new Product2(Name = 'LED 650 µm', Wavelength__c = 100),
            new Product2(Name = 'Fiber 850 µm', Wavelength__c = null),
            new Product2(Name = 'No Wavelength Product', Wavelength__c = null)
        };
        insert products;
    }

    @isTest
    static void testUpdateWavelengthFromProductName() {
        // Run the method
        Test.startTest();
        ProductWavelengthUpdater.updateWavelengthFromProductName();
        Test.stopTest();

        // Query updated products
        List<Product2> updatedProducts = [SELECT Id, Name, Wavelength__c FROM Product2];
        Map<String, Decimal> expectedValues = new Map<String, Decimal>{
            'Laser 1550 µm' => 1550.000,
            'LED 650 µm' => 650.000, // 100 existing + 650 extracted
            'Fiber 850 µm' => 850.000,
            'No Wavelength Product' => null
        };

        // Validate results
        for (Product2 product : updatedProducts) {
            if (expectedValues.containsKey(product.Name)) {
                System.assertEquals(expectedValues.get(product.Name), product.Wavelength__c,
                    'Wavelength value mismatch for product: ' + product.Name);
            }
        }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class ProductWavelengthUpdaterTest {
    @testSetup
    static void setupTestData() {
        List<Product2> products = new List<Product2>{
            new Product2(Name = 'Laser 1550 µm', Wavelength__c = null),
            new Product2(Name = 'LED 650 µm', Wavelength__c = 100),
            new Product2(Name = 'Fiber 850 µm', Wavelength__c = null),
            new Product2(Name = 'No Wavelength Product', Wavelength__c = null)
        };
        insert products;
    }

    @isTest
    static void testUpdateWavelengthFromProductName() {
        // Run the method
        Test.startTest();
        ProductWavelengthUpdater.updateWavelengthFromProductName();
        Test.stopTest();

        // Query updated products
        List<Product2> updatedProducts = [SELECT Id, Name, Wavelength__c FROM Product2];
        Map<String, Decimal> expectedValues = new Map<String, Decimal>{
            'Laser 1550 µm' => 1550.000,
            'LED 650 µm' => 650.000, // 100 existing + 650 extracted
            'Fiber 850 µm' => 850.000,
            'No Wavelength Product' => null
        };

        // Validate results
        for (Product2 product : updatedProducts) {
            if (expectedValues.containsKey(product.Name)) {
                System.assertEquals(expectedValues.get(product.Name), product.Wavelength__c,
                    'Wavelength value mismatch for product: ' + product.Name);
            }
        }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class ProductWavelengthUpdaterTest {
    @testSetup
    static void setupTestData() {
        List<Product2> products = new List<Product2>{
            new Product2(Name = 'Laser 1550 µm', Wavelength__c = null),
            new Product2(Name = 'LED 650 µm', Wavelength__c = 100),
            new Product2(Name = 'Fiber 850 µm', Wavelength__c = null),
            new Product2(Name = 'No Wavelength Product', Wavelength__c = null)
        };
        insert products;
    }

    @isTest
    static void testUpdateWavelengthFromProductName() {
        // Run the method
        Test.startTest();
        ProductWavelengthUpdater.updateWavelengthFromProductName();
        Test.stopTest();

        // Query updated products
        List<Product2> updatedProducts = [SELECT Id, Name, Wavelength__c FROM Product2];
        Map<String, Decimal> expectedValues = new Map<String, Decimal>{
            'Laser 1550 µm' => 1550.000,
            'LED 650 µm' => 650.000, // 100 existing + 650 extracted
            'Fiber 850 µm' => 850.000,
            'No Wavelength Product' => null
        };

        // Validate results
        for (Product2 product : updatedProducts) {
            if (expectedValues.containsKey(product.Name)) {
                System.assertEquals(expectedValues.get(product.Name), product.Wavelength__c,
                    'Wavelength value mismatch for product: ' + product.Name);
            }
        }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class ProductWavelengthUpdaterTest {
    @testSetup
    static void setupTestData() {
        List<Product2> products = new List<Product2>{
            new Product2(Name = 'Laser 1550 µm', Wavelength__c = null),
            new Product2(Name = 'LED 650 µm', Wavelength__c = 100),
            new Product2(Name = 'Fiber 850 µm', Wavelength__c = null),
            new Product2(Name = 'No Wavelength Product', Wavelength__c = null)
        };
        insert products;
    }

    @isTest
    static void testUpdateWavelengthFromProductName() {
        // Run the method
        Test.startTest();
        ProductWavelengthUpdater.updateWavelengthFromProductName();
        Test.stopTest();

        // Query updated products
        List<Product2> updatedProducts = [SELECT Id, Name, Wavelength__c FROM Product2];
        Map<String, Decimal> expectedValues = new Map<String, Decimal>{
            'Laser 1550 µm' => 1550.000,
            'LED 650 µm' => 650.000, // 100 existing + 650 extracted
            'Fiber 850 µm' => 850.000,
            'No Wavelength Product' => null
        };

        // Validate results
        for (Product2 product : updatedProducts) {
            if (expectedValues.containsKey(product.Name)) {
                System.assertEquals(expectedValues.get(product.Name), product.Wavelength__c,
                    'Wavelength value mismatch for product: ' + product.Name);
            }
        }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class ProductWavelengthUpdaterTest {
  @testSetup
  static void setupTestData() {
    List<Product2> products = new List<Product2>{
      new Product2(Name = 'Laser 1550 µm', Wavelength__c = null),
      new Product2(Name = 'LED 650 µm', Wavelength__c = 100),
      new Product2(Name = 'Fiber 850 µm', Wavelength__c = null),
      new Product2(Name = 'No Wavelength Product', Wavelength__c = null)
    };
    insert products;
  }

  @isTest
  static void testUpdateWavelengthFromProductName() {
    // Run the method
    Test.startTest();
    ProductWavelengthUpdater.updateWavelengthFromProductName();
    Test.stopTest();

    // Query updated products
    List<Product2> updatedProducts = [
      SELECT Id, Name, Wavelength__c
      FROM Product2
    ];
    Map<String, Decimal> expectedValues = new Map<String, Decimal>{
      'Laser 1550 µm' => 1550.000,
      'LED 650 µm' => 650.000, // 100 existing + 650 extracted
      'Fiber 850 µm' => 850.000,
      'No Wavelength Product' => null
    };

    // Validate results
    for (Product2 product : updatedProducts) {
      if (expectedValues.containsKey(product.Name)) {
        System.assertEquals(
          expectedValues.get(product.Name),
          product.Wavelength__c,
          'Wavelength value mismatch for product: ' + product.Name
        );
      }
    }
  }
}

```

## Methods
### `setupTestData()`

`TESTSETUP`

#### Signature
```apex
private static void setupTestData()
```

#### Return Type
**void**

---

### `testUpdateWavelengthFromProductName()`

`ISTEST`

#### Signature
```apex
private static void testUpdateWavelengthFromProductName()
```

#### Return Type
**void**