
# Introduction
## About the platform
<!-- Komentar -->
Product36 is a cloud platform providing [DASH](https://www.dash.org/) digital currency payment solution for retails, web stores, end users, etc.. The full benefits of the platform could be harvested by integrating with Product36 API which is [REST](https://en.wikipedia.org/wiki/Representational_state_transfer) based API. The main purpose of the API is to allow you to easily and securely accept payments in DASH digital currency. In addition to payment services, a powerful near real time reporting API is also provided.
The cross-origin resource sharing is supported, allowing you to interact securely with the REST API from your client web application. All API responses are JSON formatted.
Please use the documentation provided below to learn how to implement Product36 digital currency payment services.
##Sandbox vs Production
In order to facilitate your integration and to allow you to get the full experience of the platform and provided services, we have provided you with both [Sandbox](https://sandbox.product36.com/login) and [Production](https://product36.com/login) environment of the Product36 platform. The Sandbox environment is the exact replica of the Production with two important differences:

* Accounts on Sandbox are only used for testing purposes,
* Instead of DASH digital currency, [BTC](https://en.bitcoin.it/wiki/Testnet) [testnet](https://en.bitcoin.it/wiki/Testnet) digital currency is used in the background which does not affect in any way the end users experience.

Our sincere recommendation is to firstly create a Sandbox account and integrate with the platform based on the provided API documentation. Once you have tested the integration on Sandbox, we encourage you to create an account on Production and start exploring the benefits of the platform by changing the base URL for your API calls to corresponding URL for Production.
The base URLs for Production environment follow:

* Backend: `https://backend-dot-altthirtysixproduct36.appspot.com/`
* Reporting: `https://reporting-dot-altthirtysixproduct36.appspot.com/`
* Payment gateway: `https://paymentgateway-dot-altthirtysixproduct36.appspot.com/`
* Notifier: `https://notifier-dot-altthirtysixproduct36.appspot.com/`


The base URLs for Sandbox environment follow:

* Backend: `https://backend-dot-sandboxaltthirtysixproduct36.appspot.com/`
* Reporting: `https://reporting-dot-sandboxaltthirtysixproduct36.appspot.com/`
* Payment: `https://paymentgateway-dot-sandboxaltthirtysixproduct36.appspot.com/`
* Notifier: `https://notifier-dot-sandboxaltthirtysixproduct36.appspot.com/`

As one may notice the only difference in the base URL between sandbox and production is “sandbox” prefix in the main domain name (i.e. sandboxaltthirtysixproduct36 vs altthirtysixproduct36).

## Registration and onboarding
Registration on the platform is straightforward and requires minimum effort from your side. You can register on [Production](https://product36.com/signup) and/or [Sandbox](https://sandbox.product36.com/signup). In order to register please select the corresponding role (Partner, Merchant, Vendor, Customer) based on your business needs and proceed by filling up all the required information. You can find more info about each particular role [here](#user-roles). Once the registration form has been submitted you will receive a verification email. Please verify your email address in order to speed up the onboarding process. The final approval on the system is done by Alt Thirty Six administrator. Once you have been approved, you will receive the approvement email and you will be able to use the system.

**Important notice:** In case you need to use [External Partner APIs](#Alt36Dash-API-External-partner-resource), please send an email to [support@alt36.com](malto:support@alt36.com) explaining your business preferences in order to be authorized to use the API.
## Dependency services
Product36 is considered as platform of platforms, since it integrates multiple 3rd party services in one comprehensive solution. The most important 3rd party services which are part of the overall system solution include:

* Coinapult
* Blockcypher
* Node40

In case one of the services is not working properly, a corresponding massage will be provided to end user either as API response or within the user web interface. Alt Thirty Six is not liable in case of unavailability, downtime or technical issues with any service provided by 3rd party providers, but will work with their support teams on successful resolution of any issue that might occur.
