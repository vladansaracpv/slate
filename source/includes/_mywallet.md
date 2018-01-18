### My wallet


Pending Transaction Resource


#### Get All Payments


<a id="opIdgetAllPaymentsTransactionsUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/transactions/allpayments \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/transactions/allpayments HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/transactions/allpayments',
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


fetch('http://example.com/api/transactions/allpayments',
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


result = RestClient.get 'http://example.com/api/transactions/allpayments',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/transactions/allpayments', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/transactions/allpayments");
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


`GET /api/transactions/allpayments`


*Get all payments (Partner gets all payments for associates he enroled)*


**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`



<!-- <h3 id="getAllPaymentsTransactionsUsingGET-parameters">Parameters</h3> -->


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|date.greaterThan|query|string(date-time)|false|From date|
|date.lessThan|query|string(date-time)|false|To date|
|status.equals|query|string|false|Filter by status|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="getAllPaymentsTransactionsUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfPaymentsTransactionVm](#schemapageofpaymentstransactionvm)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|




#### Get Sales Transactions


<a id="opIdgetSalesTransactionsForAdminAndPartnerUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/transactions/allsales \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/transactions/allsales HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/transactions/allsales',
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


fetch('http://example.com/api/transactions/allsales',
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


result = RestClient.get 'http://example.com/api/transactions/allsales',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/transactions/allsales', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/transactions/allsales");
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


`GET /api/transactions/allsales`


*Get all sales (Partner gets all sales from his merchants)*


**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`


<!-- <h3 id="getSalesTransactionsForAdminAndPartnerUsingGET-parameters">Parameters</h3> -->


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|date.greaterThan|query|string(date-time)|false|From date|
|date.lessThan|query|string(date-time)|false|To date|
|status.equals|query|string|false|Filter by status|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="getSalesTransactionsForAdminAndPartnerUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfSalesTransactionVM](#schemapageofsalestransactionvm)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|



#### Get Conversions Transactions


<a id="opIdgetConversionsTransactionsUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/transactions/conversions \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/transactions/conversions HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/transactions/conversions',
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


fetch('http://example.com/api/transactions/conversions',
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


result = RestClient.get 'http://example.com/api/transactions/conversions',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/transactions/conversions', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/transactions/conversions");
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


`GET /api/transactions/conversions`


* Get Conversions Transactions*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`
  * `ROLE_VENDOR_ADMIN`
  * `ROLE_VENDOR_USER`
  * `ROLE_CUSTOMER_ADMIN`

<!-- <h3 id="getConversionsTransactionsUsingGET-parameters">Parameters</h3> -->


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|date.greaterThan|query|string(date-time)|false|From date|
|date.lessThan|query|string(date-time)|false|To date|
|status.equals|query|string|false|Filter by status|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="getConversionsTransactionsUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfConversionsTransactionsVM](#schemapageofconversionstransactionsvm)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|



#### Get All Transactions By Location


<a id="opIdgetAllPendingTransactionsByLocationUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/transactions/location/{locationId} \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/transactions/location/{locationId} HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/transactions/location/{locationId}',
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


fetch('http://example.com/api/transactions/location/{locationId}',
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


result = RestClient.get 'http://example.com/api/transactions/location/{locationId}',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/transactions/location/{locationId}', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/transactions/location/{locationId}");
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


`GET /api/transactions/location/{locationId}`


*Get Transactions by location*


**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`


<!-- <h3 id="getAllPendingTransactionsByLocationUsingGET-parameters">Parameters</h3> -->


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|locationId|path|integer(int64)|true|Location ID|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="getAllPendingTransactionsByLocationUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfPendingTransaction](#schemapageofpendingtransaction)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|



#### Get my Last Transaction


<a id="opIdgetLastTransactionByAssociateUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/transactions/mylasttransaction \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/transactions/mylasttransaction HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/transactions/mylasttransaction',
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


fetch('http://example.com/api/transactions/mylasttransaction',
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


result = RestClient.get 'http://example.com/api/transactions/mylasttransaction',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/transactions/mylasttransaction', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/transactions/mylasttransaction");
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


`GET /api/transactions/mylasttransaction`


*Get my (current user associate) last successful transaction *


**Required user role:**

  * All roles



> Example responses


<h3 id="getLastTransactionByAssociateUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[LastTransactionVm](#schemalasttransactionvm)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|




#### Get Payments Transactions


<a id="opIdgetPaymentsTransactionsUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/transactions/payments \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/transactions/payments HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/transactions/payments',
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


fetch('http://example.com/api/transactions/payments',
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


result = RestClient.get 'http://example.com/api/transactions/payments',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/transactions/payments', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/transactions/payments");
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


`GET /api/transactions/payments`


*Get Payments Transactions*

**Required user role:**

  * All roles


<!-- <h3 id="getPaymentsTransactionsUsingGET-parameters">Parameters</h3> -->


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|date.greaterThan|query|string(date-time)|false|From date|
|date.lessThan|query|string(date-time)|false|To date|
|status.equals|query|string|false|Filter by status|
|associateId|query|integer(int64)|false|associateId|
|showall|query|boolean|false|showall|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="getPaymentsTransactionsUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfPaymentsTransactionVm](#schemapageofpaymentstransactionvm)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


#### Get All Transactions By Pos


<a id="opIdgetAllPendingTransactionsByPosUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/transactions/pos/{posId} \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/transactions/pos/{posId} HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/transactions/pos/{posId}',
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


fetch('http://example.com/api/transactions/pos/{posId}',
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


result = RestClient.get 'http://example.com/api/transactions/pos/{posId}',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/transactions/pos/{posId}', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/transactions/pos/{posId}");
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


`GET /api/transactions/pos/{posId}`


*Get Transactions by POS*


**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`


<!-- <h3 id="getAllPendingTransactionsByPosUsingGET-parameters">Parameters</h3> -->


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|posId|path|integer(int64)|true|posId|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="getAllPendingTransactionsByPosUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfPendingTransaction](#schemapageofpendingtransaction)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


#### Get Sales Transactions


<a id="opIdgetSalesTransactionsUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/transactions/sales \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/transactions/sales HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/transactions/sales',
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


fetch('http://example.com/api/transactions/sales',
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


result = RestClient.get 'http://example.com/api/transactions/sales',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/transactions/sales', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/transactions/sales");
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


`GET /api/transactions/sales`


* Get Sales Transactions*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`



<!-- <h3 id="getSalesTransactionsUsingGET-parameters">Parameters</h3> -->


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|date.greaterThan|query|string(date-time)|false|From date|
|date.lessThan|query|string(date-time)|false|To date|
|status.equals|query|string|false|Filter by status|
|showall|query|boolean|false|showall|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="getSalesTransactionsUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfSalesTransactionVM](#schemapageofsalestransactionvm)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|



#### Get All Transactions By Location


<a id="opIdgetAllPendingTransactionsByLocationAndCurrentUserUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/transactions/userlocation/{locationId} \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/transactions/userlocation/{locationId} HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/transactions/userlocation/{locationId}',
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


fetch('http://example.com/api/transactions/userlocation/{locationId}',
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


result = RestClient.get 'http://example.com/api/transactions/userlocation/{locationId}',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/transactions/userlocation/{locationId}', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/transactions/userlocation/{locationId}");
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


`GET /api/transactions/userlocation/{locationId}`


*Get Transactions by location for current user*


**Required user role:**

  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`



<!-- <h3 id="getAllPendingTransactionsByLocationAndCurrentUserUsingGET-parameters">Parameters</h3> -->


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|locationId|path|integer(int64)|true|Location ID|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="getAllPendingTransactionsByLocationAndCurrentUserUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfPendingTransaction](#schemapageofpendingtransaction)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


#### Get Withdrawals Transactions


<a id="opIdgetWithdrawalsTransactionsUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/transactions/withdrawals \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/transactions/withdrawals HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/transactions/withdrawals',
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


fetch('http://example.com/api/transactions/withdrawals',
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


result = RestClient.get 'http://example.com/api/transactions/withdrawals',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/transactions/withdrawals', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/transactions/withdrawals");
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


`GET /api/transactions/withdrawals`


*Get Withdrawals Transactions*


<!-- <h3 id="getWithdrawalsTransactionsUsingGET-parameters">Parameters</h3> -->


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|date.greaterThan|query|string(date-time)|false|From date|
|date.lessThan|query|string(date-time)|false|To date|
|status.equals|query|string|false|Filter by status|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="getWithdrawalsTransactionsUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfWithdrawalsTransactionsVm](#schemapageofwithdrawalstransactionsvm)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|





#### Get single Transaction by ID


<a id="opIdgetPendingTransactionUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/transactions/{id} \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/transactions/{id} HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/transactions/{id}',
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


fetch('http://example.com/api/transactions/{id}',
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


result = RestClient.get 'http://example.com/api/transactions/{id}',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/transactions/{id}', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/transactions/{id}");
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


`GET /api/transactions/{id}`


*Get single Transaction by ID*

**Required user role:**

  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`


<!-- <h3 id="getPendingTransactionUsingGET-parameters">Parameters</h3> -->


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|


> Example responses


<h3 id="getPendingTransactionUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PendingTransaction](#schemapendingtransaction)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

