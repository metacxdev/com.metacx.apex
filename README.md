# Apex Classes and Triggers for MetaCX

## Set up Remote Sites in your Sandbox and Production Orgs
Add two remote sites in Salesforce under Setup > Security > Remote Site Settings.

- Remote Site Name: MetaCXAuth
- Remote Site URL: https://api.metacx.com/getToken

and

*Remote Site Name: MetaCXEvents
*Remote Site URL: https://api.metacx.com/events

## Setup Apex Classes and Triggers in your Salesforce Sandbox

Add the apex classes and triggers to your Salesforce instance. Replace the client id and secret in the MetacxEventHandler class with the client id and secret with those from your "Salesforce" connection in the CXreactor. If a connection doesn't exist with that name, create a new connection named "Salesforce" of type Event Handler.

## Deploy Apex Classes and Triggers to your Salesforce Production Org

- Navigate to Setup > Environments > Change Sets > Outbound Change Sets in your Salesforce sandbox.
- Create a change set and upload.

- Navigate to Setup > Environments >Change Sets > Inbound Change Sets in your Salesforce production account.
- Deploy the change set you uploaded from your sandbox.
