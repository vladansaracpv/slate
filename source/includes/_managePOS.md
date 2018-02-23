<h3 id="Alt36Dash-API-Merchant-POS">Manage POS</h3>

Point Of Sale Resource

#### Get all POS

<a id="opIdgetAllPointOfSalesUsingGET_1"></a>

> Code samples

```shell
curl -X GET http://example.com/api/point-of-sales -H Authorization: Bearer <token>
```

```php
<?php
$URL = "http://example.com/api/point-of-sales";

$aHTTP['http']['method']  = 'GET';

$aHTTP['http']['header']  = "Authorization: Bearer <token>";

$context = stream_context_create($aHTTP);

$response = file_get_contents($URL, false, $context);
?>

```

```javascript
var headers = {
  'Authorization':'Bearer <token>'
};

$.ajax({
  url: 'http://example.com/api/point-of-sales',
  method: 'get',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
});
```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Authorization' => 'Bearer <token>'
}

result = RestClient.get 'http://example.com/api/point-of-sales',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/point-of-sales',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/point-of-sales");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestProperty("Authorization", "Bearer <token>");
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

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`

<!-- <h3 id="getAllPointOfSalesUsingGET_1-parameters">Parameters</h3> -->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|locationId|query|integer(int64)|false|locationId|
|merchantId|query|integer(int64)|false|merchantId|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc/desc). Default sort order is ascending. Multiple sort criteria are supported.|

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
curl -X GET http://example.com/api/point-of-sales/<id> -H Authorization: Bearer <token>
```

```php
<?php
$URL = "http://example.com/api/point-of-sales/<id>";

$aHTTP['http']['method']  = 'GET';

$aHTTP['http']['header']  = "Authorization: Bearer <token>";

$context = stream_context_create($aHTTP);

$response = file_get_contents($URL, false, $context);
?>

```

```javascript
var headers = {
  'Authorization':'Bearer <token>'
};

$.ajax({
  url: 'http://example.com/api/point-of-sales/<id>',
  method: 'get',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
});
```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Authorization' => 'Bearer <token>'
}

result = RestClient.get 'http://example.com/api/point-of-sales/<id>',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/point-of-sales/<id>',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/point-of-sales/<id>");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestProperty("Authorization", "Bearer <token>");
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

`GET /api/point-of-sales/<id>`

*Get POS by ID*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`

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

#### Create POS

<a id="opIdcreatePointOfSaleUsingPOST_1"></a>

> Code samples

```shell
curl -X POST http://example.com/api/point-of-sales \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer <token>'
  -D '<body_here>'
```

```php
<?php
    $body="<body_here>";
    $opts = array('http' =>
      array(
        'method'  => 'POST',
        'header'  => "Authorization: Bearer <token>\r\nContent-Type: application/json\r\nAccept: application/json\r\n",
        'content' => $body
      )
    );
    $context  = stream_context_create($opts);
    $URL = "http://example.com/api/point-of-sales";
    $result = file_get_contents($url, false, $context, -1, 40000);
);


$context = stream_context_create($aHTTP);
    $response = file_get_contents($URL, false, $context);
?>

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization': 'Bearer <token>'
};

var requestBody=<body_here>

$.ajax({
  url: 'http://example.com/api/point-of-sales',
  method: 'POST',
  headers: headers,
  data: requestBody,
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
  'Accept' => 'application/json'
  'Authorization'=>'Bearer <token>'
}

result = RestClient.post 'http://example.com/api/point-of-sales',
         payload:<body_here>, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer <token>'

}

