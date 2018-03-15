## Payments
Payments service endpoints are central endpoints of Product36. Endpoints enable clients to get balance information, as well as to initiate payment process for two supported types of POS devices. Published interfaces include getting the information about user account, as well as payment capabilities - converting FIAT amount to cryptocurrency and getting the destination address. It is important to note that in background this is a multistep process and it is not as simple as getting the destination address from hot wallet. So there are firm security and business rules that have to be obeyed in order to complete any of these processes.
At the end, there is a notification process that can be used for getting events from within the system.

The base URL for Production environment is:

* `https://paymentgateway-dot-altthirtysixproduct36.appspot.com`

The base URL for Sandbox environment is:

* `https://paymentgateway-dot-sandboxaltthirtysixproduct36.appspot.com`

**Important notice**

Please replace `http://example.com` from Code samples with corresponding base URL.

### Wallet balance

> Code samples

```shell
curl -X GET http://example.com/api/account/cpaccountinfo -H Authorization: Bearer <token>
```

```php
<?php
$URL = "http://example.com/api/account/cpaccountinfo";

$aHTTP['http']['method']  = 'GET';

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
  url: 'http://example.com/api/account/cpaccountinfo',
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

result = RestClient.get 'http://example.com/api/account/cpaccountinfo',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/account/cpaccountinfo',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/account/cpaccountinfo");
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


> Example responses

```json
{
 "balances": [
   {
     "amount": 1.2,
     "currency": "BTC"
   }
 ],
 "role": "capite",
 "unconfirmed_balances": []
}
```

<a id="opIdcoinapult-account-info"></a>

`GET /api/account/cpaccountinfo`

*Get current balance of your wallet.*

**Required user role:**

  * `Available to all user roles`

<!--<h3 id="opCoinapult_API_coinapult-account">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|associateId|query|string|true|Internal associate id|
|currency|query|string|false|Currency short string (DASH for example). Currently ignored

**Responses**

Response result is passed-through from Coinapult and the system does not either store or processes it.

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[string] Received from Coinapult|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|


### Send DASH to Internal wallet

> Code samples

```shell
curl -X POST http://example.com/api/transfer/internal_crypto/2/internal_crypto \
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
    $URL = "http://example.com/api/transfer/internal_crypto/2/internal_crypto";
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
  url: 'http://example.com/api/transfer/internal_crypto/2/internal_crypto',
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

result = RestClient.post 'http://example.com/api/transfer/internal_crypto/2/internal_crypto',
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

