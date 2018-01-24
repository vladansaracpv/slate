
### Manage Partners
#### Partner self registration

<a id="opIdselfRegistrationUsingPOST_2"></a>

> Code samples

```shell
curl -X POST http://example.com/api/partner/register \
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
    $URL = "http://example.com/api/partner/register";
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
  url: 'http://example.com/api/partner/register',
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

result = RestClient.post 'http://example.com/api/partner/register',
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

r = requests.post('http://example.com/api/partner/register',
                  data=<body_here>, params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/partner/register");
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

`POST /api/partner/register`

*Partner self registration*

**Required user role:**

  * `No authentication is required`

> Body parameter

```json
{
  "legalBusinessName": "Company",
  "companyEIN": "00-55555",
  "incorporationDate": "2017-09-19",
  "phone": "0645566777",
  "companyWebsite": "http://www.examplesite.com/",
  "address": "CompanyAddress",
  "emailAddress": "email@localhost",
  "city": "City",
  "state": {
    "id": 1,
    "state": "Alabama",
    "abbreviation": "AL"
  },
  "zip": "00000",
  "authorizedSignerContact":{
    "firstName": "First name",
    "lastName": "Last Name",
    "birthDate": "1987-01-19",
    "primaryMobilePhone": "0645566777",
    "primaryEmailAddress": "email@localhost",
    "nationality": "NN",
    "beneficiaryPercent": 100,
    "passportNumber": "111-15152626-333",
    "passportExpiryDate": "2020-09-19",
    "passportIssueDate": "2017-09-19",
    "fileBytes": "",
    "fileContentType": "application/pdf"
  },
  "mainContact":{
    "firstName": "First name",
    "lastName": "Last Name",
    "primaryMobilePhone": "0645566777",
    "primaryEmailAddress": "email@localhost",
    "position": "PR"
  },
  "user": {
    "email": "email@localhost",
    "firstName": "First Name",
    "lastName": "Last Name",
    "login": "email@localhost",
    "password": "Password123"
  }
}
```

<!-- <h3 id="selfRegistrationUsingPOST_2-parameters">Parameters</h3> -->

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

#### Update Partner

<a id="opIdupdateUsingPUT_3"></a>

> Code samples

```shell
curl -X PUT http://example.com/api/partners \
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
    $URL = "http://example.com/api/partners";
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
  url: 'http://example.com/api/partners',
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

result = RestClient.put 'http://example.com/api/partners',
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

r = requests.put('http://example.com/api/partners',
                  data=<body_here>, params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/partners");
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

`PUT /api/partners`

*Updates an existing Partner*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`

> Body parameter

```json
{
  "id": 1,
  "legalBusinessName": "Company",
  "companyEIN": "00-55555",
  "incorporationDate": "2017-09-19",
  "phone": "0645566777",
  "companyWebsite": "http://www.examplesite.com/",
  "address": "CompanyAddress",
  "emailAddress": "email@localhost",
  "city": "City",
  "state": {
    "id": 1,
    "state": "Alabama",
    "abbreviation": "AL"
  },
  "zip": "00000",
  "authorizedSignerContact":{
    "firstName": "First name",
    "lastName": "Last Name",
    "birthDate": "1987-01-19",
    "primaryMobilePhone": "0645566777",
    "primaryEmailAddress": "email@localhost",
    "nationality": "NN",
    "beneficiaryPercent": 100,
    "passportNumber": "111-15152626-333",
    "passportExpiryDate": "2020-09-19",
    "passportIssueDate": "2017-09-19",
    "fileBytes": "",
    "fileContentType": "application/pdf"
  },
  "mainContact":{
    "firstName": "First name",
    "lastName": "Last Name",
    "primaryMobilePhone": "0645566777",
    "primaryEmailAddress": "email@localhost",
    "position": "PR"
  },
  "canEditOnboarded": false
}
```

<!-- <h3 id="updateUsingPUT_3-parameters">Parameters</h3> -->

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

#### Get Partner by ID

<a id="opIdgetByIdUsingGET_3"></a>

> Code samples

```shell
curl -X GET http://example.com/api/partners/<id> -H Authorization: Bearer <token>
```

```php
<?php
$URL = "http://example.com/api/partners/<id>";

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
  url: 'http://example.com/api/partners/<id>',
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

result = RestClient.get 'http://example.com/api/partners/<id>',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/partners/<id>',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/partners/<id>");
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

`GET /api/partners/<id>`

*Get the partner by ID*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`

<!-- <h3 id="getByIdUsingGET_3-parameters">Parameters</h3> -->

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