r = requests.post('http://example.com/api/point-of-sales',
                  data=<body_here>, params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/point-of-sales");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestProperty("Accept", "application/json");
con.setRequestProperty("Content-Type", "application/json");
con.setRequestProperty("Authorization", "Bearer <token>");
con.setDoOutput(true);
con.setRequestMethod("POST");
OutputStream os = con.getOutputStream();
OutputStreamWriter osw = new OutputStreamWriter(os, "UTF-8");
osw.write("<body_here>");
osw.flush();
osw.close();
os.close();  //don't forget to close the OutputStream
httpCon.connect();


//read the inputstream and print it
String result;
BufferedInputStream bis = new BufferedInputStream(con.getInputStream());
ByteArrayOutputStream buf = new ByteArrayOutputStream();
int result2 = bis.read();
while(result2 != -1) {
    buf.write((byte) result2);
    result2 = bis.read();
}
result = buf.toString();
System.out.println(result);
```

`POST /api/point-of-sales`

*Create a new POS*

**Required user role:**

  * `ROLE_MERCHANT_ADMIN`

> Body parameter

```json
{
  "location": {
    "id": 1
  },
  "pointOfSaleType": "GREENBITS",
  "virtualPointOfSalesEnabled": true,
  "name": "POS1"
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

#### Update POS

<a id="opIdupdatePointOfSaleUsingPUT_1"></a>

> Code samples

```shell
curl -X PUT http://example.com/api/point-of-sales \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer <token>'
  -D '<body_here>'
```

```php
<?php
    $body="<body_here>";
    $opts = array('http' =>
      array(
        'method'  => 'PUT',
        'header'  => "Authorization: Bearer <token>\r\nContent-Type: application/json\r\nAccept: application/json\r\n",
        'content' => $body
      )
    );
    $context  = stream_context_create($opts);
    $URL = "http://example.com/api/point-of-sales";
    $result = file_get_contents($url, false, $context, -1, 40000);

    $context = stream_context_create($aHTTP);
    $response = file_get_contents($URL, false, $context);
?>

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization': 'Bearer <token>'
};

var requestBody=<body_here>

$.ajax({
  url: 'http://example.com/api/point-of-sales',
  method: 'PUT',
  headers: headers,
  data: requestBody,
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
  'Accept' => 'application/json'
  'Authorization'=>'Bearer <token>'
}

result = RestClient.put 'http://example.com/api/point-of-sales',
         payload:<body_here>, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer <token>'

}

r = requests.put('http://example.com/api/point-of-sales',
                  data=<body_here>, params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/point-of-sales");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestProperty("Accept", "application/json");
con.setRequestProperty("Content-Type", "application/json");
con.setRequestProperty("Authorization", "Bearer <token>");
con.setDoOutput(true);
con.setRequestMethod("PUT");
OutputStream os = con.getOutputStream();
OutputStreamWriter osw = new OutputStreamWriter(os, "UTF-8");
osw.write("<body_here>");
osw.flush();
osw.close();
os.close();  //don't forget to close the OutputStream
httpCon.connect();


//read the inputstream and print it
String result;
BufferedInputStream bis = new BufferedInputStream(con.getInputStream());
ByteArrayOutputStream buf = new ByteArrayOutputStream();
int result2 = bis.read();
while(result2 != -1) {
    buf.write((byte) result2);
    result2 = bis.read();
}
result = buf.toString();
System.out.println(result);
```

`PUT /api/point-of-sales`

*Update existing POS*

**Required user role:**

  * `ROLE_MERCHANT_ADMIN`

> Body parameter

```json
{
  "id": 1,
  "location": {
    "id": 1
  },
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

#### Delete POS

<a id="opIddeletePointOfSaleUsingDELETE_1"></a>

> Code samples

```shell
curl -X DELETE http://example.com/api/point-of-sales/<id> -H Authorization: Bearer <token>
```

```php
<?php
$URL = "http://example.com/api/point-of-sales/<id>";
$aHTTP['http']['method']  = 'DELETE';
$aHTTP['http']['header']  = "Authorization: <token>";
$context = stream_context_create($aHTTP);
$response = file_get_contents($URL, false, $context);
?>
```

```javascript
var headers = {
  'Authorization':'Bearer <token>'
};

$.ajax({
  url: 'http://example.com/api/point-of-sales/<id>',
  method: 'DELETE',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
});
```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Authorization' => 'Bearer <token>'
}

result = RestClient.delete 'http://example.com/api/point-of-sales/<id>',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.delete('http://example.com/api/point-of-sales/<id>',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/point-of-sales/<id>");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestProperty("Authorization", "Bearer <token>");
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

`DELETE /api/point-of-sales/<id>`

*Delete POS by ID*

**Required user role:**

  * `ROLE_MERCHANT_ADMIN`

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
curl -X GET http://example.com/api/point-of-sales/<id>/token -H Authorization: Bearer <token>
```

```php
<?php
$URL = "http://example.com/api/point-of-sales/<id>/token";

$aHTTP['http']['method']  = 'GET';

$aHTTP['http']['header']  = "Authorization: Bearer <token>";

$context = stream_context_create($aHTTP);

$response = file_get_contents($URL, false, $context);
?>

```

```javascript
var headers = {
  'Authorization':'Bearer <token>'
};

$.ajax({
  url: 'http://example.com/api/point-of-sales/<id>/token',
  method: 'get',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
});
```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Authorization' => 'Bearer <token>'
}

result = RestClient.get 'http://example.com/api/point-of-sales/<id>/token',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/point-of-sales/<id>/token',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/point-of-sales/<id>/token");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestProperty("Authorization", "Bearer <token>");
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

`GET /api/point-of-sales/<id>/token`

*Generate POS request token code*

**Required user role:**

  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_EXTERNAL, ROLE_PARTNER_ADMIN`

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
curl -X POST http://example.com/api/pos/register?key=string -H 'Accept: */*'
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
         params: {'key' => 'string'}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Accept': '*/*'
}

r = requests.post('http://example.com/api/pos/register',
                   params={'key': 'string'}, headers = headers)

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

**Required user role:**

  * `No authentication is required`

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
curl -X GET http://example.com/api/point-of-sales/<id>/isActive -H Authorization: Bearer <token>
```

```php
<?php
$URL = "http://example.com/api/point-of-sales/<id>/isActive";

$aHTTP['http']['method']  = 'GET';

$aHTTP['http']['header']  = "Authorization: Bearer <token>";

$context = stream_context_create($aHTTP);

$response = file_get_contents($URL, false, $context);
?>

```

```javascript
var headers = {
  'Authorization':'Bearer <token>'
};

$.ajax({
  url: 'http://example.com/api/point-of-sales/<id>/isActive',
  method: 'get',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
});
```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Authorization' => 'Bearer <token>'
}

