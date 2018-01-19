## Integration workflow for PoS device providers
A specific use case for integration to Product36 platform refers to POS device providers/vendors. In order to ensure compatibility of the POS system with Product36 platform workflow described below should be considered.
### Create a POS
The first step in the process where Merchant is using physical POS device compatible with Product36 platform is to create a Location within his account on the web app. This could be done by navigating to “Merchant->Locations” from the left side menu, and use “Add Location” feature from the web app. Once Location has been created, Merchant creates a POS by navigating to “Merchant->POS” menu and using “Add POS” feature.  During the creation of a new POS, each POS must be assigned to corresponding location. Once created POS will be in **inactive/disabled** state. The state machine diagram for POS is provided below.

![POS workflow](/images/image1.png)


### Register/Activate
The next step in order to activate the physical POS is to generate API request code for newly created POS on the web app. This could be done by viewing the detail page of the POS and using “Generate new code” feature from the web app. The code for POS activation will be shown with expiration time of the code (by default 10 minutes). Use this code by entering it to the physical POS. This will allow the physical POS to authenticate itself and connect itself with your account.

![POS workflow](/images/image3.png)

**POS Vendors notice:**
The POS should use [Register POS API](#register-pos-with-api-request-code) to send newly generated request code to Product36 platform. If the code has been verified, an authorization token will be provided to the POS device. The authorization token should be stored on the device and used for all future payment requests and notification requests towards the platform.

### Deactivate
POS can be deactivated at any time from the web app by entering the detail page of the corresponding POS and selecting Disable POS option from the right menu. Once disabled, POS will no longer be able to send payment requests, or receive notification updates.
### Request payment
Once authenticated, you will be able to use the POS system to request payments and receive payment related updates/notifications.

**POS Vendor notice:**
In order for POS to send payment requests and receive notification updates following APIs should be used on the POS device:

* [Payment request](#pos)
* [Receiving payment related notifications](#payment-notification)
