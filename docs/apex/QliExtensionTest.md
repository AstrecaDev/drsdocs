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

# QliExtensionTest Class

`ISTEST`

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class QliExtensionTest {
    static testMethod void testCreateQuoteLineItems() {
        
        Pricebook2 testPricebook = new Pricebook2(Name = 'Test Pricebook', isActive = true);
        insert testPricebook;
        System.debug('testPricebook.Id' +testPricebook.Id);        
        
         //Get standard pricebook id
         Id stdPriceBookId= Test.getStandardPricebookId();        
     
        //Create Account
        Account a = new Account(
            Name = 'Test');
        Insert a;
        
        //Create Opportunity
        Opportunity o = new Opportunity();
       	o.AccountID=a.ID;
       	o.Name=a.Name;
       	o.CloseDate=System.Today().addDays(3);
       	o.StageName='Prospecting';
        o.Market_Segment__c = 'Biopharma';
       	Insert o;
        
        //Create a mock Quote object
        Quote quote = new Quote();
        quote.Name = 'Test Quote';
        quote.Pricebook2Id = testPricebook.Id;
        quote.OpportunityId= o.Id;
        insert quote;
        
        //Create a mock Product2 object
        Product2 product = new Product2();
        product.Name = 'Test Product';        
        insert product;
        
         //Make product entry in standard and custom priceooks
         PriceBookEntry stdPre1 = new PriceBookEntry(
         IsActive = true,
         PriceBook2Id = stdPriceBookId, 
         Product2Id = product.Id , 
         UnitPrice= 100);
		 insert stdPre1;
      
        PriceBookEntry pre1 = new PriceBookEntry(
        IsActive = true,
        PriceBook2Id = testPricebook.Id, 
        Product2Id = product.Id , 
        UnitPrice= 100);
		insert pre1;  
        
        // Create a list of QuoteLineItemInput objects
        List<QuoteLineItem> quoteLineItems = new List<QuoteLineItem>();
        for (Integer i = 0; i < 5; i++) {
            QuoteLineItem item = new QuoteLineItem();
            item.Product2Id = product.ID;
            item.QuoteId = quote.ID;
            item.Quantity = i + 1;
            item.UnitPrice = 100 + i; 
            item.PricebookEntryId = pre1.Id;
            quoteLineItems.add(item);
        }
		insert quoteLineItems;
  
        // Verify that the QuoteLineItems were created
        List<QuoteLineItem> dbItems = [
            SELECT Id, Product2Id, QuoteId, Quantity, ListPrice, UnitPrice
            FROM QuoteLineItem
            WHERE QuoteId = :quote.Id
            Limit 1
        ];
        
        Test.startTest();

        // Set up the controller and extension for the Quote record
        ApexPages.StandardController standardController = new ApexPages.StandardController(quote);
        QliExtension qliExtension = new QliExtension(standardController);

        // Verify that the extension has the correct current quote
        System.assertEquals(quote.Id, qliExtension.CurrentQuote.Id, 'CurrentQuote should be set correctly');

        // Verify that the extension has the correct list of quote line items
     //   System.assertEquals(5, qliExtension.QuoteLineItems.size(), 'QuoteLineItems should be retrieved correctly');
  
        Test.stopTest();
      //  }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class QliExtensionTest {
    static testMethod void testCreateQuoteLineItems() {
        
        Pricebook2 testPricebook = new Pricebook2(Name = 'Test Pricebook', isActive = true);
        insert testPricebook;
        System.debug('testPricebook.Id' +testPricebook.Id);        
        
         //Get standard pricebook id
         Id stdPriceBookId= Test.getStandardPricebookId();        
     
        //Create Account
        Account a = new Account(
            Name = 'Test');
        Insert a;
        
        //Create Opportunity
        Opportunity o = new Opportunity();
       	o.AccountID=a.ID;
       	o.Name=a.Name;
       	o.CloseDate=System.Today().addDays(3);
       	o.StageName='Prospecting';
        o.Market_Segment__c = 'Biopharma';
       	Insert o;
        
        //Create a mock Quote object
        Quote quote = new Quote();
        quote.Name = 'Test Quote';
        quote.Pricebook2Id = testPricebook.Id;
        quote.OpportunityId= o.Id;
        insert quote;
        
        //Create a mock Product2 object
        Product2 product = new Product2();
        product.Name = 'Test Product';        
        insert product;
        
         //Make product entry in standard and custom priceooks
         PriceBookEntry stdPre1 = new PriceBookEntry(
         IsActive = true,
         PriceBook2Id = stdPriceBookId, 
         Product2Id = product.Id , 
         UnitPrice= 100);
		 insert stdPre1;
      
        PriceBookEntry pre1 = new PriceBookEntry(
        IsActive = true,
        PriceBook2Id = testPricebook.Id, 
        Product2Id = product.Id , 
        UnitPrice= 100);
		insert pre1;  
        
        // Create a list of QuoteLineItemInput objects
        List<QuoteLineItem> quoteLineItems = new List<QuoteLineItem>();
        for (Integer i = 0; i < 5; i++) {
            QuoteLineItem item = new QuoteLineItem();
            item.Product2Id = product.ID;
            item.QuoteId = quote.ID;
            item.Quantity = i + 1;
            item.UnitPrice = 100 + i; 
            item.PricebookEntryId = pre1.Id;
            quoteLineItems.add(item);
        }
		insert quoteLineItems;
  
        // Verify that the QuoteLineItems were created
        List<QuoteLineItem> dbItems = [
            SELECT Id, Product2Id, QuoteId, Quantity, ListPrice, UnitPrice
            FROM QuoteLineItem
            WHERE QuoteId = :quote.Id
            Limit 1
        ];
        
        Test.startTest();

        // Set up the controller and extension for the Quote record
        ApexPages.StandardController standardController = new ApexPages.StandardController(quote);
        QliExtension qliExtension = new QliExtension(standardController);

        // Verify that the extension has the correct current quote
        System.assertEquals(quote.Id, qliExtension.CurrentQuote.Id, 'CurrentQuote should be set correctly');

        // Verify that the extension has the correct list of quote line items
     //   System.assertEquals(5, qliExtension.QuoteLineItems.size(), 'QuoteLineItems should be retrieved correctly');
  
        Test.stopTest();
      //  }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class QliExtensionTest {
    static testMethod void testCreateQuoteLineItems() {
        
        Pricebook2 testPricebook = new Pricebook2(Name = 'Test Pricebook', isActive = true);
        insert testPricebook;
        System.debug('testPricebook.Id' +testPricebook.Id);        
        
         //Get standard pricebook id
         Id stdPriceBookId= Test.getStandardPricebookId();        
     
        //Create Account
        Account a = new Account(
            Name = 'Test');
        Insert a;
        
        //Create Opportunity
        Opportunity o = new Opportunity();
       	o.AccountID=a.ID;
       	o.Name=a.Name;
       	o.CloseDate=System.Today().addDays(3);
       	o.StageName='Prospecting';
        o.Market_Segment__c = 'Biopharma';
       	Insert o;
        
        //Create a mock Quote object
        Quote quote = new Quote();
        quote.Name = 'Test Quote';
        quote.Pricebook2Id = testPricebook.Id;
        quote.OpportunityId= o.Id;
        insert quote;
        
        //Create a mock Product2 object
        Product2 product = new Product2();
        product.Name = 'Test Product';        
        insert product;
        
         //Make product entry in standard and custom priceooks
         PriceBookEntry stdPre1 = new PriceBookEntry(
         IsActive = true,
         PriceBook2Id = stdPriceBookId, 
         Product2Id = product.Id , 
         UnitPrice= 100);
		 insert stdPre1;
      
        PriceBookEntry pre1 = new PriceBookEntry(
        IsActive = true,
        PriceBook2Id = testPricebook.Id, 
        Product2Id = product.Id , 
        UnitPrice= 100);
		insert pre1;  
        
        // Create a list of QuoteLineItemInput objects
        List<QuoteLineItem> quoteLineItems = new List<QuoteLineItem>();
        for (Integer i = 0; i < 5; i++) {
            QuoteLineItem item = new QuoteLineItem();
            item.Product2Id = product.ID;
            item.QuoteId = quote.ID;
            item.Quantity = i + 1;
            item.UnitPrice = 100 + i; 
            item.PricebookEntryId = pre1.Id;
            quoteLineItems.add(item);
        }
		insert quoteLineItems;
  
        // Verify that the QuoteLineItems were created
        List<QuoteLineItem> dbItems = [
            SELECT Id, Product2Id, QuoteId, Quantity, ListPrice, UnitPrice
            FROM QuoteLineItem
            WHERE QuoteId = :quote.Id
            Limit 1
        ];
        
        Test.startTest();

        // Set up the controller and extension for the Quote record
        ApexPages.StandardController standardController = new ApexPages.StandardController(quote);
        QliExtension qliExtension = new QliExtension(standardController);

        // Verify that the extension has the correct current quote
        System.assertEquals(quote.Id, qliExtension.CurrentQuote.Id, 'CurrentQuote should be set correctly');

        // Verify that the extension has the correct list of quote line items
     //   System.assertEquals(5, qliExtension.QuoteLineItems.size(), 'QuoteLineItems should be retrieved correctly');
  
        Test.stopTest();
      //  }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class QliExtensionTest {
    static testMethod void testCreateQuoteLineItems() {
        
        Pricebook2 testPricebook = new Pricebook2(Name = 'Test Pricebook', isActive = true);
        insert testPricebook;
        System.debug('testPricebook.Id' +testPricebook.Id);        
        
         //Get standard pricebook id
         Id stdPriceBookId= Test.getStandardPricebookId();        
     
        //Create Account
        Account a = new Account(
            Name = 'Test');
        Insert a;
        
        //Create Opportunity
        Opportunity o = new Opportunity();
       	o.AccountID=a.ID;
       	o.Name=a.Name;
       	o.CloseDate=System.Today().addDays(3);
       	o.StageName='Prospecting';
        o.Market_Segment__c = 'Biopharma';
       	Insert o;
        
        //Create a mock Quote object
        Quote quote = new Quote();
        quote.Name = 'Test Quote';
        quote.Pricebook2Id = testPricebook.Id;
        quote.OpportunityId= o.Id;
        insert quote;
        
        //Create a mock Product2 object
        Product2 product = new Product2();
        product.Name = 'Test Product';        
        insert product;
        
         //Make product entry in standard and custom priceooks
         PriceBookEntry stdPre1 = new PriceBookEntry(
         IsActive = true,
         PriceBook2Id = stdPriceBookId, 
         Product2Id = product.Id , 
         UnitPrice= 100);
		 insert stdPre1;
      
        PriceBookEntry pre1 = new PriceBookEntry(
        IsActive = true,
        PriceBook2Id = testPricebook.Id, 
        Product2Id = product.Id , 
        UnitPrice= 100);
		insert pre1;  
        
        // Create a list of QuoteLineItemInput objects
        List<QuoteLineItem> quoteLineItems = new List<QuoteLineItem>();
        for (Integer i = 0; i < 5; i++) {
            QuoteLineItem item = new QuoteLineItem();
            item.Product2Id = product.ID;
            item.QuoteId = quote.ID;
            item.Quantity = i + 1;
            item.UnitPrice = 100 + i; 
            item.PricebookEntryId = pre1.Id;
            quoteLineItems.add(item);
        }
		insert quoteLineItems;
  
        // Verify that the QuoteLineItems were created
        List<QuoteLineItem> dbItems = [
            SELECT Id, Product2Id, QuoteId, Quantity, ListPrice, UnitPrice
            FROM QuoteLineItem
            WHERE QuoteId = :quote.Id
            Limit 1
        ];
        
        Test.startTest();

        // Set up the controller and extension for the Quote record
        ApexPages.StandardController standardController = new ApexPages.StandardController(quote);
        QliExtension qliExtension = new QliExtension(standardController);

        // Verify that the extension has the correct current quote
        System.assertEquals(quote.Id, qliExtension.CurrentQuote.Id, 'CurrentQuote should be set correctly');

        // Verify that the extension has the correct list of quote line items
     //   System.assertEquals(5, qliExtension.QuoteLineItems.size(), 'QuoteLineItems should be retrieved correctly');
  
        Test.stopTest();
      //  }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class QliExtensionTest {
    static testMethod void testCreateQuoteLineItems() {
        
        Pricebook2 testPricebook = new Pricebook2(Name = 'Test Pricebook', isActive = true);
        insert testPricebook;
        System.debug('testPricebook.Id' +testPricebook.Id);        
        
         //Get standard pricebook id
         Id stdPriceBookId= Test.getStandardPricebookId();        
     
        //Create Account
        Account a = new Account(
            Name = 'Test');
        Insert a;
        
        //Create Opportunity
        Opportunity o = new Opportunity();
       	o.AccountID=a.ID;
       	o.Name=a.Name;
       	o.CloseDate=System.Today().addDays(3);
       	o.StageName='Prospecting';
        o.Market_Segment__c = 'Biopharma';
       	Insert o;
        
        //Create a mock Quote object
        Quote quote = new Quote();
        quote.Name = 'Test Quote';
        quote.Pricebook2Id = testPricebook.Id;
        quote.OpportunityId= o.Id;
        insert quote;
        
        //Create a mock Product2 object
        Product2 product = new Product2();
        product.Name = 'Test Product';        
        insert product;
        
         //Make product entry in standard and custom priceooks
         PriceBookEntry stdPre1 = new PriceBookEntry(
         IsActive = true,
         PriceBook2Id = stdPriceBookId, 
         Product2Id = product.Id , 
         UnitPrice= 100);
		 insert stdPre1;
      
        PriceBookEntry pre1 = new PriceBookEntry(
        IsActive = true,
        PriceBook2Id = testPricebook.Id, 
        Product2Id = product.Id , 
        UnitPrice= 100);
		insert pre1;  
        
        // Create a list of QuoteLineItemInput objects
        List<QuoteLineItem> quoteLineItems = new List<QuoteLineItem>();
        for (Integer i = 0; i < 5; i++) {
            QuoteLineItem item = new QuoteLineItem();
            item.Product2Id = product.ID;
            item.QuoteId = quote.ID;
            item.Quantity = i + 1;
            item.UnitPrice = 100 + i; 
            item.PricebookEntryId = pre1.Id;
            quoteLineItems.add(item);
        }
		insert quoteLineItems;
  
        // Verify that the QuoteLineItems were created
        List<QuoteLineItem> dbItems = [
            SELECT Id, Product2Id, QuoteId, Quantity, ListPrice, UnitPrice
            FROM QuoteLineItem
            WHERE QuoteId = :quote.Id
            Limit 1
        ];
        
        Test.startTest();

        // Set up the controller and extension for the Quote record
        ApexPages.StandardController standardController = new ApexPages.StandardController(quote);
        QliExtension qliExtension = new QliExtension(standardController);

        // Verify that the extension has the correct current quote
        System.assertEquals(quote.Id, qliExtension.CurrentQuote.Id, 'CurrentQuote should be set correctly');

        // Verify that the extension has the correct list of quote line items
     //   System.assertEquals(5, qliExtension.QuoteLineItems.size(), 'QuoteLineItems should be retrieved correctly');
  
        Test.stopTest();
      //  }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class QliExtensionTest {
    static testMethod void testCreateQuoteLineItems() {
        
        Pricebook2 testPricebook = new Pricebook2(Name = 'Test Pricebook', isActive = true);
        insert testPricebook;
        System.debug('testPricebook.Id' +testPricebook.Id);        
        
         //Get standard pricebook id
         Id stdPriceBookId= Test.getStandardPricebookId();        
     
        //Create Account
        Account a = new Account(
            Name = 'Test');
        Insert a;
        
        //Create Opportunity
        Opportunity o = new Opportunity();
       	o.AccountID=a.ID;
       	o.Name=a.Name;
       	o.CloseDate=System.Today().addDays(3);
       	o.StageName='Prospecting';
        o.Market_Segment__c = 'Biopharma';
       	Insert o;
        
        //Create a mock Quote object
        Quote quote = new Quote();
        quote.Name = 'Test Quote';
        quote.Pricebook2Id = testPricebook.Id;
        quote.OpportunityId= o.Id;
        insert quote;
        
        //Create a mock Product2 object
        Product2 product = new Product2();
        product.Name = 'Test Product';        
        insert product;
        
         //Make product entry in standard and custom priceooks
         PriceBookEntry stdPre1 = new PriceBookEntry(
         IsActive = true,
         PriceBook2Id = stdPriceBookId, 
         Product2Id = product.Id , 
         UnitPrice= 100);
		 insert stdPre1;
      
        PriceBookEntry pre1 = new PriceBookEntry(
        IsActive = true,
        PriceBook2Id = testPricebook.Id, 
        Product2Id = product.Id , 
        UnitPrice= 100);
		insert pre1;  
        
        // Create a list of QuoteLineItemInput objects
        List<QuoteLineItem> quoteLineItems = new List<QuoteLineItem>();
        for (Integer i = 0; i < 5; i++) {
            QuoteLineItem item = new QuoteLineItem();
            item.Product2Id = product.ID;
            item.QuoteId = quote.ID;
            item.Quantity = i + 1;
            item.UnitPrice = 100 + i; 
            item.PricebookEntryId = pre1.Id;
            quoteLineItems.add(item);
        }
		insert quoteLineItems;
  
        // Verify that the QuoteLineItems were created
        List<QuoteLineItem> dbItems = [
            SELECT Id, Product2Id, QuoteId, Quantity, ListPrice, UnitPrice
            FROM QuoteLineItem
            WHERE QuoteId = :quote.Id
            Limit 1
        ];
        
        Test.startTest();

        // Set up the controller and extension for the Quote record
        ApexPages.StandardController standardController = new ApexPages.StandardController(quote);
        QliExtension qliExtension = new QliExtension(standardController);

        // Verify that the extension has the correct current quote
        System.assertEquals(quote.Id, qliExtension.CurrentQuote.Id, 'CurrentQuote should be set correctly');

        // Verify that the extension has the correct list of quote line items
     //   System.assertEquals(5, qliExtension.QuoteLineItems.size(), 'QuoteLineItems should be retrieved correctly');
  
        Test.stopTest();
      //  }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class QliExtensionTest {
    static testMethod void testCreateQuoteLineItems() {
        
        Pricebook2 testPricebook = new Pricebook2(Name = 'Test Pricebook', isActive = true);
        insert testPricebook;
        System.debug('testPricebook.Id' +testPricebook.Id);        
        
         //Get standard pricebook id
         Id stdPriceBookId= Test.getStandardPricebookId();        
     
        //Create Account
        Account a = new Account(
            Name = 'Test');
        Insert a;
        
        //Create Opportunity
        Opportunity o = new Opportunity();
       	o.AccountID=a.ID;
       	o.Name=a.Name;
       	o.CloseDate=System.Today().addDays(3);
       	o.StageName='Prospecting';
        o.Market_Segment__c = 'Biopharma';
       	Insert o;
        
        //Create a mock Quote object
        Quote quote = new Quote();
        quote.Name = 'Test Quote';
        quote.Pricebook2Id = testPricebook.Id;
        quote.OpportunityId= o.Id;
        insert quote;
        
        //Create a mock Product2 object
        Product2 product = new Product2();
        product.Name = 'Test Product';        
        insert product;
        
         //Make product entry in standard and custom priceooks
         PriceBookEntry stdPre1 = new PriceBookEntry(
         IsActive = true,
         PriceBook2Id = stdPriceBookId, 
         Product2Id = product.Id , 
         UnitPrice= 100);
		 insert stdPre1;
      
        PriceBookEntry pre1 = new PriceBookEntry(
        IsActive = true,
        PriceBook2Id = testPricebook.Id, 
        Product2Id = product.Id , 
        UnitPrice= 100);
		insert pre1;  
        
        // Create a list of QuoteLineItemInput objects
        List<QuoteLineItem> quoteLineItems = new List<QuoteLineItem>();
        for (Integer i = 0; i < 5; i++) {
            QuoteLineItem item = new QuoteLineItem();
            item.Product2Id = product.ID;
            item.QuoteId = quote.ID;
            item.Quantity = i + 1;
            item.UnitPrice = 100 + i; 
            item.PricebookEntryId = pre1.Id;
            quoteLineItems.add(item);
        }
		insert quoteLineItems;
  
        // Verify that the QuoteLineItems were created
        List<QuoteLineItem> dbItems = [
            SELECT Id, Product2Id, QuoteId, Quantity, ListPrice, UnitPrice
            FROM QuoteLineItem
            WHERE QuoteId = :quote.Id
            Limit 1
        ];
        
        Test.startTest();

        // Set up the controller and extension for the Quote record
        ApexPages.StandardController standardController = new ApexPages.StandardController(quote);
        QliExtension qliExtension = new QliExtension(standardController);

        // Verify that the extension has the correct current quote
        System.assertEquals(quote.Id, qliExtension.CurrentQuote.Id, 'CurrentQuote should be set correctly');

        // Verify that the extension has the correct list of quote line items
     //   System.assertEquals(5, qliExtension.QuoteLineItems.size(), 'QuoteLineItems should be retrieved correctly');
  
        Test.stopTest();
      //  }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class QliExtensionTest {
    static testMethod void testCreateQuoteLineItems() {
        
        Pricebook2 testPricebook = new Pricebook2(Name = 'Test Pricebook', isActive = true);
        insert testPricebook;
        System.debug('testPricebook.Id' +testPricebook.Id);        
        
         //Get standard pricebook id
         Id stdPriceBookId= Test.getStandardPricebookId();        
     
        //Create Account
        Account a = new Account(
            Name = 'Test');
        Insert a;
        
        //Create Opportunity
        Opportunity o = new Opportunity();
       	o.AccountID=a.ID;
       	o.Name=a.Name;
       	o.CloseDate=System.Today().addDays(3);
       	o.StageName='Prospecting';
        o.Market_Segment__c = 'Biopharma';
       	Insert o;
        
        //Create a mock Quote object
        Quote quote = new Quote();
        quote.Name = 'Test Quote';
        quote.Pricebook2Id = testPricebook.Id;
        quote.OpportunityId= o.Id;
        insert quote;
        
        //Create a mock Product2 object
        Product2 product = new Product2();
        product.Name = 'Test Product';        
        insert product;
        
         //Make product entry in standard and custom priceooks
         PriceBookEntry stdPre1 = new PriceBookEntry(
         IsActive = true,
         PriceBook2Id = stdPriceBookId, 
         Product2Id = product.Id , 
         UnitPrice= 100);
		 insert stdPre1;
      
        PriceBookEntry pre1 = new PriceBookEntry(
        IsActive = true,
        PriceBook2Id = testPricebook.Id, 
        Product2Id = product.Id , 
        UnitPrice= 100);
		insert pre1;  
        
        // Create a list of QuoteLineItemInput objects
        List<QuoteLineItem> quoteLineItems = new List<QuoteLineItem>();
        for (Integer i = 0; i < 5; i++) {
            QuoteLineItem item = new QuoteLineItem();
            item.Product2Id = product.ID;
            item.QuoteId = quote.ID;
            item.Quantity = i + 1;
            item.UnitPrice = 100 + i; 
            item.PricebookEntryId = pre1.Id;
            quoteLineItems.add(item);
        }
		insert quoteLineItems;
  
        // Verify that the QuoteLineItems were created
        List<QuoteLineItem> dbItems = [
            SELECT Id, Product2Id, QuoteId, Quantity, ListPrice, UnitPrice
            FROM QuoteLineItem
            WHERE QuoteId = :quote.Id
            Limit 1
        ];
        
        Test.startTest();

        // Set up the controller and extension for the Quote record
        ApexPages.StandardController standardController = new ApexPages.StandardController(quote);
        QliExtension qliExtension = new QliExtension(standardController);

        // Verify that the extension has the correct current quote
        System.assertEquals(quote.Id, qliExtension.CurrentQuote.Id, 'CurrentQuote should be set correctly');

        // Verify that the extension has the correct list of quote line items
     //   System.assertEquals(5, qliExtension.QuoteLineItems.size(), 'QuoteLineItems should be retrieved correctly');
  
        Test.stopTest();
      //  }
    }
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class QliExtensionTest {
  static testMethod void testCreateQuoteLineItems() {
    Pricebook2 testPricebook = new Pricebook2(
      Name = 'Test Pricebook',
      isActive = true
    );
    insert testPricebook;
    System.debug('testPricebook.Id' + testPricebook.Id);

    //Get standard pricebook id
    Id stdPriceBookId = Test.getStandardPricebookId();

    //Create Account
    Account a = new Account(Name = 'Test');
    insert a;

    //Create Opportunity
    Opportunity o = new Opportunity();
    o.AccountID = a.ID;
    o.Name = a.Name;
    o.CloseDate = System.Today().addDays(3);
    o.StageName = 'Prospecting';
    o.Market_Segment__c = 'Biopharma';
    insert o;

    //Create a mock Quote object
    Quote quote = new Quote();
    quote.Name = 'Test Quote';
    quote.Pricebook2Id = testPricebook.Id;
    quote.OpportunityId = o.Id;
    insert quote;

    //Create a mock Product2 object
    Product2 product = new Product2();
    product.Name = 'Test Product';
    insert product;

    //Make product entry in standard and custom priceooks
    PriceBookEntry stdPre1 = new PriceBookEntry(
      IsActive = true,
      PriceBook2Id = stdPriceBookId,
      Product2Id = product.Id,
      UnitPrice = 100
    );
    insert stdPre1;

    PriceBookEntry pre1 = new PriceBookEntry(
      IsActive = true,
      PriceBook2Id = testPricebook.Id,
      Product2Id = product.Id,
      UnitPrice = 100
    );
    insert pre1;

    // Create a list of QuoteLineItemInput objects
    List<QuoteLineItem> quoteLineItems = new List<QuoteLineItem>();
    for (Integer i = 0; i < 5; i++) {
      QuoteLineItem item = new QuoteLineItem();
      item.Product2Id = product.ID;
      item.QuoteId = quote.ID;
      item.Quantity = i + 1;
      item.UnitPrice = 100 + i;
      item.PricebookEntryId = pre1.Id;
      quoteLineItems.add(item);
    }
    insert quoteLineItems;

    // Verify that the QuoteLineItems were created
    List<QuoteLineItem> dbItems = [
      SELECT Id, Product2Id, QuoteId, Quantity, ListPrice, UnitPrice
      FROM QuoteLineItem
      WHERE QuoteId = :quote.Id
      LIMIT 1
    ];

    Test.startTest();

    // Set up the controller and extension for the Quote record
    ApexPages.StandardController standardController = new ApexPages.StandardController(
      quote
    );
    QliExtension qliExtension = new QliExtension(standardController);

    // Verify that the extension has the correct current quote
    System.assertEquals(
      quote.Id,
      qliExtension.CurrentQuote.Id,
      'CurrentQuote should be set correctly'
    );

    // Verify that the extension has the correct list of quote line items
    System.assertEquals(
      5,
      qliExtension.QuoteLineItems.size(),
      'QuoteLineItems should be retrieved correctly'
    );

    Test.stopTest();
    //  }
  }
}

```

## Methods
### `testCreateQuoteLineItems()`

#### Signature
```apex
private static testMethod void testCreateQuoteLineItems()
```

#### Return Type
**void**