result = RestClient.get 'http://example.com/api/point-of-sales/<id>/isActive',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/point-of-sales/<id>/isActive',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/point-of-sales/<id>/isActive");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestProperty("Authorization", "Bearer <token>");
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

`GET /api/point-of-sales/<id>/isActive`

*Get POS status*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`

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

#### Deactivate POS

<a id="opIddeletePosAuthUsingDELETE"></a>

> Code samples

```shell
curl -X DELETE http://example.com/api/point-of-sales/<id>/token -H Authorization: Bearer <token>
```

```php
<?php
$URL = "http://example.com/api/point-of-sales/<id>/token";
$aHTTP['http']['method']  = 'DELETE';
$aHTTP['http']['header']  = "Authorization: <token>";
$context = stream_context_create($aHTTP);
$response = file_get_contents($URL, false, $context);
?>
```

```javascript
var headers = {
  'Authorization':'Bearer <token>'
};

$.ajax({
  url: 'http://example.com/api/point-of-sales/<id>/token',
  method: 'DELETE',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
});
```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Authorization' => 'Bearer <token>'
}

result = RestClient.delete 'http://example.com/api/point-of-sales/<id>/token',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.delete('http://example.com/api/point-of-sales/<id>/token',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/point-of-sales/<id>/token");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestProperty("Authorization", "Bearer <token>");
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

`DELETE /api/point-of-sales/<id>/token`

*Deactivate POS token*

**Required user role:**

  * `ROLE_MERCHANT_ADMIN`

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
curl -X GET http://example.com/api/point-of-sale/search -H Authorization: Bearer <token>
```

```php
<?php
$URL = "http://example.com/api/point-of-sale/search";

$aHTTP['http']['method']  = 'GET';

$aHTTP['http']['header']  = "Authorization: Bearer <token>";

$context = stream_context_create($aHTTP);

$response = file_get_contents($URL, false, $context);
?>

```

```javascript
var headers = {
  'Authorization':'Bearer <token>'
};

$.ajax({
  url: 'http://example.com/api/point-of-sale/search',
  method: 'get',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
});
```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Authorization' => 'Bearer <token>'
}

result = RestClient.get 'http://example.com/api/point-of-sale/search',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/point-of-sale/search',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/point-of-sale/search");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestProperty("Authorization", "Bearer <token>");
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

*Search Point Of Sales*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`

<!-- <h3 id="searchUsingGET_4-parameters">Parameters</h3> -->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|q|query|string|false|q|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc/desc). Default sort order is ascending. Multiple sort criteria are supported.|

> Example responses

<h3 id="searchUsingGET_4-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfPointOfSale](#schemapageofpointofsale)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|
