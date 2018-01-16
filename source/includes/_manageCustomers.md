
<h3 id="Alt36Dash-API-Customer">Manage Customers</h3>


Customer Resource


#### Get all Customers

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


<!-- <h3 id="getAllPaginatedUsingGET-parameters">Parameters</h3> -->


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


#### Get Customer by ID


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


<!-- <h3 id="getByIdUsingGET-parameters">Parameters</h3> -->


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




#### Create Customer


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


<!-- <h3 id="registerNewUsingPOST-parameters">Parameters</h3> -->


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

<!-- 
<aside class="success">
This operation does not require authentication
</aside> -->




#### Invite Customer via email


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


<!-- <h3 id="inviteUsingPOST-parameters">Parameters</h3> -->


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




#### Customer self-registration

<aside class="success">
This operation does not require authentication
</aside>

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


<!-- <h3 id="selfRegistrationUsingPOST-parameters">Parameters</h3> -->


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



#### Update Customer


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


<!-- <h3 id="updateUsingPUT-parameters">Parameters</h3> -->


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


#### Delete Customer


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


<!-- <h3 id="deleteUsingDELETE-parameters">Parameters</h3> -->


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







#### Search Customers


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


<!-- <h3 id="searchUsingGET-parameters">Parameters</h3> -->


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



