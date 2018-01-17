
## Payments
Payments service endpoints are central endpoints of Product36. Endpoints enable clients to get balance information, as well as to intiate payment process for two supported types of POS devices. Published interfaces include getting the information about user account, as well as payment capabilities - converting FIAT amount to cryptocurrency and getting the destination address. It is important to note that in background this is a multistep process and it is not as simple as getting the destination address from hot wallet. So there are firm security and business rules that have to be obeyed in order to complete any of these processes.
At the end, there is a notification process that can be used for getting events from within the system.
The base URL for Production environment is:

* https://paymentgateway-dot-altthirtysixproduct36.appspot.com

The base URL for Sandbox environment is:

* https://paymentgateway-dot-sandboxaltthirtysixproduct36.appspot.com

### List bank accounts
### FIAT cash out
### Send DASH to Internal wallet
### Send DASH to External wallet
### Convert DASH
### Buy DASH
### Exchange rates
### POS
<a id="opIdcreateNewPaymentRequestPOS_1"></a>


`POST /api/pos/payment`

*Create new payment request for POS.*

Endpoint sends the amount in FIAT and gets value converted to dash along with destination address.

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

<!--<h3 id="getAllPaginatedUsingGET_4-parameters">Parameters</h3> -->
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
