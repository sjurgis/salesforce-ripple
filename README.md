# salesforce-ripple
Salesforce - Ripple API integration

I've written this during hackathon. Very dirty, but works.

You can trigger the new wallet creation by creating new record on custom object wallet__c, which will update wallet__c and secret__c fields on the record.

Then, you can create new record on transaction__c object which will update External_Transaction_Id__c field on it.

Data model / relationships are explained in these images: http://imgur.com/IWeAk1s,MNLYL0G

trigger *newWallet*.apxt calls class *newRippleWallet*.apxc and creates a new wallet
trigger *transactionControl*.apxt calls class *newRipplePayment*.apxc and creates now payment


p.s. don't forget you'll need to define API endpoint at Setup>Security Controls>Remote Site Settings. Set it to https://api.ripple.com.
