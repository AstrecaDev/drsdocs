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

# OppLineItemControllerTest Class

`ISTEST`

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class OppLineItemControllerTest {

    @isTest
    static void testCreateOppLineItems() {
        
         Product2 standaloneProduct = new Product2(Name = 'Standalone Product', Type__c = 'Standalone');
        insert standaloneProduct;
        
        
            PricebookEntry standalonePBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = standaloneProduct.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert standalonePBE;
          
         // Create a test Account
        
        Account ac = new Account(name = 'testac');
        insert ac ;    
        
        // Create a test Opportunity
        Opportunity op = new Opportunity(name = 'test' , accountid = ac.id , Product__c = 'MIRcat' , Market_Segment__c = 'Other', StageName = 'Limbo',closedate= System.today());
        insert op ;
         
        
        
      /*  Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId = op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;
        */
             
        // Test data setup
        OppLineItemController.OppLineItemInput oppLineItemInput = new OppLineItemController.OppLineItemInput();
        oppLineItemInput.quoteid = op.id ;
        oppLineItemInput.Product2Id = standaloneProduct.Id;
        oppLineItemInput.Quantity = 10;
        oppLineItemInput.ListPrice = 100.00;
        oppLineItemInput.Optional = false;

        List<OppLineItemController.OppLineItemInput> oppLineItemInputs = new List<OppLineItemController.OppLineItemInput>();
        oppLineItemInputs.add(oppLineItemInput);

        String jsonString = JSON.serialize(oppLineItemInputs);

        // Test the createOppLineItems method
        Test.startTest();
        OppLineItemController.createOppLineItems(jsonString);
        Test.stopTest();

        // Verify the results
        List<OpportunityLineItem> insertedOppLineItems = [SELECT Id FROM OpportunityLineItem];
      //  System.assertEquals(1, insertedOppLineItems.size(), 'One OpportunityLineItem should be inserted');

        // Additional assertions can be added based on your specific requirements

    }

    @isTest
    static void testCreateOppLineItemsWithError() {
        // Test data setup with invalid data
        String invalidJsonString = '[{"quoteid": "Q123"}]';

        // Test the createOppLineItems method with invalid data
        Test.startTest();
        OppLineItemController.createOppLineItems(invalidJsonString);
        Test.stopTest();

        // Verify that no OpportunityLineItems are inserted due to the error
        List<OpportunityLineItem> insertedOppLineItems = [SELECT Id FROM OpportunityLineItem];
        System.assertEquals(0, insertedOppLineItems.size(), 'No OpportunityLineItem should be inserted due to the error');

        // Additional assertions can be added based on your specific requirements

    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class OppLineItemControllerTest {

    @isTest
    static void testCreateOppLineItems() {
        
         Product2 standaloneProduct = new Product2(Name = 'Standalone Product', Type__c = 'Standalone');
        insert standaloneProduct;
        
        
            PricebookEntry standalonePBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = standaloneProduct.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert standalonePBE;
          
         // Create a test Account
        
        Account ac = new Account(name = 'testac');
        insert ac ;    
        
        // Create a test Opportunity
        Opportunity op = new Opportunity(name = 'test' , accountid = ac.id , Product__c = 'MIRcat' , Market_Segment__c = 'Other', StageName = 'Limbo',closedate= System.today());
        insert op ;
         
        
        
      /*  Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId = op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;
        */
             
        // Test data setup
        OppLineItemController.OppLineItemInput oppLineItemInput = new OppLineItemController.OppLineItemInput();
        oppLineItemInput.quoteid = op.id ;
        oppLineItemInput.Product2Id = standaloneProduct.Id;
        oppLineItemInput.Quantity = 10;
        oppLineItemInput.ListPrice = 100.00;
        oppLineItemInput.Optional = false;

        List<OppLineItemController.OppLineItemInput> oppLineItemInputs = new List<OppLineItemController.OppLineItemInput>();
        oppLineItemInputs.add(oppLineItemInput);

        String jsonString = JSON.serialize(oppLineItemInputs);

        // Test the createOppLineItems method
        Test.startTest();
        OppLineItemController.createOppLineItems(jsonString);
        Test.stopTest();

        // Verify the results
        List<OpportunityLineItem> insertedOppLineItems = [SELECT Id FROM OpportunityLineItem];
      //  System.assertEquals(1, insertedOppLineItems.size(), 'One OpportunityLineItem should be inserted');

        // Additional assertions can be added based on your specific requirements

    }

    @isTest
    static void testCreateOppLineItemsWithError() {
        // Test data setup with invalid data
        String invalidJsonString = '[{"quoteid": "Q123"}]';

        // Test the createOppLineItems method with invalid data
        Test.startTest();
        OppLineItemController.createOppLineItems(invalidJsonString);
        Test.stopTest();

        // Verify that no OpportunityLineItems are inserted due to the error
        List<OpportunityLineItem> insertedOppLineItems = [SELECT Id FROM OpportunityLineItem];
        System.assertEquals(0, insertedOppLineItems.size(), 'No OpportunityLineItem should be inserted due to the error');

        // Additional assertions can be added based on your specific requirements

    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class OppLineItemControllerTest {

    @isTest
    static void testCreateOppLineItems() {
        
         Product2 standaloneProduct = new Product2(Name = 'Standalone Product', Type__c = 'Standalone');
        insert standaloneProduct;
        
        
            PricebookEntry standalonePBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = standaloneProduct.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert standalonePBE;
          
         // Create a test Account
        
        Account ac = new Account(name = 'testac');
        insert ac ;    
        
        // Create a test Opportunity
        Opportunity op = new Opportunity(name = 'test' , accountid = ac.id , Product__c = 'MIRcat' , Market_Segment__c = 'Other', StageName = 'Limbo',closedate= System.today());
        insert op ;
         
        
        
      /*  Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId = op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;
        */
             
        // Test data setup
        OppLineItemController.OppLineItemInput oppLineItemInput = new OppLineItemController.OppLineItemInput();
        oppLineItemInput.quoteid = op.id ;
        oppLineItemInput.Product2Id = standaloneProduct.Id;
        oppLineItemInput.Quantity = 10;
        oppLineItemInput.ListPrice = 100.00;
        oppLineItemInput.Optional = false;

        List<OppLineItemController.OppLineItemInput> oppLineItemInputs = new List<OppLineItemController.OppLineItemInput>();
        oppLineItemInputs.add(oppLineItemInput);

        String jsonString = JSON.serialize(oppLineItemInputs);

        // Test the createOppLineItems method
        Test.startTest();
        OppLineItemController.createOppLineItems(jsonString);
        Test.stopTest();

        // Verify the results
        List<OpportunityLineItem> insertedOppLineItems = [SELECT Id FROM OpportunityLineItem];
      //  System.assertEquals(1, insertedOppLineItems.size(), 'One OpportunityLineItem should be inserted');

        // Additional assertions can be added based on your specific requirements

    }

    @isTest
    static void testCreateOppLineItemsWithError() {
        // Test data setup with invalid data
        String invalidJsonString = '[{"quoteid": "Q123"}]';

        // Test the createOppLineItems method with invalid data
        Test.startTest();
        OppLineItemController.createOppLineItems(invalidJsonString);
        Test.stopTest();

        // Verify that no OpportunityLineItems are inserted due to the error
        List<OpportunityLineItem> insertedOppLineItems = [SELECT Id FROM OpportunityLineItem];
        System.assertEquals(0, insertedOppLineItems.size(), 'No OpportunityLineItem should be inserted due to the error');

        // Additional assertions can be added based on your specific requirements

    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class OppLineItemControllerTest {

    @isTest
    static void testCreateOppLineItems() {
        
         Product2 standaloneProduct = new Product2(Name = 'Standalone Product', Type__c = 'Standalone');
        insert standaloneProduct;
        
        
            PricebookEntry standalonePBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = standaloneProduct.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert standalonePBE;
          
         // Create a test Account
        
        Account ac = new Account(name = 'testac');
        insert ac ;    
        
        // Create a test Opportunity
        Opportunity op = new Opportunity(name = 'test' , accountid = ac.id , Product__c = 'MIRcat' , Market_Segment__c = 'Other', StageName = 'Limbo',closedate= System.today());
        insert op ;
         
        
        
      /*  Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId = op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;
        */
             
        // Test data setup
        OppLineItemController.OppLineItemInput oppLineItemInput = new OppLineItemController.OppLineItemInput();
        oppLineItemInput.quoteid = op.id ;
        oppLineItemInput.Product2Id = standaloneProduct.Id;
        oppLineItemInput.Quantity = 10;
        oppLineItemInput.ListPrice = 100.00;
        oppLineItemInput.Optional = false;

        List<OppLineItemController.OppLineItemInput> oppLineItemInputs = new List<OppLineItemController.OppLineItemInput>();
        oppLineItemInputs.add(oppLineItemInput);

        String jsonString = JSON.serialize(oppLineItemInputs);

        // Test the createOppLineItems method
        Test.startTest();
        OppLineItemController.createOppLineItems(jsonString);
        Test.stopTest();

        // Verify the results
        List<OpportunityLineItem> insertedOppLineItems = [SELECT Id FROM OpportunityLineItem];
      //  System.assertEquals(1, insertedOppLineItems.size(), 'One OpportunityLineItem should be inserted');

        // Additional assertions can be added based on your specific requirements

    }

    @isTest
    static void testCreateOppLineItemsWithError() {
        // Test data setup with invalid data
        String invalidJsonString = '[{"quoteid": "Q123"}]';

        // Test the createOppLineItems method with invalid data
        Test.startTest();
        OppLineItemController.createOppLineItems(invalidJsonString);
        Test.stopTest();

        // Verify that no OpportunityLineItems are inserted due to the error
        List<OpportunityLineItem> insertedOppLineItems = [SELECT Id FROM OpportunityLineItem];
        System.assertEquals(0, insertedOppLineItems.size(), 'No OpportunityLineItem should be inserted due to the error');

        // Additional assertions can be added based on your specific requirements

    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class OppLineItemControllerTest {

    @isTest
    static void testCreateOppLineItems() {
        
         Product2 standaloneProduct = new Product2(Name = 'Standalone Product', Type__c = 'Standalone');
        insert standaloneProduct;
        
        
            PricebookEntry standalonePBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = standaloneProduct.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert standalonePBE;
          
         // Create a test Account
        
        Account ac = new Account(name = 'testac');
        insert ac ;    
        
        // Create a test Opportunity
        Opportunity op = new Opportunity(name = 'test' , accountid = ac.id , Product__c = 'MIRcat' , Market_Segment__c = 'Other', StageName = 'Limbo',closedate= System.today());
        insert op ;
         
        
        
      /*  Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId = op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;
        */
             
        // Test data setup
        OppLineItemController.OppLineItemInput oppLineItemInput = new OppLineItemController.OppLineItemInput();
        oppLineItemInput.quoteid = op.id ;
        oppLineItemInput.Product2Id = standaloneProduct.Id;
        oppLineItemInput.Quantity = 10;
        oppLineItemInput.ListPrice = 100.00;
        oppLineItemInput.Optional = false;

        List<OppLineItemController.OppLineItemInput> oppLineItemInputs = new List<OppLineItemController.OppLineItemInput>();
        oppLineItemInputs.add(oppLineItemInput);

        String jsonString = JSON.serialize(oppLineItemInputs);

        // Test the createOppLineItems method
        Test.startTest();
        OppLineItemController.createOppLineItems(jsonString);
        Test.stopTest();

        // Verify the results
        List<OpportunityLineItem> insertedOppLineItems = [SELECT Id FROM OpportunityLineItem];
      //  System.assertEquals(1, insertedOppLineItems.size(), 'One OpportunityLineItem should be inserted');

        // Additional assertions can be added based on your specific requirements

    }

    @isTest
    static void testCreateOppLineItemsWithError() {
        // Test data setup with invalid data
        String invalidJsonString = '[{"quoteid": "Q123"}]';

        // Test the createOppLineItems method with invalid data
        Test.startTest();
        OppLineItemController.createOppLineItems(invalidJsonString);
        Test.stopTest();

        // Verify that no OpportunityLineItems are inserted due to the error
        List<OpportunityLineItem> insertedOppLineItems = [SELECT Id FROM OpportunityLineItem];
        System.assertEquals(0, insertedOppLineItems.size(), 'No OpportunityLineItem should be inserted due to the error');

        // Additional assertions can be added based on your specific requirements

    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class OppLineItemControllerTest {

    @isTest
    static void testCreateOppLineItems() {
        
         Product2 standaloneProduct = new Product2(Name = 'Standalone Product', Type__c = 'Standalone');
        insert standaloneProduct;
        
        
            PricebookEntry standalonePBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = standaloneProduct.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert standalonePBE;
          
         // Create a test Account
        
        Account ac = new Account(name = 'testac');
        insert ac ;    
        
        // Create a test Opportunity
        Opportunity op = new Opportunity(name = 'test' , accountid = ac.id , Product__c = 'MIRcat' , Market_Segment__c = 'Other', StageName = 'Limbo',closedate= System.today());
        insert op ;
         
        
        
      /*  Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId = op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;
        */
             
        // Test data setup
        OppLineItemController.OppLineItemInput oppLineItemInput = new OppLineItemController.OppLineItemInput();
        oppLineItemInput.quoteid = op.id ;
        oppLineItemInput.Product2Id = standaloneProduct.Id;
        oppLineItemInput.Quantity = 10;
        oppLineItemInput.ListPrice = 100.00;
        oppLineItemInput.Optional = false;

        List<OppLineItemController.OppLineItemInput> oppLineItemInputs = new List<OppLineItemController.OppLineItemInput>();
        oppLineItemInputs.add(oppLineItemInput);

        String jsonString = JSON.serialize(oppLineItemInputs);

        // Test the createOppLineItems method
        Test.startTest();
        OppLineItemController.createOppLineItems(jsonString);
        Test.stopTest();

        // Verify the results
        List<OpportunityLineItem> insertedOppLineItems = [SELECT Id FROM OpportunityLineItem];
      //  System.assertEquals(1, insertedOppLineItems.size(), 'One OpportunityLineItem should be inserted');

        // Additional assertions can be added based on your specific requirements

    }

    @isTest
    static void testCreateOppLineItemsWithError() {
        // Test data setup with invalid data
        String invalidJsonString = '[{"quoteid": "Q123"}]';

        // Test the createOppLineItems method with invalid data
        Test.startTest();
        OppLineItemController.createOppLineItems(invalidJsonString);
        Test.stopTest();

        // Verify that no OpportunityLineItems are inserted due to the error
        List<OpportunityLineItem> insertedOppLineItems = [SELECT Id FROM OpportunityLineItem];
        System.assertEquals(0, insertedOppLineItems.size(), 'No OpportunityLineItem should be inserted due to the error');

        // Additional assertions can be added based on your specific requirements

    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class OppLineItemControllerTest {

    @isTest
    static void testCreateOppLineItems() {
        
         Product2 standaloneProduct = new Product2(Name = 'Standalone Product', Type__c = 'Standalone');
        insert standaloneProduct;
        
        
            PricebookEntry standalonePBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = standaloneProduct.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert standalonePBE;
          
         // Create a test Account
        
        Account ac = new Account(name = 'testac');
        insert ac ;    
        
        // Create a test Opportunity
        Opportunity op = new Opportunity(name = 'test' , accountid = ac.id , Product__c = 'MIRcat' , Market_Segment__c = 'Other', StageName = 'Limbo',closedate= System.today());
        insert op ;
         
        
        
      /*  Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId = op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;
        */
             
        // Test data setup
        OppLineItemController.OppLineItemInput oppLineItemInput = new OppLineItemController.OppLineItemInput();
        oppLineItemInput.quoteid = op.id ;
        oppLineItemInput.Product2Id = standaloneProduct.Id;
        oppLineItemInput.Quantity = 10;
        oppLineItemInput.ListPrice = 100.00;
        oppLineItemInput.Optional = false;

        List<OppLineItemController.OppLineItemInput> oppLineItemInputs = new List<OppLineItemController.OppLineItemInput>();
        oppLineItemInputs.add(oppLineItemInput);

        String jsonString = JSON.serialize(oppLineItemInputs);

        // Test the createOppLineItems method
        Test.startTest();
        OppLineItemController.createOppLineItems(jsonString);
        Test.stopTest();

        // Verify the results
        List<OpportunityLineItem> insertedOppLineItems = [SELECT Id FROM OpportunityLineItem];
      //  System.assertEquals(1, insertedOppLineItems.size(), 'One OpportunityLineItem should be inserted');

        // Additional assertions can be added based on your specific requirements

    }

    @isTest
    static void testCreateOppLineItemsWithError() {
        // Test data setup with invalid data
        String invalidJsonString = '[{"quoteid": "Q123"}]';

        // Test the createOppLineItems method with invalid data
        Test.startTest();
        OppLineItemController.createOppLineItems(invalidJsonString);
        Test.stopTest();

        // Verify that no OpportunityLineItems are inserted due to the error
        List<OpportunityLineItem> insertedOppLineItems = [SELECT Id FROM OpportunityLineItem];
        System.assertEquals(0, insertedOppLineItems.size(), 'No OpportunityLineItem should be inserted due to the error');

        // Additional assertions can be added based on your specific requirements

    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class OppLineItemControllerTest {

    @isTest
    static void testCreateOppLineItems() {
        
         Product2 standaloneProduct = new Product2(Name = 'Standalone Product', Type__c = 'Standalone');
        insert standaloneProduct;
        
        
            PricebookEntry standalonePBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = standaloneProduct.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert standalonePBE;
          
         // Create a test Account
        
        Account ac = new Account(name = 'testac');
        insert ac ;    
        
        // Create a test Opportunity
        Opportunity op = new Opportunity(name = 'test' , accountid = ac.id , Product__c = 'MIRcat' , Market_Segment__c = 'Other', StageName = 'Limbo',closedate= System.today());
        insert op ;
         
        
        
      /*  Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId = op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;
        */
             
        // Test data setup
        OppLineItemController.OppLineItemInput oppLineItemInput = new OppLineItemController.OppLineItemInput();
        oppLineItemInput.quoteid = op.id ;
        oppLineItemInput.Product2Id = standaloneProduct.Id;
        oppLineItemInput.Quantity = 10;
        oppLineItemInput.ListPrice = 100.00;
        oppLineItemInput.Optional = false;

        List<OppLineItemController.OppLineItemInput> oppLineItemInputs = new List<OppLineItemController.OppLineItemInput>();
        oppLineItemInputs.add(oppLineItemInput);

        String jsonString = JSON.serialize(oppLineItemInputs);

        // Test the createOppLineItems method
        Test.startTest();
        OppLineItemController.createOppLineItems(jsonString);
        Test.stopTest();

        // Verify the results
        List<OpportunityLineItem> insertedOppLineItems = [SELECT Id FROM OpportunityLineItem];
      //  System.assertEquals(1, insertedOppLineItems.size(), 'One OpportunityLineItem should be inserted');

        // Additional assertions can be added based on your specific requirements

    }

    @isTest
    static void testCreateOppLineItemsWithError() {
        // Test data setup with invalid data
        String invalidJsonString = '[{"quoteid": "Q123"}]';

        // Test the createOppLineItems method with invalid data
        Test.startTest();
        OppLineItemController.createOppLineItems(invalidJsonString);
        Test.stopTest();

        // Verify that no OpportunityLineItems are inserted due to the error
        List<OpportunityLineItem> insertedOppLineItems = [SELECT Id FROM OpportunityLineItem];
        System.assertEquals(0, insertedOppLineItems.size(), 'No OpportunityLineItem should be inserted due to the error');

        // Additional assertions can be added based on your specific requirements

    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class OppLineItemControllerTest {
  @isTest
  static void testCreateOppLineItems() {
    Product2 standaloneProduct = new Product2(
      Name = 'Standalone Product',
      Type__c = 'Standalone'
    );
    insert standaloneProduct;

    PricebookEntry standalonePBE = new PricebookEntry(
      Pricebook2Id = Test.getStandardPricebookId(),
      Product2Id = standaloneProduct.Id,
      UnitPrice = 100,
      IsActive = true
    );
    insert standalonePBE;

    // Create a test Account

    Account ac = new Account(name = 'testac');
    insert ac;

    // Create a test Opportunity
    Opportunity op = new Opportunity(
      name = 'test',
      accountid = ac.id,
      Product__c = 'MIRcat',
      Market_Segment__c = 'Other',
      StageName = 'Limbo',
      closedate = System.today()
    );
    insert op;

    /*  Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId = op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;
        */

    // Test data setup
    OppLineItemController.OppLineItemInput oppLineItemInput = new OppLineItemController.OppLineItemInput();
    oppLineItemInput.quoteid = op.id;
    oppLineItemInput.Product2Id = standaloneProduct.Id;
    oppLineItemInput.Quantity = 10;
    oppLineItemInput.ListPrice = 100.00;
    oppLineItemInput.Optional = false;

    List<OppLineItemController.OppLineItemInput> oppLineItemInputs = new List<OppLineItemController.OppLineItemInput>();
    oppLineItemInputs.add(oppLineItemInput);

    String jsonString = JSON.serialize(oppLineItemInputs);

    // Test the createOppLineItems method
    Test.startTest();
    OppLineItemController.createOppLineItems(jsonString);
    Test.stopTest();

    // Verify the results
    List<OpportunityLineItem> insertedOppLineItems = [
      SELECT Id
      FROM OpportunityLineItem
    ];
    //  System.assertEquals(1, insertedOppLineItems.size(), 'One OpportunityLineItem should be inserted');

    // Additional assertions can be added based on your specific requirements
  }

  @isTest
  static void testCreateOppLineItemsWithError() {
    // Test data setup with invalid data
    String invalidJsonString = '[{"quoteid": "Q123"}]';

    // Test the createOppLineItems method with invalid data
    Test.startTest();
    OppLineItemController.createOppLineItems(invalidJsonString);
    Test.stopTest();

    // Verify that no OpportunityLineItems are inserted due to the error
    List<OpportunityLineItem> insertedOppLineItems = [
      SELECT Id
      FROM OpportunityLineItem
    ];
    System.assertEquals(
      0,
      insertedOppLineItems.size(),
      'No OpportunityLineItem should be inserted due to the error'
    );

    // Additional assertions can be added based on your specific requirements
  }
}

```

## Methods
### `testCreateOppLineItems()`

`ISTEST`

#### Signature
```apex
private static void testCreateOppLineItems()
```

#### Return Type
**void**

---

### `testCreateOppLineItemsWithError()`

`ISTEST`

#### Signature
```apex
private static void testCreateOppLineItemsWithError()
```

#### Return Type
**void**