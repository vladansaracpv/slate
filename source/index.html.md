---
title: Alt36 API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - http
  - javascript
  - ruby
  - python
  - java

toc_footers:
  # - <a href='#'>Sign Up for a Developer Key</a>
  # - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

# includes:
#   - errors

search: true
---

# Introduction
## About the platform
Product36 is a cloud platform providing [DASH](https://www.dash.org/) digital currency payment solution for retails, web stores end users, etc.. The full benefits of the platform could be harvested by integrating with Product36 API which is [REST](https://en.wikipedia.org/wiki/Representational_state_transfer) based API. The main purpose of the API is to allow you to easily and securely accept payments in DASH digital currency. In addition to payment services, a powerful near real time reporting API is also provided. 
The cross-origin resource sharing is supported, allowing you to interact securely with the REST API from your client web application. All API responses are JSON formatted. 
Please use the documentation provided below to learn how to implement Product36 digital currency payment services.
##Sandbox vs Production
In order to facilitate your integration and to allow you to get the full experience of the platform and provided services, we have provided you with both [Sandbox](https://sandbox.product36.com/login) and [Production](https://product36.com/login) environment of the Product36 platform. The Sandbox environment is the exact replica of the Production with two important differences:

* Accounts on Sandbox are only used for testing purposes,
* Instead of DASH digital currency, [BTC](https://en.bitcoin.it/wiki/Testnet) [testnet](https://en.bitcoin.it/wiki/Testnet) digital currency is used in the background which does not affect in any way the end users experience.

Our sincere recommendation is to firstly create a Sandbox account and integrate with the platform based on the provided API documentation. Once you have tested the integration on Sandbox, we encourage you to create an account on Production and start exploring the benefits of the platform by changing the base URL for your API calls to corresponding URL for Production.
The base URLs for Production environment follow:

* Backend service: https://backend-dot-altthirtysixproduct36.appspot.com/ 
* Reporting service: https://reporting-dot-altthirtysixproduct36.appspot.com/ 
* Payment gateway service: https://paymentgateway-dot-altthirtysixproduct36.appspot.com/ 
* Notifier service: https://notifier-dot-altthirtysixproduct36.appspot.com/ 


The base URLs for Sandbox environment follow:

* Backend service: https://backend-dot-sandboxaltthirtysixproduct36.appspot.com/ 
* Reporting service: https://reporting-dot-sandboxaltthirtysixproduct36.appspot.com/ 
* Payment gateway service: https://paymentgateway-dot-sandboxaltthirtysixproduct36.appspot.com/
* Notifier service: https://notifier-dot-sandboxaltthirtysixproduct36.appspot.com/ 

As one may notice the only difference in the base URL between sandbox and production is “sandbox” prefix in the main domain name (i.e. sandboxaltthirtysixproduct36 vs altthirtysixproduct36).

## Registration and onboarding
Registration on the platform is straightforward and requires minimum effort from your side. You can register on [Production](https://product36.com/signup) and/or [Sandbox](https://sandbox.product36.com/signup). In order to register please select the corresponding role (Partner, Merchant, Vendor, Customer) based on your business needs and proceed by filling up all the required information. You can find more info about each particular role [here](#user-roles). Once the registration form has been submitted you will receive a verification email. Please verify your email address in order to speed up the onboarding process. The final approval on the system is done by Alt Thirty Six administrator. Once you have been approved, you will receive the approvement email and you will be able to use the system. 

**Important notice:** In case you need to use External Partner APIs (link), please send an email to [support@alt36.com](malto:support@alt36.com) explaining your business preferences in order to be authorized to use the API.
## Dependency services
Product36 is considered as platform of platforms, since it integrates multiple 3rd party services in one comprehensive solution. The most important 3rd party services which are part of the overall system solution include:

* Coinapult
* Blockcypher
* Node40

In case one of the services is not working properly, a corresponding massage will be provided to end user either as API response or within the user web interface. Lt Thirty Six is not liable in case of unavailability, downtime or technical issues with any service provided by 3rd party providers but will work with their support teams on successful resolution of any issue that might occur.

# User roles
As shown within the [registration and onboarding section](#registration-and-onboarding) of the documentation, the platform supports four different types of entities: Partners, Merchants, Vendors and Customers. More details about each user role could be found below. It’s important to properly identify your role based on business needs and current position in the business ecosystem. 
## Partners
Partner role is envisioned for any Integrated software vendor (ISV), PoS Vendors, Ecommerce platform, online retailer services, etc. Partner role is the highest in the hierarchy on the platform as related to permissions and available features. As a Partner, one might onboard his Merchants, Vendors, and Customers and have view access to Merchant’s locations, PoS, and any of his associate’s sales volume.

**Important notice:** In case you need to use External Partner APIs (link), please send an email to [support@alt36.com](mailto:support@alt36.com) explaining your business preferences in order to be authorized to use the API. By default, Partner user roles are not authorized to use these APIs.

The permission matrix for Partner role is provided below. Each Partner organization can have multiple admin and user accounts.

###Roles matrix
#### PARTNER ADMIN & PARTNER USER

| RESOURCE           | OPRATIONS       | PARTNER ADMIN                | PARTNER USER           | 
|--------------------|-----------------|------------------------------|------------------------| 
| PARTNER            | SEE             | ONLY HIMSELF                 | ONLY HIMSELF           | 
|                    | INVITE          | N                            | N                      | 
|                    | CREATE          | N                            | N                      | 
|                    | UPDATE          | ONLY HIMSELF                 | N                      | 
|                    | DELETE          | N - REQUEST DELETE - SUPPORT | N                      | 
| MERCHANT           | SEE             | Y - ONLY HIS                 | Y - ONLY HIS           | 
|                    | INVITE          | Y                            | N                      | 
|                    | CREATE          | Y                            | N                      | 
|                    | UPDATE          | SEE ONLY FOR HIMSELF         | N                      | 
|                    | DELETE          | N - REQUEST DELETE - SUPPORT | N                      | 
| VENDOR             | SEE             | Y - ONLY HIS                 | Y - ONLY HIS           | 
|                    | INVITE          | Y                            | N                      | 
|                    | CREATE          | Y                            | N                      | 
|                    | UPDATE          | Y - ONLY HIS ADMIN DECIDES   | N                      | 
|                    | DELETE          | N - REQUEST DELETE - SUPPORT | N                      | 
| CUSTOMER           | SEE             | Y - ONLY HIS                 | Y - ONLY HIS           | 
|                    | INVITE          | Y                            | N                      | 
|                    | CREATE          | Y                            | N                      | 
|                    | UPDATE          | N                            | N                      | 
|                    | DELETE          | N - REQUEST DELETE - SUPPORT | N                      | 
| LOCATION           | SEE             | Y - ONLY HIS MERCHANTS       | Y - ONLY HIS MERCHANTS | 
|                    | CREATE          | N                            | N                      | 
|                    | UPDATE          | N                            | N                      | 
|                    | DELETE          | N                            | N                      | 
| POS                | SEE             | Y - ONLY HIS MERCHANTS       | Y - ONLY HIS MERCHANTS | 
|                    | CREATE          | N                            | N                      | 
|                    | UPDATE          | N                            | N                      | 
|                    | DELETE          | N                            | N                      | 
|                    | DISABLE         | N                            | N                      | 
| "PENDING APPROVALS |                 |                              |                        | 
| FOR ALL RESOURCES" | SEE             | Y - ONLY HIS                 | N                      | 
|                    | APPROVE         | N                            | N                      | 
|                    | REJECT          | N                            | N                      | 
| USERS              | SEE             | SEE ONLY FOR HIMSELF         | SEE ONLY FOR HIMSELF   | 
|                    | CREATE          | Y - FOR HIMSELF              | N                      | 
|                    | UPDATE          | Y - FOR HIMSELF              | N                      | 
|                    | DELETE          | Y - FOR HIMSELF              | N                      | 
| ACCOUNT            | SEE             |                              |                        | 
|                    | UPDATE          |                              |                        | 
|                    | CHANGE PASSWORD |                              |                        | 
|                    | ACTIVATE        |                              |                        | 

## Merchant
Merchant role is envisioned for Brick and Mortar retailers and online retailers (B-to-C). As a Merchant one may add his Vendors and Customers, Locations and POS. The platform enables you to receive payments for your services and goods in DASH digital currency. Received funds could be stored on your account either in DASH digital currency or FIAT (USD). In order to manage how the funds received from customers are stored, please see autosell option. Additionally, you can use the platform to make payments to your Vendors in DASH.

The permission matrix for Merchant role is provided below. Each Merchant organization can have multiple admin and user accounts.

## Vendors
Vendor role is envisioned for companies in the supply chain (suppliers, growers, wholesale partners, etc.) Vendors are able to receive instant payments in DASH from their Merchants for provided goods and services.

The permission matrix for Vendor role is provided below. Each Vendor organization can have multiple admin and user accounts.

## Customers
Customer role is envisioned for end users/consumers and Merchant customers.

The permission matrix for Customer role is provided below.

# Important workflows and use cases
##POS workflow - general overview
There is a complex workflow in the background which involves many moving parts, as it can be seen on diagram below. The general POS workflow will be presented here, however in the section below, specific use cases are provided which should help you with integration process with Product36 platform, regardless of your business requirements.

Although the diagram shows variant in which user pays to the merchant using phone QR code reader or by entering the address manually (very unlikely), this model can be used in any other process. Address which is retrieved from the system can be presented to user in any preferable way. 

There are two types of addresses that can be given by the system. One is normal address which does not have expiration time. Another one is so called autosell address which is tightly bound to FIAT currency. This option cannot be defined within call, as it has to be configured in the main application. Autosell address is time bound.

Number of notifications required to assume that the transaction is successfully committed is defined by the policies in the main application and cannot be changed by the third parties.

![POS workflow](/images/image2.png)

Every POS from the system standpoint has to implement states shown on the following diagram. POS is handled through main system interface and can be enabled, disabled or deleted either by merchant or system administrator. In order to be used, POS needs appropriate non-opaque API key.

## Integration workflow for External Partners
## Integration workflow for PoS device providers
A specific use case for integration to Product36 platform refers to POS device providers/vendors. In order to ensure compatibility of the POS system with Product36 platform workflow described below should be considered. 
### Create POS
The first step in the process where Merchant is using physical POS device compatible with Product36 platform is to create a Location within his account on the web app. This could be done by navigating to “Merchant->Locations” from the left side menu, and use “Add Location” feature from the web app. Once Location has been created, Merchant creates a POS by navigating to “Merchant->POS” menu and using “Add POS” feature.  During the creation of a new POS, each POS must be assigned to corresponding location. Once created POS will be in **inactive/disabled** state. The state machine diagram for POS is provided below.

![POS workflow](/images/image1.png)


### Register/Activate
The next step in order to activate the physical POS is to generate API request code for newly created POS on the web app. This could be done by viewing the detail page of the POS and using “Generate new code” feature from the web app. The code for POS activation will be shown with expiration time of the code (by default 10 minutes). Use this code by entering it to the physical POS. This will allow the physical POS to authenticate itself and connect itself with your account.

![POS workflow](/images/image3.png)

**POS Vendors notice:**
The POS should use Register POS API to send newly generated request code to Product36 platform. If the code has been verified, an authorization token will be provided to the POS device. The authorization token should be stored on the device and used for all future payment requests and notification requests towards the platform.

### Deactivate
POS can be deactivated at any time from the web app by entering the detail page of the corresponding POS and selecting Disable POS option from the right menu. Once disabled, POS will no longer be able to send payment requests, or receive notification updates.
### Request payment
Once authenticated, you will be able to use the POS system to request payments and receive payment related updates/notifications.

**POS Vendor notice:**
In order for POS to send payment requests and receive notification updates following APIs should be used on the POS device:
[Payment request]
[Receiving payment related notifications]

#Authentication
First you retrieve a new Bearer token using login/password authentication. After that you can use it to access other resources.

The URL examples throughout this documentation use <token> as a placeholder. For these examples to work, you need to substitute the value with your own access token.

##Is Authenticated
<aside class="success">
This operation does not require authentication
</aside>

> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/authenticate \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/authenticate HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/authenticate',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```



```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/authenticate',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/authenticate', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/authenticate");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/authenticate`


*Is Authenticated*


> Example responses


<h3 id="isAuthenticatedUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<a id="opIdauthorizeUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/authenticate \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
POST http://example.com/api/authenticate HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/authenticate',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```



```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.post 'http://example.com/api/authenticate',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*',
}


r = requests.post('http://example.com/api/authenticate', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/authenticate");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/authenticate`

Access tokens are required to access nearly all endpoints of this API.



> Body parameter


```json
{
  "password": "string",
  "rememberMe": true,
  "username": "string"
}
```


<h3 id="authorizeUsingPOST-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[LoginVM](#schemaloginvm)|true|loginVM|


> Example responses

```json

{ "id_token":"eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJtZXJjaGFudCIsImF1dGgiOiJST0xFX01FUkNIQU5UX0FETUlOIiwiYXNzb2NpYXRlIjoiMjEwMiIsInVzZXJfaW2iOiIzNTQ0IiwiZXhwIjoxNTE2MTM5MDI3fQ.P5mwh63sMSYw8JXxf7KIwJZbvmI-j8SHIsZE4ACY670dxYsfpWxYUJYJNDHJBkTFaXEIC9a7ayXcbvPW9va3fw" }
```


<h3 id="authorizeUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|






# Errors


The Alt36 API uses the following error codes:


Error Code | Meaning
---------- | -------
400 | Bad Request
401 | Unauthorized -- Your API key is wrong.
403 | Forbidden -- The resource requested is hidden for administrators only.
404 | Not Found -- The specified resource could not be found.
405 | Method Not Allowed -- You tried to access a resource with an invalid method.
406 | Not Acceptable -- You requested a format that isn't json.
410 | Gone -- The resource requested has been removed from our servers.
418 | I'm a teapot.
429 | Too Many Requests -- Slow down!
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarily offline for maintenance. Please try again later.


# Pagination
All search requests return paginated results. Each page holds up to 2000 elements.  Additionally, most of the resources that appear as lists in responses are returned as paginated results. Two types of paginations are available on the platform:

* Pagination for backend service
* Pagination for reporting service

When using pagination for APIs provided by backend service, page and size attributes could be used to request page number and number of elements per page. Details regarding pagination related object could be found below for corresponding backend API. They usually include following properties:

first (Boolean) - refers to whether the requested page is first page
last (Boolean) - refers to whether the requested page is last page
number (Integer) - current number of a page, zero index rule is used
numberOfElements (Integer) - total number of elements on the current page 
size (Integer)- size of the page as requested  
totalElements (Integer)- total number of elements in the requested list of objects
totalPages (Integer)- total number of pages for the requested list of objects
content (List of objects) - array of requested data

When using pagination for APIs provided by reporting service -  *page, sort and pageSize (defaults to 25)* attributes could be used to request page number, sorting order and number of elements per page. Details regarding pagination related object could be found below for corresponding reporting API. The pagination related object is stored within the *metadata* attribute. The object includes following properties:

first (Boolean) - refers to whether the requested page is first page
last (Boolean) - refers to whether the requested page is last page
number (Integer) - current number of a page, zero index rule is used
numberOfElements (Integer) - total number of elements in the requested list of objects 
size (Integer)- size of the page as requested  
totalPages (Integer)- total number of pages for the requested list of objects
As one may notice, totalElements parameter is omitted here. instead numberOfElements is used to represent that value.

##Pagination object


```json
{
  "content": [

  ],
  "first": true,
  "last": false,
  "number": 0,
  "numberOfElements": 25,
  "size": 25,
  "sort": {},
  "totalElements": 250,
  "totalPages": 10
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|content|Paginated content|false|No description|
|first|boolean|false|is Current page first page|
|last|boolean|false|is Current page last page|
|number|integer(int32)|false|page index (start from 0)|
|numberOfElements|integer(int32)|false|number Of Elements on current page|
|size|integer(int32)|false|number of items to be returned|
|sort|[Sort](#schemasort)|false|sorting parameters|
|totalElements|integer(int64)|false|total number of elements|
|totalPages|integer(int32)|false|total number of pages|

# Metadata
Most reporting and backend APIs include *metadata* attribute. The metadata attribute usually includes info regarding the original request such as time range for reporting, pagination related data  for reporting when the retrieved object is a list, user role, number of Partners, Merchants, Vendors, Customers, Locations. POS, etc. Metadata is only visible within the API.
# Versioning
Currently, only one version of Product36 API exists. Any future updates to the API which might implicate breaking API compatibility will result in introducing new API versions accordingly. The API versioning will ensure maintaining backwards compatibility with existing integrations.
# Core resources
## Backend service
###Manage Merchants


#### Create New Merchant



<a id="opIdregisterNewUsingPOST_2"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/merchant \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'


```


```http
POST http://example.com/api/merchant HTTP/1.1
Host: null
Content-Type: application/json
Accept: application/json


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


$.ajax({
  url: 'http://example.com/api/merchant',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "address": "string",
  "address2": "string",
  "altAutosellInternal": true,
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "autosell": true,
  "beneficiaryPercent": 0,
  "canEditOnboarded": true,
  "city": "string",
  "commissionFee": 0,
  "companyEIN": "string",
  "companyWebsite": "string",
  "createdDate": "2018-01-08T16:57:23Z",
  "customers": 0,
  "emailAddress": "string",
  "enabled": true,
  "enroledBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "id": 0,
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "locationsCount": 0,
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "merchants": 0,
  "note": "string",
  "partners": 0,
  "phone": "string",
  "posCount": 0,
  "saleVolume": 0,
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  },
  "vendors": 0,
  "zip": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


fetch('http://example.com/api/merchant',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}


result = RestClient.post 'http://example.com/api/merchant',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}


r = requests.post('http://example.com/api/merchant', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/merchant");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/merchant`


*Create a new Merchant*


> Body parameter


```json
{
  "address": "string",
  "address2": "string",
  "altAutosellInternal": true,
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "autosell": true,
  "beneficiaryPercent": 0,
  "canEditOnboarded": true,
  "city": "string",
  "commissionFee": 0,
  "companyEIN": "string",
  "companyWebsite": "string",
  "createdDate": "2018-01-08T16:57:23Z",
  "customers": 0,
  "emailAddress": "string",
  "enabled": true,
  "enroledBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "id": 0,
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "locationsCount": 0,
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "merchants": 0,
  "note": "string",
  "partners": 0,
  "phone": "string",
  "posCount": 0,
  "saleVolume": 0,
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  },
  "vendors": 0,
  "zip": "string"
}
```


<h3 id="registerNewUsingPOST_2-parameters">Parameters</h3>
<!-- Parameters -->


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[NewMerchantVM](#schemanewmerchantvm)|true|partner|


> Example responses


```json
{
  "body": {},
  "statusCode": "100",
  "statusCodeValue": 0
}
```


<h3 id="registerNewUsingPOST_2-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


#### Get all Merchants paginated


<a id="opIdgetAllPaginatedUsingGET_2"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/merchants \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/merchants HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/merchants',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/merchants',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/merchants',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/merchants', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/merchants");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/merchants`


*Get the all Merchants paginated*


<h3 id="getAllPaginatedUsingGET_2-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="getAllPaginatedUsingGET_2-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<h3 id="getAllPaginatedUsingGET_2-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[Associate](#schemaassociate)]|false|No description|
|» address|string|true|No description|
|» altAutosellInternal|boolean|false|No description|
|» associateType|string|true|No description|
|» autosell|boolean|false|No description|
|» beneficiaryPercent|integer(int64)|false|No description|
|» canEditOnboarded|boolean|false|No description|
|» city|string|true|No description|
|» coinaPultApiKey|string|false|No description|
|» commissionFee|number|false|No description|
|» companyEIN|string|false|No description|
|» companyWebsite|string|false|No description|
|» createdDate|string(date-time)|false|No description|
|» cryptoCapitalApiKey|string|false|No description|
|» customers|integer(int32)|false|No description|
|» deletedDate|string(date-time)|false|No description|
|» emailAddress|string|true|No description|
|» enabled|boolean|false|No description|
|» enrolledBy|[Associate](#schemaassociate)|false|No description|
|» id|integer(int64)|false|No description|
|» incorporationDate|string(date)|false|No description|
|» internalFee|number(double)|false|No description|
|» legalBusinessName|string|true|No description|
|» locationsCount|integer(int32)|false|No description|
|» merchants|integer(int32)|false|No description|
|» note|string|false|No description|
|» partners|integer(int32)|false|No description|
|» phone|string|true|No description|
|» posCount|integer(int32)|false|No description|
|» state|[CountryState](#schemacountrystate)|true|No description|
|»» abbreviation|string|false|No description|
|»» id|integer(int64)|false|No description|
|»» state|string|false|No description|
|» usBankAccount|string|false|No description|
|» vendors|integer(int32)|false|No description|
|» zip|string|true|No description|


<aside class="success">
</aside>


#### Update Merchant


<a id="opIdupdateUsingPUT_2"></a>


> Code samples


```shell
# You can also use wget
curl -X PUT http://example.com/api/merchants \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
PUT http://example.com/api/merchants HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/merchants',
  method: 'put',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "address": "string",
  "address2": "string",
  "altAutosellInternal": true,
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "autosell": true,
  "beneficiaryPercent": 0,
  "canEditOnboarded": true,
  "city": "string",
  "commissionFee": 0,
  "companyEIN": "string",
  "companyWebsite": "string",
  "createdDate": "2018-01-08T16:57:23Z",
  "customers": 0,
  "emailAddress": "string",
  "enabled": true,
  "enroledBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "id": 0,
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "locationsCount": 0,
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "merchants": 0,
  "note": "string",
  "partners": 0,
  "phone": "string",
  "posCount": 0,
  "saleVolume": 0,
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  },
  "vendors": 0,
  "zip": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('http://example.com/api/merchants',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.put 'http://example.com/api/merchants',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.put('http://example.com/api/merchants', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/merchants");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`PUT /api/merchants`


*Updates an existing Merchant*


Updates an existing Merchant


> Body parameter


```json
{
  "address": "string",
  "address2": "string",
  "altAutosellInternal": true,
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "autosell": true,
  "beneficiaryPercent": 0,
  "canEditOnboarded": true,
  "city": "string",
  "commissionFee": 0,
  "companyEIN": "string",
  "companyWebsite": "string",
  "createdDate": "2018-01-08T16:57:23Z",
  "customers": 0,
  "emailAddress": "string",
  "enabled": true,
  "enroledBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "id": 0,
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "locationsCount": 0,
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "merchants": 0,
  "note": "string",
  "partners": 0,
  "phone": "string",
  "posCount": 0,
  "saleVolume": 0,
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  },
  "vendors": 0,
  "zip": "string"
}
```


<h3 id="updateUsingPUT_2-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[NewMerchantVM2](#schemanewmerchantvm2)|true|associate|


> Example responses


<h3 id="updateUsingPUT_2-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[Associate](#schemaassociate)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Get Merchant


<a id="opIdgetByIdUsingGET_2"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/merchants/{id} \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/merchants/{id} HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/merchants/{id}',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/merchants/{id}',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/merchants/{id}',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/merchants/{id}', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/merchants/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/merchants/{id}`


*Get the merchant by id*


<h3 id="getByIdUsingGET_2-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


> Example responses


<h3 id="getByIdUsingGET_2-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[NewPartnerVM](#schemanewpartnervm)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Request for delete Merchant


<a id="opIdcreateRequestForDeleteAcssociateUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/request-for-delete \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
POST http://example.com/api/request-for-delete HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/request-for-delete',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "associateDelete": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "dateRequested": "2018-01-08T16:57:23Z",
  "id": 0,
  "reason": "stringstri",
  "requestedBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  }
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('http://example.com/api/request-for-delete',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.post 'http://example.com/api/request-for-delete',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.post('http://example.com/api/request-for-delete', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/request-for-delete");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/request-for-delete`


*New Request for delete MERCHANT*


PARTNER/MERCHANT admin roles only


> Body parameter


```json
{
  "associateDelete": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "dateRequested": "2018-01-08T16:57:23Z",
  "id": 0,
  "reason": "stringstri",
  "requestedBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  }
}
```


<h3 id="createRequestForDeleteAcssociateUsingPOST-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[RequestForDeleteAcssociate](#schemarequestfordeleteacssociate)|true|requestForDeleteAcssociate|


> Example responses


<h3 id="createRequestForDeleteAcssociateUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RequestForDeleteAcssociate](#schemarequestfordeleteacssociate)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>





#### Get all favorite Vendors


<a id="opIdgetAllMerchantVendorsUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/merchant-vendors \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/merchant-vendors HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/merchant-vendors',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/merchant-vendors',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/merchant-vendors',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/merchant-vendors', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/merchant-vendors");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/merchant-vendors`


*Get all favorite Vendors*


Paginated ResponseEntity with status 200 (OK) and the list of merchantVendors in body


<h3 id="getAllMerchantVendorsUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="getAllMerchantVendorsUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfMerchantVendor](#schemapageofmerchantvendor)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


#### Add Vendor to favorite list


<a id="opIdcreateMerchantVendorUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/merchant-vendors \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
POST http://example.com/api/merchant-vendors HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/merchant-vendors',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "merchant": {
    "id": 12
  "vendor": {
    "id": 13
  }
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'
};


fetch('http://example.com/api/merchant-vendors',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.post 'http://example.com/api/merchant-vendors',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.post('http://example.com/api/merchant-vendors', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/merchant-vendors");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/merchant-vendors`


*Add Vendor to favorite list*


ROLE_MERCHANT_ADMIN user only allowed


> Body parameter


```json
{
  "merchant": {
    "id": 12,
    }
  "vendor": {
  
    "id": 120
  }
}
```


<h3 id="createMerchantVendorUsingPOST-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[MerchantVendor](#schemamerchantvendor)|true|merchantVendor|


> Example responses


<h3 id="createMerchantVendorUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[MerchantVendor](#schemamerchantvendor)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


#### Remove Vendor from favorite list


<a id="opIddeleteMerchantVendorUsingDELETE"></a>


> Code samples


```shell
# You can also use wget
curl -X DELETE http://example.com/api/merchant-vendors/{id}


```


```http
DELETE http://example.com/api/merchant-vendors/{id} HTTP/1.1
Host: null


```


```javascript


$.ajax({
  url: 'http://example.com/api/merchant-vendors/{id}',
  method: 'delete',


  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


fetch('http://example.com/api/merchant-vendors/{id}',
{
  method: 'DELETE'


})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


result = RestClient.delete 'http://example.com/api/merchant-vendors/{id}',
  params: {
  }


p JSON.parse(result)


```


```python
import requests


r = requests.delete('http://example.com/api/merchant-vendors/{id}', params={


)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/merchant-vendors/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`DELETE /api/merchant-vendors/{id}`


*REST request to delete Vendors from favorite list*


ROLE_MERCHANT_ADMIN role only allowed to delete


<h3 id="deleteMerchantVendorUsingDELETE-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


<h3 id="deleteMerchantVendorUsingDELETE-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|



#### Invite merchant via email


<a id="opIdinviteUsingPOST_1"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/merchant/invite \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'


```


```http
POST http://example.com/api/merchant/invite HTTP/1.1
Host: null
Content-Type: application/json
Accept: application/json


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


$.ajax({
  url: 'http://example.com/api/merchant/invite',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "email": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


fetch('http://example.com/api/merchant/invite',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}


result = RestClient.post 'http://example.com/api/merchant/invite',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}


r = requests.post('http://example.com/api/merchant/invite', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/merchant/invite");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/merchant/invite`


*Invite merchant via email*


> Body parameter


```json
{
  "email": "string"
}
```


<h3 id="inviteUsingPOST_1-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[InviteAssociateViaEmail](#schemainviteassociateviaemail)|true|associateViaEmail|


> Example responses


```json
{
  "acceptedDateTime": "2018-01-08T16:57:23Z",
  "associateType": "MERCHANT",
  "id": 0,
  "inviteKey": "string",
  "invitedMail": "string",
  "ivitationDateTime": "2018-01-08T16:57:23Z",
  "mailSent": true
}
```


<h3 id="inviteUsingPOST_1-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[Invitation](#schemainvitation)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|



#### Merchant self registration


<a id="opIdselfRegistrationUsingPOST_1"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/merchant/register \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'


```


```http
POST http://example.com/api/merchant/register HTTP/1.1
Host: null
Content-Type: application/json
Accept: application/json


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


$.ajax({
  url: 'http://example.com/api/merchant/register',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "address": "string",
  "address2": "string",
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "city": "string",
  "companyEIN": "string",
  "companyWebsite": "string",
  "emailAddress": "string",
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "note": "string",
  "phone": "string",
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string",
    "password": "string"
  },
  "zip": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


fetch('http://example.com/api/merchant/register',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}


result = RestClient.post 'http://example.com/api/merchant/register',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}


r = requests.post('http://example.com/api/merchant/register', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/merchant/register");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/merchant/register`


*Merchant self registration*


> Body parameter


```json
{
  "address": "string",
  "address2": "string",
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "city": "string",
  "companyEIN": "string",
  "companyWebsite": "string",
  "emailAddress": "string",
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "note": "string",
  "phone": "string",
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string",
    "password": "string"
  },
  "zip": "string"
}
```


<h3 id="selfRegistrationUsingPOST_1-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|key|query|string|false|key|
|body|body|[SelfRegisterVM](#schemaselfregistervm)|true|partner|


> Example responses


```json
{
  "body": {},
  "statusCode": "100",
  "statusCodeValue": 0
}
```


<h3 id="selfRegistrationUsingPOST_1-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Get Merchant autosell value


<a id="opIdgetMerchantAutosellUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/merchant/autosell \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/merchant/autosell HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/merchant/autosell',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/merchant/autosell',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/merchant/autosell',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/merchant/autosell', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/merchant/autosell");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/merchant/autosell`


*One may choose to have autosell option enabled allowing you to automatically convert and keep received funds in FIAT(USD), thus eliminating price volatility due to DASH market rate. The autosell option is enabled by default for each Merchant. You can use the API below to manage this feature.*


> Example responses


<h3 id="getMerchantAutosellUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Change Merchant autosell value


<a id="opIdsetMerchantAutosellUsingPUT"></a>


> Code samples


```shell
# You can also use wget
curl -X PUT http://example.com/api/merchant/autosell?code=string \
  -H 'Accept: */*'


```


```http
PUT http://example.com/api/merchant/autosell?code=string HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/merchant/autosell',
  method: 'put',
  data: '?code=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/merchant/autosell?code=string',
{
  method: 'PUT',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.put 'http://example.com/api/merchant/autosell',
  params: {
  'code' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.put('http://example.com/api/merchant/autosell', params={
  'code': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/merchant/autosell?code=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`PUT /api/merchant/autosell`


*Change Merchant autosell value*


<h3 id="setMerchantAutosellUsingPUT-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|enabled|query|boolean|false|enabled|
|code|query|string|true|code|


> Example responses


<h3 id="setMerchantAutosellUsingPUT-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Search Merchants


<a id="opIdsearchUsingGET_2"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/merchant/search \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/merchant/search HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/merchant/search',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/merchant/search',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/merchant/search',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/merchant/search', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/merchant/search");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/merchant/search`


*search merchants*


<h3 id="searchUsingGET_2-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|q|query|string|false|q|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="searchUsingGET_2-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfAssociate](#schemapageofassociate)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>

### Manage Partners
#### Invite Partner


<a id="opIdinviteUsingPOST_2"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/partner/invite \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'


```


```http
POST http://example.com/api/partner/invite HTTP/1.1
Host: null
Content-Type: application/json
Accept: application/json


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


$.ajax({
  url: 'http://example.com/api/partner/invite',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "email": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


fetch('http://example.com/api/partner/invite',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}


result = RestClient.post 'http://example.com/api/partner/invite',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}


r = requests.post('http://example.com/api/partner/invite', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/partner/invite");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/partner/invite`


*Invite partner via email*


> Body parameter


```json
{
  "email": "string"
}
```


<h3 id="inviteUsingPOST_2-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[InviteAssociateViaEmail](#schemainviteassociateviaemail)|true|associateViaEmail|


> Example responses


```json
{
  "body": {},
  "statusCode": "100",
  "statusCodeValue": 0
}
```


<h3 id="inviteUsingPOST_2-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Accept invitation


<a id="opIdfinishInviteUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/partner/invite/finish?key=string \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'


```


```http
POST http://example.com/api/partner/invite/finish?key=string HTTP/1.1
Host: null
Content-Type: application/json
Accept: application/json


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


$.ajax({
  url: 'http://example.com/api/partner/invite/finish',
  method: 'post',
  data: '?key=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "address": "string",
  "address2": "string",
  "altAutosellInternal": true,
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "autosell": true,
  "canEditOnboarded": true,
  "city": "string",
  "commissionFee": 0,
  "companyEIN": "string",
  "companyWebsite": "string",
  "createdDate": "2018-01-08T16:57:23Z",
  "customers": 0,
  "emailAddress": "string",
  "enabled": true,
  "enroledBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "id": 0,
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "locationsCount": 0,
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "merchants": 0,
  "note": "string",
  "partners": 0,
  "phone": "string",
  "posCount": 0,
  "saleVolume": 0,
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  },
  "vendors": 0,
  "zip": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


fetch('http://example.com/api/partner/invite/finish?key=string',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}


result = RestClient.post 'http://example.com/api/partner/invite/finish',
  params: {
  'key' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}


r = requests.post('http://example.com/api/partner/invite/finish', params={
  'key': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/partner/invite/finish?key=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/partner/invite/finish`


*Finish partner email sign up.*


Finish via email sign up for new partner invited by email.


> Body parameter


```json
{
  "address": "string",
  "address2": "string",
  "altAutosellInternal": true,
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "autosell": true,
  "canEditOnboarded": true,
  "city": "string",
  "commissionFee": 0,
  "companyEIN": "string",
  "companyWebsite": "string",
  "createdDate": "2018-01-08T16:57:23Z",
  "customers": 0,
  "emailAddress": "string",
  "enabled": true,
  "enroledBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "id": 0,
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "locationsCount": 0,
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "merchants": 0,
  "note": "string",
  "partners": 0,
  "phone": "string",
  "posCount": 0,
  "saleVolume": 0,
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  },
  "vendors": 0,
  "zip": "string"
}
```


<h3 id="finishInviteUsingPOST-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|key|query|string|true|key|
|body|body|[NewPartnerVM](#schemanewpartnervm)|true|associate|


> Example responses


```json
{
  "body": {},
  "statusCode": "100",
  "statusCodeValue": 0
}
```


<h3 id="finishInviteUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Partner self registration


<a id="opIdselfRegistrationUsingPOST_2"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/partner/register \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'


```


```http
POST http://example.com/api/partner/register HTTP/1.1
Host: null
Content-Type: application/json
Accept: application/json


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


$.ajax({
  url: 'http://example.com/api/partner/register',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "address": "string",
  "address2": "string",
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "city": "string",
  "companyEIN": "string",
  "companyWebsite": "string",
  "emailAddress": "string",
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "note": "string",
  "phone": "string",
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string",
    "password": "string"
  },
  "zip": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


fetch('http://example.com/api/partner/register',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}


result = RestClient.post 'http://example.com/api/partner/register',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}


r = requests.post('http://example.com/api/partner/register', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/partner/register");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/partner/register`


*Partner self registration*


> Body parameter


```json
{
  "address": "string",
  "address2": "string",
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "city": "string",
  "companyEIN": "string",
  "companyWebsite": "string",
  "emailAddress": "string",
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "note": "string",
  "phone": "string",
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string",
    "password": "string"
  },
  "zip": "string"
}
```


<h3 id="selfRegistrationUsingPOST_2-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|key|query|string|false|key|
|body|body|[SelfRegisterVM](#schemaselfregistervm)|true|partner|


> Example responses


```json
{
  "body": {},
  "statusCode": "100",
  "statusCodeValue": 0
}
```


<h3 id="selfRegistrationUsingPOST_2-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Update Partner


<a id="opIdupdateUsingPUT_3"></a>


> Code samples


```shell
# You can also use wget
curl -X PUT http://example.com/api/partners \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
PUT http://example.com/api/partners HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/partners',
  method: 'put',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "address": "string",
  "address2": "string",
  "altAutosellInternal": true,
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "autosell": true,
  "canEditOnboarded": true,
  "city": "string",
  "commissionFee": 0,
  "companyEIN": "string",
  "companyWebsite": "string",
  "createdDate": "2018-01-08T16:57:23Z",
  "customers": 0,
  "emailAddress": "string",
  "enabled": true,
  "enroledBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "id": 0,
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "locationsCount": 0,
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "merchants": 0,
  "note": "string",
  "partners": 0,
  "phone": "string",
  "posCount": 0,
  "saleVolume": 0,
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  },
  "vendors": 0,
  "zip": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('http://example.com/api/partners',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.put 'http://example.com/api/partners',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.put('http://example.com/api/partners', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/partners");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`PUT /api/partners`


*Updates an existing Partner*


Updates an existing Partner


> Body parameter


```json
{
  "address": "string",
  "address2": "string",
  "altAutosellInternal": true,
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "autosell": true,
  "canEditOnboarded": true,
  "city": "string",
  "commissionFee": 0,
  "companyEIN": "string",
  "companyWebsite": "string",
  "createdDate": "2018-01-08T16:57:23Z",
  "customers": 0,
  "emailAddress": "string",
  "enabled": true,
  "enroledBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "id": 0,
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "locationsCount": 0,
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "merchants": 0,
  "note": "string",
  "partners": 0,
  "phone": "string",
  "posCount": 0,
  "saleVolume": 0,
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  },
  "vendors": 0,
  "zip": "string"
}
```


<h3 id="updateUsingPUT_3-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[NewPartnerVM](#schemanewpartnervm)|true|associate|


> Example responses


<h3 id="updateUsingPUT_3-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[Associate](#schemaassociate)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Get Partner by ID


<a id="opIdgetByIdUsingGET_3"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/partners/{id} \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/partners/{id} HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/partners/{id}',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/partners/{id}',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/partners/{id}',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/partners/{id}', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/partners/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/partners/{id}`


*Get the partner by ID*


<h3 id="getByIdUsingGET_3-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


> Example responses


<h3 id="getByIdUsingGET_3-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[NewPartnerVM](#schemanewpartnervm)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>

<h3 id="Alt36Dash-API-External-partner-resource">Manage External Partners</h3>


External Partner Resource


#### Get all locations


<a id="opIdgetAllLocationsUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/externalpartner/locations \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/externalpartner/locations HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/externalpartner/locations',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/externalpartner/locations',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/externalpartner/locations',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/externalpartner/locations', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/externalpartner/locations");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/externalpartner/locations`


*Get all the locations*


<h3 id="getAllLocationsUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|merchantId|query|integer(int64)|false|merchantId|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="getAllLocationsUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfLocation](#schemapageoflocation)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Create a new location


<a id="opIdcreateLocationUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/externalpartner/locations \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
POST http://example.com/api/externalpartner/locations HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/externalpartner/locations',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "address": "string",
  "address2": "string",
  "city": "string",
  "contact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "contactType": "MAIN",
    "file": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "notificationCronSchedule": "string",
    "notificationEvent": "INBOUND_TRANSACTION",
    "notifyByEmail": true,
    "notifyByTextMessage": true,
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "zip": "string"
  },
  "country": "string",
  "emailAddress": "string",
  "file": "string",
  "fileBytes": "string",
  "fileContentType": "string",
  "geoLocation": "string",
  "id": 0,
  "merchantId": 0,
  "name": "string",
  "noOfPos": 0,
  "note": "string",
  "parentLocationId": 0,
  "phone": "string",
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "website": "string",
  "zip": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('http://example.com/api/externalpartner/locations',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.post 'http://example.com/api/externalpartner/locations',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.post('http://example.com/api/externalpartner/locations', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/externalpartner/locations");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/externalpartner/locations`


*Create a new location*


> Body parameter


```json
{
  "address": "string",
  "address2": "string",
  "city": "string",
  "contact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "contactType": "MAIN",
    "file": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "notificationCronSchedule": "string",
    "notificationEvent": "INBOUND_TRANSACTION",
    "notifyByEmail": true,
    "notifyByTextMessage": true,
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "zip": "string"
  },
  "country": "string",
  "emailAddress": "string",
  "file": "string",
  "fileBytes": "string",
  "fileContentType": "string",
  "geoLocation": "string",
  "id": 0,
  "merchantId": 0,
  "name": "string",
  "noOfPos": 0,
  "note": "string",
  "parentLocationId": 0,
  "phone": "string",
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "website": "string",
  "zip": "string"
}
```


<h3 id="createLocationUsingPOST-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[LocationExternalVm](#schemalocationexternalvm)|true|locationVm|


> Example responses


<h3 id="createLocationUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[Location](#schemalocation)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Update Location


<a id="opIdupdateLocationUsingPUT"></a>


> Code samples


```shell
# You can also use wget
curl -X PUT http://example.com/api/externalpartner/locations \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
PUT http://example.com/api/externalpartner/locations HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/externalpartner/locations',
  method: 'put',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "address": "string",
  "address2": "string",
  "city": "string",
  "contact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "contactType": "MAIN",
    "file": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "notificationCronSchedule": "string",
    "notificationEvent": "INBOUND_TRANSACTION",
    "notifyByEmail": true,
    "notifyByTextMessage": true,
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "zip": "string"
  },
  "country": "string",
  "emailAddress": "string",
  "file": "string",
  "fileBytes": "string",
  "fileContentType": "string",
  "geoLocation": "string",
  "id": 0,
  "name": "string",
  "noOfPos": 0,
  "note": "string",
  "parentLocationId": 0,
  "phone": "string",
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "website": "string",
  "zip": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('http://example.com/api/externalpartner/locations',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.put 'http://example.com/api/externalpartner/locations',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.put('http://example.com/api/externalpartner/locations', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/externalpartner/locations");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`PUT /api/externalpartner/locations`


*Updates an existing location*


> Body parameter


```json
{
  "address": "string",
  "address2": "string",
  "city": "string",
  "contact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "contactType": "MAIN",
    "file": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "notificationCronSchedule": "string",
    "notificationEvent": "INBOUND_TRANSACTION",
    "notifyByEmail": true,
    "notifyByTextMessage": true,
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "zip": "string"
  },
  "country": "string",
  "emailAddress": "string",
  "file": "string",
  "fileBytes": "string",
  "fileContentType": "string",
  "geoLocation": "string",
  "id": 0,
  "name": "string",
  "noOfPos": 0,
  "note": "string",
  "parentLocationId": 0,
  "phone": "string",
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "website": "string",
  "zip": "string"
}
```


<h3 id="updateLocationUsingPUT-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[LocationVm](#schemalocationvm)|true|locationVm|


> Example responses


<h3 id="updateLocationUsingPUT-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[Location](#schemalocation)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Get Location by ID


<a id="opIdgetLocationUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/externalpartner/locations/{id} \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/externalpartner/locations/{id} HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/externalpartner/locations/{id}',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/externalpartner/locations/{id}',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/externalpartner/locations/{id}',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/externalpartner/locations/{id}', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/externalpartner/locations/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/externalpartner/locations/{id}`


*Get location by ID*


<h3 id="getLocationUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


> Example responses


<h3 id="getLocationUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[LocationWithTransactionVm](#schemalocationwithtransactionvm)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Delete Location


<a id="opIddeleteLocationUsingDELETE"></a>


> Code samples


```shell
# You can also use wget
curl -X DELETE http://example.com/api/externalpartner/locations/{id}


```


```http
DELETE http://example.com/api/externalpartner/locations/{id} HTTP/1.1
Host: null


```


```javascript


$.ajax({
  url: 'http://example.com/api/externalpartner/locations/{id}',
  method: 'delete',


  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


fetch('http://example.com/api/externalpartner/locations/{id}',
{
  method: 'DELETE'


})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


result = RestClient.delete 'http://example.com/api/externalpartner/locations/{id}',
  params: {
  }


p JSON.parse(result)


```


```python
import requests


r = requests.delete('http://example.com/api/externalpartner/locations/{id}', params={


)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/externalpartner/locations/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`DELETE /api/externalpartner/locations/{id}`


*Delete location by ID*


<h3 id="deleteLocationUsingDELETE-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


<h3 id="deleteLocationUsingDELETE-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<aside class="success">
</aside>


#### Create Merchant


<a id="opIdregisterNewUsingPOST_1"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/externalpartner/merchant \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'


```


```http
POST http://example.com/api/externalpartner/merchant HTTP/1.1
Host: null
Content-Type: application/json
Accept: application/json


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


$.ajax({
  url: 'http://example.com/api/externalpartner/merchant',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "address": "string",
  "address2": "string",
  "altAutosellInternal": true,
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "autosell": true,
  "beneficiaryPercent": 0,
  "canEditOnboarded": true,
  "city": "string",
  "commissionFee": 0,
  "companyEIN": "string",
  "companyWebsite": "string",
  "createdDate": "2018-01-08T16:57:22Z",
  "customers": 0,
  "emailAddress": "string",
  "enabled": true,
  "enroledBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:22Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:22Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "id": 0,
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "locationsCount": 0,
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "merchants": 0,
  "note": "string",
  "partners": 0,
  "phone": "string",
  "posCount": 0,
  "saleVolume": 0,
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  },
  "vendors": 0,
  "zip": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


fetch('http://example.com/api/externalpartner/merchant',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}


result = RestClient.post 'http://example.com/api/externalpartner/merchant',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}


r = requests.post('http://example.com/api/externalpartner/merchant', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/externalpartner/merchant");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/externalpartner/merchant`


*Creates a new merchant*


> Body parameter


```json
{
  "address": "string",
  "address2": "string",
  "altAutosellInternal": true,
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "autosell": true,
  "beneficiaryPercent": 0,
  "canEditOnboarded": true,
  "city": "string",
  "commissionFee": 0,
  "companyEIN": "string",
  "companyWebsite": "string",
  "createdDate": "2018-01-08T16:57:22Z",
  "customers": 0,
  "emailAddress": "string",
  "enabled": true,
  "enroledBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:22Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:22Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "id": 0,
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "locationsCount": 0,
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "merchants": 0,
  "note": "string",
  "partners": 0,
  "phone": "string",
  "posCount": 0,
  "saleVolume": 0,
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  },
  "vendors": 0,
  "zip": "string"
}
```


<h3 id="registerNewUsingPOST_1-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[NewMerchantVM](#schemanewmerchantvm)|true|partner|


> Example responses


```json
{
  "body": {},
  "statusCode": "100",
  "statusCodeValue": 0
}
```


<h3 id="registerNewUsingPOST_1-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Delete merchant


<a id="opIddeleteUsingDELETE_1"></a>


> Code samples


```shell
# You can also use wget
curl -X DELETE http://example.com/api/externalpartner/merchant/{id}


```


```http
DELETE http://example.com/api/externalpartner/merchant/{id} HTTP/1.1
Host: null


```


```javascript


$.ajax({
  url: 'http://example.com/api/externalpartner/merchant/{id}',
  method: 'delete',


  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


fetch('http://example.com/api/externalpartner/merchant/{id}',
{
  method: 'DELETE'


})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


result = RestClient.delete 'http://example.com/api/externalpartner/merchant/{id}',
  params: {
  }


p JSON.parse(result)


```


```python
import requests


r = requests.delete('http://example.com/api/externalpartner/merchant/{id}', params={


)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/externalpartner/merchant/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`DELETE /api/externalpartner/merchant/{id}`


*Delete the Merchant with id*


delete the Merchant with id. Deletes/Disables all merchant users first


<h3 id="deleteUsingDELETE_1-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


<h3 id="deleteUsingDELETE_1-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<aside class="success">
</aside>


#### Get Merchants paginated


<a id="opIdgetAllPaginatedUsingGET_1"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/externalpartner/merchants \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/externalpartner/merchants HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/externalpartner/merchants',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/externalpartner/merchants',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/externalpartner/merchants',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/externalpartner/merchants', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/externalpartner/merchants");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/externalpartner/merchants`


*Get the all Merchants paginated*


<h3 id="getAllPaginatedUsingGET_1-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="getAllPaginatedUsingGET_1-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<h3 id="getAllPaginatedUsingGET_1-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[Associate](#schemaassociate)]|false|No description|
|» address|string|true|No description|
|» altAutosellInternal|boolean|false|No description|
|» associateType|string|true|No description|
|» autosell|boolean|false|No description|
|» beneficiaryPercent|integer(int64)|false|No description|
|» canEditOnboarded|boolean|false|No description|
|» city|string|true|No description|
|» coinaPultApiKey|string|false|No description|
|» commissionFee|number|false|No description|
|» companyEIN|string|false|No description|
|» companyWebsite|string|false|No description|
|» createdDate|string(date-time)|false|No description|
|» cryptoCapitalApiKey|string|false|No description|
|» customers|integer(int32)|false|No description|
|» deletedDate|string(date-time)|false|No description|
|» emailAddress|string|true|No description|
|» enabled|boolean|false|No description|
|» enrolledBy|[Associate](#schemaassociate)|false|No description|
|» id|integer(int64)|false|No description|
|» incorporationDate|string(date)|false|No description|
|» internalFee|number(double)|false|No description|
|» legalBusinessName|string|true|No description|
|» locationsCount|integer(int32)|false|No description|
|» merchants|integer(int32)|false|No description|
|» note|string|false|No description|
|» partners|integer(int32)|false|No description|
|» phone|string|true|No description|
|» posCount|integer(int32)|false|No description|
|» state|[CountryState](#schemacountrystate)|true|No description|
|»» abbreviation|string|false|No description|
|»» id|integer(int64)|false|No description|
|»» state|string|false|No description|
|» usBankAccount|string|false|No description|
|» vendors|integer(int32)|false|No description|
|» zip|string|true|No description|


<aside class="success">
</aside>


#### Update Merchant


<a id="opIdupdateUsingPUT_1"></a>


> Code samples


```shell
# You can also use wget
curl -X PUT http://example.com/api/externalpartner/merchants \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
PUT http://example.com/api/externalpartner/merchants HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/externalpartner/merchants',
  method: 'put',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "address": "string",
  "address2": "string",
  "altAutosellInternal": true,
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "autosell": true,
  "beneficiaryPercent": 0,
  "canEditOnboarded": true,
  "city": "string",
  "commissionFee": 0,
  "companyEIN": "string",
  "companyWebsite": "string",
  "createdDate": "2018-01-08T16:57:22Z",
  "customers": 0,
  "emailAddress": "string",
  "enabled": true,
  "enroledBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:22Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:22Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "id": 0,
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "locationsCount": 0,
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "merchants": 0,
  "note": "string",
  "partners": 0,
  "phone": "string",
  "posCount": 0,
  "saleVolume": 0,
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  },
  "vendors": 0,
  "zip": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('http://example.com/api/externalpartner/merchants',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.put 'http://example.com/api/externalpartner/merchants',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.put('http://example.com/api/externalpartner/merchants', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/externalpartner/merchants");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`PUT /api/externalpartner/merchants`


*Updates an existing Merchant*


Updates an existing Merchant


> Body parameter


```json
{
  "address": "string",
  "address2": "string",
  "altAutosellInternal": true,
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "autosell": true,
  "beneficiaryPercent": 0,
  "canEditOnboarded": true,
  "city": "string",
  "commissionFee": 0,
  "companyEIN": "string",
  "companyWebsite": "string",
  "createdDate": "2018-01-08T16:57:22Z",
  "customers": 0,
  "emailAddress": "string",
  "enabled": true,
  "enroledBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:22Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:22Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "id": 0,
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "locationsCount": 0,
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "merchants": 0,
  "note": "string",
  "partners": 0,
  "phone": "string",
  "posCount": 0,
  "saleVolume": 0,
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  },
  "vendors": 0,
  "zip": "string"
}
```


<h3 id="updateUsingPUT_1-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[NewMerchantVM2](#schemanewmerchantvm2)|true|associate|


> Example responses


<h3 id="updateUsingPUT_1-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[Associate](#schemaassociate)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Get the Merchant by ID


<a id="opIdgetByIdUsingGET_1"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/externalpartner/merchants/{id} \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/externalpartner/merchants/{id} HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/externalpartner/merchants/{id}',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/externalpartner/merchants/{id}',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/externalpartner/merchants/{id}',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/externalpartner/merchants/{id}', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/externalpartner/merchants/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/externalpartner/merchants/{id}`


*Get the merchant by id*


<h3 id="getByIdUsingGET_1-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


> Example responses


<h3 id="getByIdUsingGET_1-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[NewPartnerVM](#schemanewpartnervm)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Get all POS paginated


<a id="opIdgetAllPointOfSalesUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/externalpartner/point-of-sales \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/externalpartner/point-of-sales HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/externalpartner/point-of-sales',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/externalpartner/point-of-sales',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/externalpartner/point-of-sales',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/externalpartner/point-of-sales', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/externalpartner/point-of-sales");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/externalpartner/point-of-sales`


*Get all POS*


<h3 id="getAllPointOfSalesUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|locationId|query|integer(int64)|false|locationId|
|merchantId|query|integer(int64)|false|merchantId|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="getAllPointOfSalesUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfPointOfSale](#schemapageofpointofsale)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Create POS


<a id="opIdcreatePointOfSaleUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/externalpartner/point-of-sales \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
POST http://example.com/api/externalpartner/point-of-sales HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/externalpartner/point-of-sales',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "active": true,
  "deletedDate": "2018-01-08T16:57:22Z",
  "id": 0,
  "inventoryNumber": "string",
  "location": {
    "address": "string",
    "address2": "string",
    "associate": {
      "address": "string",
      "altAutosellInternal": true,
      "associateType": "ALT36",
      "autosell": true,
      "beneficiaryPercent": 0,
      "canEditOnboarded": true,
      "city": "string",
      "coinaPultApiKey": "string",
      "commissionFee": 0,
      "companyEIN": "string",
      "companyWebsite": "string",
      "createdDate": "2018-01-08T16:57:22Z",
      "cryptoCapitalApiKey": "string",
      "customers": 0,
      "deletedDate": "2018-01-08T16:57:22Z",
      "emailAddress": "string",
      "enabled": true,
      "enrolledBy": null,
      "id": 0,
      "incorporationDate": "2018-01-08",
      "internalFee": 0,
      "legalBusinessName": "string",
      "locationsCount": 0,
      "merchants": 0,
      "note": "string",
      "partners": 0,
      "phone": "string",
      "posCount": 0,
      "state": {
        "abbreviation": "string",
        "id": 0,
        "state": "string"
      },
      "usBankAccount": "string",
      "vendors": 0,
      "zip": "string"
    },
    "city": "string",
    "country": "string",
    "deletedDate": "2018-01-08T16:57:22Z",
    "emailAddress": "string",
    "file": "string",
    "geoLocation": "string",
    "id": 0,
    "name": "string",
    "note": "string",
    "parentLocation": null,
    "phone": "string",
    "pointOfSales": [
      null
    ],
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "website": "string",
    "zip": "string"
  },
  "name": "string",
  "note": "string",
  "pointOfSaleType": "GREENBITS",
  "virtualPointOfSalesEnabled": true
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('http://example.com/api/externalpartner/point-of-sales',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.post 'http://example.com/api/externalpartner/point-of-sales',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.post('http://example.com/api/externalpartner/point-of-sales', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/externalpartner/point-of-sales");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/externalpartner/point-of-sales`


*Create a new POS*


> Body parameter


```json
{
  "active": true,
  "deletedDate": "2018-01-08T16:57:22Z",
  "id": 0,
  "inventoryNumber": "string",
  "location": {
    "address": "string",
    "address2": "string",
    "associate": {
      "address": "string",
      "altAutosellInternal": true,
      "associateType": "ALT36",
      "autosell": true,
      "beneficiaryPercent": 0,
      "canEditOnboarded": true,
      "city": "string",
      "coinaPultApiKey": "string",
      "commissionFee": 0,
      "companyEIN": "string",
      "companyWebsite": "string",
      "createdDate": "2018-01-08T16:57:22Z",
      "cryptoCapitalApiKey": "string",
      "customers": 0,
      "deletedDate": "2018-01-08T16:57:22Z",
      "emailAddress": "string",
      "enabled": true,
      "enrolledBy": null,
      "id": 0,
      "incorporationDate": "2018-01-08",
      "internalFee": 0,
      "legalBusinessName": "string",
      "locationsCount": 0,
      "merchants": 0,
      "note": "string",
      "partners": 0,
      "phone": "string",
      "posCount": 0,
      "state": {
        "abbreviation": "string",
        "id": 0,
        "state": "string"
      },
      "usBankAccount": "string",
      "vendors": 0,
      "zip": "string"
    },
    "city": "string",
    "country": "string",
    "deletedDate": "2018-01-08T16:57:22Z",
    "emailAddress": "string",
    "file": "string",
    "geoLocation": "string",
    "id": 0,
    "name": "string",
    "note": "string",
    "parentLocation": null,
    "phone": "string",
    "pointOfSales": [
      null
    ],
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "website": "string",
    "zip": "string"
  },
  "name": "string",
  "note": "string",
  "pointOfSaleType": "GREENBITS",
  "virtualPointOfSalesEnabled": true
}
```


<h3 id="createPointOfSaleUsingPOST-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[PointOfSale](#schemapointofsale)|true|pointOfSale|


> Example responses


<h3 id="createPointOfSaleUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PointOfSale](#schemapointofsale)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Update POS


<a id="opIdupdatePointOfSaleUsingPUT"></a>


> Code samples


```shell
# You can also use wget
curl -X PUT http://example.com/api/externalpartner/point-of-sales \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
PUT http://example.com/api/externalpartner/point-of-sales HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/externalpartner/point-of-sales',
  method: 'put',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "active": true,
  "deletedDate": "2018-01-08T16:57:23Z",
  "id": 0,
  "inventoryNumber": "string",
  "location": {
    "address": "string",
    "address2": "string",
    "associate": {
      "address": "string",
      "altAutosellInternal": true,
      "associateType": "ALT36",
      "autosell": true,
      "beneficiaryPercent": 0,
      "canEditOnboarded": true,
      "city": "string",
      "coinaPultApiKey": "string",
      "commissionFee": 0,
      "companyEIN": "string",
      "companyWebsite": "string",
      "createdDate": "2018-01-08T16:57:23Z",
      "cryptoCapitalApiKey": "string",
      "customers": 0,
      "deletedDate": "2018-01-08T16:57:23Z",
      "emailAddress": "string",
      "enabled": true,
      "enrolledBy": null,
      "id": 0,
      "incorporationDate": "2018-01-08",
      "internalFee": 0,
      "legalBusinessName": "string",
      "locationsCount": 0,
      "merchants": 0,
      "note": "string",
      "partners": 0,
      "phone": "string",
      "posCount": 0,
      "state": {
        "abbreviation": "string",
        "id": 0,
        "state": "string"
      },
      "usBankAccount": "string",
      "vendors": 0,
      "zip": "string"
    },
    "city": "string",
    "country": "string",
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "file": "string",
    "geoLocation": "string",
    "id": 0,
    "name": "string",
    "note": "string",
    "parentLocation": null,
    "phone": "string",
    "pointOfSales": [
      null
    ],
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "website": "string",
    "zip": "string"
  },
  "name": "string",
  "note": "string",
  "pointOfSaleType": "GREENBITS",
  "virtualPointOfSalesEnabled": true
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('http://example.com/api/externalpartner/point-of-sales',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.put 'http://example.com/api/externalpartner/point-of-sales',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.put('http://example.com/api/externalpartner/point-of-sales', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/externalpartner/point-of-sales");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`PUT /api/externalpartner/point-of-sales`


*Update existing POS*


> Body parameter


```json
{
  "active": true,
  "deletedDate": "2018-01-08T16:57:23Z",
  "id": 0,
  "inventoryNumber": "string",
  "location": {
    "address": "string",
    "address2": "string",
    "associate": {
      "address": "string",
      "altAutosellInternal": true,
      "associateType": "ALT36",
      "autosell": true,
      "beneficiaryPercent": 0,
      "canEditOnboarded": true,
      "city": "string",
      "coinaPultApiKey": "string",
      "commissionFee": 0,
      "companyEIN": "string",
      "companyWebsite": "string",
      "createdDate": "2018-01-08T16:57:23Z",
      "cryptoCapitalApiKey": "string",
      "customers": 0,
      "deletedDate": "2018-01-08T16:57:23Z",
      "emailAddress": "string",
      "enabled": true,
      "enrolledBy": null,
      "id": 0,
      "incorporationDate": "2018-01-08",
      "internalFee": 0,
      "legalBusinessName": "string",
      "locationsCount": 0,
      "merchants": 0,
      "note": "string",
      "partners": 0,
      "phone": "string",
      "posCount": 0,
      "state": {
        "abbreviation": "string",
        "id": 0,
        "state": "string"
      },
      "usBankAccount": "string",
      "vendors": 0,
      "zip": "string"
    },
    "city": "string",
    "country": "string",
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "file": "string",
    "geoLocation": "string",
    "id": 0,
    "name": "string",
    "note": "string",
    "parentLocation": null,
    "phone": "string",
    "pointOfSales": [
      null
    ],
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "website": "string",
    "zip": "string"
  },
  "name": "string",
  "note": "string",
  "pointOfSaleType": "GREENBITS",
  "virtualPointOfSalesEnabled": true
}
```


<h3 id="updatePointOfSaleUsingPUT-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[PointOfSale](#schemapointofsale)|true|pointOfSale|


> Example responses


<h3 id="updatePointOfSaleUsingPUT-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PointOfSale](#schemapointofsale)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Get POS by ID


<a id="opIdgetPointOfSaleUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/externalpartner/point-of-sales/{id} \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/externalpartner/point-of-sales/{id} HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/externalpartner/point-of-sales/{id}',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/externalpartner/point-of-sales/{id}',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/externalpartner/point-of-sales/{id}',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/externalpartner/point-of-sales/{id}', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/externalpartner/point-of-sales/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/externalpartner/point-of-sales/{id}`


*Get POS by ID*


<h3 id="getPointOfSaleUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


> Example responses


<h3 id="getPointOfSaleUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PointOfSale](#schemapointofsale)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Delete Point Of Sale


<a id="opIddeletePointOfSaleUsingDELETE"></a>


> Code samples


```shell
# You can also use wget
curl -X DELETE http://example.com/api/externalpartner/point-of-sales/{id}


```


```http
DELETE http://example.com/api/externalpartner/point-of-sales/{id} HTTP/1.1
Host: null


```


```javascript


$.ajax({
  url: 'http://example.com/api/externalpartner/point-of-sales/{id}',
  method: 'delete',


  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


fetch('http://example.com/api/externalpartner/point-of-sales/{id}',
{
  method: 'DELETE'


})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


result = RestClient.delete 'http://example.com/api/externalpartner/point-of-sales/{id}',
  params: {
  }


p JSON.parse(result)


```


```python
import requests


r = requests.delete('http://example.com/api/externalpartner/point-of-sales/{id}', params={


)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/externalpartner/point-of-sales/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`DELETE /api/externalpartner/point-of-sales/{id}`


*Delete POS by ID*


<h3 id="deletePointOfSaleUsingDELETE-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


<h3 id="deletePointOfSaleUsingDELETE-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<aside class="success">
</aside>


<h3 id="Alt36Dash-API-Merchant-locations">Manage Locations</h3>


Location Resource


#### Get All Locations


<a id="opIdgetAllLocationsForDashboardUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/dashboard-locations \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/dashboard-locations HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/dashboard-locations',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/dashboard-locations',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/dashboard-locations',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/dashboard-locations', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/dashboard-locations");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/dashboard-locations`


*Get all the locations*


<h3 id="getAllLocationsForDashboardUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|merchantId|query|integer(int64)|false|merchantId|


> Example responses


<h3 id="getAllLocationsForDashboardUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<h3 id="getAllLocationsForDashboardUsingGET-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[PosForDashboardVm](#schemaposfordashboardvm)]|false|No description|
|» address|string|false|No description|
|» city|string|false|No description|
|» geolocation|string|false|No description|
|» id|integer(int64)|false|No description|
|» name|string|false|No description|
|» noofpos|integer(int64)|false|No description|
|» state|string|false|No description|



#### Search locations


<a id="opIdsearchUsingGET_1"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/location/search \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/location/search HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/location/search',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/location/search',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/location/search',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/location/search', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/location/search");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/location/search`


*search locations*


<h3 id="searchUsingGET_1-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|q|query|string|false|q|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(asc\|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses

```json
{  
   "content":[  
      {  
         "id":303,
         "name":"Phoenix",
         "address":"340 N 3rd St",
         "deletedDate":null,
         "address2":null,
         "city":"Phoenix",
         "file":null,
         "zip":"85004",
         "state":{  
            "id":3,
            "state":"Arizona",
            "abbreviation":"AZ"
         },
         "country":"Alabama",
         "emailAddress":null,
         "phone":"0640272551",
         "note":null,
         "website":"http://www.vizlore.com",
         "geoLocation":"33.4522379,-112.0705419",
         "pointOfSales":[  
            {  
               "id":707,
               "pointOfSaleType":"OTHER",
               "virtualPointOfSalesEnabled":false,
               "active":true,
               "deletedDate":null,
               "inventoryNumber":"POS 5",
               "note":null,
               "name":"POS 5"
            }
         ],
         "parentLocation":null,
         "associate":{  
            "id":2102,
            "enabled":true,
            "canEditOnboarded":false,
            "associateType":"MERCHANT",
            "legalBusinessName":"Demo Merchant",
            "emailAddress":"merchant_AA_1855@021.com",
            "address":"Merchant Address 1855",
            "city":"Novi Sad",
            "zip":"21000",
            "state":{  
               "id":1,
               "state":"Alabama",
               "abbreviation":"AL"
            },
            "phone":"064 5566777",
            "companyEIN":"00-55555",
            "incorporationDate":"2017-09-19",
            "companyWebsite":"http://www.55dsl.com/",
            "beneficiaryPercent":null,
            "commissionFee":0.10,
            "internalFee":0.03,
            "coinaPultApiKey":null,
            "cryptoCapitalApiKey":null,
            "usBankAccount":null,
            "note":null,
            "createdDate":"2017-09-20T10:03:04Z",
            "deletedDate":null,
            "autosell":false,
            "altAutosellInternal":false,
            "partners":0,
            "vendors":31,
            "merchants":0,
            "customers":511,
            "locationsCount":49,
            "posCount":5,
            "enrolledBy":{  
               "id":2054,
               "enabled":true,
               "canEditOnboarded":false,
               "associateType":"PARTNER",
               "legalBusinessName":"Demo Partner",
               "emailAddress":"partner_AA_24306@021.com",
               "address":"Partner Address 24306",
               "city":"Novi Sad",
               "zip":"21000",
               "state":{  
                  "id":1,
                  "state":"Alabama",
                  "abbreviation":"AL"
               },
               "phone":"064 5566776",
               "companyEIN":"00-55555",
               "incorporationDate":"2017-09-03",
               "companyWebsite":"http://www.55dsl.com/",
               "beneficiaryPercent":null,
               "commissionFee":0.10,
               "internalFee":0.03,
               "coinaPultApiKey":null,
               "cryptoCapitalApiKey":null,
               "usBankAccount":null,
               "note":null,
               "createdDate":"2017-09-20T07:11:33Z",
               "deletedDate":null,
               "autosell":false,
               "altAutosellInternal":false,
               "partners":0,
               "vendors":12,
               "merchants":22,
               "customers":477,
               "locationsCount":0,
               "posCount":0,
               "enrolledBy":{  
                  "id":1,
                  "enabled":true,
                  "canEditOnboarded":true,
                  "associateType":"ALT36",
                  "legalBusinessName":"alt thirty six",
                  "emailAddress":"ognjen.miletic@gmail.com",
                  "address":"Kozaracka 12",
                  "city":"Some City",
                  "zip":"81000",
                  "state":{  
                     "id":1,
                     "state":"Alabama",
                     "abbreviation":"AL"
                  },
                  "phone":"+38267246776",
                  "companyEIN":"sdf",
                  "incorporationDate":"2017-07-27",
                  "companyWebsite":"http://alt36.com",
                  "beneficiaryPercent":0,
                  "commissionFee":0.10,
                  "internalFee":0.1,
                  "coinaPultApiKey":"asd",
                  "cryptoCapitalApiKey":"qwe",
                  "usBankAccount":"asd",
                  "note":"note",
                  "createdDate":"2017-08-13T20:29:08Z",
                  "deletedDate":null,
                  "autosell":false,
                  "altAutosellInternal":false,
                  "partners":55,
                  "vendors":60,
                  "merchants":53,
                  "customers":99,
                  "locationsCount":44,
                  "posCount":0,
                  "enrolledBy":null
               }
            }
         }
      }
   ],
   "totalElements":11,
   "last":true,
   "totalPages":1,
   "sort":[  
      {  
         "direction":"DESC",
         "property":"id",
         "ignoreCase":false,
         "nullHandling":"NATIVE",
         "ascending":false,
         "descending":true
      }
   ],
   "size":1,
   "number":0,
   "first":true,
   "numberOfElements":1
}
```


<h3 id="searchUsingGET_1-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfLocation](#schemapageoflocation)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Get all locations paginated

<a id="opIdgetAllLocationsUsingGET_1"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/locations \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/locations HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/locations',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/locations',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/locations',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/locations', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/locations");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/locations`


*Get all the locations paginated*





<h3 id="getAllLocationsUsingGET_1-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|merchantId|query|integer(int64)|false|merchantId|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses

```json
{  
   "content":[  
      {  
         "id":303,
         "name":"Phoenix",
         "address":"340 N 3rd St",
         "deletedDate":null,
         "address2":null,
         "city":"Phoenix",
         "file":null,
         "zip":"85004",
         "state":{  
            "id":3,
            "state":"Arizona",
            "abbreviation":"AZ"
         },
         "country":"Alabama",
         "emailAddress":null,
         "phone":"0640272551",
         "note":null,
         "website":"http://www.vizlore.com",
         "geoLocation":"33.4522379,-112.0705419",
         "pointOfSales":[  
            {  
               "id":707,
               "pointOfSaleType":"OTHER",
               "virtualPointOfSalesEnabled":false,
               "active":true,
               "deletedDate":null,
               "inventoryNumber":"POS 5",
               "note":null,
               "name":"POS 5"
            }
         ],
         "parentLocation":null,
         "associate":{  
            "id":2102,
            "enabled":true,
            "canEditOnboarded":false,
            "associateType":"MERCHANT",
            "legalBusinessName":"Demo Merchant",
            "emailAddress":"merchant_AA_1855@021.com",
            "address":"Merchant Address 1855",
            "city":"Novi Sad",
            "zip":"21000",
            "state":{  
               "id":1,
               "state":"Alabama",
               "abbreviation":"AL"
            },
            "phone":"064 5566777",
            "companyEIN":"00-55555",
            "incorporationDate":"2017-09-19",
            "companyWebsite":"http://www.55dsl.com/",
            "beneficiaryPercent":null,
            "commissionFee":0.10,
            "internalFee":0.03,
            "coinaPultApiKey":null,
            "cryptoCapitalApiKey":null,
            "usBankAccount":null,
            "note":null,
            "createdDate":"2017-09-20T10:03:04Z",
            "deletedDate":null,
            "autosell":false,
            "altAutosellInternal":false,
            "partners":0,
            "vendors":31,
            "merchants":0,
            "customers":511,
            "locationsCount":49,
            "posCount":5,
            "enrolledBy":{  
               "id":2054,
               "enabled":true,
               "canEditOnboarded":false,
               "associateType":"PARTNER",
               "legalBusinessName":"Demo Partner",
               "emailAddress":"partner_AA_24306@021.com",
               "address":"Partner Address 24306",
               "city":"Novi Sad",
               "zip":"21000",
               "state":{  
                  "id":1,
                  "state":"Alabama",
                  "abbreviation":"AL"
               },
               "phone":"064 5566776",
               "companyEIN":"00-55555",
               "incorporationDate":"2017-09-03",
               "companyWebsite":"http://www.55dsl.com/",
               "beneficiaryPercent":null,
               "commissionFee":0.10,
               "internalFee":0.03,
               "coinaPultApiKey":null,
               "cryptoCapitalApiKey":null,
               "usBankAccount":null,
               "note":null,
               "createdDate":"2017-09-20T07:11:33Z",
               "deletedDate":null,
               "autosell":false,
               "altAutosellInternal":false,
               "partners":0,
               "vendors":12,
               "merchants":22,
               "customers":477,
               "locationsCount":0,
               "posCount":0,
               "enrolledBy":{  
                  "id":1,
                  "enabled":true,
                  "canEditOnboarded":true,
                  "associateType":"ALT36",
                  "legalBusinessName":"alt thirty six",
                  "emailAddress":"ognjen.miletic@gmail.com",
                  "address":"Kozaracka 12",
                  "city":"Some City",
                  "zip":"81000",
                  "state":{  
                     "id":1,
                     "state":"Alabama",
                     "abbreviation":"AL"
                  },
                  "phone":"+38267246776",
                  "companyEIN":"sdf",
                  "incorporationDate":"2017-07-27",
                  "companyWebsite":"http://alt36.com",
                  "beneficiaryPercent":0,
                  "commissionFee":0.10,
                  "internalFee":0.1,
                  "coinaPultApiKey":"asd",
                  "cryptoCapitalApiKey":"qwe",
                  "usBankAccount":"asd",
                  "note":"note",
                  "createdDate":"2017-08-13T20:29:08Z",
                  "deletedDate":null,
                  "autosell":false,
                  "altAutosellInternal":false,
                  "partners":55,
                  "vendors":60,
                  "merchants":53,
                  "customers":99,
                  "locationsCount":44,
                  "posCount":0,
                  "enrolledBy":null
               }
            }
         }
      }
   ],
   "totalElements":11,
   "last":true,
   "totalPages":1,
   "sort":[  
      {  
         "direction":"DESC",
         "property":"id",
         "ignoreCase":false,
         "nullHandling":"NATIVE",
         "ascending":false,
         "descending":true
      }
   ],
   "size":1,
   "number":0,
   "first":true,
   "numberOfElements":1
}

```

<h3 id="getAllLocationsUsingGET_1-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfLocation](#schemapageoflocation)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Create location


<a id="opIdcreateLocationUsingPOST_1"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/locations \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
POST http://example.com/api/locations HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/locations',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "name": "New location",
  "phone": "+18267246776",
  "website": "http://mysite.com",
  "address": "751 S Weir Canyon Rd # 173",
  "city": "Anaheim",
  "zip": "92808",
  "state": {
    "id": 5,
    "state": "California",
    "abbreviation": "CA"
  },
  "geoLocation": "33.8608908,-117.7381407",
  "country": "Alabama",
  "file": "data:image/png;base64,image_in_base_64",
  "fileContentType": "image/png",
  "contact": {
    "firstName": "John",
    "lastName": "Dale",
    "primaryMobilePhone": "+18267246776",
    "primaryEmailAddress": "example@gmail.com",
    "position": "some position",
    "contactType": "LOCATION"
  }
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('http://example.com/api/locations',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.post 'http://example.com/api/locations',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.post('http://example.com/api/locations', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/locations");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/locations`


*Create a new location*


> Body parameter


```json
{
  "name": "New location",
  "phone": "+18267246776",
  "website": "http://mysite.com",
  "address": "751 S Weir Canyon Rd # 173",
  "city": "Anaheim",
  "zip": "92808",
  "state": {
    "id": 5,
    "state": "California",
    "abbreviation": "CA"
  },
  "geoLocation": "33.8608908,-117.7381407",
  "country": "Alabama",
  "file": "data:image/png;base64,image_in_base_64",
  "fileContentType": "image/png",
  "contact": {
    "firstName": "John",
    "lastName": "Dale",
    "primaryMobilePhone": "+18267246776",
    "primaryEmailAddress": "example@gmail.com",
    "position": "some position",
    "contactType": "LOCATION"
  }
}
```


<h3 id="createLocationUsingPOST_1-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|merchantId|query|integer(int64)|false|merchantId|
|body|body|[LocationVm](#schemalocationvm)|true|locationVm|


> Example responses


<h3 id="createLocationUsingPOST_1-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[Location](#schemalocation)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>

```json
{  
   "id":2498,
   "name":"New location",
   "address":"751 S Weir Canyon Rd # 173",
   "deletedDate":null,
   "address2":null,
   "city":"Anaheim",
   "file":"d6fb5ec0-33fe-492d-a663-80e95beba983",
   "zip":"92808",
   "state":{  
      "id":5,
      "state":"California",
      "abbreviation":"CA"
   },
   "country":"Alabama",
   "emailAddress":null,
   "phone":"+18267246776",
   "note":null,
   "website":"http://mysite.com",
   "geoLocation":"33.8608908,-117.7381407",
   "pointOfSales":[  

   ],
   "parentLocation":null,
   "associate":{  
      "id":2102,
      "enabled":true,
      "canEditOnboarded":false,
      "associateType":"MERCHANT",
      "legalBusinessName":"Demo Merchant",
      "emailAddress":"merchant_AA_1855@021.com",
      "address":"Merchant Address 1855",
      "city":"Novi Sad",
      "zip":"21000",
      "state":{  
         "id":1,
         "state":"Alabama",
         "abbreviation":"AL"
      },
      "phone":"064 5566777",
      "companyEIN":"00-55555",
      "incorporationDate":"2017-09-19",
      "companyWebsite":"http://www.55dsl.com/",
      "beneficiaryPercent":null,
      "commissionFee":0.10,
      "internalFee":0.03,
      "coinaPultApiKey":null,
      "cryptoCapitalApiKey":null,
      "usBankAccount":null,
      "note":null,
      "createdDate":"2017-09-20T10:03:04Z",
      "deletedDate":null,
      "autosell":false,
      "altAutosellInternal":false,
      "partners":0,
      "vendors":31,
      "merchants":0,
      "customers":511,
      "locationsCount":49,
      "posCount":5
      
   }
}
```


#### Update location


<a id="opIdupdateLocationUsingPUT_1"></a>


> Code samples


```shell
# You can also use wget
curl -X PUT http://example.com/api/locations \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
PUT http://example.com/api/locations HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/locations',
  method: 'put',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "id": 2354,
  "name": "New location",
  "phone": "+18267246776",
  "website": "http://mysite.com",
  "address": "751 S Weir Canyon Rd # 173",
  "city": "Anaheim",
  "zip": "92808",
  "state": {
    "id": 5,
    "state": "California",
    "abbreviation": "CA"
  },
  "geoLocation": "33.8608908,-117.7381407",
  "country": "Alabama",
  "file": "data:image/png;base64,image_in_base_64",
  "fileContentType": "image/png",
  "contact": {
    "firstName": "John",
    "lastName": "Dale",
    "primaryMobilePhone": "+18267246776",
    "primaryEmailAddress": "example@gmail.com",
    "position": "some position",
    "contactType": "LOCATION"
  }
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('http://example.com/api/locations',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.put 'http://example.com/api/locations',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.put('http://example.com/api/locations', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/locations");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`PUT /api/locations`


*Updates an existing location*


> Body parameter


```json
{
  "id": 2354,
  "name": "New location",
  "phone": "+18267246776",
  "website": "http://mysite.com",
  "address": "751 S Weir Canyon Rd # 173",
  "city": "Anaheim",
  "zip": "92808",
  "state": {
    "id": 5,
    "state": "California",
    "abbreviation": "CA"
  },
  "geoLocation": "33.8608908,-117.7381407",
  "country": "Alabama",
  "file": "data:image/png;base64,image_in_base_64",
  "fileContentType": "image/png",
  "contact": {
    "firstName": "John",
    "lastName": "Dale",
    "primaryMobilePhone": "+18267246776",
    "primaryEmailAddress": "example@gmail.com",
    "position": "some position",
    "contactType": "LOCATION"
  }
}
```


<h3 id="updateLocationUsingPUT_1-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[LocationVm](#schemalocationvm)|true|locationVm|


> Example responses


<h3 id="updateLocationUsingPUT_1-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[Location](#schemalocation)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


#### Get location by ID


<a id="opIdgetLocationUsingGET_1"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/locations/{id} \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/locations/{id} HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/locations/{id}',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/locations/{id}',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/locations/{id}',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/locations/{id}', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/locations/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/locations/{id}`


*Get location by ID*


<h3 id="getLocationUsingGET_1-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


> Example responses

```json
{
  "id": 2354,
  "name": "New location",
  "phone": "+18267246776",
  "website": "http://mysite.com",
  "address": "751 S Weir Canyon Rd # 173",
  "city": "Anaheim",
  "zip": "92808",
  "state": {
    "id": 5,
    "state": "California",
    "abbreviation": "CA"
  },
  "geoLocation": "33.8608908,-117.7381407",
  "country": "Alabama",
  "file": "data:image/png;base64,image_in_base_64",
  "fileContentType": "image/png",
  "contact": {
    "firstName": "John",
    "lastName": "Dale",
    "primaryMobilePhone": "+18267246776",
    "primaryEmailAddress": "example@gmail.com",
    "position": "some position",
    "contactType": "LOCATION"
  }
}
```


<h3 id="getLocationUsingGET_1-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[LocationWithTransactionVm](#schemalocationwithtransactionvm)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Delete location


<a id="opIddeleteLocationUsingDELETE_1"></a>


> Code samples


```shell
# You can also use wget
curl -X DELETE http://example.com/api/locations/{id}


```


```http
DELETE http://example.com/api/locations/{id} HTTP/1.1
Host: null


```


```javascript


$.ajax({
  url: 'http://example.com/api/locations/{id}',
  method: 'delete',


  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


fetch('http://example.com/api/locations/{id}',
{
  method: 'DELETE'


})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


result = RestClient.delete 'http://example.com/api/locations/{id}',
  params: {
  }


p JSON.parse(result)


```


```python
import requests


r = requests.delete('http://example.com/api/locations/{id}', params={


)


print r.json()


```


```java

URL obj = new URL("http://example.com/api/locations/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`DELETE /api/locations/{id}`


*Delete location by ID*


<h3 id="deleteLocationUsingDELETE_1-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


<h3 id="deleteLocationUsingDELETE_1-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|

<h3 id="Alt36Dash-API-Merchant-POS">Manage POS</h3>


Point Of Sale Resource


#### Search Point Of Sales


<a id="opIdsearchUsingGET_4"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/point-of-sale/search \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/point-of-sale/search HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/point-of-sale/search',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/point-of-sale/search',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/point-of-sale/search',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/point-of-sale/search', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/point-of-sale/search");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/point-of-sale/search`


*Search Point Of Sales
*


<h3 id="searchUsingGET_4-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|q|query|string|false|q|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="searchUsingGET_4-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfPointOfSale](#schemapageofpointofsale)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Get Point Of Sales paginated

<a id="opIdgetAllPointOfSalesUsingGET_1"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/point-of-sales \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/point-of-sales HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/point-of-sales',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/point-of-sales',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/point-of-sales',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/point-of-sales', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/point-of-sales");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/point-of-sales`


*Get all POS paginated*


<h3 id="getAllPointOfSalesUsingGET_1-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|locationId|query|integer(int64)|false|locationId|
|merchantId|query|integer(int64)|false|merchantId|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="getAllPointOfSalesUsingGET_1-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfPointOfSale](#schemapageofpointofsale)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Create POS


<a id="opIdcreatePointOfSaleUsingPOST_1"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/point-of-sales \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
POST http://example.com/api/point-of-sales HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/point-of-sales',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "active": true,
  "deletedDate": "2018-01-08T16:57:23Z",
  "id": 0,
  "inventoryNumber": "string",
  "location": {
    "address": "string",
    "address2": "string",
    "associate": {
      "address": "string",
      "altAutosellInternal": true,
      "associateType": "ALT36",
      "autosell": true,
      "beneficiaryPercent": 0,
      "canEditOnboarded": true,
      "city": "string",
      "coinaPultApiKey": "string",
      "commissionFee": 0,
      "companyEIN": "string",
      "companyWebsite": "string",
      "createdDate": "2018-01-08T16:57:23Z",
      "cryptoCapitalApiKey": "string",
      "customers": 0,
      "deletedDate": "2018-01-08T16:57:23Z",
      "emailAddress": "string",
      "enabled": true,
      "enrolledBy": null,
      "id": 0,
      "incorporationDate": "2018-01-08",
      "internalFee": 0,
      "legalBusinessName": "string",
      "locationsCount": 0,
      "merchants": 0,
      "note": "string",
      "partners": 0,
      "phone": "string",
      "posCount": 0,
      "state": {
        "abbreviation": "string",
        "id": 0,
        "state": "string"
      },
      "usBankAccount": "string",
      "vendors": 0,
      "zip": "string"
    },
    "city": "string",
    "country": "string",
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "file": "string",
    "geoLocation": "string",
    "id": 0,
    "name": "string",
    "note": "string",
    "parentLocation": null,
    "phone": "string",
    "pointOfSales": [
      null
    ],
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "website": "string",
    "zip": "string"
  },
  "name": "string",
  "note": "string",
  "pointOfSaleType": "GREENBITS",
  "virtualPointOfSalesEnabled": true
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('http://example.com/api/point-of-sales',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.post 'http://example.com/api/point-of-sales',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.post('http://example.com/api/point-of-sales', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/point-of-sales");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/point-of-sales`


*Create a new POS*


> Body parameter


```json
{
  "active": true,
  "deletedDate": "2018-01-08T16:57:23Z",
  "id": 0,
  "inventoryNumber": "string",
  "location": {
    "address": "string",
    "address2": "string",
    "associate": {
      "address": "string",
      "altAutosellInternal": true,
      "associateType": "ALT36",
      "autosell": true,
      "beneficiaryPercent": 0,
      "canEditOnboarded": true,
      "city": "string",
      "coinaPultApiKey": "string",
      "commissionFee": 0,
      "companyEIN": "string",
      "companyWebsite": "string",
      "createdDate": "2018-01-08T16:57:23Z",
      "cryptoCapitalApiKey": "string",
      "customers": 0,
      "deletedDate": "2018-01-08T16:57:23Z",
      "emailAddress": "string",
      "enabled": true,
      "enrolledBy": null,
      "id": 0,
      "incorporationDate": "2018-01-08",
      "internalFee": 0,
      "legalBusinessName": "string",
      "locationsCount": 0,
      "merchants": 0,
      "note": "string",
      "partners": 0,
      "phone": "string",
      "posCount": 0,
      "state": {
        "abbreviation": "string",
        "id": 0,
        "state": "string"
      },
      "usBankAccount": "string",
      "vendors": 0,
      "zip": "string"
    },
    "city": "string",
    "country": "string",
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "file": "string",
    "geoLocation": "string",
    "id": 0,
    "name": "string",
    "note": "string",
    "parentLocation": null,
    "phone": "string",
    "pointOfSales": [
      null
    ],
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "website": "string",
    "zip": "string"
  },
  "name": "string",
  "note": "string",
  "pointOfSaleType": "GREENBITS",
  "virtualPointOfSalesEnabled": true
}
```


<h3 id="createPointOfSaleUsingPOST_1-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[PointOfSale](#schemapointofsale)|true|pointOfSale|


> Example responses


<h3 id="createPointOfSaleUsingPOST_1-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PointOfSale](#schemapointofsale)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Update POS


<a id="opIdupdatePointOfSaleUsingPUT_1"></a>


> Code samples


```shell
# You can also use wget
curl -X PUT http://example.com/api/point-of-sales \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
PUT http://example.com/api/point-of-sales HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/point-of-sales',
  method: 'put',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "active": true,
  "deletedDate": "2018-01-08T16:57:23Z",
  "id": 0,
  "inventoryNumber": "string",
  "location": {
    "address": "string",
    "address2": "string",
    "associate": {
      "address": "string",
      "altAutosellInternal": true,
      "associateType": "ALT36",
      "autosell": true,
      "beneficiaryPercent": 0,
      "canEditOnboarded": true,
      "city": "string",
      "coinaPultApiKey": "string",
      "commissionFee": 0,
      "companyEIN": "string",
      "companyWebsite": "string",
      "createdDate": "2018-01-08T16:57:23Z",
      "cryptoCapitalApiKey": "string",
      "customers": 0,
      "deletedDate": "2018-01-08T16:57:23Z",
      "emailAddress": "string",
      "enabled": true,
      "enrolledBy": null,
      "id": 0,
      "incorporationDate": "2018-01-08",
      "internalFee": 0,
      "legalBusinessName": "string",
      "locationsCount": 0,
      "merchants": 0,
      "note": "string",
      "partners": 0,
      "phone": "string",
      "posCount": 0,
      "state": {
        "abbreviation": "string",
        "id": 0,
        "state": "string"
      },
      "usBankAccount": "string",
      "vendors": 0,
      "zip": "string"
    },
    "city": "string",
    "country": "string",
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "file": "string",
    "geoLocation": "string",
    "id": 0,
    "name": "string",
    "note": "string",
    "parentLocation": null,
    "phone": "string",
    "pointOfSales": [
      null
    ],
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "website": "string",
    "zip": "string"
  },
  "name": "string",
  "note": "string",
  "pointOfSaleType": "GREENBITS",
  "virtualPointOfSalesEnabled": true
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('http://example.com/api/point-of-sales',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.put 'http://example.com/api/point-of-sales',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.put('http://example.com/api/point-of-sales', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/point-of-sales");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`PUT /api/point-of-sales`


*Update existing POS*


> Body parameter


```json
{
  "active": true,
  "deletedDate": "2018-01-08T16:57:23Z",
  "id": 0,
  "inventoryNumber": "string",
  "location": {
    "address": "string",
    "address2": "string",
    "associate": {
      "address": "string",
      "altAutosellInternal": true,
      "associateType": "ALT36",
      "autosell": true,
      "beneficiaryPercent": 0,
      "canEditOnboarded": true,
      "city": "string",
      "coinaPultApiKey": "string",
      "commissionFee": 0,
      "companyEIN": "string",
      "companyWebsite": "string",
      "createdDate": "2018-01-08T16:57:23Z",
      "cryptoCapitalApiKey": "string",
      "customers": 0,
      "deletedDate": "2018-01-08T16:57:23Z",
      "emailAddress": "string",
      "enabled": true,
      "enrolledBy": null,
      "id": 0,
      "incorporationDate": "2018-01-08",
      "internalFee": 0,
      "legalBusinessName": "string",
      "locationsCount": 0,
      "merchants": 0,
      "note": "string",
      "partners": 0,
      "phone": "string",
      "posCount": 0,
      "state": {
        "abbreviation": "string",
        "id": 0,
        "state": "string"
      },
      "usBankAccount": "string",
      "vendors": 0,
      "zip": "string"
    },
    "city": "string",
    "country": "string",
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "file": "string",
    "geoLocation": "string",
    "id": 0,
    "name": "string",
    "note": "string",
    "parentLocation": null,
    "phone": "string",
    "pointOfSales": [
      null
    ],
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "website": "string",
    "zip": "string"
  },
  "name": "string",
  "note": "string",
  "pointOfSaleType": "GREENBITS",
  "virtualPointOfSalesEnabled": true
}
```


<h3 id="updatePointOfSaleUsingPUT_1-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[PointOfSale](#schemapointofsale)|true|pointOfSale|


> Example responses


<h3 id="updatePointOfSaleUsingPUT_1-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PointOfSale](#schemapointofsale)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Get POS by ID


<a id="opIdgetPointOfSaleUsingGET_1"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/point-of-sales/{id} \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/point-of-sales/{id} HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/point-of-sales/{id}',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/point-of-sales/{id}',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/point-of-sales/{id}',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/point-of-sales/{id}', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/point-of-sales/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/point-of-sales/{id}`


*Get POS by ID*


<h3 id="getPointOfSaleUsingGET_1-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


> Example responses


<h3 id="getPointOfSaleUsingGET_1-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PointOfSale](#schemapointofsale)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Delete POS


<a id="opIddeletePointOfSaleUsingDELETE_1"></a>


> Code samples


```shell
# You can also use wget
curl -X DELETE http://example.com/api/point-of-sales/{id}


```


```http
DELETE http://example.com/api/point-of-sales/{id} HTTP/1.1
Host: null


```


```javascript


$.ajax({
  url: 'http://example.com/api/point-of-sales/{id}',
  method: 'delete',


  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


fetch('http://example.com/api/point-of-sales/{id}',
{
  method: 'DELETE'


})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


result = RestClient.delete 'http://example.com/api/point-of-sales/{id}',
  params: {
  }


p JSON.parse(result)


```


```python
import requests


r = requests.delete('http://example.com/api/point-of-sales/{id}', params={


)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/point-of-sales/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`DELETE /api/point-of-sales/{id}`


*Delete POS by ID*


<h3 id="deletePointOfSaleUsingDELETE_1-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


<h3 id="deletePointOfSaleUsingDELETE_1-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<aside class="success">
</aside>


#### Get POS status


<a id="opIdisPosActiveUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/point-of-sales/{id}/isActive \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/point-of-sales/{id}/isActive HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/point-of-sales/{id}/isActive',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/point-of-sales/{id}/isActive',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/point-of-sales/{id}/isActive',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/point-of-sales/{id}/isActive', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/point-of-sales/{id}/isActive");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/point-of-sales/{id}/isActive`


*Get POS status*


<h3 id="isPosActiveUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


> Example responses


<h3 id="isPosActiveUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Generate POS register token


<a id="opIdcreateNewPosAuthUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/point-of-sales/{id}/token \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/point-of-sales/{id}/token HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/point-of-sales/{id}/token',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/point-of-sales/{id}/token',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/point-of-sales/{id}/token',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/point-of-sales/{id}/token', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/point-of-sales/{id}/token");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/point-of-sales/{id}/token`


*Generate POS request token code*


<h3 id="createNewPosAuthUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


> Example responses


<h3 id="createNewPosAuthUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


#### Deactivate POS


<a id="opIddeletePosAuthUsingDELETE"></a>


> Code samples


```shell
# You can also use wget
curl -X DELETE http://example.com/api/point-of-sales/{id}/token \
  -H 'Accept: */*'


```


```http
DELETE http://example.com/api/point-of-sales/{id}/token HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/point-of-sales/{id}/token',
  method: 'delete',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/point-of-sales/{id}/token',
{
  method: 'DELETE',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.delete 'http://example.com/api/point-of-sales/{id}/token',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.delete('http://example.com/api/point-of-sales/{id}/token', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/point-of-sales/{id}/token");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`DELETE /api/point-of-sales/{id}/token`


*Deactivate POS token*


<h3 id="deletePosAuthUsingDELETE-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


> Example responses


<h3 id="deletePosAuthUsingDELETE-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<aside class="success">
</aside>


#### Register pos with key


<a id="opIdregisterNewPosWithKeyUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/pos/register?key=string \
  -H 'Accept: */*'


```


```http
POST http://example.com/api/pos/register?key=string HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/pos/register',
  method: 'post',
  data: '?key=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/pos/register?key=string',
{
  method: 'POST',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.post 'http://example.com/api/pos/register',
  params: {
  'key' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.post('http://example.com/api/pos/register', params={
  'key': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/pos/register?key=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/pos/register`


*Register POS with temp key*


<h3 id="registerNewPosWithKeyUsingPOST-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|key|query|string|true|key|


> Example responses


<h3 id="registerNewPosWithKeyUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>


<h3 id="Alt36Dash-API-Vendor">Manage Vendor</h3>

Vendor Resource

#### Get all Vendors paginated


<a id="opIdgetAllPaginatedUsingGET_4"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/vendors \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/vendors HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/vendors',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/vendors',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/vendors',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/vendors', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/vendors");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/vendors`


*Get the all Vendors paginated*


<h3 id="getAllPaginatedUsingGET_4-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="getAllPaginatedUsingGET_4-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<h3 id="getAllPaginatedUsingGET_4-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[Associate](#schemaassociate)]|false|No description|
|» address|string|true|No description|
|» altAutosellInternal|boolean|false|No description|
|» associateType|string|true|No description|
|» autosell|boolean|false|No description|
|» beneficiaryPercent|integer(int64)|false|No description|
|» canEditOnboarded|boolean|false|No description|
|» city|string|true|No description|
|» coinaPultApiKey|string|false|No description|
|» commissionFee|number|false|No description|
|» companyEIN|string|false|No description|
|» companyWebsite|string|false|No description|
|» createdDate|string(date-time)|false|No description|
|» cryptoCapitalApiKey|string|false|No description|
|» customers|integer(int32)|false|No description|
|» deletedDate|string(date-time)|false|No description|
|» emailAddress|string|true|No description|
|» enabled|boolean|false|No description|
|» enrolledBy|[Associate](#schemaassociate)|false|No description|
|» id|integer(int64)|false|No description|
|» incorporationDate|string(date)|false|No description|
|» internalFee|number(double)|false|No description|
|» legalBusinessName|string|true|No description|
|» locationsCount|integer(int32)|false|No description|
|» merchants|integer(int32)|false|No description|
|» note|string|false|No description|
|» partners|integer(int32)|false|No description|
|» phone|string|true|No description|
|» posCount|integer(int32)|false|No description|
|» state|[CountryState](#schemacountrystate)|true|No description|
|»» abbreviation|string|false|No description|
|»» id|integer(int64)|false|No description|
|»» state|string|false|No description|
|» usBankAccount|string|false|No description|
|» vendors|integer(int32)|false|No description|
|» zip|string|true|No description|


<aside class="success">
</aside>

#### Get the all Vendors


<a id="opIdgetAllUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/allvendors \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/allvendors HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/allvendors',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/allvendors',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/allvendors',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/allvendors', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/allvendors");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/allvendors`


*Get the all Vendors*


> Example responses


<h3 id="getAllUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<h3 id="getAllUsingGET-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[Associate](#schemaassociate)]|false|No description|
|» address|string|true|No description|
|» altAutosellInternal|boolean|false|No description|
|» associateType|string|true|No description|
|» autosell|boolean|false|No description|
|» beneficiaryPercent|integer(int64)|false|No description|
|» canEditOnboarded|boolean|false|No description|
|» city|string|true|No description|
|» coinaPultApiKey|string|false|No description|
|» commissionFee|number|false|No description|
|» companyEIN|string|false|No description|
|» companyWebsite|string|false|No description|
|» createdDate|string(date-time)|false|No description|
|» cryptoCapitalApiKey|string|false|No description|
|» customers|integer(int32)|false|No description|
|» deletedDate|string(date-time)|false|No description|
|» emailAddress|string|true|No description|
|» enabled|boolean|false|No description|
|» enrolledBy|[Associate](#schemaassociate)|false|No description|
|» id|integer(int64)|false|No description|
|» incorporationDate|string(date)|false|No description|
|» internalFee|number(double)|false|No description|
|» legalBusinessName|string|true|No description|
|» locationsCount|integer(int32)|false|No description|
|» merchants|integer(int32)|false|No description|
|» note|string|false|No description|
|» partners|integer(int32)|false|No description|
|» phone|string|true|No description|
|» posCount|integer(int32)|false|No description|
|» state|[CountryState](#schemacountrystate)|true|No description|
|»» abbreviation|string|false|No description|
|»» id|integer(int64)|false|No description|
|»» state|string|false|No description|
|» usBankAccount|string|false|No description|
|» vendors|integer(int32)|false|No description|
|» zip|string|true|No description|



#### Register New Vendor


<a id="opIdregisterNewUsingPOST_4"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/vendor \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'


```


```http
POST http://example.com/api/vendor HTTP/1.1
Host: null
Content-Type: application/json
Accept: application/json


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


$.ajax({
  url: 'http://example.com/api/vendor',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "address": "string",
  "address2": "string",
  "altAutosellInternal": true,
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "autosell": true,
  "beneficiaryPercent": 0,
  "canEditOnboarded": true,
  "city": "string",
  "commissionFee": 0,
  "companyEIN": "string",
  "companyWebsite": "string",
  "createdDate": "2018-01-08T16:57:22Z",
  "customers": 0,
  "emailAddress": "string",
  "enabled": true,
  "enroledBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:22Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:22Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "id": 0,
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "locationsCount": 0,
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "merchants": 0,
  "note": "string",
  "partners": 0,
  "phone": "string",
  "posCount": 0,
  "saleVolume": 0,
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  },
  "vendors": 0,
  "zip": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


fetch('http://example.com/api/vendor',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}


result = RestClient.post 'http://example.com/api/vendor',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}


r = requests.post('http://example.com/api/vendor', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/vendor");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/vendor`


*Creates a new vendor*


> Body parameter


```json
{
  "address": "string",
  "address2": "string",
  "altAutosellInternal": true,
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "autosell": true,
  "beneficiaryPercent": 0,
  "canEditOnboarded": true,
  "city": "string",
  "commissionFee": 0,
  "companyEIN": "string",
  "companyWebsite": "string",
  "createdDate": "2018-01-08T16:57:22Z",
  "customers": 0,
  "emailAddress": "string",
  "enabled": true,
  "enroledBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:22Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:22Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "id": 0,
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "locationsCount": 0,
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "merchants": 0,
  "note": "string",
  "partners": 0,
  "phone": "string",
  "posCount": 0,
  "saleVolume": 0,
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  },
  "vendors": 0,
  "zip": "string"
}
```


<h3 id="registerNewUsingPOST_4-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[NewMerchantVM](#schemanewmerchantvm)|true|partner|


> Example responses


```json
{
  "body": {},
  "statusCode": "100",
  "statusCodeValue": 0
}
```


<h3 id="registerNewUsingPOST_4-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


#### Invite Vendor via Email


<a id="opIdinviteUsingPOST_3"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/vendor/invite \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'


```


```http
POST http://example.com/api/vendor/invite HTTP/1.1
Host: null
Content-Type: application/json
Accept: application/json


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


$.ajax({
  url: 'http://example.com/api/vendor/invite',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "email": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


fetch('http://example.com/api/vendor/invite',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}


result = RestClient.post 'http://example.com/api/vendor/invite',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}


r = requests.post('http://example.com/api/vendor/invite', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/vendor/invite");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/vendor/invite`


*Invite vendor via email*


> Body parameter


```json
{
  "email": "string"
}
```


<h3 id="inviteUsingPOST_3-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[InviteAssociateViaEmail](#schemainviteassociateviaemail)|true|associateViaEmail|


> Example responses


```json
{
  "acceptedDateTime": "2018-01-08T16:57:22Z",
  "associateType": "ALT36",
  "id": 0,
  "inviteKey": "string",
  "invitedMail": "string",
  "ivitationDateTime": "2018-01-08T16:57:22Z",
  "mailSent": true
}
```


<h3 id="inviteUsingPOST_3-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[Invitation](#schemainvitation)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


#### Vendor self-registration


<a id="opIdselfRegistrationUsingPOST_3"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/vendor/register \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'


```


```http
POST http://example.com/api/vendor/register HTTP/1.1
Host: null
Content-Type: application/json
Accept: application/json


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


$.ajax({
  url: 'http://example.com/api/vendor/register',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "address": "string",
  "address2": "string",
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "city": "string",
  "companyEIN": "string",
  "companyWebsite": "string",
  "emailAddress": "string",
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "note": "string",
  "phone": "string",
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string",
    "password": "string"
  },
  "zip": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


fetch('http://example.com/api/vendor/register',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}


result = RestClient.post 'http://example.com/api/vendor/register',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}


r = requests.post('http://example.com/api/vendor/register', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/vendor/register");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/vendor/register`


*Vendor self registration*


> Body parameter


```json
{
  "address": "string",
  "address2": "string",
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "city": "string",
  "companyEIN": "string",
  "companyWebsite": "string",
  "emailAddress": "string",
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "note": "string",
  "phone": "string",
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string",
    "password": "string"
  },
  "zip": "string"
}
```


<h3 id="selfRegistrationUsingPOST_3-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|key|query|string|false|key|
|body|body|[SelfRegisterVM](#schemaselfregistervm)|true|partner|


> Example responses


```json
{
  "body": {},
  "statusCode": "100",
  "statusCodeValue": 0
}
```


<h3 id="selfRegistrationUsingPOST_3-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


#### Search Vendors


<a id="opIdsearchUsingGET_5"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/vendor/search \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/vendor/search HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/vendor/search',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/vendor/search',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/vendor/search',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/vendor/search', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/vendor/search");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/vendor/search`


*search*


<h3 id="searchUsingGET_5-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|q|query|string|false|q|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="searchUsingGET_5-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfAssociate](#schemapageofassociate)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


#### Delete the Vendor with id


<a id="opIddeleteUsingDELETE_4"></a>


> Code samples


```shell
# You can also use wget
curl -X DELETE http://example.com/api/vendor/{id}


```


```http
DELETE http://example.com/api/vendor/{id} HTTP/1.1
Host: null


```


```javascript


$.ajax({
  url: 'http://example.com/api/vendor/{id}',
  method: 'delete',


  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


fetch('http://example.com/api/vendor/{id}',
{
  method: 'DELETE'


})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


result = RestClient.delete 'http://example.com/api/vendor/{id}',
  params: {
  }


p JSON.parse(result)


```


```python
import requests


r = requests.delete('http://example.com/api/vendor/{id}', params={


)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/vendor/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`DELETE /api/vendor/{id}`


*Delete the Vendor with id*


delete the Vendor with id. Deletes/Disables all vendor users first


<h3 id="deleteUsingDELETE_4-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


<h3 id="deleteUsingDELETE_4-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<aside class="success">
This operation does not require authentication
</aside>





#### Update vendor


<a id="opIdupdateUsingPUT_4"></a>


> Code samples


```shell
# You can also use wget
curl -X PUT http://example.com/api/vendors \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
PUT http://example.com/api/vendors HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/vendors',
  method: 'put',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "address": "string",
  "address2": "string",
  "altAutosellInternal": true,
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "autosell": true,
  "canEditOnboarded": true,
  "city": "string",
  "commissionFee": 0,
  "companyEIN": "string",
  "companyWebsite": "string",
  "createdDate": "2018-01-08T16:57:22Z",
  "customers": 0,
  "emailAddress": "string",
  "enabled": true,
  "enroledBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:22Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:22Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "id": 0,
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "locationsCount": 0,
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "merchants": 0,
  "note": "string",
  "partners": 0,
  "phone": "string",
  "posCount": 0,
  "saleVolume": 0,
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  },
  "vendors": 0,
  "zip": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('http://example.com/api/vendors',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.put 'http://example.com/api/vendors',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.put('http://example.com/api/vendors', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/vendors");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`PUT /api/vendors`


*Updates an existing Merchant*


Updates an existing Partner


> Body parameter


```json
{
  "address": "string",
  "address2": "string",
  "altAutosellInternal": true,
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "autosell": true,
  "canEditOnboarded": true,
  "city": "string",
  "commissionFee": 0,
  "companyEIN": "string",
  "companyWebsite": "string",
  "createdDate": "2018-01-08T16:57:22Z",
  "customers": 0,
  "emailAddress": "string",
  "enabled": true,
  "enroledBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:22Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:22Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "id": 0,
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "locationsCount": 0,
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "merchants": 0,
  "note": "string",
  "partners": 0,
  "phone": "string",
  "posCount": 0,
  "saleVolume": 0,
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  },
  "vendors": 0,
  "zip": "string"
}
```


<h3 id="updateUsingPUT_4-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[NewPartnerVM](#schemanewpartnervm)|true|associate|


> Example responses


<h3 id="updateUsingPUT_4-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[Associate](#schemaassociate)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


#### Get Vendor by ID


<a id="opIdgetByIdUsingGET_4"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/vendors/{id} \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/vendors/{id} HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/vendors/{id}',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/vendors/{id}',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/vendors/{id}',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/vendors/{id}', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/vendors/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/vendors/{id}`


*Get the vendor by id*


<h3 id="getByIdUsingGET_4-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


> Example responses


<h3 id="getByIdUsingGET_4-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[NewPartnerVM](#schemanewpartnervm)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>

<h3 id="Alt36Dash-API-Customer">Manage Customers</h3>


Customer Resource


#### Close account


<a id="opIdshutDownAccountUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/close-account \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
POST http://example.com/api/close-account HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/close-account',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "reason": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('http://example.com/api/close-account',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.post 'http://example.com/api/close-account',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.post('http://example.com/api/close-account', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/close-account");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/close-account`


*New Request for closing Account*


PARTNER/MERCHANT/VENDOR/CUSTOMER admin roles only


> Body parameter


```json
{
  "reason": "string"
}
```


<h3 id="shutDownAccountUsingPOST-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[ShutDownAccountRequestVM](#schemashutdownaccountrequestvm)|true|requestForDeleteAcssociate|


> Example responses


<h3 id="shutDownAccountUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RequestForDeleteAcssociate](#schemarequestfordeleteacssociate)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


#### Create new Customer


<a id="opIdregisterNewUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/customer \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```


```http
POST http://example.com/api/customer HTTP/1.1
Host: null
Content-Type: application/json
Accept: application/json


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


$.ajax({
  url: 'http://example.com/api/customer',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "emailAddress": "string",
  "id": 0,
  "legalBusinessName": "string",
  "phone": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  }
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


fetch('http://example.com/api/customer',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}


result = RestClient.post 'http://example.com/api/customer',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}


r = requests.post('http://example.com/api/customer', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/customer");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/customer`


*Creates a new customer*


> Body parameter


```json
{
  "emailAddress": "string",
  "id": 0,
  "legalBusinessName": "string",
  "phone": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  }
}
```


<h3 id="registerNewUsingPOST-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[NewCustomerVM](#schemanewcustomervm)|true|partner|


> Example responses


```json
{
  "body": {},
  "statusCode": "100",
  "statusCodeValue": 0
}
```


<h3 id="registerNewUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


#### Invite customer via email


<a id="opIdinviteUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/customer/invite \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'


```


```http
POST http://example.com/api/customer/invite HTTP/1.1
Host: null
Content-Type: application/json
Accept: application/json


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


$.ajax({
  url: 'http://example.com/api/customer/invite',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "email": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


fetch('http://example.com/api/customer/invite',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}


result = RestClient.post 'http://example.com/api/customer/invite',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}


r = requests.post('http://example.com/api/customer/invite', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/customer/invite");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/customer/invite`


*Invite customer via email*


> Body parameter


```json
{
  "email": "string"
}
```


<h3 id="inviteUsingPOST-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[InviteAssociateViaEmail](#schemainviteassociateviaemail)|true|associateViaEmail|


> Example responses


```json
{
  "acceptedDateTime": "2018-01-08T16:57:22Z",
  "associateType": "ALT36",
  "id": 0,
  "inviteKey": "string",
  "invitedMail": "string",
  "ivitationDateTime": "2018-01-08T16:57:22Z",
  "mailSent": true
}
```


<h3 id="inviteUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[Invitation](#schemainvitation)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|




#### Customer self registration


<a id="opIdselfRegistrationUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/customer/register \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'


```


```http
POST http://example.com/api/customer/register HTTP/1.1
Host: null
Content-Type: application/json
Accept: application/json


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


$.ajax({
  url: 'http://example.com/api/customer/register',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "emailAddress": "string",
  "legalBusinessName": "string",
  "phone": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string",
    "password": "string"
  }
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


fetch('http://example.com/api/customer/register',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}


result = RestClient.post 'http://example.com/api/customer/register',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}


r = requests.post('http://example.com/api/customer/register', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/customer/register");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/customer/register`


*Customer self registration*


> Body parameter


```json
{
  "emailAddress": "string",
  "legalBusinessName": "string",
  "phone": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string",
    "password": "string"
  }
}
```


<h3 id="selfRegistrationUsingPOST-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|key|query|string|false|key|
|body|body|[SelfRegisterCustomerVM](#schemaselfregistercustomervm)|true|partner|


> Example responses


```json
{
  "body": {},
  "statusCode": "100",
  "statusCodeValue": 0
}
```


<h3 id="selfRegistrationUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


####Customers search


<a id="opIdsearchUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/customer/search \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/customer/search HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/customer/search',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/customer/search',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/customer/search',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/customer/search', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/customer/search");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/customer/search`


*search*


<h3 id="searchUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|q|query|string|false|q|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="searchUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfAssociate](#schemapageofassociate)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|




#### Delete customer


<a id="opIddeleteUsingDELETE"></a>


> Code samples


```shell
# You can also use wget
curl -X DELETE http://example.com/api/customer/{id}


```


```http
DELETE http://example.com/api/customer/{id} HTTP/1.1
Host: null


```


```javascript


$.ajax({
  url: 'http://example.com/api/customer/{id}',
  method: 'delete',


  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


fetch('http://example.com/api/customer/{id}',
{
  method: 'DELETE'


})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


result = RestClient.delete 'http://example.com/api/customer/{id}',
  params: {
  }


p JSON.parse(result)


```


```python
import requests


r = requests.delete('http://example.com/api/customer/{id}', params={


)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/customer/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`DELETE /api/customer/{id}`


*Delete the Customer with id*


delete the Customer with id. Deletes/Disables all customer users first


<h3 id="deleteUsingDELETE-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


<h3 id="deleteUsingDELETE-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|




#### Get all custoers paginated


<a id="opIdgetAllPaginatedUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/customers \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/customers HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/customers',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/customers',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/customers',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/customers', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/customers");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/customers`


*Get the all Customers paginated*


<h3 id="getAllPaginatedUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="getAllPaginatedUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<h3 id="getAllPaginatedUsingGET-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[Associate](#schemaassociate)]|false|No description|
|» address|string|true|No description|
|» altAutosellInternal|boolean|false|No description|
|» associateType|string|true|No description|
|» autosell|boolean|false|No description|
|» beneficiaryPercent|integer(int64)|false|No description|
|» canEditOnboarded|boolean|false|No description|
|» city|string|true|No description|
|» coinaPultApiKey|string|false|No description|
|» commissionFee|number|false|No description|
|» companyEIN|string|false|No description|
|» companyWebsite|string|false|No description|
|» createdDate|string(date-time)|false|No description|
|» cryptoCapitalApiKey|string|false|No description|
|» customers|integer(int32)|false|No description|
|» deletedDate|string(date-time)|false|No description|
|» emailAddress|string|true|No description|
|» enabled|boolean|false|No description|
|» enrolledBy|[Associate](#schemaassociate)|false|No description|
|» id|integer(int64)|false|No description|
|» incorporationDate|string(date)|false|No description|
|» internalFee|number(double)|false|No description|
|» legalBusinessName|string|true|No description|
|» locationsCount|integer(int32)|false|No description|
|» merchants|integer(int32)|false|No description|
|» note|string|false|No description|
|» partners|integer(int32)|false|No description|
|» phone|string|true|No description|
|» posCount|integer(int32)|false|No description|
|» state|[CountryState](#schemacountrystate)|true|No description|
|»» abbreviation|string|false|No description|
|»» id|integer(int64)|false|No description|
|»» state|string|false|No description|
|» usBankAccount|string|false|No description|
|» vendors|integer(int32)|false|No description|
|» zip|string|true|No description|




#### Update customer


<a id="opIdupdateUsingPUT"></a>


> Code samples


```shell
# You can also use wget
curl -X PUT http://example.com/api/customers \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
PUT http://example.com/api/customers HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/customers',
  method: 'put',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "emailAddress": "string",
  "id": 0,
  "legalBusinessName": "string",
  "phone": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  }
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('http://example.com/api/customers',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.put 'http://example.com/api/customers',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.put('http://example.com/api/customers', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/customers");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`PUT /api/customers`


*Updates an existing Customer*


> Body parameter


```json
{
  "emailAddress": "string",
  "id": 0,
  "legalBusinessName": "string",
  "phone": "string",
  "user": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  }
}
```


<h3 id="updateUsingPUT-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[NewCustomerVM](#schemanewcustomervm)|true|associate|


> Example responses


<h3 id="updateUsingPUT-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[Associate](#schemaassociate)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


#### Get customer by ID


<a id="opIdgetByIdUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/customers/{id} \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/customers/{id} HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/customers/{id}',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/customers/{id}',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/customers/{id}',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/customers/{id}', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/customers/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/customers/{id}`


*Get the customer by id*


<h3 id="getByIdUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


> Example responses


<h3 id="getByIdUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[NewPartnerVM](#schemanewpartnervm)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


### Manage account
#### Get account


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/account \
  -H 'Accept: */*'

```


```http
GET http://example.com/api/account HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/account',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/account',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/account',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/account', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/account");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/account`


*getAccount*


> Example responses

> The above command returns JSON structured like this:

```json
{ 
  "id":3544,
  "login":"merchant",
  "firstName":"Merchant",
  "lastName":"Admin",
  "email":"example@gmail.com",
  "imageUrl":"",
  "activated":true,
  "langKey":"en",
  "createdBy":"partner",
  "createdDate":"2017-09-21T21:16:49Z",
  "lastModifiedBy":"merchant",
  "lastModifiedDate":"2018-01-15T21:43:47Z",
  "authorities":["ROLE_MERCHANT_ADMIN"],
  "splashscreenEnabled":true,
  "associateActive":true,
  "using2fa":false
}
```

<h3 id="getAccountUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[UserDTOExtended](#schemauserdtoextended)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


#### Create new user account


<a id="opIdsaveAccountUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/account \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
POST http://example.com/api/account HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/account',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "activated": true,
  "authorities": [
    "string"
  ],
  "createdBy": "string",
  "createdDate": "2018-01-03T09:04:22Z",
  "email": "string",
  "firstName": "string",
  "id": 0,
  "imageUrl": "string",
  "langKey": "strin",
  "lastLoginDateTime": "2018-01-03T09:04:22Z",
  "lastModifiedBy": "string",
  "lastModifiedDate": "2018-01-03T09:04:22Z",
  "lastName": "string",
  "login": "string",
  "splashscreenEnabled": true,
  "using2fa": true
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('http://example.com/api/account',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.post 'http://example.com/api/account',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.post('http://example.com/api/account', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/account");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/account`


*saveAccount*


> Body parameter


```json
{
  "activated": true,
  "authorities": [
    "string"
  ],
  "createdBy": "string",
  "createdDate": "2018-01-03T09:04:22Z",
  "email": "string",
  "firstName": "string",
  "id": 0,
  "imageUrl": "string",
  "langKey": "strin",
  "lastLoginDateTime": "2018-01-03T09:04:22Z",
  "lastModifiedBy": "string",
  "lastModifiedDate": "2018-01-03T09:04:22Z",
  "lastName": "string",
  "login": "string",
  "splashscreenEnabled": true,
  "using2fa": true
}
```


<h3 id="saveAccountUsingPOST-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UserDTO](#schemauserdto)|true|userDTO|


> Example responses


<h3 id="saveAccountUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does require authentication
</aside>


#### Get 2FA Barcode image


<a id="opIdgetBarCodeImageUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/account/2fa/barcode?use2FA=true \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/account/2fa/barcode?use2FA=true HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/account/2fa/barcode',
  method: 'get',
  data: '?use2FA=true',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/account/2fa/barcode?use2FA=true',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/account/2fa/barcode',
  params: {
  'use2FA' => 'boolean'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/account/2fa/barcode', params={
  'use2FA': 'true'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/account/2fa/barcode?use2FA=true");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/account/2fa/barcode`


*Get 2FA barcode image*


<h3 id="getBarCodeImageUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|use2FA|query|boolean|true|use2FA|


> Example responses


<h3 id="getBarCodeImageUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation require authentication
</aside>


#### Modify 2FA status


<a id="opIdmodifyUser2FAUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/account/2fa/update?use2FA=true?code=string \
  -H 'Accept: */*'


```


```http
POST http://example.com/api/account/2fa/update?use2FA=true?code=string HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/account/2fa/update',
  method: 'post',
  data: '?use2FA=true?code=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/account/2fa/update?use2FA=true?code=string',
{
  method: 'POST',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.post 'http://example.com/api/account/2fa/update',
  params: {
  'use2FA' => 'boolean',
'code' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.post('http://example.com/api/account/2fa/update', params={
  'use2FA': 'true',  'code': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/account/2fa/update?use2FA=true?code=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/account/2fa/update`


*Modify 2FA status*


<h3 id="modifyUser2FAUsingPOST-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|use2FA|query|boolean|true|use2FA|
|code|query|string|true|code|


> Example responses


<h3 id="modifyUser2FAUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[User](#schemauser)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


#### Change password


<a id="opIdchangePasswordUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/account/change_password \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
POST http://example.com/api/account/change_password HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/account/change_password',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "password": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('http://example.com/api/account/change_password',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.post 'http://example.com/api/account/change_password',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.post('http://example.com/api/account/change_password', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/account/change_password");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/account/change_password`


*changePassword*


> Body parameter


```json
{
  "password": "string"
}
```


<h3 id="changePasswordUsingPOST-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[ChangePasswordVM](#schemachangepasswordvm)|true|password|


> Example responses


<h3 id="changePasswordUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation require authentication
</aside>


#### Finish password reset


<a id="opIdfinishPasswordResetUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/account/reset_password/finish \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
POST http://example.com/api/account/reset_password/finish HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/account/reset_password/finish',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "key": "string",
  "newPassword": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('http://example.com/api/account/reset_password/finish',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.post 'http://example.com/api/account/reset_password/finish',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.post('http://example.com/api/account/reset_password/finish', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/account/reset_password/finish");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/account/reset_password/finish`


*finish Password Reset*


> Body parameter


```json
{
  "key": "string",
  "newPassword": "string"
}
```


<h3 id="finishPasswordResetUsingPOST-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[KeyAndPasswordVM](#schemakeyandpasswordvm)|true|keyAndPassword|


> Example responses


<h3 id="finishPasswordResetUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|string|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation require authentication
</aside>

 
#### Request Password Reset


<a id="opIdrequestPasswordResetUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/account/reset_password/init \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'


```


```http
POST http://example.com/api/account/reset_password/init HTTP/1.1
Host: null
Content-Type: application/json
Accept: application/json


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


$.ajax({
  url: 'http://example.com/api/account/reset_password/init',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "email": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};


fetch('http://example.com/api/account/reset_password/init',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}


result = RestClient.post 'http://example.com/api/account/reset_password/init',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}


r = requests.post('http://example.com/api/account/reset_password/init', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/account/reset_password/init");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /api/account/reset_password/init`


*Request Password Reset*


> Body parameter


```json
{
  "email": "string"
}
```


<h3 id="requestPasswordResetUsingPOST-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[ResetPasswordVM](#schemaresetpasswordvm)|true|mail|


> Example responses


```json
{
  "body": {},
  "statusCode": "100",
  "statusCodeValue": 0
}
```


<h3 id="requestPasswordResetUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation require authentication
</aside>


#### Confirm email address


<a id="opIdactivateAccountUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/activate?key=string \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/activate?key=string HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/activate',
  method: 'get',
  data: '?key=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/activate?key=string',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/activate',
  params: {
  'key' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/activate', params={
  'key': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/activate?key=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/activate`


*Confirm email address with key sent to email*


<h3 id="activateAccountUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|key|query|string|true|key|


> Example responses


<h3 id="activateAccountUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation require authentication
</aside>


#### is Authenticated


<a id="opIdisAuthenticatedUsingGET"></a>



<aside class="success">
This operation does not require authentication
</aside>




#### Get currrent user Associate


<a id="opIdgetAssociateUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/isactive \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/isactive HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/isactive',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/isactive',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/isactive',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/isactive', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/isactive");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/isactive`


*Is current user Associate activated*


> Example responses


<h3 id="getAssociateUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation require authentication
</aside>


<h3 id="Alt36Dash-API-Common-API-s">Common API-s</h3>


USA State Resource


#### Get all states


<a id="opIdgetAllCountryStatesUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/common/states/us \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/common/states/us HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/common/states/us',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/common/states/us',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/common/states/us',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/common/states/us', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/common/states/us");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/common/states/us`


*Get USA states list*


> Example responses

```
[
   {
      "id":1,
      "state":"Alabama",
      "abbreviation":"AL"
   },
   {
      "id":2,
      "state":"Alaska",
      "abbreviation":"AK"
   },
   {
      "id":3,
      "state":"Arizona",
      "abbreviation":"AZ"
   },
   {
      "id":4,
      "state":"Arkansas",
      "abbreviation":"AR"
   },
   {
      "id":5,
      "state":"California",
      "abbreviation":"CA"
   },
   {
      "id":6,
      "state":"Colorado",
      "abbreviation":"CO"
   },
   {
      "id":7,
      "state":"Connecticut",
      "abbreviation":"CT"
   },
   {
      "id":8,
      "state":"Delaware",
      "abbreviation":"DE"
   },
   {
      "id":9,
      "state":"District of Columbia",
      "abbreviation":"DC"
   },
   {
      "id":10,
      "state":"Florida",
      "abbreviation":"FL"
   },
   {
      "id":11,
      "state":"Georgia",
      "abbreviation":"GA"
   },
   {
      "id":12,
      "state":"Hawaii",
      "abbreviation":"HI"
   },
   {
      "id":13,
      "state":"Idaho",
      "abbreviation":"ID"
   },
   {
      "id":14,
      "state":"Illinois",
      "abbreviation":"IL"
   },
   {
      "id":15,
      "state":"Indiana",
      "abbreviation":"IN"
   },
   {
      "id":16,
      "state":"Iowa",
      "abbreviation":"IA"
   },
   {
      "id":17,
      "state":"Kansas",
      "abbreviation":"KS"
   },
   {
      "id":18,
      "state":"Kentucky",
      "abbreviation":"KY"
   },
   {
      "id":19,
      "state":"Louisiana",
      "abbreviation":"LA"
   },
   {
      "id":20,
      "state":"Maine",
      "abbreviation":"ME"
   },
   {
      "id":21,
      "state":"Montana",
      "abbreviation":"MT"
   },
   {
      "id":22,
      "state":"Nebraska",
      "abbreviation":"NE"
   },
   {
      "id":23,
      "state":"Nevada",
      "abbreviation":"NV"
   },
   {
      "id":24,
      "state":"New Hampshire",
      "abbreviation":"NH"
   },
   {
      "id":25,
      "state":"New Jersey",
      "abbreviation":"NJ"
   },
   {
      "id":26,
      "state":"New Mexico",
      "abbreviation":"NM"
   },
   {
      "id":27,
      "state":"New York",
      "abbreviation":"NY"
   },
   {
      "id":28,
      "state":"North Carolina",
      "abbreviation":"NC"
   },
   {
      "id":29,
      "state":"North Dakota",
      "abbreviation":"ND"
   },
   {
      "id":30,
      "state":"Ohio",
      "abbreviation":"OH"
   },
   {
      "id":31,
      "state":"Oklahoma",
      "abbreviation":"OK"
   },
   {
      "id":32,
      "state":"Oregon",
      "abbreviation":"OR"
   },
   {
      "id":33,
      "state":"Maryland",
      "abbreviation":"MD"
   },
   {
      "id":34,
      "state":"Massachusetts",
      "abbreviation":"MA"
   },
   {
      "id":35,
      "state":"Michigan",
      "abbreviation":"MI"
   },
   {
      "id":36,
      "state":"Minnesota",
      "abbreviation":"MN"
   },
   {
      "id":37,
      "state":"Mississippi",
      "abbreviation":"MS"
   },
   {
      "id":38,
      "state":"Missouri",
      "abbreviation":"MO"
   },
   {
      "id":39,
      "state":"Pennsylvania",
      "abbreviation":"PA"
   },
   {
      "id":40,
      "state":"Rhode Island",
      "abbreviation":"RI"
   },
   {
      "id":41,
      "state":"South Carolina",
      "abbreviation":"SC"
   },
   {
      "id":42,
      "state":"South Dakota",
      "abbreviation":"SD"
   },
   {
      "id":43,
      "state":"Tennessee",
      "abbreviation":"TN"
   },
   {
      "id":44,
      "state":"Texas",
      "abbreviation":"TX"
   },
   {
      "id":45,
      "state":"Utah",
      "abbreviation":"UT"
   },
   {
      "id":46,
      "state":"Vermont",
      "abbreviation":"VT"
   },
   {
      "id":47,
      "state":"Virginia",
      "abbreviation":"VA"
   },
   {
      "id":48,
      "state":"Washington",
      "abbreviation":"WA"
   },
   {
      "id":49,
      "state":"West Virginia",
      "abbreviation":"WV"
   },
   {
      "id":50,
      "state":"Wisconsin",
      "abbreviation":"WI"
   },
   {
      "id":51,
      "state":"Wyoming",
      "abbreviation":"WY"
   }
]
```


<h3 id="getAllCountryStatesUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<h3 id="getAllCountryStatesUsingGET-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[CountryStateDTO](#schemacountrystatedto)]|false|No description|
|» abbreviation|string|false|No description|
|» id|integer(int64)|false|No description|
|» state|string|false|No description|


#### Get file by uuid

##### HTTP Request

`GET /api/get/file/{uuid}`


### Parameters

Parameter | In | Type | Required | Description
--- | --- | --- | --- |---
uuid | path | string | true | uuid

### Responses

Code | Type | Description
--- | --- | ---
200 |  | OK
401 |  | Unauthorized
403 |  | Forbidden
404 |  | Not Found



#### Get all invitations


<a id="opIdgetAllInvitationsUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/invitations \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/invitations HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/invitations',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('http://example.com/api/invitations',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/invitations',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/invitations', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/invitations");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/invitations`


*Get all invitations sent by current Associate*


<h3 id="getAllInvitationsUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="getAllInvitationsUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfInvitation](#schemapageofinvitation)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>




## Payments
Payments service endpoints are central endpoints of Product36. Endpoints enable clients to get balance information, as well as to intiate payment process for two supported types of POS devices. Published interfaces include getting the information about user account, as well as payment capabilities - converting FIAT amount to cryptocurrency and getting the destination address. It is important to note that in background this is a multistep process and it is not as simple as getting the destination address from hot wallet. So there are firm security and business rules that have to be obeyed in order to complete any of these processes.
At the end, there is a notification process that can be used for getting events from within the system.
The base URL for Production environment is:

* https://paymentgateway-dot-altthirtysixproduct36.appspot.com 

The base URL for Sandbox environment is:

* https://paymentgateway-dot-sandboxaltthirtysixproduct36.appspot.com

### List of bank account
### Fiat cash out
### Send to Internal wallet
### Send to External wallet
### Convert
### Buy
### Exchange rates
### POS
#### Create new payment request

<a id="opIdcreateNewPaymentRequestPOS_1"></a>


`POST /api/pos/payment`

*Create new payment request for POS.*

Endpoint sends the amount in FIAT and gets value converted to dash along with destination address.

<h3 id="getAllPaginatedUsingGET_4-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[POSRequest](#schemaposrequest)|false|Page number of the requested page|

>Body parameter

```json
{
  "timestamp_req":"1503913839",
  "amount":"25.00",
  "currency":"USD",
  "convert_to": "DASH",
  "user_id":"ke2309s2399d"
}
```
<h3 id="poscreatenewpaymentrequest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[POSResponce](#schemaposresponce)|
|401|[Bad request](https://tools.ietf.org/html/rfc7235#section-3.1)|Bad request|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|



> Example responses


```json
{
"tx_id": "TXtbbSjB4HdQ",
"requested_amount": 25,
"requested_currency": "USD",
"converted_amount": 0.06778558065128386,
"converted_currency": "DASH",
"conversion_rate": 368.81,
"timetamp_system": 1504047876,
"pay_to_address": "msJfkM8XmwTxwVVV9EvWLXb4fjCpSvbKWT"
}

```
> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/pos/payment \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'
```

```http
POST http://example.com/api/pos/payment HTTP/1.1
Host: null
Content-Type: application/json
Accept: application/json
```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};
$.ajax({
  url: 'http://example.com/api/pos/payment',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})
```
```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
{
  "timestamp_req":"1503913839",
  "amount":"25.00",
  "currency":"USD",
  "convert_to": "DASH",
  "location_id”:123,
  "user_id":"ke2309s2399d"
};

fetch('http://example.com/api/pos/payment',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
```

```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'http://example.com/api/pos/payment',
  params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('http://example.com/api/vendor', params={
'timestamp_req':'1503913839',
'amount':'25.00',
'currency':'USD',
'convert_to': 'DASH',
'location_id':123,
'user_id':'ke2309s2399d'
}, headers = headers)


print r.json()
```
```java
URL obj = new URL("http://example.com/api/vendor");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```

### Virtual POS

<!-- VIRTUAL POS SECTION-->

#### Create new payment request virtual POS

Endpoint sends the amount in FIAT and gets value converted to dash along with destination address.

<a id="opIdcreateNewPaymentRequest_2"></a>


`POST /api/pos/payment/vpos`

*Create new payment request for virtual POS.*

<h3 id="getAllPaginatedUsingGET_4-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[POSRequest](#schemaposrequest)|false|Page number of the requested page|

>Body parameter

```json
{
  "timestamp_req":"1503913839",
  "amount":"25.00",
  "currency":"USD",
  "convert_to": "DASH",
  "location_id":123,
  "user_id":"ke2309s2399d"
}
```
<h3 id="poscreatenewpaymentrequest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[POSResponce](#schemaposresponce)|
|401|[Bad request](https://tools.ietf.org/html/rfc7235#section-3.1)|Bad request|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|



> Example responses


```json
{
"tx_id": "TXtbbSjB4HdQ",
"requested_amount": 25,
"requested_currency": "USD",
"converted_amount": 0.06778558065128386,
"converted_currency": "DASH",
"conversion_rate": 368.81,
"timetamp_system": 1504047876,
"pay_to_address": "msJfkM8XmwTxwVVV9EvWLXb4fjCpSvbKWT"
}

```
> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/pos/payment \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'
```

```http
POST http://example.com/api/pos/payment HTTP/1.1
Host: null
Content-Type: application/json
Accept: application/json
```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'


};
$.ajax({
  url: 'http://example.com/api/pos/payment',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})
```
```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
{
  "timestamp_req":"1503913839",
  "amount":"25.00",
  "currency":"USD",
  "convert_to": "DASH",
  "location_id”:123,
  "user_id":"ke2309s2399d"
};

fetch('http://example.com/api/pos/payment',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
```

```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'http://example.com/api/pos/payment',
  params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('http://example.com/api/vendor', params={
'timestamp_req':'1503913839',
'amount':'25.00',
'currency':'USD',
'convert_to': 'DASH',
'location_id':123,
'user_id':'ke2309s2399d'
}, headers = headers)


print r.json()
```
```java
URL obj = new URL("http://example.com/api/vendor");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```

## Notifications
Notification service uses EventSource capability of HTTP protocol. That is a variant of standard GET request, but conformed to long pulling use case. The notification service is used to get notifications on transaction status updates. The notification is provided for PoS related transactions and transactions of DASH digital currency to an external or internal wallet.
The base URL for Production environment is:

* https:/notifier-dot-altthirtysixproduct36.appspot.com 

The base URL for Sandbox environment is:

* https://notifier-dot-sandboxaltthirtysixproduct36.appspot.com

### Payment Notification

## Reporting
Reporting subsystem is a comprehensive list of endpoints that are used for getting various statistic information about user performance, and accounting. 
The base URL for Production environment is:

* https:/reporting-dot-altthirtysixproduct36.appspot.com 

The base URL for Sandbox environment is:

* https://reporting-dot-sandboxaltthirtysixproduct36.appspot.com

**Important notice:** There is a uniform date format which is used for time bound results. Generally, all ISO formats can be used. Nevertheless, following format is commonly used on the platform:

* *epoch_second* - A formatter for the number of seconds since the epoch
* *date or strict_date* - A formatter for a full date as four digit year, two digit month of year, and two digit day of month: yyyy-MM-dd.
* *date_hour_minute_second or strict_date_hour_minute_second* - full date, two digit hour of day, two digit minute of hour, and two digit second of minute: yyyy-MM-dd'T'HH:mm:ss. 
* *date_hour_minute_second_fraction* or strict_date_hour_minute_second_fraction 
* A formatter that combines a full date, two digit hour of day, two digit minute of hour, two digit second of minute, and three digit fraction of second: yyyy-MM-dd'T'HH:mm:ss.SSS

In the case of datetime ranges, if one uses date or strict_date format, it is considered by the system that the range is from 00:00.00 hour of the start date to 00:00.00 to the end date.

If the response contains cryptocurrency value, it always comes with FIAT value pair, so there is no need for conversion on client side. This considerably reduces the processing amount needed on client side, as client uses the data directly without need for further calculations.

All messages have two parts - metadata part which contain general information of data (such as current page number, number of elements per page, total number of elements etc), summary part (not provided for all report types) which contains summary information and page of data itself. This format reduces the need for clients to make excessive number of calls to the server. 

Note that all information is contextualized - related only to user that asks for informations. As the system is heavily relied on roles, every request needs proper JWT token embedded in Authorization Bearer header field in order to work.

### Dashboard Summary

Dashboard summary data

#### General system summary data

<a id="opIdcreateDashboard_general"></a>

`GET /api/v1/analytics/summary/general`

*Get general system summary data.*

This is info on system wide values of appropriate variables related to a given user. Information about user is read from request jwt token.

<h3 id="opIdcreateDashboard_general_summary-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|timerange_from|query|string|true|start date/datetime in ISO format|
|timerange_to|query|string|true|end date/datetime in ISO format|


<h3 id="opIdcreateDashboard_general_summary-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[GeneralSummaryResponse](#schemageneralsummaryresponse)|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|

> Example responses

```json
{
  "timerange_from": "2017-11-01T00:00:00.0Z",
  "timerange_to": "2018-01-11T23:59:59.1Z",
  "number_of_sales": 84,
  "avg_tx_amount": 0.12657074607143,
  "avg_tx_amount_fiat": 88.72505512713,
  "total_sales": 10.63194267,
  "total_sales_fiat": 7452.9046306789,
  "total_commission_fee_charged": 0.85386515,
  "total_commission_fee_charged_fiat": 602.6705777301
}
```

### Dashboard performance 
#### Location performance

<a id="opIdcreateDashboard_performance_location"></a>

`GET /api/v1/analytics/performance/location`

*Returns top 5 locations in the system.*

<h3 id="opIdcreateDashboard_performance_location-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|currency|query|string|false|which currency result should respond (currently ignored)|
|timerange_from|query|string|true|start date/datetime in ISO format|
|timerange_to|query|string|true|end date/datetime in ISO format|
|page_number|integer|string|true| represents requested page number (currently ignored)|


<h3 id="opIdcreateDashboard_performance_location--responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[LocationPerformanceResponse](#tocLocationPerformanceResponse)|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|

>Example responses

```json
{
  "metadata":{
      "timerangeFrom": "2017-09-01T00:00:00.0Z",
      "timerangeTo": "2018-01-15T23:59:59.1Z",
      "number": 0,
      "size": 2,
      "numberOfElements": 531,
      "totalPages": 54,
      "first": true,
      "last": false
    },
  "data":[
    {
      "location_id": 2432,
      "location_name": "Phoenician",
      "location_address": "6000 E Camelback Rd",
      "item_sales_crypto": 3.03869975,
      "item_sales_fiat": 2213.7153887805,
      "associate_owner": "Demo Merchant",
      "associate_owner_id": 2102
    },
    {
      "location_id": 743,
      "location_name": "Peoria",
      "location_address": "29701 N Sunrise Point",
      "item_sales_crypto": 1.41153177,
      "item_sales_fiat": 936.622608258,
      "associate_owner": "Demo Merchant",
      "associate_owner_id": 2102
    },
    {
      "location_id": 303,
      "location_name": "Phoenix",
      "location_address": "340 N 3rd St",
      "item_sales_crypto": 1.26886494,
      "item_sales_fiat": 767.8435600896,
      "associate_owner": "Demo Merchant",
      "associate_owner_id": 2102
    },
    {
      "location_id": 2427,
      "location_name": "ByMerchant",
      "location_address": "N 7th St",
      "item_sales_crypto": 1.05366415,
      "item_sales_fiat": 720.2720775932,
      "associate_owner": "Demo Merchant",
      "associate_owner_id": 2102
    },
    {
      "location_id": 744,
      "location_name": "Oakland",
      "location_address": "1411 E 31st St",
      "item_sales_crypto": 1.02292684,
      "item_sales_fiat": 690.7045676177,
      "associate_owner": "Demo Merchant",
      "associate_owner_id": 2102
    }
  ]
}
```

####Merchant performance

<a id="opIdcreateDashboard_performance_role"></a>

`GET /api/v1/analytics/performance/merchant`

*Returns top 5 merchants in the system.*

<h3 id="opIdcreateDashboard_performance_location-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|currency|query|string|false|which currency result should respond (currently ignored)|
|timerange_from|query|string|true|start date/datetime in ISO format|
|timerange_to|query|string|true|end date/datetime in ISO format|
|page_number|integer|string|true| represents requested page number (currently ignored)|


<h3 id="opIdcreateDashboard_performance_merchant-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SalesSummaryResponse](#tocSalesSummaryResponse)|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|

>Example responses

```json
{
  "metadata":{
      "timerangeFrom": "2017-09-01T00:00:00.0Z",
      "timerangeTo": "2018-01-15T23:59:59.1Z",
      "number": 0,
      "size": 2,
      "numberOfElements": 531,
      "totalPages": 54,
      "first": true,
      "last": false
    },
  "data":[
    {
      "item_id": 2432,
      "item_name": "Merchant Phoenix",
      "item_sales_crypto": 3.03869975,
      "item_sales_fiat": 2213.7153887805,
      "pos_count": 12
    },
    {
      "item_id": 743,
      "item_name": "Red hat",
      "item_sales_crypto": 1.41153177,
      "item_sales_fiat": 936.622608258,
      "pos_count": 23
    },
    {
      "item_id": 303,
      "item_name": "Merlin",
      "item_sales_crypto": 1.26886494,
      "item_sales_fiat": 767.8435600896,
      "pos_count": 42
    },
    {
      "item_id": 2427,
      "item_name": "Luna",
      "item_sales_crypto": 1.05366415,
      "item_sales_fiat": 720.2720775932,
      "pos_count": 11
    },
    {
      "item_id": 744,
      "item_name": "Venus",
      "item_sales_crypto": 1.02292684,
      "item_sales_fiat": 690.7045676177,
      "pos_count": 35
    }
  ]

}

```

### Sales Summary
#### Total sales by timerange

<a id="opIdcreateDashboard_total_sales_by_timerange"></a>

`GET /api/v1/analytics/summary/sales`

*Total sales by time-range which is further divided on one hour interval. Note that the time intervals are rounded in hours. All values within hour intervals are aggregated. *

<h3 id="opIdcreateDashboard_total_sales_by_timerange-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|currency|query|string|false|which currency result should respond (currently ignored)|
|timerange_from|query|string|true|start date/datetime in ISO format|
|timerange_to|query|string|true|end date/datetime in ISO format|
|page_number|integer|string|true| represents requested page number (currently ignored)|


<h3 id="opIdcreateDashboard_performance_merchant-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RolePerformanceResponse](#tocRolePerformanceResponse)|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|

> Example responses

```json
{
  "metadata":{
      "timerangeFrom": "2017-09-01T00:00:00.0Z",
      "timerangeTo": "2018-01-15T23:59:59.1Z",
      "number": 0,
      "size": 2,
      "numberOfElements": 531,
      "totalPages": 54,
      "first": true,
      "last": false
    },
  "data":[
          {
              "total_amount_of_sales": 0,
              "total_amount_of_sales_fiat":0,
              "time_from": "2017-10-12T13:00:00.000Z",
              "time_to": "2017-10-12T14:00:00.000Z"
          },
          {
              "total_amount_of_sales": 0.01242642,
              "total_amount_of_sales_fiat":24.23,
              "time_from": "2017-10-12T14:00:00.000Z",
              "time_to": "2017-10-12T15:00:00.000Z"
          }
    ]
}
```


#### General
#### Sales
#### Tax

### Sales Summary
#### Associate
#### Location
#### POS
### Reports Merchant
#### Merchant
#### Merchant’s locations
#### POS for Merchant’s locations
### Reports Locations
#### Location
#### POS for Locations
### Reports Point of sale
Point of sale Resource

### Reports Tax

Tax report for period of time

#### Tax report for associate

<a id="opIdcreateTaxReport"></a>

`GET /api/v1/analytics/reports/tax/{associateId}`

<h3 id="opIdcreateDashboard_tax-report-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|timerange_from|query|string|true|start date/datetime in ISO format|
|timerange_to|query|string|true|end date/datetime in ISO format|

<h3 id="opIdcreateDashboard_tax-report-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[TaxReportResponse](#tocTaxReportResponse)|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|

> Example responses

```json
{
    "metadata": {
        "timerangeFrom": "2017-11-11T00:00:00.000Z",
        "timerangeTo": "2017-11-11T23:00:00.000Z"
    },
    "content": {
        "totalTax":  256.23,
        "totalAmountReceived": 0.00223456,
        "totalAmountReceivedFiat": 25.36,
        "totalAmountSent": 0.001232,
        "totalAmountSentFiat": 15.25,
        "totalFee": 0.00012356,
        "totalFeeFiat": 1.0012356,
        "totalNumTxSpent": 52,
        "totalNumTxReceived": 23,
    }
}
```
<!-- #-------------- -->
# Sign Up/Login
# Support
In case you have any integration related questions, please contact us at [support@alt36.com](mailto:support@alt36.com). In order to expedite and facilitate the troubleshooting process, please provide us with any relevant information such as your username on the platform, code samples, exact API calls, returned response from our API, error messages, API call date and time, etc.

<!-- #[Documentation Powered by Slate](http://github.com/tripit/slate) -->



