
## Payments
Payments service endpoints are central endpoints of Product36. Endpoints enable clients to get balance information, as well as to initiate payment process for two supported types of POS devices. Published interfaces include getting the information about user account, as well as payment capabilities - converting FIAT amount to cryptocurrency and getting the destination address. It is important to note that in background this is a multistep process and it is not as simple as getting the destination address from hot wallet. So there are firm security and business rules that have to be obeyed in order to complete any of these processes.
At the end, there is a notification process that can be used for getting events from within the system.
The base URL for Production environment is:

* `https://paymentgateway-dot-altthirtysixproduct36.appspot.com`

The base URL for Sandbox environment is:

* `https://paymentgateway-dot-sandboxaltthirtysixproduct36.appspot.com`

### Wallet balance

<a id="opIdcoinapult-account-info"></a>

`GET /api/account/cpaccountinfo`

**Required user role:**

  * `Available to all user roles`

<!--<h3 id="opCoinapult_API_coinapult-account">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|associateId|query|string|true|Internal associate id|
|currency|query|string|false|Currency short string (DASH for example). Currently ignored

<h3 id="opIdcreateDashboard_tax-coinapult-account">Responses</h3>

Response result is passed-through from coinapult and the system does not either store or processes it.

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[string])|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|

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

### Send DASH to Internal wallet

Internal transfer of cryptocirrency between coinapult accounts.

<a id="opIdcreate_intenal_crypto_2_internal_crypto"></a>

`POST /api/transfer/internal_crypto/2/internal_crypto`

*Create new internal payment request.*

**Required user role:**

   * `ROLE_PARTNER_ADMIN`
   * `ROLE_MERCHANT_ADMIN`
   * `ROLE_VENDOR_ADMIN`
   * `ROLE_CUSTOMER_ADMIN`

<!--<h3 id="getAllPaginatedUsingGET_4-parameters">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[InternalRequest](#tocInternalRequest)|false|InternalRequest object|

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
<h3 id="poscreatenewpaymentrequest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[InternalResponce](#tocInternalResponse)|
|401|[Bad request](https://tools.ietf.org/html/rfc7235#section-3.1)|Bad request|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|

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

### Send DASH to External wallet

Internal transfer of cryptocurrency from coinapult account to an external wallet

<a id="opIdcreate_intenal_crypto_2_external_crypto"></a>

`POST /api/transfer/internal_crypto/2/external_crypto`

*Create new internal payment request.*

**Required user role:**

   * `ROLE_PARTNER_ADMIN`
   * `ROLE_MERCHANT_ADMIN`
   * `ROLE_VENDOR_ADMIN`
   * `ROLE_CUSTOMER_ADMIN`

<!--<h3 id="getAllPaginatedUsingGET_4-internal_crypto_to_extenal_crypto">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[InternalRequest](#tocInternalRequest)|false|InternalRequest object|

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
<h3 id="poscreatenewpaymentrequest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[InternalResponce](#tocInternalResponse)|
|401|[Bad request](https://tools.ietf.org/html/rfc7235#section-3.1)|Bad request|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|



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

### Convert DASH

Internal transfer from cryptocurrency to fiat (internal)

<a id="opIdcreate_intenal_crypto_2_fiat"></a>

`POST /api/convert/crypto/2/fiat`

*Internal conversion from cryptocurrency to fiat*

**Required user role:**

   * `ROLE_PARTNER_ADMIN`
   * `ROLE_MERCHANT_ADMIN`
   * `ROLE_VENDOR_ADMIN`
   * `ROLE_CUSTOMER_ADMIN`

<!--<h3 id="getAllPaginatedUsingGET_4-internal_crypto_to_fiat">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[InternalRequest](#tocInternalRequest)|false|InternalRequest object|

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
<h3 id="poscreatenewpaymentrequest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[InternalResponce](#tocInternalResponse)|
|401|[Bad request](https://tools.ietf.org/html/rfc7235#section-3.1)|Bad request|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|



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

### Buy DASH

Internal transfer from fiat to cryptocurrency

<a id="opIdcreate_fiat_to_crypto"></a>

`POST /api/convert/fiat/2/crypto`

*Internal conversion from fiat to cryptocurrency*

**Required user role:**

   * `ROLE_PARTNER_ADMIN`
   * `ROLE_MERCHANT_ADMIN`
   * `ROLE_VENDOR_ADMIN`
   * `ROLE_CUSTOMER_ADMIN`

<!--<h3 id="getAllPaginatedUsingGET_4-internal_fiat_to_crypto">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[InternalRequest](#tocInternalRequest)|false|InternalRequest object|

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
<h3 id="poscreatenewpaymentrequest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[InternalResponce](#tocInternalResponse)|
|401|[Bad request](https://tools.ietf.org/html/rfc7235#section-3.1)|Bad request|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|

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

### List bank accounts

**Required user role:**

   * `Available to all user roles`

### FIAT cash out

Internal transfer from internal fiat to external fiat

<a id="opIdcreate_fiat_to_external_fiat"></a>

`POST /api/transfer/internalfiat/2/externalfiat`

*Internal conversion from internal fiat to external fiat*

**Required user role:**

   * `ROLE_PARTNER_ADMIN`
   * `ROLE_MERCHANT_ADMIN`
   * `ROLE_VENDOR_ADMIN`
   * `ROLE_CUSTOMER_ADMIN`

<!--<h3 id="getAllPaginatedUsingGET_4-internal_fiat_to_crypto">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[InternalRequest](#tocInternalRequest)|false|InternalRequest object|

>Body parameter

```json
{
    "type": "INTERNAL_FIAT_TO_EXTERNAL_FIAT",
    "timestamp_req":"1506895789",
    "bank_account": "9000000000",
    "amount":  1,
    "currency_out": "USD",
    "note":"Some transaction note string"
}

```
<h3 id="poscreatenewpaymentrequest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[InternalResponce](#tocInternalResponse)|
|401|[Bad request](https://tools.ietf.org/html/rfc7235#section-3.1)|Bad request|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|



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

### Exchange rates

<a id="opIdcoinapult-currency-exchange-rate"></a>

`/api/pos/exchange_rates`

**Parameters**

`None`

**Required user role:**

   * `Available to all user roles`

**Responses**

Response result is passed-through from Coinapult and the system does not either store or processes it.

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[string])|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|

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

### POS
<a id="opIdcreateNewPaymentRequestPOS_1"></a>

`POST /api/pos/payment`

*Create new payment request for POS.*

Endpoint sends the amount in FIAT and gets value converted to dash along with destination address.

**Required authentication:**

   * `Please use API key received by registering POS`

<!-- <h3 id="getAllPaginatedUsingGET_4-parameters">Parameters</h3> -->

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

Endpoint sends the amount in FIAT and gets value converted to dash along with destination address.

<a id="opIdcreateNewPaymentRequest_2"></a>


`POST /api/pos/payment/vpos`

*Create new payment request for virtual POS.*

**Required user role:**

   * `ROLE_MERCHANT_ADMIN`
   * `ROLE_MERCHANT_USER`

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
