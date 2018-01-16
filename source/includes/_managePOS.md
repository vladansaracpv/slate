

<h3 id="Alt36Dash-API-Merchant-POS">Manage POS</h3>


Point Of Sale Resource


#### Get all POS

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


<!-- <h3 id="getAllPointOfSalesUsingGET_1-parameters">Parameters</h3> -->


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


<!-- <h3 id="getPointOfSaleUsingGET_1-parameters">Parameters</h3> -->


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

<!-- 
<aside class="success">
</aside> -->


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


<!-- <h3 id="createPointOfSaleUsingPOST_1-parameters">Parameters</h3> -->


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

<!-- 
<aside class="success">
</aside> -->


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


<!-- <h3 id="updatePointOfSaleUsingPUT_1-parameters">Parameters</h3> -->


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

<!-- 
<aside class="success">
</aside> -->

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


<!-- <h3 id="deletePointOfSaleUsingDELETE_1-parameters">Parameters</h3> -->


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



#### Generate POS API request code


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


<!-- <h3 id="createNewPosAuthUsingGET-parameters">Parameters</h3> -->


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



#### Register POS with API request code


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


<!-- <h3 id="registerNewPosWithKeyUsingPOST-parameters">Parameters</h3> -->


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


<!-- <h3 id="isPosActiveUsingGET-parameters">Parameters</h3> -->


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

<!-- 
<aside class="success">
</aside> -->



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


<!-- <h3 id="deletePosAuthUsingDELETE-parameters">Parameters</h3> -->


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



#### Search POS


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


<!-- <h3 id="searchUsingGET_4-parameters">Parameters</h3> -->


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

<!-- 
<aside class="success">
</aside> -->

