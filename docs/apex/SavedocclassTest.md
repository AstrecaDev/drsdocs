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

# SavedocclassTest Class

`ISTEST`

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
Public class SavedocclassTest {
  
      @isTest
    static void testGetTimeDate() {
        // Set up test user with a specific time zone
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Run the method to test
        Test.startTest();
        String formattedDate = Savedocclass.gettimedate();
        Test.stopTest();

        // Verify the result
        System.debug('Formatted Date: ' + formattedDate);
        
        // Verify that the returned date matches the expected format
        // Example format: 2023-06-26 4:05 PM
        String dateTimePattern = '\\d{4}-\\d{2}-\\d{2} \\d{1,2}:\\d{2} (AM|PM)';
        System.assert(Pattern.matches(dateTimePattern, formattedDate), 'The formatted date does not match the expected pattern');
    }
    
    
    @isTest
    static void testCreateContentFromQuote() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.newquote;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromQuote(testQuote.Id, mockPdfContent);
        
         String result2 = Savedocclass.createContentFromQuote(testQuote.Id,null);
        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'Quote-%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('Quote'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }

    //Test method for Quote term 
      @isTest
    static void testcreateContentFromQuoteterm() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.QuoteTerms;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromQuoteterm(testQuote.Id, mockPdfContent);
        
        String result2 = Savedocclass.createContentFromQuoteterm(testQuote.Id,null);
        
        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'QuoteTerms%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('QuoteTerms'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }
    
    // Test method for Product Specification
      @isTest
    static void testcreateContentFromPS() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.ProductSpecification;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromPS(testQuote.Id, mockPdfContent);
        
        String result2 = Savedocclass.createContentFromPS(testQuote.Id,null);

        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'ProductSpecification%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('ProductSpecification'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }
    
     @IsTest
    static void testCreateContentFromQuoteNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromQuote(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
      @IsTest
    static void testCreateContentFromQuotetermNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromQuoteterm(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
      @IsTest
    static void testCreateContentFromPSNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromPS(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
    @IsTest
    static void testCreateContentFromQuoteErrorGeneratingPdf() {
        // Setup test data
        Quote testQuote = new Quote(Name = 'Test Quote');
        insert testQuote;
        
        // Call the method without mock PDF content
        // This will cause the pdfPage.getContent() to be called, which will throw an exception in a test context
        String result = Savedocclass.createContentFromQuote(testQuote.Id, null);
         String result2 = Savedocclass.createContentFromQuoteterm(testQuote.Id, null);
         String result3 = Savedocclass.createContentFromPS(testQuote.Id, null);
        
        // Verify the result
        System.assert(result.startsWith('Error generating PDF'));
         System.assert(result2.startsWith('Error generating PDF'));
         System.assert(result3.startsWith('Error generating PDF'));
    }
    
    
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
Public class SavedocclassTest {
  
      @isTest
    static void testGetTimeDate() {
        // Set up test user with a specific time zone
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Run the method to test
        Test.startTest();
        String formattedDate = Savedocclass.gettimedate();
        Test.stopTest();

        // Verify the result
        System.debug('Formatted Date: ' + formattedDate);
        
        // Verify that the returned date matches the expected format
        // Example format: 2023-06-26 4:05 PM
        String dateTimePattern = '\\d{4}-\\d{2}-\\d{2} \\d{1,2}:\\d{2} (AM|PM)';
        System.assert(Pattern.matches(dateTimePattern, formattedDate), 'The formatted date does not match the expected pattern');
    }
    
    
    @isTest
    static void testCreateContentFromQuote() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.newquote;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromQuote(testQuote.Id, mockPdfContent);
        
         String result2 = Savedocclass.createContentFromQuote(testQuote.Id,null);
        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'Quote-%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('Quote'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }

    //Test method for Quote term 
      @isTest
    static void testcreateContentFromQuoteterm() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.QuoteTerms;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromQuoteterm(testQuote.Id, mockPdfContent);
        
        String result2 = Savedocclass.createContentFromQuoteterm(testQuote.Id,null);
        
        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'QuoteTerms%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('QuoteTerms'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }
    
    // Test method for Product Specification
      @isTest
    static void testcreateContentFromPS() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.ProductSpecification;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromPS(testQuote.Id, mockPdfContent);
        
        String result2 = Savedocclass.createContentFromPS(testQuote.Id,null);

        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'ProductSpecification%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('ProductSpecification'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }
    
     @IsTest
    static void testCreateContentFromQuoteNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromQuote(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
      @IsTest
    static void testCreateContentFromQuotetermNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromQuoteterm(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
      @IsTest
    static void testCreateContentFromPSNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromPS(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
    @IsTest
    static void testCreateContentFromQuoteErrorGeneratingPdf() {
        // Setup test data
        Quote testQuote = new Quote(Name = 'Test Quote');
        insert testQuote;
        
        // Call the method without mock PDF content
        // This will cause the pdfPage.getContent() to be called, which will throw an exception in a test context
        String result = Savedocclass.createContentFromQuote(testQuote.Id, null);
         String result2 = Savedocclass.createContentFromQuoteterm(testQuote.Id, null);
         String result3 = Savedocclass.createContentFromPS(testQuote.Id, null);
        
        // Verify the result
        System.assert(result.startsWith('Error generating PDF'));
         System.assert(result2.startsWith('Error generating PDF'));
         System.assert(result3.startsWith('Error generating PDF'));
    }
    
    
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
Public class SavedocclassTest {
  
      @isTest
    static void testGetTimeDate() {
        // Set up test user with a specific time zone
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Run the method to test
        Test.startTest();
        String formattedDate = Savedocclass.gettimedate();
        Test.stopTest();

        // Verify the result
        System.debug('Formatted Date: ' + formattedDate);
        
        // Verify that the returned date matches the expected format
        // Example format: 2023-06-26 4:05 PM
        String dateTimePattern = '\\d{4}-\\d{2}-\\d{2} \\d{1,2}:\\d{2} (AM|PM)';
        System.assert(Pattern.matches(dateTimePattern, formattedDate), 'The formatted date does not match the expected pattern');
    }
    
    
    @isTest
    static void testCreateContentFromQuote() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.newquote;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromQuote(testQuote.Id, mockPdfContent);
        
         String result2 = Savedocclass.createContentFromQuote(testQuote.Id,null);
        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'Quote-%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('Quote'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }

    //Test method for Quote term 
      @isTest
    static void testcreateContentFromQuoteterm() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.QuoteTerms;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromQuoteterm(testQuote.Id, mockPdfContent);
        
        String result2 = Savedocclass.createContentFromQuoteterm(testQuote.Id,null);
        
        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'QuoteTerms%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('QuoteTerms'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }
    
    // Test method for Product Specification
      @isTest
    static void testcreateContentFromPS() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.ProductSpecification;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromPS(testQuote.Id, mockPdfContent);
        
        String result2 = Savedocclass.createContentFromPS(testQuote.Id,null);

        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'ProductSpecification%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('ProductSpecification'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }
    
     @IsTest
    static void testCreateContentFromQuoteNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromQuote(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
      @IsTest
    static void testCreateContentFromQuotetermNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromQuoteterm(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
      @IsTest
    static void testCreateContentFromPSNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromPS(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
    @IsTest
    static void testCreateContentFromQuoteErrorGeneratingPdf() {
        // Setup test data
        Quote testQuote = new Quote(Name = 'Test Quote');
        insert testQuote;
        
        // Call the method without mock PDF content
        // This will cause the pdfPage.getContent() to be called, which will throw an exception in a test context
        String result = Savedocclass.createContentFromQuote(testQuote.Id, null);
         String result2 = Savedocclass.createContentFromQuoteterm(testQuote.Id, null);
         String result3 = Savedocclass.createContentFromPS(testQuote.Id, null);
        
        // Verify the result
        System.assert(result.startsWith('Error generating PDF'));
         System.assert(result2.startsWith('Error generating PDF'));
         System.assert(result3.startsWith('Error generating PDF'));
    }
    
    
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
Public class SavedocclassTest {
  
      @isTest
    static void testGetTimeDate() {
        // Set up test user with a specific time zone
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Run the method to test
        Test.startTest();
        String formattedDate = Savedocclass.gettimedate();
        Test.stopTest();

        // Verify the result
        System.debug('Formatted Date: ' + formattedDate);
        
        // Verify that the returned date matches the expected format
        // Example format: 2023-06-26 4:05 PM
        String dateTimePattern = '\\d{4}-\\d{2}-\\d{2} \\d{1,2}:\\d{2} (AM|PM)';
        System.assert(Pattern.matches(dateTimePattern, formattedDate), 'The formatted date does not match the expected pattern');
    }
    
    
    @isTest
    static void testCreateContentFromQuote() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.newquote;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromQuote(testQuote.Id, mockPdfContent);
        
         String result2 = Savedocclass.createContentFromQuote(testQuote.Id,null);
        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'Quote-%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('Quote'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }

    //Test method for Quote term 
      @isTest
    static void testcreateContentFromQuoteterm() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.QuoteTerms;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromQuoteterm(testQuote.Id, mockPdfContent);
        
        String result2 = Savedocclass.createContentFromQuoteterm(testQuote.Id,null);
        
        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'QuoteTerms%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('QuoteTerms'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }
    
    // Test method for Product Specification
      @isTest
    static void testcreateContentFromPS() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.ProductSpecification;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromPS(testQuote.Id, mockPdfContent);
        
        String result2 = Savedocclass.createContentFromPS(testQuote.Id,null);

        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'ProductSpecification%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('ProductSpecification'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }
    
     @IsTest
    static void testCreateContentFromQuoteNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromQuote(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
      @IsTest
    static void testCreateContentFromQuotetermNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromQuoteterm(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
      @IsTest
    static void testCreateContentFromPSNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromPS(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
    @IsTest
    static void testCreateContentFromQuoteErrorGeneratingPdf() {
        // Setup test data
        Quote testQuote = new Quote(Name = 'Test Quote');
        insert testQuote;
        
        // Call the method without mock PDF content
        // This will cause the pdfPage.getContent() to be called, which will throw an exception in a test context
        String result = Savedocclass.createContentFromQuote(testQuote.Id, null);
         String result2 = Savedocclass.createContentFromQuoteterm(testQuote.Id, null);
         String result3 = Savedocclass.createContentFromPS(testQuote.Id, null);
        
        // Verify the result
        System.assert(result.startsWith('Error generating PDF'));
         System.assert(result2.startsWith('Error generating PDF'));
         System.assert(result3.startsWith('Error generating PDF'));
    }
    
    
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
Public class SavedocclassTest {
  
      @isTest
    static void testGetTimeDate() {
        // Set up test user with a specific time zone
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Run the method to test
        Test.startTest();
        String formattedDate = Savedocclass.gettimedate();
        Test.stopTest();

        // Verify the result
        System.debug('Formatted Date: ' + formattedDate);
        
        // Verify that the returned date matches the expected format
        // Example format: 2023-06-26 4:05 PM
        String dateTimePattern = '\\d{4}-\\d{2}-\\d{2} \\d{1,2}:\\d{2} (AM|PM)';
        System.assert(Pattern.matches(dateTimePattern, formattedDate), 'The formatted date does not match the expected pattern');
    }
    
    
    @isTest
    static void testCreateContentFromQuote() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.newquote;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromQuote(testQuote.Id, mockPdfContent);
        
         String result2 = Savedocclass.createContentFromQuote(testQuote.Id,null);
        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'Quote-%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('Quote'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }

    //Test method for Quote term 
      @isTest
    static void testcreateContentFromQuoteterm() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.QuoteTerms;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromQuoteterm(testQuote.Id, mockPdfContent);
        
        String result2 = Savedocclass.createContentFromQuoteterm(testQuote.Id,null);
        
        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'QuoteTerms%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('QuoteTerms'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }
    
    // Test method for Product Specification
      @isTest
    static void testcreateContentFromPS() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.ProductSpecification;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromPS(testQuote.Id, mockPdfContent);
        
        String result2 = Savedocclass.createContentFromPS(testQuote.Id,null);

        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'ProductSpecification%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('ProductSpecification'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }
    
     @IsTest
    static void testCreateContentFromQuoteNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromQuote(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
      @IsTest
    static void testCreateContentFromQuotetermNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromQuoteterm(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
      @IsTest
    static void testCreateContentFromPSNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromPS(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
    @IsTest
    static void testCreateContentFromQuoteErrorGeneratingPdf() {
        // Setup test data
        Quote testQuote = new Quote(Name = 'Test Quote');
        insert testQuote;
        
        // Call the method without mock PDF content
        // This will cause the pdfPage.getContent() to be called, which will throw an exception in a test context
        String result = Savedocclass.createContentFromQuote(testQuote.Id, null);
         String result2 = Savedocclass.createContentFromQuoteterm(testQuote.Id, null);
         String result3 = Savedocclass.createContentFromPS(testQuote.Id, null);
        
        // Verify the result
        System.assert(result.startsWith('Error generating PDF'));
         System.assert(result2.startsWith('Error generating PDF'));
         System.assert(result3.startsWith('Error generating PDF'));
    }
    
    
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
Public class SavedocclassTest {
  
      @isTest
    static void testGetTimeDate() {
        // Set up test user with a specific time zone
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Run the method to test
        Test.startTest();
        String formattedDate = Savedocclass.gettimedate();
        Test.stopTest();

        // Verify the result
        System.debug('Formatted Date: ' + formattedDate);
        
        // Verify that the returned date matches the expected format
        // Example format: 2023-06-26 4:05 PM
        String dateTimePattern = '\\d{4}-\\d{2}-\\d{2} \\d{1,2}:\\d{2} (AM|PM)';
        System.assert(Pattern.matches(dateTimePattern, formattedDate), 'The formatted date does not match the expected pattern');
    }
    
    
    @isTest
    static void testCreateContentFromQuote() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.newquote;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromQuote(testQuote.Id, mockPdfContent);
        
         String result2 = Savedocclass.createContentFromQuote(testQuote.Id,null);
        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'Quote-%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('Quote'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }

    //Test method for Quote term 
      @isTest
    static void testcreateContentFromQuoteterm() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.QuoteTerms;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromQuoteterm(testQuote.Id, mockPdfContent);
        
        String result2 = Savedocclass.createContentFromQuoteterm(testQuote.Id,null);
        
        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'QuoteTerms%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('QuoteTerms'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }
    
    // Test method for Product Specification
      @isTest
    static void testcreateContentFromPS() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.ProductSpecification;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromPS(testQuote.Id, mockPdfContent);
        
        String result2 = Savedocclass.createContentFromPS(testQuote.Id,null);

        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'ProductSpecification%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('ProductSpecification'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }
    
     @IsTest
    static void testCreateContentFromQuoteNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromQuote(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
      @IsTest
    static void testCreateContentFromQuotetermNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromQuoteterm(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
      @IsTest
    static void testCreateContentFromPSNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromPS(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
    @IsTest
    static void testCreateContentFromQuoteErrorGeneratingPdf() {
        // Setup test data
        Quote testQuote = new Quote(Name = 'Test Quote');
        insert testQuote;
        
        // Call the method without mock PDF content
        // This will cause the pdfPage.getContent() to be called, which will throw an exception in a test context
        String result = Savedocclass.createContentFromQuote(testQuote.Id, null);
         String result2 = Savedocclass.createContentFromQuoteterm(testQuote.Id, null);
         String result3 = Savedocclass.createContentFromPS(testQuote.Id, null);
        
        // Verify the result
        System.assert(result.startsWith('Error generating PDF'));
         System.assert(result2.startsWith('Error generating PDF'));
         System.assert(result3.startsWith('Error generating PDF'));
    }
    
    
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
Public class SavedocclassTest {
  
      @isTest
    static void testGetTimeDate() {
        // Set up test user with a specific time zone
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Run the method to test
        Test.startTest();
        String formattedDate = Savedocclass.gettimedate();
        Test.stopTest();

        // Verify the result
        System.debug('Formatted Date: ' + formattedDate);
        
        // Verify that the returned date matches the expected format
        // Example format: 2023-06-26 4:05 PM
        String dateTimePattern = '\\d{4}-\\d{2}-\\d{2} \\d{1,2}:\\d{2} (AM|PM)';
        System.assert(Pattern.matches(dateTimePattern, formattedDate), 'The formatted date does not match the expected pattern');
    }
    
    
    @isTest
    static void testCreateContentFromQuote() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.newquote;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromQuote(testQuote.Id, mockPdfContent);
        
         String result2 = Savedocclass.createContentFromQuote(testQuote.Id,null);
        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'Quote-%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('Quote'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }

    //Test method for Quote term 
      @isTest
    static void testcreateContentFromQuoteterm() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.QuoteTerms;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromQuoteterm(testQuote.Id, mockPdfContent);
        
        String result2 = Savedocclass.createContentFromQuoteterm(testQuote.Id,null);
        
        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'QuoteTerms%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('QuoteTerms'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }
    
    // Test method for Product Specification
      @isTest
    static void testcreateContentFromPS() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.ProductSpecification;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromPS(testQuote.Id, mockPdfContent);
        
        String result2 = Savedocclass.createContentFromPS(testQuote.Id,null);

        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'ProductSpecification%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('ProductSpecification'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }
    
     @IsTest
    static void testCreateContentFromQuoteNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromQuote(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
      @IsTest
    static void testCreateContentFromQuotetermNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromQuoteterm(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
      @IsTest
    static void testCreateContentFromPSNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromPS(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
    @IsTest
    static void testCreateContentFromQuoteErrorGeneratingPdf() {
        // Setup test data
        Quote testQuote = new Quote(Name = 'Test Quote');
        insert testQuote;
        
        // Call the method without mock PDF content
        // This will cause the pdfPage.getContent() to be called, which will throw an exception in a test context
        String result = Savedocclass.createContentFromQuote(testQuote.Id, null);
         String result2 = Savedocclass.createContentFromQuoteterm(testQuote.Id, null);
         String result3 = Savedocclass.createContentFromPS(testQuote.Id, null);
        
        // Verify the result
        System.assert(result.startsWith('Error generating PDF'));
         System.assert(result2.startsWith('Error generating PDF'));
         System.assert(result3.startsWith('Error generating PDF'));
    }
    
    
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
Public class SavedocclassTest {
  
      @isTest
    static void testGetTimeDate() {
        // Set up test user with a specific time zone
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Run the method to test
        Test.startTest();
        String formattedDate = Savedocclass.gettimedate();
        Test.stopTest();

        // Verify the result
        System.debug('Formatted Date: ' + formattedDate);
        
        // Verify that the returned date matches the expected format
        // Example format: 2023-06-26 4:05 PM
        String dateTimePattern = '\\d{4}-\\d{2}-\\d{2} \\d{1,2}:\\d{2} (AM|PM)';
        System.assert(Pattern.matches(dateTimePattern, formattedDate), 'The formatted date does not match the expected pattern');
    }
    
    
    @isTest
    static void testCreateContentFromQuote() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.newquote;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromQuote(testQuote.Id, mockPdfContent);
        
         String result2 = Savedocclass.createContentFromQuote(testQuote.Id,null);
        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'Quote-%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('Quote'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }

    //Test method for Quote term 
      @isTest
    static void testcreateContentFromQuoteterm() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.QuoteTerms;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromQuoteterm(testQuote.Id, mockPdfContent);
        
        String result2 = Savedocclass.createContentFromQuoteterm(testQuote.Id,null);
        
        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'QuoteTerms%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('QuoteTerms'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }
    
    // Test method for Product Specification
      @isTest
    static void testcreateContentFromPS() {
        // Arrange
        Account a = new Account(Name = 'test1');
        insert a;
        Opportunity o = new Opportunity(AccountId = a.Id, CloseDate = system.today(),StageName = 'Funded', Name = 'Test opp',market_segment__c='AAM');
        insert o;
        Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
        insert testQuote;

        // Assert
      
        // Setup current user with specific time zone if necessary
        User testUser = [SELECT Id, TimeZoneSidKey FROM User WHERE Id = :UserInfo.getUserId()];
        testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
        update testUser;

        // Mock PDF content
        Blob mockPdfContent = Blob.valueOf('Mock PDF content');
        
        // Set the current page to simulate the PageReference
        PageReference testPageRef = Page.ProductSpecification;
        testPageRef.getParameters().put('id', testQuote.Id);
        Test.setCurrentPage(testPageRef);

        // Start test
        Test.startTest();

        // Call the method to test
        String result = Savedocclass.createContentFromPS(testQuote.Id, mockPdfContent);
        
        String result2 = Savedocclass.createContentFromPS(testQuote.Id,null);

        // Stop test
        Test.stopTest();

        // Verify the result
        System.assertEquals('Success', result, 'The method did not return the expected result.');

        // Verify ContentVersion was created
        List<ContentVersion> contentVersions = [SELECT Id, Title, VersionData FROM ContentVersion WHERE Title LIKE 'ProductSpecification%'];
        System.assert(contentVersions.size() == 1, 'ContentVersion was not created correctly.');
        System.assert(contentVersions[0].Title.contains('ProductSpecification'), 'ContentVersion title does not match.');

        // Verify ContentDocumentLink was created
        List<ContentDocumentLink> contentDocumentLinks = [SELECT Id FROM ContentDocumentLink WHERE LinkedEntityId = :testQuote.Id];
        System.assert(contentDocumentLinks.size() == 1, 'ContentDocumentLink was not created correctly.');
    }
    
     @IsTest
    static void testCreateContentFromQuoteNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromQuote(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
      @IsTest
    static void testCreateContentFromQuotetermNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromQuoteterm(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
      @IsTest
    static void testCreateContentFromPSNoQuote() {
        // Call the method with a non-existing quote Id
        String result = Savedocclass.createContentFromPS(Id.valueOf('0Q0VB0000005hVl0AI'), null);
        
        // Verify the result
        System.assertEquals('No Quote found', result);
    }
    
    @IsTest
    static void testCreateContentFromQuoteErrorGeneratingPdf() {
        // Setup test data
        Quote testQuote = new Quote(Name = 'Test Quote');
        insert testQuote;
        
        // Call the method without mock PDF content
        // This will cause the pdfPage.getContent() to be called, which will throw an exception in a test context
        String result = Savedocclass.createContentFromQuote(testQuote.Id, null);
         String result2 = Savedocclass.createContentFromQuoteterm(testQuote.Id, null);
         String result3 = Savedocclass.createContentFromPS(testQuote.Id, null);
        
        // Verify the result
        System.assert(result.startsWith('Error generating PDF'));
         System.assert(result2.startsWith('Error generating PDF'));
         System.assert(result3.startsWith('Error generating PDF'));
    }
    
    
}
```

## AI-Generated description

Activate [AI configuration](https://sfdx-hardis.cloudity.com/salesforce-ai-setup/) to generate AI description

## Apex Code

```java
@isTest
public class SavedocclassTest {
  @isTest
  static void testGetTimeDate() {
    // Set up test user with a specific time zone
    User testUser = [
      SELECT Id, TimeZoneSidKey
      FROM User
      WHERE Id = :UserInfo.getUserId()
    ];
    testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
    update testUser;

    // Run the method to test
    Test.startTest();
    String formattedDate = Savedocclass.gettimedate();
    Test.stopTest();

    // Verify the result
    System.debug('Formatted Date: ' + formattedDate);

    // Verify that the returned date matches the expected format
    // Example format: 2023-06-26 4:05 PM
    String dateTimePattern = '\\d{4}-\\d{2}-\\d{2} \\d{1,2}:\\d{2} (AM|PM)';
    System.assert(
      Pattern.matches(dateTimePattern, formattedDate),
      'The formatted date does not match the expected pattern'
    );
  }

  @isTest
  static void testCreateContentFromQuote() {
    // Arrange
    Account a = new Account(Name = 'test1');
    insert a;
    Opportunity o = new Opportunity(
      AccountId = a.Id,
      CloseDate = system.today(),
      StageName = 'Funded',
      Name = 'Test opp',
      market_segment__c = 'AAM'
    );
    insert o;
    Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
    insert testQuote;

    // Assert

    // Setup current user with specific time zone if necessary
    User testUser = [
      SELECT Id, TimeZoneSidKey
      FROM User
      WHERE Id = :UserInfo.getUserId()
    ];
    testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
    update testUser;

    // Mock PDF content
    Blob mockPdfContent = Blob.valueOf('Mock PDF content');

    // Set the current page to simulate the PageReference
    PageReference testPageRef = Page.newquote;
    testPageRef.getParameters().put('id', testQuote.Id);
    Test.setCurrentPage(testPageRef);

    // Start test
    Test.startTest();

    // Call the method to test
    String result = Savedocclass.createContentFromQuote(
      testQuote.Id,
      mockPdfContent
    );

    String result2 = Savedocclass.createContentFromQuote(testQuote.Id, null);
    // Stop test
    Test.stopTest();

    // Verify the result
    System.assertEquals(
      'Success',
      result,
      'The method did not return the expected result.'
    );

    // Verify ContentVersion was created
    List<ContentVersion> contentVersions = [
      SELECT Id, Title, VersionData
      FROM ContentVersion
      WHERE Title LIKE 'Quote-%'
    ];
    System.assert(
      contentVersions.size() == 1,
      'ContentVersion was not created correctly.'
    );
    System.assert(
      contentVersions[0].Title.contains('Quote'),
      'ContentVersion title does not match.'
    );

    // Verify ContentDocumentLink was created
    List<ContentDocumentLink> contentDocumentLinks = [
      SELECT Id
      FROM ContentDocumentLink
      WHERE LinkedEntityId = :testQuote.Id
    ];
    System.assert(
      contentDocumentLinks.size() == 1,
      'ContentDocumentLink was not created correctly.'
    );
  }

  //Test method for Quote term
  @isTest
  static void testcreateContentFromQuoteterm() {
    // Arrange
    Account a = new Account(Name = 'test1');
    insert a;
    Opportunity o = new Opportunity(
      AccountId = a.Id,
      CloseDate = system.today(),
      StageName = 'Funded',
      Name = 'Test opp',
      market_segment__c = 'AAM'
    );
    insert o;
    Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
    insert testQuote;

    // Assert

    // Setup current user with specific time zone if necessary
    User testUser = [
      SELECT Id, TimeZoneSidKey
      FROM User
      WHERE Id = :UserInfo.getUserId()
    ];
    testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
    update testUser;

    // Mock PDF content
    Blob mockPdfContent = Blob.valueOf('Mock PDF content');

    // Set the current page to simulate the PageReference
    PageReference testPageRef = Page.QuoteTerms;
    testPageRef.getParameters().put('id', testQuote.Id);
    Test.setCurrentPage(testPageRef);

    // Start test
    Test.startTest();

    // Call the method to test
    String result = Savedocclass.createContentFromQuoteterm(
      testQuote.Id,
      mockPdfContent
    );

    String result2 = Savedocclass.createContentFromQuoteterm(
      testQuote.Id,
      null
    );

    // Stop test
    Test.stopTest();

    // Verify the result
    System.assertEquals(
      'Success',
      result,
      'The method did not return the expected result.'
    );

    // Verify ContentVersion was created
    List<ContentVersion> contentVersions = [
      SELECT Id, Title, VersionData
      FROM ContentVersion
      WHERE Title LIKE 'QuoteTerms%'
    ];
    System.assert(
      contentVersions.size() == 1,
      'ContentVersion was not created correctly.'
    );
    System.assert(
      contentVersions[0].Title.contains('QuoteTerms'),
      'ContentVersion title does not match.'
    );

    // Verify ContentDocumentLink was created
    List<ContentDocumentLink> contentDocumentLinks = [
      SELECT Id
      FROM ContentDocumentLink
      WHERE LinkedEntityId = :testQuote.Id
    ];
    System.assert(
      contentDocumentLinks.size() == 1,
      'ContentDocumentLink was not created correctly.'
    );
  }

  // Test method for Product Specification
  @isTest
  static void testcreateContentFromPS() {
    // Arrange
    Account a = new Account(Name = 'test1');
    insert a;
    Opportunity o = new Opportunity(
      AccountId = a.Id,
      CloseDate = system.today(),
      StageName = 'Funded',
      Name = 'Test opp',
      market_segment__c = 'AAM'
    );
    insert o;
    Quote testQuote = new Quote(Name = 'Quote-123', OpportunityId = o.Id);
    insert testQuote;

    // Assert

    // Setup current user with specific time zone if necessary
    User testUser = [
      SELECT Id, TimeZoneSidKey
      FROM User
      WHERE Id = :UserInfo.getUserId()
    ];
    testUser.TimeZoneSidKey = 'America/Los_Angeles'; // Example time zone
    update testUser;

    // Mock PDF content
    Blob mockPdfContent = Blob.valueOf('Mock PDF content');

    // Set the current page to simulate the PageReference
    PageReference testPageRef = Page.ProductSpecification;
    testPageRef.getParameters().put('id', testQuote.Id);
    Test.setCurrentPage(testPageRef);

    // Start test
    Test.startTest();

    // Call the method to test
    String result = Savedocclass.createContentFromPS(
      testQuote.Id,
      mockPdfContent
    );

    String result2 = Savedocclass.createContentFromPS(testQuote.Id, null);

    // Stop test
    Test.stopTest();

    // Verify the result
    System.assertEquals(
      'Success',
      result,
      'The method did not return the expected result.'
    );

    // Verify ContentVersion was created
    List<ContentVersion> contentVersions = [
      SELECT Id, Title, VersionData
      FROM ContentVersion
      WHERE Title LIKE 'ProductSpecification%'
    ];
    System.assert(
      contentVersions.size() == 1,
      'ContentVersion was not created correctly.'
    );
    System.assert(
      contentVersions[0].Title.contains('ProductSpecification'),
      'ContentVersion title does not match.'
    );

    // Verify ContentDocumentLink was created
    List<ContentDocumentLink> contentDocumentLinks = [
      SELECT Id
      FROM ContentDocumentLink
      WHERE LinkedEntityId = :testQuote.Id
    ];
    System.assert(
      contentDocumentLinks.size() == 1,
      'ContentDocumentLink was not created correctly.'
    );
  }

  @IsTest
  static void testCreateContentFromQuoteNoQuote() {
    // Call the method with a non-existing quote Id
    String result = Savedocclass.createContentFromQuote(
      Id.valueOf('0Q0VB0000005hVl0AI'),
      null
    );

    // Verify the result
    System.assertEquals('No Quote found', result);
  }

  @IsTest
  static void testCreateContentFromQuotetermNoQuote() {
    // Call the method with a non-existing quote Id
    String result = Savedocclass.createContentFromQuoteterm(
      Id.valueOf('0Q0VB0000005hVl0AI'),
      null
    );

    // Verify the result
    System.assertEquals('No Quote found', result);
  }

  @IsTest
  static void testCreateContentFromPSNoQuote() {
    // Call the method with a non-existing quote Id
    String result = Savedocclass.createContentFromPS(
      Id.valueOf('0Q0VB0000005hVl0AI'),
      null
    );

    // Verify the result
    System.assertEquals('No Quote found', result);
  }

  @IsTest
  static void testCreateContentFromQuoteErrorGeneratingPdf() {
    // Setup test data
    Quote testQuote = new Quote(Name = 'Test Quote');
    insert testQuote;

    // Call the method without mock PDF content
    // This will cause the pdfPage.getContent() to be called, which will throw an exception in a test context
    String result = Savedocclass.createContentFromQuote(testQuote.Id, null);
    String result2 = Savedocclass.createContentFromQuoteterm(
      testQuote.Id,
      null
    );
    String result3 = Savedocclass.createContentFromPS(testQuote.Id, null);

    // Verify the result
    System.assert(result.startsWith('Error generating PDF'));
    System.assert(result2.startsWith('Error generating PDF'));
    System.assert(result3.startsWith('Error generating PDF'));
  }
}

```

## Methods
### `testGetTimeDate()`

`ISTEST`

#### Signature
```apex
private static void testGetTimeDate()
```

#### Return Type
**void**

---

### `testCreateContentFromQuote()`

`ISTEST`

#### Signature
```apex
private static void testCreateContentFromQuote()
```

#### Return Type
**void**

---

### `testcreateContentFromQuoteterm()`

`ISTEST`

#### Signature
```apex
private static void testcreateContentFromQuoteterm()
```

#### Return Type
**void**

---

### `testcreateContentFromPS()`

`ISTEST`

#### Signature
```apex
private static void testcreateContentFromPS()
```

#### Return Type
**void**

---

### `testCreateContentFromQuoteNoQuote()`

`ISTEST`

#### Signature
```apex
private static void testCreateContentFromQuoteNoQuote()
```

#### Return Type
**void**

---

### `testCreateContentFromQuotetermNoQuote()`

`ISTEST`

#### Signature
```apex
private static void testCreateContentFromQuotetermNoQuote()
```

#### Return Type
**void**

---

### `testCreateContentFromPSNoQuote()`

`ISTEST`

#### Signature
```apex
private static void testCreateContentFromPSNoQuote()
```

#### Return Type
**void**

---

### `testCreateContentFromQuoteErrorGeneratingPdf()`

`ISTEST`

#### Signature
```apex
private static void testCreateContentFromQuoteErrorGeneratingPdf()
```

#### Return Type
**void**