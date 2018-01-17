
# User roles
As shown within the [registration and onboarding section](#registration-and-onboarding) of the documentation, the platform supports four different types of entities: Partners, Merchants, Vendors and Customers. More details about each user role could be found below. It’s important to properly identify your role based on business needs and current position in the business ecosystem.
## Partners
Partner role is envisioned for any Integrated software vendor (ISV), PoS Vendors, Ecommerce platform, online retailer services, etc. Partner role is the highest in the hierarchy on the platform as related to permissions and available features. As a Partner, one might onboard his Merchants, Vendors, and Customers and have view access to Merchant’s locations, PoS, and any of his associate’s sales volume.

**Available user roles:**

   * `ROLE_PARTNER_ADMIN`
   * `ROLE_PARTNER_USER`

**Important notice:** In case you need to use [External Partner APIs](#Alt36Dash-API-External-partner-resource), please send an email to [support@alt36.com](malto:support@alt36.com) explaining your business preferences in order to be authorized to use the API. By default, Partner user roles `(ROLE_PARTNER_ADMIN, ROLE_PARTNER_USER)` are not authorized to use these APIs. `ROLE_EXTERNAL` is required for this API.

## Merchant
Merchant role is envisioned for Brick and Mortar retailers and online retailers (B-to-C). As a Merchant one may add his Vendors and Customers, Locations and POS. The platform enables you to receive payments for your services and goods in DASH digital currency. Received funds could be stored on your account either in DASH digital currency or FIAT (USD). In order to manage how the funds received from customers are stored, please see autosell option. Additionally, you can use the platform to make payments to your Vendors in DASH.

**Available user roles:**

   * `ROLE_MERCHANT_ADMIN`
   * `ROLE_MERCHANT_USER`

## Vendors
Vendor role is envisioned for companies in the supply chain (suppliers, growers, wholesale partners, etc.) Vendors are able to receive instant payments in DASH from their Merchants for provided goods and services.

**Available user roles:**

   * `ROLE_VENDOR_ADMIN`
   * `ROLE_VENDOR_USER`

## Customers
Customer role is envisioned for end users/consumers and Merchant customers.

**Available user roles:**

   * `ROLE_CUSTOMER_ADMIN`
