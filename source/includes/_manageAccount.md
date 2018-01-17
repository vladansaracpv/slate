

### Manage Account



#### Get Account


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

**Required user role:**

  * `Available to all user roles`

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



#### Create new user Account


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

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_VENDOR_ADMIN`

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


<!-- <h3 id="saveAccountUsingPOST-parameters">Parameters</h3> -->


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

**Required user role:**

 * `Available to all user roles`

<!-- <h3 id="activateAccountUsingGET-parameters">Parameters</h3> -->


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

**Required user role:**

 * `Available to all user roles`

> Body parameter


```json
{
  "password": "string"
}
```


<!-- <h3 id="changePasswordUsingPOST-parameters">Parameters</h3> -->


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

<!--
<aside class="success">
This operation require authentication
</aside> -->


#### Request password reset


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

**Required user role:**

 * `Available to all user roles`

> Body parameter


```json
{
  "email": "string"
}
```


<!-- <h3 id="requestPasswordResetUsingPOST-parameters">Parameters</h3> -->


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
This operation does not require authentication
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

**Required user role:**

 * `Available to all user roles`

> Body parameter


```json
{
  "key": "string",
  "newPassword": "string"
}
```


<!-- <h3 id="finishPasswordResetUsingPOST-parameters">Parameters</h3> -->


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

**Required user role:**

 * `ROLE_PARTNER_ADMIN`
 * `ROLE_MERCHANT_ADMIN`
 * `ROLE_VENDOR_ADMIN`
 * `ROLE_CUSTOMER_ADMIN`

> Body parameter


```json
{
  "reason": "string"
}
```


<!-- <h3 id="shutDownAccountUsingPOST-parameters">Parameters</h3> -->


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

<!--
<aside class="success">
This operation does not require authentication
</aside> -->

#### Get 2FA barcode image


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

**Required user role:**

 * `Available to all user roles`

<!-- <h3 id="getBarCodeImageUsingGET-parameters">Parameters</h3> -->


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

<!--
<aside class="success">
This operation require authentication
</aside> -->


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

**Required user role:**

 * `Available to all user roles`

<!-- <h3 id="modifyUser2FAUsingPOST-parameters">Parameters</h3> -->


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

**Required user role:**

 * `Available to all user roles`

> Example responses


<h3 id="getAssociateUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|
