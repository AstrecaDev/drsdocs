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

# QuoteLineItemControllerTest Class

`ISTEST`

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class QuoteLineItemControllerTest {

    @isTest
    static void testCreateQuoteLineItems() {
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
         
        
        
        Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId = op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;
  
        QuoteLineItem testQuoteLineItem = new QuoteLineItem(
            Quantity = 1,
            UnitPrice = 100,
            PricebookEntryId = standalonePBE.Id ,
            QuoteId = testQuote.ID
        );
        insert testQuoteLineItem;
        
        // Create a test QuoteLineItemInput
        QuoteLineItemController.QuoteLineItemInput testInput = new QuoteLineItemController.QuoteLineItemInput() ;
          testInput.quoteid = testQuote.Id ;
            testInput.Product2Id = standaloneProduct.Id ;
            testInput.Id = Test.getStandardPricebookId() ; // Set the PricebookEntryId to null for testing
            testInput.Quantity = 2 ;
            testInput.ListPrice = 100.00 ;
            testInput.Optional = false ;
            // Add more fields as needed
      // );

        // Convert the input to JSON
        String jsonString = JSON.serialize(new List<QuoteLineItemController.QuoteLineItemInput>{ testInput });

        // Call the createQuoteLineItems method
        Test.startTest();
        QuoteLineItemController.createQuoteLineItems(jsonString);
        Test.stopTest();

        // Verify that the QuoteLineItem is created
        List<QuoteLineItem> createdQuoteLineItems = [SELECT Id FROM QuoteLineItem WHERE QuoteId = :testQuote.Id];
        System.assertEquals(1, createdQuoteLineItems.size(), 'One QuoteLineItem should be created');

        // Clean up the created records
        delete createdQuoteLineItems;
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class QuoteLineItemControllerTest {

    @isTest
    static void testCreateQuoteLineItems() {
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
         
        
        
        Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId = op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;
  
        QuoteLineItem testQuoteLineItem = new QuoteLineItem(
            Quantity = 1,
            UnitPrice = 100,
            PricebookEntryId = standalonePBE.Id ,
            QuoteId = testQuote.ID
        );
        insert testQuoteLineItem;
        
        // Create a test QuoteLineItemInput
        QuoteLineItemController.QuoteLineItemInput testInput = new QuoteLineItemController.QuoteLineItemInput() ;
          testInput.quoteid = testQuote.Id ;
            testInput.Product2Id = standaloneProduct.Id ;
            testInput.Id = Test.getStandardPricebookId() ; // Set the PricebookEntryId to null for testing
            testInput.Quantity = 2 ;
            testInput.ListPrice = 100.00 ;
            testInput.Optional = false ;
            // Add more fields as needed
      // );

        // Convert the input to JSON
        String jsonString = JSON.serialize(new List<QuoteLineItemController.QuoteLineItemInput>{ testInput });

        // Call the createQuoteLineItems method
        Test.startTest();
        QuoteLineItemController.createQuoteLineItems(jsonString);
        Test.stopTest();

        // Verify that the QuoteLineItem is created
        List<QuoteLineItem> createdQuoteLineItems = [SELECT Id FROM QuoteLineItem WHERE QuoteId = :testQuote.Id];
        System.assertEquals(1, createdQuoteLineItems.size(), 'One QuoteLineItem should be created');

        // Clean up the created records
        delete createdQuoteLineItems;
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class QuoteLineItemControllerTest {

    @isTest
    static void testCreateQuoteLineItems() {
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
         
        
        
        Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId = op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;
  
        QuoteLineItem testQuoteLineItem = new QuoteLineItem(
            Quantity = 1,
            UnitPrice = 100,
            PricebookEntryId = standalonePBE.Id ,
            QuoteId = testQuote.ID
        );
        insert testQuoteLineItem;
        
        // Create a test QuoteLineItemInput
        QuoteLineItemController.QuoteLineItemInput testInput = new QuoteLineItemController.QuoteLineItemInput() ;
          testInput.quoteid = testQuote.Id ;
            testInput.Product2Id = standaloneProduct.Id ;
            testInput.Id = Test.getStandardPricebookId() ; // Set the PricebookEntryId to null for testing
            testInput.Quantity = 2 ;
            testInput.ListPrice = 100.00 ;
            testInput.Optional = false ;
            // Add more fields as needed
      // );

        // Convert the input to JSON
        String jsonString = JSON.serialize(new List<QuoteLineItemController.QuoteLineItemInput>{ testInput });

        // Call the createQuoteLineItems method
        Test.startTest();
        QuoteLineItemController.createQuoteLineItems(jsonString);
        Test.stopTest();

        // Verify that the QuoteLineItem is created
        List<QuoteLineItem> createdQuoteLineItems = [SELECT Id FROM QuoteLineItem WHERE QuoteId = :testQuote.Id];
        System.assertEquals(1, createdQuoteLineItems.size(), 'One QuoteLineItem should be created');

        // Clean up the created records
        delete createdQuoteLineItems;
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class QuoteLineItemControllerTest {

    @isTest
    static void testCreateQuoteLineItems() {
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
         
        
        
        Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId = op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;
  
        QuoteLineItem testQuoteLineItem = new QuoteLineItem(
            Quantity = 1,
            UnitPrice = 100,
            PricebookEntryId = standalonePBE.Id ,
            QuoteId = testQuote.ID
        );
        insert testQuoteLineItem;
        
        // Create a test QuoteLineItemInput
        QuoteLineItemController.QuoteLineItemInput testInput = new QuoteLineItemController.QuoteLineItemInput() ;
          testInput.quoteid = testQuote.Id ;
            testInput.Product2Id = standaloneProduct.Id ;
            testInput.Id = Test.getStandardPricebookId() ; // Set the PricebookEntryId to null for testing
            testInput.Quantity = 2 ;
            testInput.ListPrice = 100.00 ;
            testInput.Optional = false ;
            // Add more fields as needed
      // );

        // Convert the input to JSON
        String jsonString = JSON.serialize(new List<QuoteLineItemController.QuoteLineItemInput>{ testInput });

        // Call the createQuoteLineItems method
        Test.startTest();
        QuoteLineItemController.createQuoteLineItems(jsonString);
        Test.stopTest();

        // Verify that the QuoteLineItem is created
        List<QuoteLineItem> createdQuoteLineItems = [SELECT Id FROM QuoteLineItem WHERE QuoteId = :testQuote.Id];
        System.assertEquals(1, createdQuoteLineItems.size(), 'One QuoteLineItem should be created');

        // Clean up the created records
        delete createdQuoteLineItems;
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class QuoteLineItemControllerTest {

    @isTest
    static void testCreateQuoteLineItems() {
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
         
        
        
        Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId = op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;
  
        QuoteLineItem testQuoteLineItem = new QuoteLineItem(
            Quantity = 1,
            UnitPrice = 100,
            PricebookEntryId = standalonePBE.Id ,
            QuoteId = testQuote.ID
        );
        insert testQuoteLineItem;
        
        // Create a test QuoteLineItemInput
        QuoteLineItemController.QuoteLineItemInput testInput = new QuoteLineItemController.QuoteLineItemInput() ;
          testInput.quoteid = testQuote.Id ;
            testInput.Product2Id = standaloneProduct.Id ;
            testInput.Id = Test.getStandardPricebookId() ; // Set the PricebookEntryId to null for testing
            testInput.Quantity = 2 ;
            testInput.ListPrice = 100.00 ;
            testInput.Optional = false ;
            // Add more fields as needed
      // );

        // Convert the input to JSON
        String jsonString = JSON.serialize(new List<QuoteLineItemController.QuoteLineItemInput>{ testInput });

        // Call the createQuoteLineItems method
        Test.startTest();
        QuoteLineItemController.createQuoteLineItems(jsonString);
        Test.stopTest();

        // Verify that the QuoteLineItem is created
        List<QuoteLineItem> createdQuoteLineItems = [SELECT Id FROM QuoteLineItem WHERE QuoteId = :testQuote.Id];
        System.assertEquals(1, createdQuoteLineItems.size(), 'One QuoteLineItem should be created');

        // Clean up the created records
        delete createdQuoteLineItems;
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class QuoteLineItemControllerTest {

    @isTest
    static void testCreateQuoteLineItems() {
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
         
        
        
        Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId = op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;
  
        QuoteLineItem testQuoteLineItem = new QuoteLineItem(
            Quantity = 1,
            UnitPrice = 100,
            PricebookEntryId = standalonePBE.Id ,
            QuoteId = testQuote.ID
        );
        insert testQuoteLineItem;
        
        // Create a test QuoteLineItemInput
        QuoteLineItemController.QuoteLineItemInput testInput = new QuoteLineItemController.QuoteLineItemInput() ;
          testInput.quoteid = testQuote.Id ;
            testInput.Product2Id = standaloneProduct.Id ;
            testInput.Id = Test.getStandardPricebookId() ; // Set the PricebookEntryId to null for testing
            testInput.Quantity = 2 ;
            testInput.ListPrice = 100.00 ;
            testInput.Optional = false ;
            // Add more fields as needed
      // );

        // Convert the input to JSON
        String jsonString = JSON.serialize(new List<QuoteLineItemController.QuoteLineItemInput>{ testInput });

        // Call the createQuoteLineItems method
        Test.startTest();
        QuoteLineItemController.createQuoteLineItems(jsonString);
        Test.stopTest();

        // Verify that the QuoteLineItem is created
        List<QuoteLineItem> createdQuoteLineItems = [SELECT Id FROM QuoteLineItem WHERE QuoteId = :testQuote.Id];
        System.assertEquals(1, createdQuoteLineItems.size(), 'One QuoteLineItem should be created');

        // Clean up the created records
        delete createdQuoteLineItems;
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class QuoteLineItemControllerTest {

    @isTest
    static void testCreateQuoteLineItems() {
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
         
        
        
        Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId = op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;
  
        QuoteLineItem testQuoteLineItem = new QuoteLineItem(
            Quantity = 1,
            UnitPrice = 100,
            PricebookEntryId = standalonePBE.Id ,
            QuoteId = testQuote.ID
        );
        insert testQuoteLineItem;
        
        // Create a test QuoteLineItemInput
        QuoteLineItemController.QuoteLineItemInput testInput = new QuoteLineItemController.QuoteLineItemInput() ;
          testInput.quoteid = testQuote.Id ;
            testInput.Product2Id = standaloneProduct.Id ;
            testInput.Id = Test.getStandardPricebookId() ; // Set the PricebookEntryId to null for testing
            testInput.Quantity = 2 ;
            testInput.ListPrice = 100.00 ;
            testInput.Optional = false ;
            // Add more fields as needed
      // );

        // Convert the input to JSON
        String jsonString = JSON.serialize(new List<QuoteLineItemController.QuoteLineItemInput>{ testInput });

        // Call the createQuoteLineItems method
        Test.startTest();
        QuoteLineItemController.createQuoteLineItems(jsonString);
        Test.stopTest();

        // Verify that the QuoteLineItem is created
        List<QuoteLineItem> createdQuoteLineItems = [SELECT Id FROM QuoteLineItem WHERE QuoteId = :testQuote.Id];
        System.assertEquals(1, createdQuoteLineItems.size(), 'One QuoteLineItem should be created');

        // Clean up the created records
        delete createdQuoteLineItems;
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class QuoteLineItemControllerTest {

    @isTest
    static void testCreateQuoteLineItems() {
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
         
        
        
        Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId = op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;
  
        QuoteLineItem testQuoteLineItem = new QuoteLineItem(
            Quantity = 1,
            UnitPrice = 100,
            PricebookEntryId = standalonePBE.Id ,
            QuoteId = testQuote.ID
        );
        insert testQuoteLineItem;
        
        // Create a test QuoteLineItemInput
        QuoteLineItemController.QuoteLineItemInput testInput = new QuoteLineItemController.QuoteLineItemInput() ;
          testInput.quoteid = testQuote.Id ;
            testInput.Product2Id = standaloneProduct.Id ;
            testInput.Id = Test.getStandardPricebookId() ; // Set the PricebookEntryId to null for testing
            testInput.Quantity = 2 ;
            testInput.ListPrice = 100.00 ;
            testInput.Optional = false ;
            // Add more fields as needed
      // );

        // Convert the input to JSON
        String jsonString = JSON.serialize(new List<QuoteLineItemController.QuoteLineItemInput>{ testInput });

        // Call the createQuoteLineItems method
        Test.startTest();
        QuoteLineItemController.createQuoteLineItems(jsonString);
        Test.stopTest();

        // Verify that the QuoteLineItem is created
        List<QuoteLineItem> createdQuoteLineItems = [SELECT Id FROM QuoteLineItem WHERE QuoteId = :testQuote.Id];
        System.assertEquals(1, createdQuoteLineItems.size(), 'One QuoteLineItem should be created');

        // Clean up the created records
        delete createdQuoteLineItems;
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class QuoteLineItemControllerTest {
  @isTest
  static void testCreateQuoteLineItems() {
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

    Quote testQuote = new Quote(
      Name = 'Test Quote',
      OpportunityId = op.id,
      Pricebook2Id = Test.getStandardPricebookId()
    );
    insert testQuote;

    QuoteLineItem testQuoteLineItem = new QuoteLineItem(
      Quantity = 1,
      UnitPrice = 100,
      PricebookEntryId = standalonePBE.Id,
      QuoteId = testQuote.ID
    );
    insert testQuoteLineItem;

    // Create a test QuoteLineItemInput
    QuoteLineItemController.QuoteLineItemInput testInput = new QuoteLineItemController.QuoteLineItemInput();
    testInput.quoteid = testQuote.Id;
    testInput.Product2Id = standaloneProduct.Id;
    testInput.Id = Test.getStandardPricebookId(); // Set the PricebookEntryId to null for testing
    testInput.Quantity = 2;
    testInput.ListPrice = 100.00;
    testInput.Optional = false;
    // Add more fields as needed
    // );

    // Convert the input to JSON
    String jsonString = JSON.serialize(
      new List<QuoteLineItemController.QuoteLineItemInput>{ testInput }
    );

    // Call the createQuoteLineItems method
    Test.startTest();
    QuoteLineItemController.createQuoteLineItems(jsonString);
    Test.stopTest();

    // Verify that the QuoteLineItem is created
    List<QuoteLineItem> createdQuoteLineItems = [
      SELECT Id
      FROM QuoteLineItem
      WHERE QuoteId = :testQuote.Id
    ];
    System.assertEquals(
      1,
      createdQuoteLineItems.size(),
      'One QuoteLineItem should be created'
    );

    // Clean up the created records
    delete createdQuoteLineItems;
  }
}

```

## Methods
### `testCreateQuoteLineItems()`

`ISTEST`

#### Signature
```apex
private static void testCreateQuoteLineItems()
```

#### Return Type
**void**