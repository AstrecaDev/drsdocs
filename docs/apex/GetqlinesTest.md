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

# GetqlinesTest Class

`ISTEST`

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class GetqlinesTest {

    @isTest
    static void testGetQuoteLineItem() {
        // Create a test Quote 
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

        // Call the getQuoteLineItem method
        Test.startTest();
        List<QuoteLineItem> result = Getqlines.getQuoteLineItem(testQuote.Id);
        Test.stopTest();

        // Verify that the result is not null and contains the expected QuoteLineItem
        System.assertNotEquals(null, result, 'Result should not be null');
        System.assertEquals(1, result.size(), 'Result should contain one QuoteLineItem');
        System.assertEquals(testQuoteLineItem.Id, result[0].Id, 'Returned QuoteLineItem should match the created one');
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class GetqlinesTest {

    @isTest
    static void testGetQuoteLineItem() {
        // Create a test Quote 
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

        // Call the getQuoteLineItem method
        Test.startTest();
        List<QuoteLineItem> result = Getqlines.getQuoteLineItem(testQuote.Id);
        Test.stopTest();

        // Verify that the result is not null and contains the expected QuoteLineItem
        System.assertNotEquals(null, result, 'Result should not be null');
        System.assertEquals(1, result.size(), 'Result should contain one QuoteLineItem');
        System.assertEquals(testQuoteLineItem.Id, result[0].Id, 'Returned QuoteLineItem should match the created one');
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class GetqlinesTest {

    @isTest
    static void testGetQuoteLineItem() {
        // Create a test Quote 
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

        // Call the getQuoteLineItem method
        Test.startTest();
        List<QuoteLineItem> result = Getqlines.getQuoteLineItem(testQuote.Id);
        Test.stopTest();

        // Verify that the result is not null and contains the expected QuoteLineItem
        System.assertNotEquals(null, result, 'Result should not be null');
        System.assertEquals(1, result.size(), 'Result should contain one QuoteLineItem');
        System.assertEquals(testQuoteLineItem.Id, result[0].Id, 'Returned QuoteLineItem should match the created one');
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class GetqlinesTest {

    @isTest
    static void testGetQuoteLineItem() {
        // Create a test Quote 
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

        // Call the getQuoteLineItem method
        Test.startTest();
        List<QuoteLineItem> result = Getqlines.getQuoteLineItem(testQuote.Id);
        Test.stopTest();

        // Verify that the result is not null and contains the expected QuoteLineItem
        System.assertNotEquals(null, result, 'Result should not be null');
        System.assertEquals(1, result.size(), 'Result should contain one QuoteLineItem');
        System.assertEquals(testQuoteLineItem.Id, result[0].Id, 'Returned QuoteLineItem should match the created one');
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class GetqlinesTest {

    @isTest
    static void testGetQuoteLineItem() {
        // Create a test Quote 
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

        // Call the getQuoteLineItem method
        Test.startTest();
        List<QuoteLineItem> result = Getqlines.getQuoteLineItem(testQuote.Id);
        Test.stopTest();

        // Verify that the result is not null and contains the expected QuoteLineItem
        System.assertNotEquals(null, result, 'Result should not be null');
        System.assertEquals(1, result.size(), 'Result should contain one QuoteLineItem');
        System.assertEquals(testQuoteLineItem.Id, result[0].Id, 'Returned QuoteLineItem should match the created one');
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class GetqlinesTest {

    @isTest
    static void testGetQuoteLineItem() {
        // Create a test Quote 
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

        // Call the getQuoteLineItem method
        Test.startTest();
        List<QuoteLineItem> result = Getqlines.getQuoteLineItem(testQuote.Id);
        Test.stopTest();

        // Verify that the result is not null and contains the expected QuoteLineItem
        System.assertNotEquals(null, result, 'Result should not be null');
        System.assertEquals(1, result.size(), 'Result should contain one QuoteLineItem');
        System.assertEquals(testQuoteLineItem.Id, result[0].Id, 'Returned QuoteLineItem should match the created one');
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class GetqlinesTest {

    @isTest
    static void testGetQuoteLineItem() {
        // Create a test Quote 
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

        // Call the getQuoteLineItem method
        Test.startTest();
        List<QuoteLineItem> result = Getqlines.getQuoteLineItem(testQuote.Id);
        Test.stopTest();

        // Verify that the result is not null and contains the expected QuoteLineItem
        System.assertNotEquals(null, result, 'Result should not be null');
        System.assertEquals(1, result.size(), 'Result should contain one QuoteLineItem');
        System.assertEquals(testQuoteLineItem.Id, result[0].Id, 'Returned QuoteLineItem should match the created one');
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class GetqlinesTest {

    @isTest
    static void testGetQuoteLineItem() {
        // Create a test Quote 
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

        // Call the getQuoteLineItem method
        Test.startTest();
        List<QuoteLineItem> result = Getqlines.getQuoteLineItem(testQuote.Id);
        Test.stopTest();

        // Verify that the result is not null and contains the expected QuoteLineItem
        System.assertNotEquals(null, result, 'Result should not be null');
        System.assertEquals(1, result.size(), 'Result should contain one QuoteLineItem');
        System.assertEquals(testQuoteLineItem.Id, result[0].Id, 'Returned QuoteLineItem should match the created one');
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class GetqlinesTest {
  @isTest
  static void testGetQuoteLineItem() {
    // Create a test Quote
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

    // Call the getQuoteLineItem method
    Test.startTest();
    List<QuoteLineItem> result = Getqlines.getQuoteLineItem(testQuote.Id);
    Test.stopTest();

    // Verify that the result is not null and contains the expected QuoteLineItem
    System.assertNotEquals(null, result, 'Result should not be null');
    System.assertEquals(
      1,
      result.size(),
      'Result should contain one QuoteLineItem'
    );
    System.assertEquals(
      testQuoteLineItem.Id,
      result[0].Id,
      'Returned QuoteLineItem should match the created one'
    );
  }
}

```

## Methods
### `testGetQuoteLineItem()`

`ISTEST`

#### Signature
```apex
private static void testGetQuoteLineItem()
```

#### Return Type
**void**