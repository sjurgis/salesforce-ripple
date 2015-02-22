# salesforce-ripple
Salesforce - Ripple API integration

I've written this during hackathon. Very dirty, but works.

You can trigger the new wallet creation by creating new record on custom object wallet__c, which will update wallet__c and secret__c fields on the record.

Then, you can create new record on transaction__c object which will update External_Transaction_Id__c field on it.

Data model / relationships are explained in these images: http://imgur.com/IWeAk1s,MNLYL0G