r = requests.post('http://example.com/api/transfer/internal_crypto/2/internal_crypto',
                  data=<body_here>, params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/transfer/internal_crypto/2/internal_crypto");
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


>Body parameter

```json
{
    "type":"INTERNAL_CRYPTO_TO_INTERNAL_CRYPTO",
    "source_associate_id": 20,
    "destination_associate_id": 100,
    "amount": 1.2,
    "currency_in": "DASH",
    "currency_out": "DASH",
    "timestamp_req":"152345465564",
    "note":"Some transaction note string"
}
```

> Example responses

```json
{
    "timestamp_accepted": "152345465566",
    "tx_id": "TXtbbSjB4HdQ",
    "destination_address":"myzREJCjMo3peEcvpmPBWdgDpNhvVHTNBZ"
    "status": "PENDING",
    "request_was":{
                "type":"INTERNAL_CRYPTO_TO_INTERNAL_CRYPTO",
                "source_associate_id": 20,
                "destination_associate_id": 100,
                "amount": 1.2,
                "currency_in": "DASH",
                "currency_out": "DASH",
                "timestamp_req":"152345465564",
                "note":"Some transaction note string"
        }
}  
```

<a id="opIdcreate_intenal_crypto_2_internal_crypto"></a>

`POST /api/transfer/internal_crypto/2/internal_crypto`

*Send DASH to an internal wallet (to someone on the platform).*

**Required user role:**

   * `ROLE_PARTNER_ADMIN`
   * `ROLE_MERCHANT_ADMIN`
   * `ROLE_VENDOR_ADMIN`
   * `ROLE_CUSTOMER_ADMIN`

<!--<h3 id="getAllPaginatedUsingGET_4-parameters">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[InternalRequest](#tocInternalRequest)|false|InternalRequest object|


<h3 id="poscreatenewpaymentrequest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[InternalResponse](#tocInternalResponse)|
|401|[Bad request](https://tools.ietf.org/html/rfc7235#section-3.1)|Bad request|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|


### Send DASH to External wallet

> Code samples

```shell
curl -X POST http://example.com/api/transfer/internal_crypto/2/external_crypto \
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
    $URL = "http://example.com/api/transfer/internal_crypto/2/external_crypto";
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
  url: 'http://example.com/api/transfer/internal_crypto/2/external_crypto',
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

result = RestClient.post 'http://example.com/api/transfer/internal_crypto/2/external_crypto',
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

r = requests.post('http://example.com/api/transfer/internal_crypto/2/external_crypto',
                  data=<body_here>, params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/transfer/internal_crypto/2/external_crypto");
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


>Body parameter

```json
{
    "type":"INTERNAL_CRYPTO_TO_EXTERNAL_CRYPTO",
    "source_associate_id": 20,
    "destination_address":"myzREJCjMo3peEcvpmPBWdgDpNhvVHTNBZ",
    "amount": 1.2,
    "currency_in": "DASH",
    "currency_out": "DASH",
    "timestamp_req":152345465564,
    "note":"Some transaction note string"
}
```


> Example responses

```json
{
    "timestamp_accepted": "152345465566",
    "tx_id": "TXtbbSjB4HdQ",
    "destination_address":"myzREJCjMo3peEcvpmPBWdgDpNhvVHTNBZ",
    "status": "PENDING",
    "request_was":{
            "type":"INTERNAL_CRYPTO_TO_EXTERNAL_CRYPTO",
            "source_associate_id": 20,
            "destination_associate_id": 20,
            "destination_address":"myzREJCjMo3peEcvpmPBWdgDpNhvVHTNBZ",
            "amount": 1.2,
            "currency_in": "DASH",
            "currency_out": "DASH",
            "timestamp_req":"152345465564",
            "note":"Some transaction note string"
    }
}
```

<a id="opIdcreate_intenal_crypto_2_external_crypto"></a>

`POST /api/transfer/internal_crypto/2/external_crypto`

*Send DASH to an external wallet by providing destination address.*

**Required user role:**

   * `ROLE_PARTNER_ADMIN`
   * `ROLE_MERCHANT_ADMIN`
   * `ROLE_VENDOR_ADMIN`
   * `ROLE_CUSTOMER_ADMIN`

<!--<h3 id="getAllPaginatedUsingGET_4-internal_crypto_to_extenal_crypto">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[InternalRequest](#tocInternalRequest)|false|InternalRequest object|


<h3 id="poscreatenewpaymentrequest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[InternalResponse](#tocInternalResponse)|
|401|[Bad request](https://tools.ietf.org/html/rfc7235#section-3.1)|Bad request|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|


### Convert DASH

> Code samples

```shell
curl -X POST http://example.com/api/convert/crypto/2/fiat \
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
    $URL = "http://example.com/api/convert/crypto/2/fiat";
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
  url: 'http://example.com/api/convert/crypto/2/fiat',
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

result = RestClient.post 'http://example.com/api/convert/crypto/2/fiat',
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

r = requests.post('http://example.com/api/convert/crypto/2/fiat',
                  data=<body_here>, params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/convert/crypto/2/fiat");
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

>Body parameter

```json
{
    "type":"INTERNAL_CRYPTO_TO_FIAT",
    "source_associate_id": 20,
    "amount": 1.2,
    "currency_in": "DASH",
    "currency_out": "USD",
    "timestamp_req":"152345465564",
    "note":"Some transaction note string"
}
```

> Example responses

```json
{
    "timestamp_accepted": "152345465566",
    "tx_id": "TXtbbSjB4HdQ",
    "status": "PENDING",
    "request_was":{
        "type":"INTERNAL_CRYPTO_TO_FIAT",
        "source_associate_id": 20,
        "amount": 1.2,
        "currency_in": "DASH",
        "currency_out": "USD",
        "timestamp_req":"152345465564",
        "note":"Some transaction note string"
    }
}
```
<a id="opIdcreate_intenal_crypto_2_fiat"></a>

`POST /api/convert/crypto/2/fiat`

*Internal conversion from cryptocurrency (DASH) to FIAT (USD).*

**Required user role:**

   * `ROLE_PARTNER_ADMIN`
   * `ROLE_MERCHANT_ADMIN`
   * `ROLE_VENDOR_ADMIN`
   * `ROLE_CUSTOMER_ADMIN`

<!--<h3 id="getAllPaginatedUsingGET_4-internal_crypto_to_fiat">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[InternalRequest](#tocInternalRequest)|false|InternalRequest object|

<h3 id="poscreatenewpaymentrequest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[InternalResponse](#tocInternalResponse)|
|401|[Bad request](https://tools.ietf.org/html/rfc7235#section-3.1)|Bad request|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|


### Buy DASH

> Code samples

```shell
curl -X POST http://example.com/api/convert/fiat/2/crypto \
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
    $URL = "http://example.com/api/convert/fiat/2/crypto";
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
  url: 'http://example.com/api/convert/fiat/2/crypto',
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

result = RestClient.post 'http://example.com/api/convert/fiat/2/crypto',
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

r = requests.post('http://example.com/api/convert/fiat/2/crypto',
                  data=<body_here>, params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/convert/fiat/2/crypto");
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


>Body parameter

```json
{
    "type":"FIAT_TO_INTERNAL_CRYPTO",
    "source_associate_id": 20,
    "amount": 20,
    "currency_in": "USD",
    "currency_out": "DASH",
    "timestamp_req":"152345465564",
    "note":"Some transaction note string"
}
```


> Example responses

```json
{
    "timestamp_accepted": "152345465566",
    "tx_id": "TXtbbSjB4HdQ",
    "status": "PENDING",
    "request_was":{
        "type":"FIAT_TO_INTERNAL_CRYPTO",
        "source_associate_id": 20,
        "amount": 20,
        "currency_in": "USD",
        "currency_out": "DASH",
        "timestamp_req":152345465564,
        "note":"Some transaction note string"
    }
}
```

<a id="opIdcreate_fiat_to_crypto"></a>

`POST /api/convert/fiat/2/crypto`

*Internal conversion from FIAT (USD) to cryptocurrency (DASH) - Buy DASH.*

**Required user role:**

   * `ROLE_PARTNER_ADMIN`
   * `ROLE_MERCHANT_ADMIN`
   * `ROLE_VENDOR_ADMIN`
   * `ROLE_CUSTOMER_ADMIN`

<!--<h3 id="getAllPaginatedUsingGET_4-internal_fiat_to_crypto">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[InternalRequest](#tocInternalRequest)|false|InternalRequest object|


<h3 id="poscreatenewpaymentrequest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[InternalResponse](#tocInternalResponse)|
|401|[Bad request](https://tools.ietf.org/html/rfc7235#section-3.1)|Bad request|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|


### List bank accounts

> Code samples

```shell
curl -X POST http://example.com/api/account/bank_account \
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
    $URL = "http://example.com/api/account/bank_account";
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
  url: 'http://example.com/api/account/bank_account',
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

result = RestClient.post 'http://example.com/api/account/bank_account',
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

r = requests.post('http://example.com/api/account/bank_account',
                  data=<body_here>, params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/account/bank_account");
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

>Body parameter

```json
{
    "type":"INTERNAL_FIAT_TO_EXTERNAL_FIAT",
}
```

> Example responses

```json
{
  "accounts": [
    {
      "currency": "USD",
      "number": "9000000000",
      "description": "my account",
      "institution": "Crypto Capital"
    }
  ]
}
```

<a id="opIdcreate_bank_account_list"></a>

`POST /api/account/bank_account`

*List your FIAT (USD) accounts*

**Required user role:**

   * `Available to all user roles`

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[FIATCashout](#tocFIATCashoutRequest)|true|FIATCashout object|

<h3 id="poscreatenewpaymentrequest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[string] Received from Coinapult|
|401|[Bad request](https://tools.ietf.org/html/rfc7235#section-3.1)|Bad request|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|

### FIAT cash out

> Code samples

```shell
curl -X POST http://example.com/api/transfer/internalfiat/2/externalfiat \
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
    $URL = "http://example.com/api/transfer/internalfiat/2/externalfiat";
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
  url: 'http://example.com/api/transfer/internalfiat/2/externalfiat',
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

result = RestClient.post 'http://example.com/api/transfer/internalfiat/2/externalfiat',
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

r = requests.post('http://example.com/api/transfer/internalfiat/2/externalfiat',
                  data=<body_here>, params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/transfer/internalfiat/2/externalfiat");
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


>Body parameter

```json
{
    "type": "INTERNAL_FIAT_TO_EXTERNAL_FIAT",
    "timestamp_req":"1506895789",
    "source_associate_id": 20,
    "bank_account": "9000000000",
    "amount":  1,
    "currency_out": "USD",
    "note":"Some transaction note string"
}
```

> Example responses

```json
{
    "timestamp_accepted": 152345465566,
    "tx_id": "TXtbbSjB4HdQ",
    "status": "PENDING",
    "request_was":{
        "type": "INTERNAL_FIAT_TO_EXTERNAL_FIAT",
        "timestamp_req":"1506895789",
        "bank_account": "9000000000",
        "amount":  1,
        "currency_out": "USD",
        "note":"Some transaction note string"
    }
}
```


<a id="opIdcreate_fiat_to_external_fiat"></a>

`POST /api/transfer/internalfiat/2/externalfiat`

*Transfer FIAT (USD) funds to Crypto Capital Bank.*

**Required user role:**

   * `ROLE_PARTNER_ADMIN`
   * `ROLE_MERCHANT_ADMIN`
   * `ROLE_VENDOR_ADMIN`
   * `ROLE_CUSTOMER_ADMIN`

<!--<h3 id="getAllPaginatedUsingGET_4-internal_fiat_to_crypto">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[InternalRequest](#tocInternalRequest)|true|InternalRequest object|



<h3 id="poscreatenewpaymentrequest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[InternalResponse](#tocInternalResponse)|
|401|[Bad request](https://tools.ietf.org/html/rfc7235#section-3.1)|Bad request|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|

### Exchange rates

> Code samples

```shell
curl -X GET http://example.com/api/pos/exchange_rates -H Authorization: Bearer <token>
```

```php
<?php
$URL = "http://example.com/api/pos/exchange_rates";

$aHTTP['http']['method']  = 'GET';

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
  url: 'http://example.com/api/pos/exchange_rates',
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

result = RestClient.get 'http://example.com/api/pos/exchange_rates',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/pos/exchange_rates',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/pos/exchange_rates");
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


> Example responses

```json
{
   "100": {
       "ask": 330.65,
       "bid": 322.06
   },
   "500": {
       "ask": 336.67,
       "bid": 301.4
   },
   "2000": {
       "ask": 345.69,
       "bid": 249.5
   },
   "5000": {
       "ask": 366.36,
       "bid": 179.64
   },
   "10000": {
       "ask": 65130000,
       "bid": 99.8
   },
   "small": {
       "ask": 330.65,
       "bid": 322.06
   },
   "medium": {
       "ask": 335.14,
       "bid": 318.8
   },
   "large": {
       "ask": 338.41,
       "bid": 315.53
   },
   "vip": {
       "ask": 343.32,
       "bid": 310.62
   },
   "vip+": {
       "ask": 351.49,
       "bid": 302.45
   },
   "index": 326.97,
   "updatetime": 1505820460,
   "market": "USD_DASH"
}
```
<a id="opIdcoinapult-currency-exchange-rate"></a>

`GET /api/pos/exchange_rates`

*Get current market rate from Coinapult for DASH*

**Parameters**

`None`

**Required user role:**

   * `Available to all user roles`

**Responses**

Response result is passed-through from Coinapult and the system does not either store or processes it.

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[string] Received from Coinapult|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|


### POS

> Code samples

```shell
curl -X POST http://example.com/api/pos/payment \
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
    $URL = "http://example.com/api/pos/payment";
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
  url: 'http://example.com/api/pos/payment',
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

result = RestClient.post 'http://example.com/api/pos/payment',
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

r = requests.post('http://example.com/api/pos/payment',
                  data=<body_here>, params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/pos/payment");
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

<a id="opIdcreateNewPaymentRequestPOS_1"></a>

`POST /api/pos/payment`

*Create new payment request for POS. Endpoint expects the amount in FIAT and returns value converted to DASH along with destination/payment address.*

**Required authentication:**

   * Please use API key received by registering/activating POS
   * API key should be used in request header in following manner: `Authorization: Bearer API_KEY`
   * Please replace `API_KEY` with your own API key for POS

<!-- <h3 id="getAllPaginatedUsingGET_4-parameters">Parameters</h3> -->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[POSRequest](#schemaposrequest)|false|POSRequest object|


<h3 id="poscreatenewpaymentrequest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[POSResponse](#schemaposresponse)|
|401|[Bad request](https://tools.ietf.org/html/rfc7235#section-3.1)|Bad request|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|

### Virtual POS
> Code samples

```shell
curl -X POST http://example.com/api/pos/payment/vpos \
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
    $URL = "http://example.com/api/pos/payment/vpos";
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
  url: 'http://example.com/api/pos/payment/vpos',
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

result = RestClient.post 'http://example.com/api/pos/payment/vpos',
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

r = requests.post('http://example.com/api/pos/payment/vpos',
                  data=<body_here>, params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/pos/payment/vpos");
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

<!-- VIRTUAL POS SECTION-->

<a id="opIdcreateNewPaymentRequest_2"></a>

`POST /api/pos/payment/vpos`

*Create new payment request for virtual POS. Endpoint expects the amount in FIAT and returns value converted to DASH along with destination/payment address.*

**Required user role:**

   * `ROLE_MERCHANT_ADMIN`
   * `ROLE_MERCHANT_USER`

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[POSRequest](#schemaposrequest)|false|POSRequest object|


<h3 id="poscreatenewpaymentrequest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[POSResponse](#schemaposresponse)|
|401|[Bad request](https://tools.ietf.org/html/rfc7235#section-3.1)|Bad request|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
