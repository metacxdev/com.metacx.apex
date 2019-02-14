# Apex Classes and Triggers for MetaCX

Add two remote sites in Salesforce under Setup > Security > Remote Site Settings.

Remote Site Name: MetaCXAuth
Remote Site URL: https://api.metacx.com/getToken

and

Remote Site Name: MetaCXEvents
Remote Site URL: https://api.metacx.com/events

## Setup Apex Classes and Triggers in your Salesforce Sandbox

Add the apex classes and triggers to your Salesforce instance. Replace the clientId and ClientSecret in the MetacxEventHandler class with yours. We recommend you create a "Salesforce" connection of type Event Handler in the MetaCX CXreactor.


## Deploy Apex Classes and Triggers to your Salesforce Production Org
