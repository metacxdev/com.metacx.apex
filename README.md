# Apex Classes and Triggers for MetaCX

While the MetaCX Platform does not currently offer an official Salesforce integration, developers can still send events to the MetaCX platform using APEX triggers. The code samples in this project will send Account record insert and update events to a MetaCX connection.

## 1. Set up Remote Sites in your Sandbox and Production Orgs
Add two remote sites in Salesforce under Setup > Security > Remote Site Settings.

- Remote Site Name: MetaCXAuth
- Remote Site URL: https://api.metacx.com/getToken

and

- Remote Site Name: MetaCXEvents
- Remote Site URL: https://api.metacx.com/events

## 2. Setup Apex Classes and Triggers in your Salesforce Sandbox

Add the apex classes and triggers to your Salesforce instance. Replace the client id and secret in the MetacxEventHandler class with the client id and secret with those from your "Salesforce" connection in the CXreactor. If a connection doesn't exist with that name, create a new connection named "Salesforce" of type Event Handler.

## 3. Deploy Apex Classes and Triggers to your Salesforce Production Org

Once testing from within the Salesforce Sandbox is completed, publish a changeset and deploy the apex classes and triggers to the production org.

- Navigate to Setup > Environments > Change Sets > Outbound Change Sets in your Salesforce sandbox.
- Create a change set and upload.

- Navigate to Setup > Environments >Change Sets > Inbound Change Sets in your Salesforce production account.
- Deploy the change set you uploaded from your sandbox.
