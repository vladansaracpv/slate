## Integration workflow for External Partners

Integration of ecommerce platforms or online retailer services with Product36 platform is likely the most interesting use cases that could be showcased here. Let's assume that you are running an ecommerce platform offering products of multiple merchants to end customers. Product36 platform allows you to offer DASH digital currency as payment option on your ecommerce platform in addition to the usual payment methods.

The list of steps required for basic integration with Product36 platform follows.

### Signup as a Partner

In order to sign up as a Partner, please follow the details from the [Registration and onboarding](#registration-and-onboarding) section and select Partner role during registration process (Partner signup box).

### Apply for usage of External Partner APIs

Once you have been approved on the system by Alt Thirty Six administrator, please submit a request for enabling External Partner APIs by sending an email to [support@alt36.com](malto:support@alt36.com)

### Onboard/Register your Merchant

The next step requires onboarding of your Merchants. In order to create a Merchant, please use [EXT Create Merchant](#ext-create-merchant) API. Once created, Merchant also needs to be approved by Alt Thirty Six administrator. They will receive an email welcoming them to Product36 platform based on the data specified for authorized signer parameter during the creation process.

### Create a Location for your Merchant

Next, please create a location for newly created Merchant to which the POS will be assigned. In order to create a Location, please use [EXT Create Location](#ext-create-location) API.

### Create a POS for the Location

The next step is to create a POS and assign it to newly created location. Please use [EXT Create POS](#ext-create-pos) API to do so.

### Generate API request code for POS

In order to authenticate your POS, you would need to generate an API request code for the POS. This code is used in the next step to activate/register the POS. Please use [this](#generate-pos-api-request-code) API to generate API request code for POS. The code has time expiration of 10 minutes, and therefore you must use it prior to it's expiration in order to activate/register the POS as explain in the next step.

### Register the POS

Please use the API request code from the previous step to activate/register the POS. In order to do so, please use [Register POS with API request code](#register-pos-with-api-request-code) API. As a result authorization token will be provided which should be used for all future payment requests as shown in the next step. Please store this token and use it only to request payments for corresponding Merchant. The token has expiration time of 32 years. If expired, please repeat the last to steps in order to generate a new authorization token.

**Important notice**

In case you have multiple Merchants, each Merchant you onboard needs to have his own POS created, activated and used for payment requests. This way you ensure that DASH sent by customers, get credited to corresponding Merchant's wallet. Do not use one POS for payments toward multiple Merchants!

### Start using the platform

You are now ready to offer DASH as payment option to your customers. In order to request a payment in DASH please use [POS](#pos) payment request API. As input parameter you need to specify the amount to be paid in USD among other parameters.

Within the response you will be provided with address to which end user needs to send DASH digital currency and amount that needs to be paid. You can present these info to end user in different forms but most convenient option is to present it as a QR code which customers can scan by their mobile wallet. In order to generate a mobile wallet readable QR code, please see the text example below that needs to be encoded into the QR code:

**Sandbox**

`bitcoin:pay_to_address?amount=converted_amount`

**Production**

`dash:pay_to_address?amount=converted_amount`

Parameters `pay_to_address` and `converted_amount` are retrieved from the response of the [POS](#pos) payment request API.

Once a payment request has been made, please use the `tx_id` received in order to receive notifications regarding the payment. In order to do so, please use [Payment Notification](#payment-notification) API.

Happy integrating!

> Example Sandbox

```
bitcoin:mkrVgHEVduruFNYV9YZ4tNkhJy3egr9Dpb?amount=0.22257849
```

> Example Production

```
dash:XqNPAU2oZ2pce3LjxbE7hPQX935a1E8feG?amount=0.17737206
```
