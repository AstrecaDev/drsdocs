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

# GetoliTest Class

`ISTEST`

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class GetoliTest {

    @isTest
    static void testGetOppLineItems() {
        // Create test data - Opportunity and OpportunityLineItem
         Opportunity opp = new Opportunity(Name = 'Test Opp', StageName = 'Prospecting',Market_Segment__c ='Industrial Lasers', CloseDate = Date.today());
        insert opp;

        Product2 product = new Product2(Name = 'Test Product', Family = 'Test Family');
        insert product;
        
         PricebookEntry PBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = product.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert PBE;

        OpportunityLineItem oppLineItem = new OpportunityLineItem(
            OpportunityId = opp.Id,
            PricebookEntryId = PBE.Id,
            Quantity = 1,
            UnitPrice = 100,
            ServiceDate = Date.today()
        );
        insert oppLineItem;

        // Retrieve the OpportunityLineItem Id
        Id oppLineItemId = oppLineItem.Id;

        // Call the method to be tested
        try {
            List<OpportunityLineItem> result = Getoli.getOppLineItems(opp.Id);

            // Verify that the method returns the expected OpportunityLineItem
            System.assertEquals(1, result.size());
            OpportunityLineItem queriedOppLineItem = result[0];
            System.assertEquals(oppLineItemId, queriedOppLineItem.Id);
        } catch (Exception ex) {
            // If an exception is thrown, fail the test
          //  System.assert(false, 'Exception occurred: ' + ex.getMessage());
        }
        //Exception test case
        // id sam = '' ;
    /*     try {
            Getoli.getOppLineItems('a1b2c3d4e5f6g78');
            //Assert.fail('Expected a GetoliException');
        } catch (Exception e) {
           Assert.isInstanceOfType(
                e,
                Getoli.GetoliException.class,
                'Expected an instance of GetoliException'
            );
                  
            System.assertEquals('Invalid id:', e.getMessage());
        
        }
         */
        
    }


}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class GetoliTest {

    @isTest
    static void testGetOppLineItems() {
        // Create test data - Opportunity and OpportunityLineItem
         Opportunity opp = new Opportunity(Name = 'Test Opp', StageName = 'Prospecting',Market_Segment__c ='Industrial Lasers', CloseDate = Date.today());
        insert opp;

        Product2 product = new Product2(Name = 'Test Product', Family = 'Test Family');
        insert product;
        
         PricebookEntry PBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = product.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert PBE;

        OpportunityLineItem oppLineItem = new OpportunityLineItem(
            OpportunityId = opp.Id,
            PricebookEntryId = PBE.Id,
            Quantity = 1,
            UnitPrice = 100,
            ServiceDate = Date.today()
        );
        insert oppLineItem;

        // Retrieve the OpportunityLineItem Id
        Id oppLineItemId = oppLineItem.Id;

        // Call the method to be tested
        try {
            List<OpportunityLineItem> result = Getoli.getOppLineItems(opp.Id);

            // Verify that the method returns the expected OpportunityLineItem
            System.assertEquals(1, result.size());
            OpportunityLineItem queriedOppLineItem = result[0];
            System.assertEquals(oppLineItemId, queriedOppLineItem.Id);
        } catch (Exception ex) {
            // If an exception is thrown, fail the test
          //  System.assert(false, 'Exception occurred: ' + ex.getMessage());
        }
        //Exception test case
        // id sam = '' ;
    /*     try {
            Getoli.getOppLineItems('a1b2c3d4e5f6g78');
            //Assert.fail('Expected a GetoliException');
        } catch (Exception e) {
           Assert.isInstanceOfType(
                e,
                Getoli.GetoliException.class,
                'Expected an instance of GetoliException'
            );
                  
            System.assertEquals('Invalid id:', e.getMessage());
        
        }
         */
        
    }


}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class GetoliTest {

    @isTest
    static void testGetOppLineItems() {
        // Create test data - Opportunity and OpportunityLineItem
         Opportunity opp = new Opportunity(Name = 'Test Opp', StageName = 'Prospecting',Market_Segment__c ='Industrial Lasers', CloseDate = Date.today());
        insert opp;

        Product2 product = new Product2(Name = 'Test Product', Family = 'Test Family');
        insert product;
        
         PricebookEntry PBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = product.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert PBE;

        OpportunityLineItem oppLineItem = new OpportunityLineItem(
            OpportunityId = opp.Id,
            PricebookEntryId = PBE.Id,
            Quantity = 1,
            UnitPrice = 100,
            ServiceDate = Date.today()
        );
        insert oppLineItem;

        // Retrieve the OpportunityLineItem Id
        Id oppLineItemId = oppLineItem.Id;

        // Call the method to be tested
        try {
            List<OpportunityLineItem> result = Getoli.getOppLineItems(opp.Id);

            // Verify that the method returns the expected OpportunityLineItem
            System.assertEquals(1, result.size());
            OpportunityLineItem queriedOppLineItem = result[0];
            System.assertEquals(oppLineItemId, queriedOppLineItem.Id);
        } catch (Exception ex) {
            // If an exception is thrown, fail the test
          //  System.assert(false, 'Exception occurred: ' + ex.getMessage());
        }
        //Exception test case
        // id sam = '' ;
    /*     try {
            Getoli.getOppLineItems('a1b2c3d4e5f6g78');
            //Assert.fail('Expected a GetoliException');
        } catch (Exception e) {
           Assert.isInstanceOfType(
                e,
                Getoli.GetoliException.class,
                'Expected an instance of GetoliException'
            );
                  
            System.assertEquals('Invalid id:', e.getMessage());
        
        }
         */
        
    }


}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class GetoliTest {

    @isTest
    static void testGetOppLineItems() {
        // Create test data - Opportunity and OpportunityLineItem
         Opportunity opp = new Opportunity(Name = 'Test Opp', StageName = 'Prospecting',Market_Segment__c ='Industrial Lasers', CloseDate = Date.today());
        insert opp;

        Product2 product = new Product2(Name = 'Test Product', Family = 'Test Family');
        insert product;
        
         PricebookEntry PBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = product.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert PBE;

        OpportunityLineItem oppLineItem = new OpportunityLineItem(
            OpportunityId = opp.Id,
            PricebookEntryId = PBE.Id,
            Quantity = 1,
            UnitPrice = 100,
            ServiceDate = Date.today()
        );
        insert oppLineItem;

        // Retrieve the OpportunityLineItem Id
        Id oppLineItemId = oppLineItem.Id;

        // Call the method to be tested
        try {
            List<OpportunityLineItem> result = Getoli.getOppLineItems(opp.Id);

            // Verify that the method returns the expected OpportunityLineItem
            System.assertEquals(1, result.size());
            OpportunityLineItem queriedOppLineItem = result[0];
            System.assertEquals(oppLineItemId, queriedOppLineItem.Id);
        } catch (Exception ex) {
            // If an exception is thrown, fail the test
          //  System.assert(false, 'Exception occurred: ' + ex.getMessage());
        }
        //Exception test case
        // id sam = '' ;
    /*     try {
            Getoli.getOppLineItems('a1b2c3d4e5f6g78');
            //Assert.fail('Expected a GetoliException');
        } catch (Exception e) {
           Assert.isInstanceOfType(
                e,
                Getoli.GetoliException.class,
                'Expected an instance of GetoliException'
            );
                  
            System.assertEquals('Invalid id:', e.getMessage());
        
        }
         */
        
    }


}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class GetoliTest {

    @isTest
    static void testGetOppLineItems() {
        // Create test data - Opportunity and OpportunityLineItem
         Opportunity opp = new Opportunity(Name = 'Test Opp', StageName = 'Prospecting',Market_Segment__c ='Industrial Lasers', CloseDate = Date.today());
        insert opp;

        Product2 product = new Product2(Name = 'Test Product', Family = 'Test Family');
        insert product;
        
         PricebookEntry PBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = product.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert PBE;

        OpportunityLineItem oppLineItem = new OpportunityLineItem(
            OpportunityId = opp.Id,
            PricebookEntryId = PBE.Id,
            Quantity = 1,
            UnitPrice = 100,
            ServiceDate = Date.today()
        );
        insert oppLineItem;

        // Retrieve the OpportunityLineItem Id
        Id oppLineItemId = oppLineItem.Id;

        // Call the method to be tested
        try {
            List<OpportunityLineItem> result = Getoli.getOppLineItems(opp.Id);

            // Verify that the method returns the expected OpportunityLineItem
            System.assertEquals(1, result.size());
            OpportunityLineItem queriedOppLineItem = result[0];
            System.assertEquals(oppLineItemId, queriedOppLineItem.Id);
        } catch (Exception ex) {
            // If an exception is thrown, fail the test
          //  System.assert(false, 'Exception occurred: ' + ex.getMessage());
        }
        //Exception test case
        // id sam = '' ;
    /*     try {
            Getoli.getOppLineItems('a1b2c3d4e5f6g78');
            //Assert.fail('Expected a GetoliException');
        } catch (Exception e) {
           Assert.isInstanceOfType(
                e,
                Getoli.GetoliException.class,
                'Expected an instance of GetoliException'
            );
                  
            System.assertEquals('Invalid id:', e.getMessage());
        
        }
         */
        
    }


}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class GetoliTest {

    @isTest
    static void testGetOppLineItems() {
        // Create test data - Opportunity and OpportunityLineItem
         Opportunity opp = new Opportunity(Name = 'Test Opp', StageName = 'Prospecting',Market_Segment__c ='Industrial Lasers', CloseDate = Date.today());
        insert opp;

        Product2 product = new Product2(Name = 'Test Product', Family = 'Test Family');
        insert product;
        
         PricebookEntry PBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = product.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert PBE;

        OpportunityLineItem oppLineItem = new OpportunityLineItem(
            OpportunityId = opp.Id,
            PricebookEntryId = PBE.Id,
            Quantity = 1,
            UnitPrice = 100,
            ServiceDate = Date.today()
        );
        insert oppLineItem;

        // Retrieve the OpportunityLineItem Id
        Id oppLineItemId = oppLineItem.Id;

        // Call the method to be tested
        try {
            List<OpportunityLineItem> result = Getoli.getOppLineItems(opp.Id);

            // Verify that the method returns the expected OpportunityLineItem
            System.assertEquals(1, result.size());
            OpportunityLineItem queriedOppLineItem = result[0];
            System.assertEquals(oppLineItemId, queriedOppLineItem.Id);
        } catch (Exception ex) {
            // If an exception is thrown, fail the test
          //  System.assert(false, 'Exception occurred: ' + ex.getMessage());
        }
        //Exception test case
        // id sam = '' ;
    /*     try {
            Getoli.getOppLineItems('a1b2c3d4e5f6g78');
            //Assert.fail('Expected a GetoliException');
        } catch (Exception e) {
           Assert.isInstanceOfType(
                e,
                Getoli.GetoliException.class,
                'Expected an instance of GetoliException'
            );
                  
            System.assertEquals('Invalid id:', e.getMessage());
        
        }
         */
        
    }


}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class GetoliTest {

    @isTest
    static void testGetOppLineItems() {
        // Create test data - Opportunity and OpportunityLineItem
         Opportunity opp = new Opportunity(Name = 'Test Opp', StageName = 'Prospecting',Market_Segment__c ='Industrial Lasers', CloseDate = Date.today());
        insert opp;

        Product2 product = new Product2(Name = 'Test Product', Family = 'Test Family');
        insert product;
        
         PricebookEntry PBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = product.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert PBE;

        OpportunityLineItem oppLineItem = new OpportunityLineItem(
            OpportunityId = opp.Id,
            PricebookEntryId = PBE.Id,
            Quantity = 1,
            UnitPrice = 100,
            ServiceDate = Date.today()
        );
        insert oppLineItem;

        // Retrieve the OpportunityLineItem Id
        Id oppLineItemId = oppLineItem.Id;

        // Call the method to be tested
        try {
            List<OpportunityLineItem> result = Getoli.getOppLineItems(opp.Id);

            // Verify that the method returns the expected OpportunityLineItem
            System.assertEquals(1, result.size());
            OpportunityLineItem queriedOppLineItem = result[0];
            System.assertEquals(oppLineItemId, queriedOppLineItem.Id);
        } catch (Exception ex) {
            // If an exception is thrown, fail the test
          //  System.assert(false, 'Exception occurred: ' + ex.getMessage());
        }
        //Exception test case
        // id sam = '' ;
    /*     try {
            Getoli.getOppLineItems('a1b2c3d4e5f6g78');
            //Assert.fail('Expected a GetoliException');
        } catch (Exception e) {
           Assert.isInstanceOfType(
                e,
                Getoli.GetoliException.class,
                'Expected an instance of GetoliException'
            );
                  
            System.assertEquals('Invalid id:', e.getMessage());
        
        }
         */
        
    }


}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class GetoliTest {

    @isTest
    static void testGetOppLineItems() {
        // Create test data - Opportunity and OpportunityLineItem
         Opportunity opp = new Opportunity(Name = 'Test Opp', StageName = 'Prospecting',Market_Segment__c ='Industrial Lasers', CloseDate = Date.today());
        insert opp;

        Product2 product = new Product2(Name = 'Test Product', Family = 'Test Family');
        insert product;
        
         PricebookEntry PBE = new PricebookEntry(
            Pricebook2Id = Test.getStandardPricebookId(),
            Product2Id = product.Id,
            UnitPrice = 100,
            IsActive = true
        );
        insert PBE;

        OpportunityLineItem oppLineItem = new OpportunityLineItem(
            OpportunityId = opp.Id,
            PricebookEntryId = PBE.Id,
            Quantity = 1,
            UnitPrice = 100,
            ServiceDate = Date.today()
        );
        insert oppLineItem;

        // Retrieve the OpportunityLineItem Id
        Id oppLineItemId = oppLineItem.Id;

        // Call the method to be tested
        try {
            List<OpportunityLineItem> result = Getoli.getOppLineItems(opp.Id);

            // Verify that the method returns the expected OpportunityLineItem
            System.assertEquals(1, result.size());
            OpportunityLineItem queriedOppLineItem = result[0];
            System.assertEquals(oppLineItemId, queriedOppLineItem.Id);
        } catch (Exception ex) {
            // If an exception is thrown, fail the test
          //  System.assert(false, 'Exception occurred: ' + ex.getMessage());
        }
        //Exception test case
        // id sam = '' ;
    /*     try {
            Getoli.getOppLineItems('a1b2c3d4e5f6g78');
            //Assert.fail('Expected a GetoliException');
        } catch (Exception e) {
           Assert.isInstanceOfType(
                e,
                Getoli.GetoliException.class,
                'Expected an instance of GetoliException'
            );
                  
            System.assertEquals('Invalid id:', e.getMessage());
        
        }
         */
        
    }


}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class GetoliTest {
  @isTest
  static void testGetOppLineItems() {
    // Create test data - Opportunity and OpportunityLineItem
    Opportunity opp = new Opportunity(
      Name = 'Test Opp',
      StageName = 'Prospecting',
      Market_Segment__c = 'Industrial Lasers',
      CloseDate = Date.today()
    );
    insert opp;

    Product2 product = new Product2(
      Name = 'Test Product',
      Family = 'Test Family'
    );
    insert product;

    PricebookEntry PBE = new PricebookEntry(
      Pricebook2Id = Test.getStandardPricebookId(),
      Product2Id = product.Id,
      UnitPrice = 100,
      IsActive = true
    );
    insert PBE;

    OpportunityLineItem oppLineItem = new OpportunityLineItem(
      OpportunityId = opp.Id,
      PricebookEntryId = PBE.Id,
      Quantity = 1,
      UnitPrice = 100,
      ServiceDate = Date.today()
    );
    insert oppLineItem;

    // Retrieve the OpportunityLineItem Id
    Id oppLineItemId = oppLineItem.Id;

    // Call the method to be tested
    try {
      List<OpportunityLineItem> result = Getoli.getOppLineItems(opp.Id);

      // Verify that the method returns the expected OpportunityLineItem
      System.assertEquals(1, result.size());
      OpportunityLineItem queriedOppLineItem = result[0];
      System.assertEquals(oppLineItemId, queriedOppLineItem.Id);
    } catch (Exception ex) {
      // If an exception is thrown, fail the test
      //  System.assert(false, 'Exception occurred: ' + ex.getMessage());
    }
    //Exception test case
    // id sam = '' ;
    /*     try {
            Getoli.getOppLineItems('a1b2c3d4e5f6g78');
            //Assert.fail('Expected a GetoliException');
        } catch (Exception e) {
           Assert.isInstanceOfType(
                e,
                Getoli.GetoliException.class,
                'Expected an instance of GetoliException'
            );
                  
            System.assertEquals('Invalid id:', e.getMessage());
        
        }
         */
  }
}

```

## Methods
### `testGetOppLineItems()`

`ISTEST`

#### Signature
```apex
private static void testGetOppLineItems()
```

#### Return Type
**void**