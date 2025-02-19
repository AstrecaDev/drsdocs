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

# DeleteQuoteLineItemsTest Class

`ISTEST`

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class DeleteQuoteLineItemsTest {
    @isTest
    static void testDeleteQuoteLines() {
        // Create a test QuoteLineItem
       
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
  
     /*   QuoteLineItem testQuoteLineItem = new QuoteLineItem(
            Quantity = 1,
            UnitPrice = 100,
            PricebookEntryId = standalonePBE.Id ,
            QuoteId = testQuote.ID
        );
        insert testQuoteLineItem; */

           List<QuoteLineItem> testQuoteLineItems = new List<QuoteLineItem>();
        for (Integer i = 0; i < 3; i++) {
            testQuoteLineItems.add(new QuoteLineItem(
                Quantity = 1,
                UnitPrice = 100 * (i + 1),
                QuoteId = testQuote.ID ,
                PricebookEntryId = standalonePBE.Id
            ));
        }
        insert testQuoteLineItems;

        // Get the Ids of the created QuoteLineItems
        List<Id> quoteLineItemIds = new List<Id>();
        for (QuoteLineItem qlItem : testQuoteLineItems) {
            quoteLineItemIds.add(qlItem.Id);
        }

        // Call the deleteQuoteLines method
        deleteQuoteLineItems.deleteQuoteLines(quoteLineItemIds);

        // Attempt to query the deleted QuoteLineItems
        List<QuoteLineItem> deletedQuoteLineItems = [SELECT Id FROM QuoteLineItem WHERE Id IN :quoteLineItemIds];
        System.assertEquals(0, deletedQuoteLineItems.size(), 'QuoteLineItems should be deleted');
       
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class DeleteQuoteLineItemsTest {
    @isTest
    static void testDeleteQuoteLines() {
        // Create a test QuoteLineItem
       
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
  
     /*   QuoteLineItem testQuoteLineItem = new QuoteLineItem(
            Quantity = 1,
            UnitPrice = 100,
            PricebookEntryId = standalonePBE.Id ,
            QuoteId = testQuote.ID
        );
        insert testQuoteLineItem; */

           List<QuoteLineItem> testQuoteLineItems = new List<QuoteLineItem>();
        for (Integer i = 0; i < 3; i++) {
            testQuoteLineItems.add(new QuoteLineItem(
                Quantity = 1,
                UnitPrice = 100 * (i + 1),
                QuoteId = testQuote.ID ,
                PricebookEntryId = standalonePBE.Id
            ));
        }
        insert testQuoteLineItems;

        // Get the Ids of the created QuoteLineItems
        List<Id> quoteLineItemIds = new List<Id>();
        for (QuoteLineItem qlItem : testQuoteLineItems) {
            quoteLineItemIds.add(qlItem.Id);
        }

        // Call the deleteQuoteLines method
        deleteQuoteLineItems.deleteQuoteLines(quoteLineItemIds);

        // Attempt to query the deleted QuoteLineItems
        List<QuoteLineItem> deletedQuoteLineItems = [SELECT Id FROM QuoteLineItem WHERE Id IN :quoteLineItemIds];
        System.assertEquals(0, deletedQuoteLineItems.size(), 'QuoteLineItems should be deleted');
       
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class DeleteQuoteLineItemsTest {
    @isTest
    static void testDeleteQuoteLines() {
        // Create a test QuoteLineItem
       
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
  
     /*   QuoteLineItem testQuoteLineItem = new QuoteLineItem(
            Quantity = 1,
            UnitPrice = 100,
            PricebookEntryId = standalonePBE.Id ,
            QuoteId = testQuote.ID
        );
        insert testQuoteLineItem; */

           List<QuoteLineItem> testQuoteLineItems = new List<QuoteLineItem>();
        for (Integer i = 0; i < 3; i++) {
            testQuoteLineItems.add(new QuoteLineItem(
                Quantity = 1,
                UnitPrice = 100 * (i + 1),
                QuoteId = testQuote.ID ,
                PricebookEntryId = standalonePBE.Id
            ));
        }
        insert testQuoteLineItems;

        // Get the Ids of the created QuoteLineItems
        List<Id> quoteLineItemIds = new List<Id>();
        for (QuoteLineItem qlItem : testQuoteLineItems) {
            quoteLineItemIds.add(qlItem.Id);
        }

        // Call the deleteQuoteLines method
        deleteQuoteLineItems.deleteQuoteLines(quoteLineItemIds);

        // Attempt to query the deleted QuoteLineItems
        List<QuoteLineItem> deletedQuoteLineItems = [SELECT Id FROM QuoteLineItem WHERE Id IN :quoteLineItemIds];
        System.assertEquals(0, deletedQuoteLineItems.size(), 'QuoteLineItems should be deleted');
       
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class DeleteQuoteLineItemsTest {
    @isTest
    static void testDeleteQuoteLines() {
        // Create a test QuoteLineItem
       
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
  
     /*   QuoteLineItem testQuoteLineItem = new QuoteLineItem(
            Quantity = 1,
            UnitPrice = 100,
            PricebookEntryId = standalonePBE.Id ,
            QuoteId = testQuote.ID
        );
        insert testQuoteLineItem; */

           List<QuoteLineItem> testQuoteLineItems = new List<QuoteLineItem>();
        for (Integer i = 0; i < 3; i++) {
            testQuoteLineItems.add(new QuoteLineItem(
                Quantity = 1,
                UnitPrice = 100 * (i + 1),
                QuoteId = testQuote.ID ,
                PricebookEntryId = standalonePBE.Id
            ));
        }
        insert testQuoteLineItems;

        // Get the Ids of the created QuoteLineItems
        List<Id> quoteLineItemIds = new List<Id>();
        for (QuoteLineItem qlItem : testQuoteLineItems) {
            quoteLineItemIds.add(qlItem.Id);
        }

        // Call the deleteQuoteLines method
        deleteQuoteLineItems.deleteQuoteLines(quoteLineItemIds);

        // Attempt to query the deleted QuoteLineItems
        List<QuoteLineItem> deletedQuoteLineItems = [SELECT Id FROM QuoteLineItem WHERE Id IN :quoteLineItemIds];
        System.assertEquals(0, deletedQuoteLineItems.size(), 'QuoteLineItems should be deleted');
       
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class DeleteQuoteLineItemsTest {
    @isTest
    static void testDeleteQuoteLines() {
        // Create a test QuoteLineItem
       
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
  
     /*   QuoteLineItem testQuoteLineItem = new QuoteLineItem(
            Quantity = 1,
            UnitPrice = 100,
            PricebookEntryId = standalonePBE.Id ,
            QuoteId = testQuote.ID
        );
        insert testQuoteLineItem; */

           List<QuoteLineItem> testQuoteLineItems = new List<QuoteLineItem>();
        for (Integer i = 0; i < 3; i++) {
            testQuoteLineItems.add(new QuoteLineItem(
                Quantity = 1,
                UnitPrice = 100 * (i + 1),
                QuoteId = testQuote.ID ,
                PricebookEntryId = standalonePBE.Id
            ));
        }
        insert testQuoteLineItems;

        // Get the Ids of the created QuoteLineItems
        List<Id> quoteLineItemIds = new List<Id>();
        for (QuoteLineItem qlItem : testQuoteLineItems) {
            quoteLineItemIds.add(qlItem.Id);
        }

        // Call the deleteQuoteLines method
        deleteQuoteLineItems.deleteQuoteLines(quoteLineItemIds);

        // Attempt to query the deleted QuoteLineItems
        List<QuoteLineItem> deletedQuoteLineItems = [SELECT Id FROM QuoteLineItem WHERE Id IN :quoteLineItemIds];
        System.assertEquals(0, deletedQuoteLineItems.size(), 'QuoteLineItems should be deleted');
       
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class DeleteQuoteLineItemsTest {
    @isTest
    static void testDeleteQuoteLines() {
        // Create a test QuoteLineItem
       
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
  
     /*   QuoteLineItem testQuoteLineItem = new QuoteLineItem(
            Quantity = 1,
            UnitPrice = 100,
            PricebookEntryId = standalonePBE.Id ,
            QuoteId = testQuote.ID
        );
        insert testQuoteLineItem; */

           List<QuoteLineItem> testQuoteLineItems = new List<QuoteLineItem>();
        for (Integer i = 0; i < 3; i++) {
            testQuoteLineItems.add(new QuoteLineItem(
                Quantity = 1,
                UnitPrice = 100 * (i + 1),
                QuoteId = testQuote.ID ,
                PricebookEntryId = standalonePBE.Id
            ));
        }
        insert testQuoteLineItems;

        // Get the Ids of the created QuoteLineItems
        List<Id> quoteLineItemIds = new List<Id>();
        for (QuoteLineItem qlItem : testQuoteLineItems) {
            quoteLineItemIds.add(qlItem.Id);
        }

        // Call the deleteQuoteLines method
        deleteQuoteLineItems.deleteQuoteLines(quoteLineItemIds);

        // Attempt to query the deleted QuoteLineItems
        List<QuoteLineItem> deletedQuoteLineItems = [SELECT Id FROM QuoteLineItem WHERE Id IN :quoteLineItemIds];
        System.assertEquals(0, deletedQuoteLineItems.size(), 'QuoteLineItems should be deleted');
       
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class DeleteQuoteLineItemsTest {
    @isTest
    static void testDeleteQuoteLines() {
        // Create a test QuoteLineItem
       
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
  
     /*   QuoteLineItem testQuoteLineItem = new QuoteLineItem(
            Quantity = 1,
            UnitPrice = 100,
            PricebookEntryId = standalonePBE.Id ,
            QuoteId = testQuote.ID
        );
        insert testQuoteLineItem; */

           List<QuoteLineItem> testQuoteLineItems = new List<QuoteLineItem>();
        for (Integer i = 0; i < 3; i++) {
            testQuoteLineItems.add(new QuoteLineItem(
                Quantity = 1,
                UnitPrice = 100 * (i + 1),
                QuoteId = testQuote.ID ,
                PricebookEntryId = standalonePBE.Id
            ));
        }
        insert testQuoteLineItems;

        // Get the Ids of the created QuoteLineItems
        List<Id> quoteLineItemIds = new List<Id>();
        for (QuoteLineItem qlItem : testQuoteLineItems) {
            quoteLineItemIds.add(qlItem.Id);
        }

        // Call the deleteQuoteLines method
        deleteQuoteLineItems.deleteQuoteLines(quoteLineItemIds);

        // Attempt to query the deleted QuoteLineItems
        List<QuoteLineItem> deletedQuoteLineItems = [SELECT Id FROM QuoteLineItem WHERE Id IN :quoteLineItemIds];
        System.assertEquals(0, deletedQuoteLineItems.size(), 'QuoteLineItems should be deleted');
       
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class DeleteQuoteLineItemsTest {
    @isTest
    static void testDeleteQuoteLines() {
        // Create a test QuoteLineItem
       
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
  
     /*   QuoteLineItem testQuoteLineItem = new QuoteLineItem(
            Quantity = 1,
            UnitPrice = 100,
            PricebookEntryId = standalonePBE.Id ,
            QuoteId = testQuote.ID
        );
        insert testQuoteLineItem; */

           List<QuoteLineItem> testQuoteLineItems = new List<QuoteLineItem>();
        for (Integer i = 0; i < 3; i++) {
            testQuoteLineItems.add(new QuoteLineItem(
                Quantity = 1,
                UnitPrice = 100 * (i + 1),
                QuoteId = testQuote.ID ,
                PricebookEntryId = standalonePBE.Id
            ));
        }
        insert testQuoteLineItems;

        // Get the Ids of the created QuoteLineItems
        List<Id> quoteLineItemIds = new List<Id>();
        for (QuoteLineItem qlItem : testQuoteLineItems) {
            quoteLineItemIds.add(qlItem.Id);
        }

        // Call the deleteQuoteLines method
        deleteQuoteLineItems.deleteQuoteLines(quoteLineItemIds);

        // Attempt to query the deleted QuoteLineItems
        List<QuoteLineItem> deletedQuoteLineItems = [SELECT Id FROM QuoteLineItem WHERE Id IN :quoteLineItemIds];
        System.assertEquals(0, deletedQuoteLineItems.size(), 'QuoteLineItems should be deleted');
       
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class DeleteQuoteLineItemsTest {
  @isTest
  static void testDeleteQuoteLines() {
    // Create a test QuoteLineItem

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

    /*   QuoteLineItem testQuoteLineItem = new QuoteLineItem(
            Quantity = 1,
            UnitPrice = 100,
            PricebookEntryId = standalonePBE.Id ,
            QuoteId = testQuote.ID
        );
        insert testQuoteLineItem; */

    List<QuoteLineItem> testQuoteLineItems = new List<QuoteLineItem>();
    for (Integer i = 0; i < 3; i++) {
      testQuoteLineItems.add(
        new QuoteLineItem(
          Quantity = 1,
          UnitPrice = 100 * (i + 1),
          QuoteId = testQuote.ID,
          PricebookEntryId = standalonePBE.Id
        )
      );
    }
    insert testQuoteLineItems;

    // Get the Ids of the created QuoteLineItems
    List<Id> quoteLineItemIds = new List<Id>();
    for (QuoteLineItem qlItem : testQuoteLineItems) {
      quoteLineItemIds.add(qlItem.Id);
    }

    // Call the deleteQuoteLines method
    deleteQuoteLineItems.deleteQuoteLines(quoteLineItemIds);

    // Attempt to query the deleted QuoteLineItems
    List<QuoteLineItem> deletedQuoteLineItems = [
      SELECT Id
      FROM QuoteLineItem
      WHERE Id IN :quoteLineItemIds
    ];
    System.assertEquals(
      0,
      deletedQuoteLineItems.size(),
      'QuoteLineItems should be deleted'
    );
  }
}

```

## Methods
### `testDeleteQuoteLines()`

`ISTEST`

#### Signature
```apex
private static void testDeleteQuoteLines()
```

#### Return Type
**void**