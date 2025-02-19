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

# QuoteLineItemsExtensionTest Class

`ISTEST`

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class QuoteLineItemsExtensionTest {
    @isTest
    static void testQuoteLineItemsExtension() {
        // Create a test Pricebook
        Pricebook2 testPricebook = new Pricebook2(Name = 'Test Pricebook', IsActive = true);
        insert testPricebook;
        
        // Create a test Account
        
        Account ac = new Account(name = 'testac');
        insert ac ;    
        
        // Create a test Opportunity
        Opportunity op = new Opportunity(name = 'test' , accountid = ac.id , Product__c = 'MIRcat' , Market_Segment__c = 'Other', StageName = 'Limbo',closedate= System.today());
        insert op ;
         
       
        
        // Create a test Quote record associated with the test Pricebook
        Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId =  op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;

        // Create test Product records
        Product2 standaloneProduct = new Product2(Name = 'Standalone Product', Type__c = 'Standalone');
        insert standaloneProduct;

        Product2 mircatProduct = new Product2(Name = 'MIRCAT Product', Type__c = 'Options');
        insert mircatProduct;

        Product2 baseUnitProduct = new Product2(Name = 'Base Unit Product', Type__c = 'Base Unit');
        insert baseUnitProduct;

    //    insert new PriceBookEntry(Product2Id=pro2.Id, Pricebook2Id=Test.getStandardPricebookId(), UnitPrice=0);
        
        
        
        // Create test PricebookEntries for the test Pricebook
        PricebookEntry standalonePBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = standaloneProduct.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert standalonePBE;

        PricebookEntry mircatPBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = mircatProduct.Id,
            UnitPrice = 150,
            IsActive = true
        );
        insert mircatPBE;

        PricebookEntry baseUnitPBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = baseUnitProduct.Id,
            UnitPrice = 200,
            IsActive = true
        );
        insert baseUnitPBE;

        //PricebookEntryId, UnitPrice
        
        // Create test QuoteLineItem records
        QuoteLineItem standaloneQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = standaloneProduct.Id,
            Quantity = 1,
            PricebookEntryId = standalonePBE.Id,
            UnitPrice = 100
        );
        insert standaloneQLI;

        QuoteLineItem mircatQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = mircatProduct.Id,
            Quantity = 2,
            PricebookEntryId = mircatPBE.Id,
            UnitPrice = 200,
            MSRP__c= 80,
            ISP__c =50
        );
        insert mircatQLI;

        QuoteLineItem baseUnitQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = baseUnitProduct.Id,
            Quantity = 3,
             PricebookEntryId = baseUnitPBE.Id,
            UnitPrice = 300,
             MSRP__c= 100,
            ISP__c =60

        );
        insert baseUnitQLI;

        // Set up a test page and controller
        PageReference pageRef = Page.newquote; // Replace 'YourPage' with the actual page name
        Test.setCurrentPage(pageRef);

        ApexPages.StandardController stdController = new ApexPages.StandardController(testQuote);

        // Instantiate the QuoteLineItemsExtension class
        QuoteLineItemsExtension extension = new QuoteLineItemsExtension(stdController);

        // Verify that the extension properties are set correctly
        System.assertEquals(testQuote.Id, extension.CurrentQuote.Id, 'CurrentQuote Id should match');
        System.assertNotEquals(null, extension.QuoteLineItems, 'QuoteLineItems should not be null');
        System.assertNotEquals(null, extension.MircatQLIs, 'MircatQLIs should not be null');
        System.assertNotEquals(null, extension.BUnitMQLIs, 'BUnitMQLIs should not be null');

        // Add additional assertions based on your business logic

        // For example, check if the QuoteLineItems property contains the correct records
        System.assertEquals(1, extension.QuoteLineItems.size(), 'There should be one QuoteLineItem');
        System.assertEquals(1, extension.MircatQLIs.size(), 'There should be one MircatQLIs');
        System.assertEquals(1, extension.BUnitMQLIs.size(), 'There should be one BUnitMQLIs');

        // Add more test assertions as needed
        System.assertEquals(null, extension.totalCSSClass, 'CSS class should be totalstdpbk'); 
        System.assertEquals(null, extension.totaltxtCSSClass, 'CSS class should be totaltxtstdpbk'); 
        
        
        
        
        
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class QuoteLineItemsExtensionTest {
    @isTest
    static void testQuoteLineItemsExtension() {
        // Create a test Pricebook
        Pricebook2 testPricebook = new Pricebook2(Name = 'Test Pricebook', IsActive = true);
        insert testPricebook;
        
        // Create a test Account
        
        Account ac = new Account(name = 'testac');
        insert ac ;    
        
        // Create a test Opportunity
        Opportunity op = new Opportunity(name = 'test' , accountid = ac.id , Product__c = 'MIRcat' , Market_Segment__c = 'Other', StageName = 'Limbo',closedate= System.today());
        insert op ;
         
       
        
        // Create a test Quote record associated with the test Pricebook
        Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId =  op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;

        // Create test Product records
        Product2 standaloneProduct = new Product2(Name = 'Standalone Product', Type__c = 'Standalone');
        insert standaloneProduct;

        Product2 mircatProduct = new Product2(Name = 'MIRCAT Product', Type__c = 'Options');
        insert mircatProduct;

        Product2 baseUnitProduct = new Product2(Name = 'Base Unit Product', Type__c = 'Base Unit');
        insert baseUnitProduct;

    //    insert new PriceBookEntry(Product2Id=pro2.Id, Pricebook2Id=Test.getStandardPricebookId(), UnitPrice=0);
        
        
        
        // Create test PricebookEntries for the test Pricebook
        PricebookEntry standalonePBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = standaloneProduct.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert standalonePBE;

        PricebookEntry mircatPBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = mircatProduct.Id,
            UnitPrice = 150,
            IsActive = true
        );
        insert mircatPBE;

        PricebookEntry baseUnitPBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = baseUnitProduct.Id,
            UnitPrice = 200,
            IsActive = true
        );
        insert baseUnitPBE;

        //PricebookEntryId, UnitPrice
        
        // Create test QuoteLineItem records
        QuoteLineItem standaloneQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = standaloneProduct.Id,
            Quantity = 1,
            PricebookEntryId = standalonePBE.Id,
            UnitPrice = 100
        );
        insert standaloneQLI;

        QuoteLineItem mircatQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = mircatProduct.Id,
            Quantity = 2,
            PricebookEntryId = mircatPBE.Id,
            UnitPrice = 200,
            MSRP__c= 80,
            ISP__c =50
        );
        insert mircatQLI;

        QuoteLineItem baseUnitQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = baseUnitProduct.Id,
            Quantity = 3,
             PricebookEntryId = baseUnitPBE.Id,
            UnitPrice = 300,
             MSRP__c= 100,
            ISP__c =60

        );
        insert baseUnitQLI;

        // Set up a test page and controller
        PageReference pageRef = Page.newquote; // Replace 'YourPage' with the actual page name
        Test.setCurrentPage(pageRef);

        ApexPages.StandardController stdController = new ApexPages.StandardController(testQuote);

        // Instantiate the QuoteLineItemsExtension class
        QuoteLineItemsExtension extension = new QuoteLineItemsExtension(stdController);

        // Verify that the extension properties are set correctly
        System.assertEquals(testQuote.Id, extension.CurrentQuote.Id, 'CurrentQuote Id should match');
        System.assertNotEquals(null, extension.QuoteLineItems, 'QuoteLineItems should not be null');
        System.assertNotEquals(null, extension.MircatQLIs, 'MircatQLIs should not be null');
        System.assertNotEquals(null, extension.BUnitMQLIs, 'BUnitMQLIs should not be null');

        // Add additional assertions based on your business logic

        // For example, check if the QuoteLineItems property contains the correct records
        System.assertEquals(1, extension.QuoteLineItems.size(), 'There should be one QuoteLineItem');
        System.assertEquals(1, extension.MircatQLIs.size(), 'There should be one MircatQLIs');
        System.assertEquals(1, extension.BUnitMQLIs.size(), 'There should be one BUnitMQLIs');

        // Add more test assertions as needed
        System.assertEquals(null, extension.totalCSSClass, 'CSS class should be totalstdpbk'); 
        System.assertEquals(null, extension.totaltxtCSSClass, 'CSS class should be totaltxtstdpbk'); 
        
        
        
        
        
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class QuoteLineItemsExtensionTest {
    @isTest
    static void testQuoteLineItemsExtension() {
        // Create a test Pricebook
        Pricebook2 testPricebook = new Pricebook2(Name = 'Test Pricebook', IsActive = true);
        insert testPricebook;
        
        // Create a test Account
        
        Account ac = new Account(name = 'testac');
        insert ac ;    
        
        // Create a test Opportunity
        Opportunity op = new Opportunity(name = 'test' , accountid = ac.id , Product__c = 'MIRcat' , Market_Segment__c = 'Other', StageName = 'Limbo',closedate= System.today());
        insert op ;
         
       
        
        // Create a test Quote record associated with the test Pricebook
        Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId =  op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;

        // Create test Product records
        Product2 standaloneProduct = new Product2(Name = 'Standalone Product', Type__c = 'Standalone');
        insert standaloneProduct;

        Product2 mircatProduct = new Product2(Name = 'MIRCAT Product', Type__c = 'Options');
        insert mircatProduct;

        Product2 baseUnitProduct = new Product2(Name = 'Base Unit Product', Type__c = 'Base Unit');
        insert baseUnitProduct;

    //    insert new PriceBookEntry(Product2Id=pro2.Id, Pricebook2Id=Test.getStandardPricebookId(), UnitPrice=0);
        
        
        
        // Create test PricebookEntries for the test Pricebook
        PricebookEntry standalonePBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = standaloneProduct.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert standalonePBE;

        PricebookEntry mircatPBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = mircatProduct.Id,
            UnitPrice = 150,
            IsActive = true
        );
        insert mircatPBE;

        PricebookEntry baseUnitPBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = baseUnitProduct.Id,
            UnitPrice = 200,
            IsActive = true
        );
        insert baseUnitPBE;

        //PricebookEntryId, UnitPrice
        
        // Create test QuoteLineItem records
        QuoteLineItem standaloneQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = standaloneProduct.Id,
            Quantity = 1,
            PricebookEntryId = standalonePBE.Id,
            UnitPrice = 100
        );
        insert standaloneQLI;

        QuoteLineItem mircatQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = mircatProduct.Id,
            Quantity = 2,
            PricebookEntryId = mircatPBE.Id,
            UnitPrice = 200,
            MSRP__c= 80,
            ISP__c =50
        );
        insert mircatQLI;

        QuoteLineItem baseUnitQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = baseUnitProduct.Id,
            Quantity = 3,
             PricebookEntryId = baseUnitPBE.Id,
            UnitPrice = 300,
             MSRP__c= 100,
            ISP__c =60

        );
        insert baseUnitQLI;

        // Set up a test page and controller
        PageReference pageRef = Page.newquote; // Replace 'YourPage' with the actual page name
        Test.setCurrentPage(pageRef);

        ApexPages.StandardController stdController = new ApexPages.StandardController(testQuote);

        // Instantiate the QuoteLineItemsExtension class
        QuoteLineItemsExtension extension = new QuoteLineItemsExtension(stdController);

        // Verify that the extension properties are set correctly
        System.assertEquals(testQuote.Id, extension.CurrentQuote.Id, 'CurrentQuote Id should match');
        System.assertNotEquals(null, extension.QuoteLineItems, 'QuoteLineItems should not be null');
        System.assertNotEquals(null, extension.MircatQLIs, 'MircatQLIs should not be null');
        System.assertNotEquals(null, extension.BUnitMQLIs, 'BUnitMQLIs should not be null');

        // Add additional assertions based on your business logic

        // For example, check if the QuoteLineItems property contains the correct records
        System.assertEquals(1, extension.QuoteLineItems.size(), 'There should be one QuoteLineItem');
        System.assertEquals(1, extension.MircatQLIs.size(), 'There should be one MircatQLIs');
        System.assertEquals(1, extension.BUnitMQLIs.size(), 'There should be one BUnitMQLIs');

        // Add more test assertions as needed
        System.assertEquals(null, extension.totalCSSClass, 'CSS class should be totalstdpbk'); 
        System.assertEquals(null, extension.totaltxtCSSClass, 'CSS class should be totaltxtstdpbk'); 
        
        
        
        
        
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class QuoteLineItemsExtensionTest {
    @isTest
    static void testQuoteLineItemsExtension() {
        // Create a test Pricebook
        Pricebook2 testPricebook = new Pricebook2(Name = 'Test Pricebook', IsActive = true);
        insert testPricebook;
        
        // Create a test Account
        
        Account ac = new Account(name = 'testac');
        insert ac ;    
        
        // Create a test Opportunity
        Opportunity op = new Opportunity(name = 'test' , accountid = ac.id , Product__c = 'MIRcat' , Market_Segment__c = 'Other', StageName = 'Limbo',closedate= System.today());
        insert op ;
         
       
        
        // Create a test Quote record associated with the test Pricebook
        Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId =  op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;

        // Create test Product records
        Product2 standaloneProduct = new Product2(Name = 'Standalone Product', Type__c = 'Standalone');
        insert standaloneProduct;

        Product2 mircatProduct = new Product2(Name = 'MIRCAT Product', Type__c = 'Options');
        insert mircatProduct;

        Product2 baseUnitProduct = new Product2(Name = 'Base Unit Product', Type__c = 'Base Unit');
        insert baseUnitProduct;

    //    insert new PriceBookEntry(Product2Id=pro2.Id, Pricebook2Id=Test.getStandardPricebookId(), UnitPrice=0);
        
        
        
        // Create test PricebookEntries for the test Pricebook
        PricebookEntry standalonePBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = standaloneProduct.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert standalonePBE;

        PricebookEntry mircatPBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = mircatProduct.Id,
            UnitPrice = 150,
            IsActive = true
        );
        insert mircatPBE;

        PricebookEntry baseUnitPBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = baseUnitProduct.Id,
            UnitPrice = 200,
            IsActive = true
        );
        insert baseUnitPBE;

        //PricebookEntryId, UnitPrice
        
        // Create test QuoteLineItem records
        QuoteLineItem standaloneQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = standaloneProduct.Id,
            Quantity = 1,
            PricebookEntryId = standalonePBE.Id,
            UnitPrice = 100
        );
        insert standaloneQLI;

        QuoteLineItem mircatQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = mircatProduct.Id,
            Quantity = 2,
            PricebookEntryId = mircatPBE.Id,
            UnitPrice = 200,
            MSRP__c= 80,
            ISP__c =50
        );
        insert mircatQLI;

        QuoteLineItem baseUnitQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = baseUnitProduct.Id,
            Quantity = 3,
             PricebookEntryId = baseUnitPBE.Id,
            UnitPrice = 300,
             MSRP__c= 100,
            ISP__c =60

        );
        insert baseUnitQLI;

        // Set up a test page and controller
        PageReference pageRef = Page.newquote; // Replace 'YourPage' with the actual page name
        Test.setCurrentPage(pageRef);

        ApexPages.StandardController stdController = new ApexPages.StandardController(testQuote);

        // Instantiate the QuoteLineItemsExtension class
        QuoteLineItemsExtension extension = new QuoteLineItemsExtension(stdController);

        // Verify that the extension properties are set correctly
        System.assertEquals(testQuote.Id, extension.CurrentQuote.Id, 'CurrentQuote Id should match');
        System.assertNotEquals(null, extension.QuoteLineItems, 'QuoteLineItems should not be null');
        System.assertNotEquals(null, extension.MircatQLIs, 'MircatQLIs should not be null');
        System.assertNotEquals(null, extension.BUnitMQLIs, 'BUnitMQLIs should not be null');

        // Add additional assertions based on your business logic

        // For example, check if the QuoteLineItems property contains the correct records
        System.assertEquals(1, extension.QuoteLineItems.size(), 'There should be one QuoteLineItem');
        System.assertEquals(1, extension.MircatQLIs.size(), 'There should be one MircatQLIs');
        System.assertEquals(1, extension.BUnitMQLIs.size(), 'There should be one BUnitMQLIs');

        // Add more test assertions as needed
        System.assertEquals(null, extension.totalCSSClass, 'CSS class should be totalstdpbk'); 
        System.assertEquals(null, extension.totaltxtCSSClass, 'CSS class should be totaltxtstdpbk'); 
        
        
        
        
        
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class QuoteLineItemsExtensionTest {
    @isTest
    static void testQuoteLineItemsExtension() {
        // Create a test Pricebook
        Pricebook2 testPricebook = new Pricebook2(Name = 'Test Pricebook', IsActive = true);
        insert testPricebook;
        
        // Create a test Account
        
        Account ac = new Account(name = 'testac');
        insert ac ;    
        
        // Create a test Opportunity
        Opportunity op = new Opportunity(name = 'test' , accountid = ac.id , Product__c = 'MIRcat' , Market_Segment__c = 'Other', StageName = 'Limbo',closedate= System.today());
        insert op ;
         
       
        
        // Create a test Quote record associated with the test Pricebook
        Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId =  op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;

        // Create test Product records
        Product2 standaloneProduct = new Product2(Name = 'Standalone Product', Type__c = 'Standalone');
        insert standaloneProduct;

        Product2 mircatProduct = new Product2(Name = 'MIRCAT Product', Type__c = 'Options');
        insert mircatProduct;

        Product2 baseUnitProduct = new Product2(Name = 'Base Unit Product', Type__c = 'Base Unit');
        insert baseUnitProduct;

    //    insert new PriceBookEntry(Product2Id=pro2.Id, Pricebook2Id=Test.getStandardPricebookId(), UnitPrice=0);
        
        
        
        // Create test PricebookEntries for the test Pricebook
        PricebookEntry standalonePBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = standaloneProduct.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert standalonePBE;

        PricebookEntry mircatPBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = mircatProduct.Id,
            UnitPrice = 150,
            IsActive = true
        );
        insert mircatPBE;

        PricebookEntry baseUnitPBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = baseUnitProduct.Id,
            UnitPrice = 200,
            IsActive = true
        );
        insert baseUnitPBE;

        //PricebookEntryId, UnitPrice
        
        // Create test QuoteLineItem records
        QuoteLineItem standaloneQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = standaloneProduct.Id,
            Quantity = 1,
            PricebookEntryId = standalonePBE.Id,
            UnitPrice = 100
        );
        insert standaloneQLI;

        QuoteLineItem mircatQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = mircatProduct.Id,
            Quantity = 2,
            PricebookEntryId = mircatPBE.Id,
            UnitPrice = 200,
            MSRP__c= 80,
            ISP__c =50
        );
        insert mircatQLI;

        QuoteLineItem baseUnitQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = baseUnitProduct.Id,
            Quantity = 3,
             PricebookEntryId = baseUnitPBE.Id,
            UnitPrice = 300,
             MSRP__c= 100,
            ISP__c =60

        );
        insert baseUnitQLI;

        // Set up a test page and controller
        PageReference pageRef = Page.newquote; // Replace 'YourPage' with the actual page name
        Test.setCurrentPage(pageRef);

        ApexPages.StandardController stdController = new ApexPages.StandardController(testQuote);

        // Instantiate the QuoteLineItemsExtension class
        QuoteLineItemsExtension extension = new QuoteLineItemsExtension(stdController);

        // Verify that the extension properties are set correctly
        System.assertEquals(testQuote.Id, extension.CurrentQuote.Id, 'CurrentQuote Id should match');
        System.assertNotEquals(null, extension.QuoteLineItems, 'QuoteLineItems should not be null');
        System.assertNotEquals(null, extension.MircatQLIs, 'MircatQLIs should not be null');
        System.assertNotEquals(null, extension.BUnitMQLIs, 'BUnitMQLIs should not be null');

        // Add additional assertions based on your business logic

        // For example, check if the QuoteLineItems property contains the correct records
        System.assertEquals(1, extension.QuoteLineItems.size(), 'There should be one QuoteLineItem');
        System.assertEquals(1, extension.MircatQLIs.size(), 'There should be one MircatQLIs');
        System.assertEquals(1, extension.BUnitMQLIs.size(), 'There should be one BUnitMQLIs');

        // Add more test assertions as needed
        System.assertEquals(null, extension.totalCSSClass, 'CSS class should be totalstdpbk'); 
        System.assertEquals(null, extension.totaltxtCSSClass, 'CSS class should be totaltxtstdpbk'); 
        
        
        
        
        
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class QuoteLineItemsExtensionTest {
    @isTest
    static void testQuoteLineItemsExtension() {
        // Create a test Pricebook
        Pricebook2 testPricebook = new Pricebook2(Name = 'Test Pricebook', IsActive = true);
        insert testPricebook;
        
        // Create a test Account
        
        Account ac = new Account(name = 'testac');
        insert ac ;    
        
        // Create a test Opportunity
        Opportunity op = new Opportunity(name = 'test' , accountid = ac.id , Product__c = 'MIRcat' , Market_Segment__c = 'Other', StageName = 'Limbo',closedate= System.today());
        insert op ;
         
       
        
        // Create a test Quote record associated with the test Pricebook
        Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId =  op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;

        // Create test Product records
        Product2 standaloneProduct = new Product2(Name = 'Standalone Product', Type__c = 'Standalone');
        insert standaloneProduct;

        Product2 mircatProduct = new Product2(Name = 'MIRCAT Product', Type__c = 'Options');
        insert mircatProduct;

        Product2 baseUnitProduct = new Product2(Name = 'Base Unit Product', Type__c = 'Base Unit');
        insert baseUnitProduct;

    //    insert new PriceBookEntry(Product2Id=pro2.Id, Pricebook2Id=Test.getStandardPricebookId(), UnitPrice=0);
        
        
        
        // Create test PricebookEntries for the test Pricebook
        PricebookEntry standalonePBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = standaloneProduct.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert standalonePBE;

        PricebookEntry mircatPBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = mircatProduct.Id,
            UnitPrice = 150,
            IsActive = true
        );
        insert mircatPBE;

        PricebookEntry baseUnitPBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = baseUnitProduct.Id,
            UnitPrice = 200,
            IsActive = true
        );
        insert baseUnitPBE;

        //PricebookEntryId, UnitPrice
        
        // Create test QuoteLineItem records
        QuoteLineItem standaloneQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = standaloneProduct.Id,
            Quantity = 1,
            PricebookEntryId = standalonePBE.Id,
            UnitPrice = 100
        );
        insert standaloneQLI;

        QuoteLineItem mircatQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = mircatProduct.Id,
            Quantity = 2,
            PricebookEntryId = mircatPBE.Id,
            UnitPrice = 200,
            MSRP__c= 80,
            ISP__c =50
        );
        insert mircatQLI;

        QuoteLineItem baseUnitQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = baseUnitProduct.Id,
            Quantity = 3,
             PricebookEntryId = baseUnitPBE.Id,
            UnitPrice = 300,
             MSRP__c= 100,
            ISP__c =60

        );
        insert baseUnitQLI;

        // Set up a test page and controller
        PageReference pageRef = Page.newquote; // Replace 'YourPage' with the actual page name
        Test.setCurrentPage(pageRef);

        ApexPages.StandardController stdController = new ApexPages.StandardController(testQuote);

        // Instantiate the QuoteLineItemsExtension class
        QuoteLineItemsExtension extension = new QuoteLineItemsExtension(stdController);

        // Verify that the extension properties are set correctly
        System.assertEquals(testQuote.Id, extension.CurrentQuote.Id, 'CurrentQuote Id should match');
        System.assertNotEquals(null, extension.QuoteLineItems, 'QuoteLineItems should not be null');
        System.assertNotEquals(null, extension.MircatQLIs, 'MircatQLIs should not be null');
        System.assertNotEquals(null, extension.BUnitMQLIs, 'BUnitMQLIs should not be null');

        // Add additional assertions based on your business logic

        // For example, check if the QuoteLineItems property contains the correct records
        System.assertEquals(1, extension.QuoteLineItems.size(), 'There should be one QuoteLineItem');
        System.assertEquals(1, extension.MircatQLIs.size(), 'There should be one MircatQLIs');
        System.assertEquals(1, extension.BUnitMQLIs.size(), 'There should be one BUnitMQLIs');

        // Add more test assertions as needed
        System.assertEquals(null, extension.totalCSSClass, 'CSS class should be totalstdpbk'); 
        System.assertEquals(null, extension.totaltxtCSSClass, 'CSS class should be totaltxtstdpbk'); 
        
        
        
        
        
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class QuoteLineItemsExtensionTest {
    @isTest
    static void testQuoteLineItemsExtension() {
        // Create a test Pricebook
        Pricebook2 testPricebook = new Pricebook2(Name = 'Test Pricebook', IsActive = true);
        insert testPricebook;
        
        // Create a test Account
        
        Account ac = new Account(name = 'testac');
        insert ac ;    
        
        // Create a test Opportunity
        Opportunity op = new Opportunity(name = 'test' , accountid = ac.id , Product__c = 'MIRcat' , Market_Segment__c = 'Other', StageName = 'Limbo',closedate= System.today());
        insert op ;
         
       
        
        // Create a test Quote record associated with the test Pricebook
        Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId =  op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;

        // Create test Product records
        Product2 standaloneProduct = new Product2(Name = 'Standalone Product', Type__c = 'Standalone');
        insert standaloneProduct;

        Product2 mircatProduct = new Product2(Name = 'MIRCAT Product', Type__c = 'Options');
        insert mircatProduct;

        Product2 baseUnitProduct = new Product2(Name = 'Base Unit Product', Type__c = 'Base Unit');
        insert baseUnitProduct;

    //    insert new PriceBookEntry(Product2Id=pro2.Id, Pricebook2Id=Test.getStandardPricebookId(), UnitPrice=0);
        
        
        
        // Create test PricebookEntries for the test Pricebook
        PricebookEntry standalonePBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = standaloneProduct.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert standalonePBE;

        PricebookEntry mircatPBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = mircatProduct.Id,
            UnitPrice = 150,
            IsActive = true
        );
        insert mircatPBE;

        PricebookEntry baseUnitPBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = baseUnitProduct.Id,
            UnitPrice = 200,
            IsActive = true
        );
        insert baseUnitPBE;

        //PricebookEntryId, UnitPrice
        
        // Create test QuoteLineItem records
        QuoteLineItem standaloneQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = standaloneProduct.Id,
            Quantity = 1,
            PricebookEntryId = standalonePBE.Id,
            UnitPrice = 100
        );
        insert standaloneQLI;

        QuoteLineItem mircatQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = mircatProduct.Id,
            Quantity = 2,
            PricebookEntryId = mircatPBE.Id,
            UnitPrice = 200,
            MSRP__c= 80,
            ISP__c =50
        );
        insert mircatQLI;

        QuoteLineItem baseUnitQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = baseUnitProduct.Id,
            Quantity = 3,
             PricebookEntryId = baseUnitPBE.Id,
            UnitPrice = 300,
             MSRP__c= 100,
            ISP__c =60

        );
        insert baseUnitQLI;

        // Set up a test page and controller
        PageReference pageRef = Page.newquote; // Replace 'YourPage' with the actual page name
        Test.setCurrentPage(pageRef);

        ApexPages.StandardController stdController = new ApexPages.StandardController(testQuote);

        // Instantiate the QuoteLineItemsExtension class
        QuoteLineItemsExtension extension = new QuoteLineItemsExtension(stdController);

        // Verify that the extension properties are set correctly
        System.assertEquals(testQuote.Id, extension.CurrentQuote.Id, 'CurrentQuote Id should match');
        System.assertNotEquals(null, extension.QuoteLineItems, 'QuoteLineItems should not be null');
        System.assertNotEquals(null, extension.MircatQLIs, 'MircatQLIs should not be null');
        System.assertNotEquals(null, extension.BUnitMQLIs, 'BUnitMQLIs should not be null');

        // Add additional assertions based on your business logic

        // For example, check if the QuoteLineItems property contains the correct records
        System.assertEquals(1, extension.QuoteLineItems.size(), 'There should be one QuoteLineItem');
        System.assertEquals(1, extension.MircatQLIs.size(), 'There should be one MircatQLIs');
        System.assertEquals(1, extension.BUnitMQLIs.size(), 'There should be one BUnitMQLIs');

        // Add more test assertions as needed
        System.assertEquals(null, extension.totalCSSClass, 'CSS class should be totalstdpbk'); 
        System.assertEquals(null, extension.totaltxtCSSClass, 'CSS class should be totaltxtstdpbk'); 
        
        
        
        
        
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class QuoteLineItemsExtensionTest {
    @isTest
    static void testQuoteLineItemsExtension() {
        // Create a test Pricebook
        Pricebook2 testPricebook = new Pricebook2(Name = 'Test Pricebook', IsActive = true);
        insert testPricebook;
        
        // Create a test Account
        
        Account ac = new Account(name = 'testac');
        insert ac ;    
        
        // Create a test Opportunity
        Opportunity op = new Opportunity(name = 'test' , accountid = ac.id , Product__c = 'MIRcat' , Market_Segment__c = 'Other', StageName = 'Limbo',closedate= System.today());
        insert op ;
         
       
        
        // Create a test Quote record associated with the test Pricebook
        Quote testQuote = new Quote(
            Name = 'Test Quote',
            OpportunityId =  op.id,
            Pricebook2Id =  Test.getStandardPricebookId()
        );
        insert testQuote;

        // Create test Product records
        Product2 standaloneProduct = new Product2(Name = 'Standalone Product', Type__c = 'Standalone');
        insert standaloneProduct;

        Product2 mircatProduct = new Product2(Name = 'MIRCAT Product', Type__c = 'Options');
        insert mircatProduct;

        Product2 baseUnitProduct = new Product2(Name = 'Base Unit Product', Type__c = 'Base Unit');
        insert baseUnitProduct;

    //    insert new PriceBookEntry(Product2Id=pro2.Id, Pricebook2Id=Test.getStandardPricebookId(), UnitPrice=0);
        
        
        
        // Create test PricebookEntries for the test Pricebook
        PricebookEntry standalonePBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = standaloneProduct.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert standalonePBE;

        PricebookEntry mircatPBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = mircatProduct.Id,
            UnitPrice = 150,
            IsActive = true
        );
        insert mircatPBE;

        PricebookEntry baseUnitPBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = baseUnitProduct.Id,
            UnitPrice = 200,
            IsActive = true
        );
        insert baseUnitPBE;

        //PricebookEntryId, UnitPrice
        
        // Create test QuoteLineItem records
        QuoteLineItem standaloneQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = standaloneProduct.Id,
            Quantity = 1,
            PricebookEntryId = standalonePBE.Id,
            UnitPrice = 100
        );
        insert standaloneQLI;

        QuoteLineItem mircatQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = mircatProduct.Id,
            Quantity = 2,
            PricebookEntryId = mircatPBE.Id,
            UnitPrice = 200,
            MSRP__c= 80,
            ISP__c =50
        );
        insert mircatQLI;

        QuoteLineItem baseUnitQLI = new QuoteLineItem(
            QuoteId = testQuote.Id,
            Product2Id = baseUnitProduct.Id,
            Quantity = 3,
             PricebookEntryId = baseUnitPBE.Id,
            UnitPrice = 300,
             MSRP__c= 100,
            ISP__c =60

        );
        insert baseUnitQLI;

        // Set up a test page and controller
        PageReference pageRef = Page.newquote; // Replace 'YourPage' with the actual page name
        Test.setCurrentPage(pageRef);

        ApexPages.StandardController stdController = new ApexPages.StandardController(testQuote);

        // Instantiate the QuoteLineItemsExtension class
        QuoteLineItemsExtension extension = new QuoteLineItemsExtension(stdController);

        // Verify that the extension properties are set correctly
        System.assertEquals(testQuote.Id, extension.CurrentQuote.Id, 'CurrentQuote Id should match');
        System.assertNotEquals(null, extension.QuoteLineItems, 'QuoteLineItems should not be null');
        System.assertNotEquals(null, extension.MircatQLIs, 'MircatQLIs should not be null');
        System.assertNotEquals(null, extension.BUnitMQLIs, 'BUnitMQLIs should not be null');

        // Add additional assertions based on your business logic

        // For example, check if the QuoteLineItems property contains the correct records
        System.assertEquals(1, extension.QuoteLineItems.size(), 'There should be one QuoteLineItem');
        System.assertEquals(1, extension.MircatQLIs.size(), 'There should be one MircatQLIs');
        System.assertEquals(1, extension.BUnitMQLIs.size(), 'There should be one BUnitMQLIs');

        // Add more test assertions as needed
        System.assertEquals(null, extension.totalCSSClass, 'CSS class should be totalstdpbk'); 
        System.assertEquals(null, extension.totaltxtCSSClass, 'CSS class should be totaltxtstdpbk'); 
        
        
        
        
        
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
private class QuoteLineItemsExtensionTest {
  @isTest
  static void testQuoteLineItemsExtension() {
    // Create a test Pricebook
    Pricebook2 testPricebook = new Pricebook2(
      Name = 'Test Pricebook',
      IsActive = true
    );
    insert testPricebook;

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

    // Create a test Quote record associated with the test Pricebook
    Quote testQuote = new Quote(
      Name = 'Test Quote',
      OpportunityId = op.id,
      Pricebook2Id = Test.getStandardPricebookId()
    );
    insert testQuote;

    // Create test Product records
    Product2 standaloneProduct = new Product2(
      Name = 'Standalone Product',
      Type__c = 'Standalone'
    );
    insert standaloneProduct;

    Product2 mircatProduct = new Product2(
      Name = 'MIRCAT Product',
      Type__c = 'Options'
    );
    insert mircatProduct;

    Product2 baseUnitProduct = new Product2(
      Name = 'Base Unit Product',
      Type__c = 'Base Unit'
    );
    insert baseUnitProduct;

    //    insert new PriceBookEntry(Product2Id=pro2.Id, Pricebook2Id=Test.getStandardPricebookId(), UnitPrice=0);

    // Create test PricebookEntries for the test Pricebook
    PricebookEntry standalonePBE = new PricebookEntry(
      Pricebook2Id = Test.getStandardPricebookId(),
      Product2Id = standaloneProduct.Id,
      UnitPrice = 100,
      IsActive = true
    );
    insert standalonePBE;

    PricebookEntry mircatPBE = new PricebookEntry(
      Pricebook2Id = Test.getStandardPricebookId(),
      Product2Id = mircatProduct.Id,
      UnitPrice = 150,
      IsActive = true
    );
    insert mircatPBE;

    PricebookEntry baseUnitPBE = new PricebookEntry(
      Pricebook2Id = Test.getStandardPricebookId(),
      Product2Id = baseUnitProduct.Id,
      UnitPrice = 200,
      IsActive = true
    );
    insert baseUnitPBE;

    //PricebookEntryId, UnitPrice

    // Create test QuoteLineItem records
    QuoteLineItem standaloneQLI = new QuoteLineItem(
      QuoteId = testQuote.Id,
      Product2Id = standaloneProduct.Id,
      Quantity = 1,
      PricebookEntryId = standalonePBE.Id,
      UnitPrice = 100
    );
    insert standaloneQLI;

    QuoteLineItem mircatQLI = new QuoteLineItem(
      QuoteId = testQuote.Id,
      Product2Id = mircatProduct.Id,
      Quantity = 2,
      PricebookEntryId = mircatPBE.Id,
      UnitPrice = 200,
      MSRP__c = 80,
      ISP__c = 50
    );
    insert mircatQLI;

    QuoteLineItem baseUnitQLI = new QuoteLineItem(
      QuoteId = testQuote.Id,
      Product2Id = baseUnitProduct.Id,
      Quantity = 3,
      PricebookEntryId = baseUnitPBE.Id,
      UnitPrice = 300,
      MSRP__c = 100,
      ISP__c = 60
    );
    insert baseUnitQLI;

    // Set up a test page and controller
    PageReference pageRef = Page.newquote; // Replace 'YourPage' with the actual page name
    Test.setCurrentPage(pageRef);

    ApexPages.StandardController stdController = new ApexPages.StandardController(
      testQuote
    );

    // Instantiate the QuoteLineItemsExtension class
    QuoteLineItemsExtension extension = new QuoteLineItemsExtension(
      stdController
    );

    // Verify that the extension properties are set correctly
    System.assertEquals(
      testQuote.Id,
      extension.CurrentQuote.Id,
      'CurrentQuote Id should match'
    );
    System.assertNotEquals(
      null,
      extension.QuoteLineItems,
      'QuoteLineItems should not be null'
    );
    System.assertNotEquals(
      null,
      extension.MircatQLIs,
      'MircatQLIs should not be null'
    );
    System.assertNotEquals(
      null,
      extension.BUnitMQLIs,
      'BUnitMQLIs should not be null'
    );

    // Add additional assertions based on your business logic

    // For example, check if the QuoteLineItems property contains the correct records
    System.assertEquals(
      1,
      extension.QuoteLineItems.size(),
      'There should be one QuoteLineItem'
    );
    System.assertEquals(
      1,
      extension.MircatQLIs.size(),
      'There should be two MircatQLIs'
    );
    System.assertEquals(
      1,
      extension.BUnitMQLIs.size(),
      'There should be three BUnitMQLIs'
    );

    // Add more test assertions as needed
  }
}

```

## Methods
### `testQuoteLineItemsExtension()`

`ISTEST`

#### Signature
```apex
private static void testQuoteLineItemsExtension()
```

#### Return Type
**void**