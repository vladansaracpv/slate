<h3 id="Alt36Dash-API-Vendor">Manage Vendors</h3>

Vendor Resource

#### Get all Vendors paginated

<a id="opIdgetAllPaginatedUsingGET_4"></a>

> Code samples

```shell
curl -X GET http://example.com/api/vendors -H Authorization: Bearer <token>
```

```php
<?php
$URL = "http://example.com/api/vendors";

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
  url: 'http://example.com/api/vendors',
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

result = RestClient.get 'http://example.com/api/vendors',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/vendors',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/vendors");
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

`GET /api/vendors`

*Get the all Vendors paginated*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`

<!-- <h3 id="getAllPaginatedUsingGET_4-parameters">Parameters</h3> -->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc/desc). Default sort order is ascending. Multiple sort criteria are supported.|

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
|» companyWebsite|string|true|No description|
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

#### Get all Vendors

<a id="opIdgetAllUsingGET"></a>

> Code samples

```shell
curl -X GET http://example.com/api/allvendors -H Authorization: Bearer <token>
```

```php
<?php
$URL = "http://example.com/api/allvendors";

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
  url: 'http://example.com/api/allvendors',
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

result = RestClient.get 'http://example.com/api/allvendors',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/allvendors',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/allvendors");
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

`GET /api/allvendors`

*Get the all Vendors*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`

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
|» companyWebsite|string|true|No description|
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

#### Get Vendor by ID

<a id="opIdgetByIdUsingGET_4"></a>

> Code samples

```shell
curl -X GET http://example.com/api/vendors/<id> -H Authorization: Bearer <token>
```

```php
<?php
$URL = "http://example.com/api/vendors/<id>";

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
  url: 'http://example.com/api/vendors/<id>',
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

result = RestClient.get 'http://example.com/api/vendors/<id>',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/vendors/<id>',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/vendors/<id>");
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

`GET /api/vendors/<id>`

*Get the vendor by id*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`
  * `ROLE_VENDOR_ADMIN`

<!-- <h3 id="getByIdUsingGET_4-parameters">Parameters</h3> -->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|

> Example responses

<h3 id="getByIdUsingGET_4-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[NewVendorVM](#schemanewvendorvm)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

#### Create Vendor

<a id="opIdregisterNewUsingPOST_4"></a>

> Code samples

```shell
curl -X POST http://example.com/api/vendor \
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
    $URL = "http://example.com/api/vendor";
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
  url: 'http://example.com/api/vendor',
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

result = RestClient.post 'http://example.com/api/vendor',
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

r = requests.post('http://example.com/api/vendor',
                  data=<body_here>, params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/vendor");
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

`POST /api/vendor`

*Creates a new vendor*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`
  * `ROLE_VENDOR_ADMIN`

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

<!-- <h3 id="registerNewUsingPOST_4-parameters">Parameters</h3> -->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[NewVendorVM](#schemanewvendorvm)|true|partner|

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

#### Invite Vendor via Email

<a id="opIdinviteUsingPOST_3"></a>

> Code samples

```shell
curl -X POST http://example.com/api/vendor/invite \
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
    $URL = "http://example.com/api/vendor/invite";
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
  url: 'http://example.com/api/vendor/invite',
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

result = RestClient.post 'http://example.com/api/vendor/invite',
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

r = requests.post('http://example.com/api/vendor/invite',
                  data=<body_here>, params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/vendor/invite");
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

`POST /api/vendor/invite`

*Invite vendor via email*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_VENDOR_ADMIN`

> Body parameter

```json
{
  "email": "string"
}
```

<!-- <h3 id="inviteUsingPOST_3-parameters">Parameters</h3> -->

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

#### Vendor self-registration

<a id="opIdselfRegistrationUsingPOST_3"></a>

> Code samples

```shell
curl -X POST http://example.com/api/vendor/register \
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
    $URL = "http://example.com/api/vendor/register";
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
  url: 'http://example.com/api/vendor/register',
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

result = RestClient.post 'http://example.com/api/vendor/register',
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

r = requests.post('http://example.com/api/vendor/register',
                  data=<body_here>, params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/vendor/register");
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

`POST /api/vendor/register`

*Vendor self registration*

**Required user role:**

  * `No authentication is required`

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

<!-- <h3 id="selfRegistrationUsingPOST_3-parameters">Parameters</h3> -->

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

#### Update Vendor

<a id="opIdupdateUsingPUT_4"></a>

> Code samples

```shell
curl -X PUT http://example.com/api/vendors \
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
    $URL = "http://example.com/api/vendors";
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
  url: 'http://example.com/api/vendors',
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

result = RestClient.put 'http://example.com/api/vendors',
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

r = requests.put('http://example.com/api/vendors',
                  data=<body_here>, params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/vendors");
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


`PUT /api/vendors`

*Updates an existing Vendor*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_VENDOR_ADMIN`

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

<!-- <h3 id="updateUsingPUT_4-parameters">Parameters</h3> -->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[NewVendorVM](#schemanewvendorvm)|true|associate|

> Example responses

<h3 id="updateUsingPUT_4-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[Associate](#schemaassociate)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

#### Delete Vendor

<a id="opIddeleteUsingDELETE_4"></a>

> Code samples

```shell
curl -X DELETE http://example.com/api/vendor/<id> -H Authorization: Bearer <token>
```

```php
<?php
$URL = "http://example.com/api/vendor/<id>";
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
  url: 'http://example.com/api/vendor/<id>',
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

result = RestClient.delete 'http://example.com/api/vendor/<id>',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.delete('http://example.com/api/vendor/<id>',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/vendor/<id>");
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


`DELETE /api/vendor/<id>`

*Delete the Vendor with ID*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_VENDOR_ADMIN`

<!-- <h3 id="deleteUsingDELETE_4-parameters">Parameters</h3> -->

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

#### Search Vendors

<a id="opIdsearchUsingGET_5"></a>

> Code samples

```shell
curl -X GET http://example.com/api/vendor/search -H Authorization: Bearer <token>
```

```php
<?php
$URL = "http://example.com/api/vendor/search";

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
  url: 'http://example.com/api/vendor/search',
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

result = RestClient.get 'http://example.com/api/vendor/search',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/vendor/search',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/vendor/search");
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

`GET /api/vendor/search`

*search*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`
  * `ROLE_VENDOR_ADMIN`

<!-- <h3 id="searchUsingGET_5-parameters">Parameters</h3> -->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|q|query|string|false|q|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc/desc). Default sort order is ascending. Multiple sort criteria are supported.|

> Example responses

<h3 id="searchUsingGET_5-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfAssociate](#schemapageofassociate)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|
