

#### Get all states


<a id="opIdgetAllCountryStatesUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/common/states/us \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/common/states/us HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/common/states/us',
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


fetch('http://example.com/api/common/states/us',
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


result = RestClient.get 'http://example.com/api/common/states/us',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/common/states/us', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/common/states/us");
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


`GET /api/common/states/us`


*Get USA states list*


> Example responses

```
[
   {
      "id":1,
      "state":"Alabama",
      "abbreviation":"AL"
   },
   {
      "id":2,
      "state":"Alaska",
      "abbreviation":"AK"
   },
   {
      "id":3,
      "state":"Arizona",
      "abbreviation":"AZ"
   },
   {
      "id":4,
      "state":"Arkansas",
      "abbreviation":"AR"
   },
   {
      "id":5,
      "state":"California",
      "abbreviation":"CA"
   },
   {
      "id":6,
      "state":"Colorado",
      "abbreviation":"CO"
   },
   {
      "id":7,
      "state":"Connecticut",
      "abbreviation":"CT"
   },
   {
      "id":8,
      "state":"Delaware",
      "abbreviation":"DE"
   },
   {
      "id":9,
      "state":"District of Columbia",
      "abbreviation":"DC"
   },
   {
      "id":10,
      "state":"Florida",
      "abbreviation":"FL"
   },
   {
      "id":11,
      "state":"Georgia",
      "abbreviation":"GA"
   },
   {
      "id":12,
      "state":"Hawaii",
      "abbreviation":"HI"
   },
   {
      "id":13,
      "state":"Idaho",
      "abbreviation":"ID"
   },
   {
      "id":14,
      "state":"Illinois",
      "abbreviation":"IL"
   },
   {
      "id":15,
      "state":"Indiana",
      "abbreviation":"IN"
   },
   {
      "id":16,
      "state":"Iowa",
      "abbreviation":"IA"
   },
   {
      "id":17,
      "state":"Kansas",
      "abbreviation":"KS"
   },
   {
      "id":18,
      "state":"Kentucky",
      "abbreviation":"KY"
   },
   {
      "id":19,
      "state":"Louisiana",
      "abbreviation":"LA"
   },
   {
      "id":20,
      "state":"Maine",
      "abbreviation":"ME"
   },
   {
      "id":21,
      "state":"Montana",
      "abbreviation":"MT"
   },
   {
      "id":22,
      "state":"Nebraska",
      "abbreviation":"NE"
   },
   {
      "id":23,
      "state":"Nevada",
      "abbreviation":"NV"
   },
   {
      "id":24,
      "state":"New Hampshire",
      "abbreviation":"NH"
   },
   {
      "id":25,
      "state":"New Jersey",
      "abbreviation":"NJ"
   },
   {
      "id":26,
      "state":"New Mexico",
      "abbreviation":"NM"
   },
   {
      "id":27,
      "state":"New York",
      "abbreviation":"NY"
   },
   {
      "id":28,
      "state":"North Carolina",
      "abbreviation":"NC"
   },
   {
      "id":29,
      "state":"North Dakota",
      "abbreviation":"ND"
   },
   {
      "id":30,
      "state":"Ohio",
      "abbreviation":"OH"
   },
   {
      "id":31,
      "state":"Oklahoma",
      "abbreviation":"OK"
   },
   {
      "id":32,
      "state":"Oregon",
      "abbreviation":"OR"
   },
   {
      "id":33,
      "state":"Maryland",
      "abbreviation":"MD"
   },
   {
      "id":34,
      "state":"Massachusetts",
      "abbreviation":"MA"
   },
   {
      "id":35,
      "state":"Michigan",
      "abbreviation":"MI"
   },
   {
      "id":36,
      "state":"Minnesota",
      "abbreviation":"MN"
   },
   {
      "id":37,
      "state":"Mississippi",
      "abbreviation":"MS"
   },
   {
      "id":38,
      "state":"Missouri",
      "abbreviation":"MO"
   },
   {
      "id":39,
      "state":"Pennsylvania",
      "abbreviation":"PA"
   },
   {
      "id":40,
      "state":"Rhode Island",
      "abbreviation":"RI"
   },
   {
      "id":41,
      "state":"South Carolina",
      "abbreviation":"SC"
   },
   {
      "id":42,
      "state":"South Dakota",
      "abbreviation":"SD"
   },
   {
      "id":43,
      "state":"Tennessee",
      "abbreviation":"TN"
   },
   {
      "id":44,
      "state":"Texas",
      "abbreviation":"TX"
   },
   {
      "id":45,
      "state":"Utah",
      "abbreviation":"UT"
   },
   {
      "id":46,
      "state":"Vermont",
      "abbreviation":"VT"
   },
   {
      "id":47,
      "state":"Virginia",
      "abbreviation":"VA"
   },
   {
      "id":48,
      "state":"Washington",
      "abbreviation":"WA"
   },
   {
      "id":49,
      "state":"West Virginia",
      "abbreviation":"WV"
   },
   {
      "id":50,
      "state":"Wisconsin",
      "abbreviation":"WI"
   },
   {
      "id":51,
      "state":"Wyoming",
      "abbreviation":"WY"
   }
]
```


<h3 id="getAllCountryStatesUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<h3 id="getAllCountryStatesUsingGET-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[CountryStateDTO](#schemacountrystatedto)]|false|No description|
|» abbreviation|string|false|No description|
|» id|integer(int64)|false|No description|
|» state|string|false|No description|


#### Get file by uuid

##### HTTP Request

`GET /api/get/file/{uuid}`


### Parameters

Parameter | In | Type | Required | Description
--- | --- | --- | --- |---
uuid | path | string | true | uuid

### Responses

Code | Type | Description
--- | --- | ---
200 |  | OK
401 |  | Unauthorized
403 |  | Forbidden
404 |  | Not Found



#### Get all invitations


<a id="opIdgetAllInvitationsUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/invitations \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/invitations HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/invitations',
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


fetch('http://example.com/api/invitations',
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


result = RestClient.get 'http://example.com/api/invitations',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/invitations', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/invitations");
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


`GET /api/invitations`


*Get all invitations sent by current Associate*


<h3 id="getAllInvitationsUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses


<h3 id="getAllInvitationsUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfInvitation](#schemapageofinvitation)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
</aside>




## Payments
Payments service endpoints are central endpoints of Product36. Endpoints enable clients to get balance information, as well as to intiate payment process for two supported types of POS devices. Published interfaces include getting the information about user account, as well as payment capabilities - converting FIAT amount to cryptocurrency and getting the destination address. It is important to note that in background this is a multistep process and it is not as simple as getting the destination address from hot wallet. So there are firm security and business rules that have to be obeyed in order to complete any of these processes.
At the end, there is a notification process that can be used for getting events from within the system.
The base URL for Production environment is:

* https://paymentgateway-dot-altthirtysixproduct36.appspot.com 

The base URL for Sandbox environment is:

* https://paymentgateway-dot-sandboxaltthirtysixproduct36.appspot.com

### List of bank account
### Fiat cash out
### Send to Internal wallet
### Send to External wallet
### Convert
### Buy
### Exchange rates
### POS
#### Create new payment request

<a id="opIdcreateNewPaymentRequestPOS_1"></a>


`POST /api/pos/payment`

*Create new payment request for POS.*

Endpoint sends the amount in FIAT and gets value converted to dash along with destination address.

<h3 id="getAllPaginatedUsingGET_4-parameters">Parameters</h3>

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

#### Create new payment request virtual POS

Endpoint sends the amount in FIAT and gets value converted to dash along with destination address.

<a id="opIdcreateNewPaymentRequest_2"></a>


`POST /api/pos/payment/vpos`

*Create new payment request for virtual POS.*

<h3 id="getAllPaginatedUsingGET_4-parameters">Parameters</h3>

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

## Notifications
Notification service uses EventSource capability of HTTP protocol. That is a variant of standard GET request, but conformed to long pulling use case. The notification service is used to get notifications on transaction status updates. The notification is provided for PoS related transactions and transactions of DASH digital currency to an external or internal wallet.
The base URL for Production environment is:

* https:/notifier-dot-altthirtysixproduct36.appspot.com 

The base URL for Sandbox environment is:

* https://notifier-dot-sandboxaltthirtysixproduct36.appspot.com

### Payment Notification

## Reporting
Reporting subsystem is a comprehensive list of endpoints that are used for getting various statistic information about user performance, and accounting. 
The base URL for Production environment is:

* https:/reporting-dot-altthirtysixproduct36.appspot.com 

The base URL for Sandbox environment is:

* https://reporting-dot-sandboxaltthirtysixproduct36.appspot.com

**Important notice:** There is a uniform date format which is used for time bound results. Generally, all ISO formats can be used. Nevertheless, following format is commonly used on the platform:

* *epoch_second* - A formatter for the number of seconds since the epoch
* *date or strict_date* - A formatter for a full date as four digit year, two digit month of year, and two digit day of month: yyyy-MM-dd.
* *date_hour_minute_second or strict_date_hour_minute_second* - full date, two digit hour of day, two digit minute of hour, and two digit second of minute: yyyy-MM-dd'T'HH:mm:ss. 
* *date_hour_minute_second_fraction* or strict_date_hour_minute_second_fraction 
* A formatter that combines a full date, two digit hour of day, two digit minute of hour, two digit second of minute, and three digit fraction of second: yyyy-MM-dd'T'HH:mm:ss.SSS

In the case of datetime ranges, if one uses date or strict_date format, it is considered by the system that the range is from 00:00.00 hour of the start date to 00:00.00 to the end date.

If the response contains cryptocurrency value, it always comes with FIAT value pair, so there is no need for conversion on client side. This considerably reduces the processing amount needed on client side, as client uses the data directly without need for further calculations.

All messages have two parts - metadata part which contain general information of data (such as current page number, number of elements per page, total number of elements etc), summary part (not provided for all report types) which contains summary information and page of data itself. This format reduces the need for clients to make excessive number of calls to the server. 

Note that all information is contextualized - related only to user that asks for informations. As the system is heavily relied on roles, every request needs proper JWT token embedded in Authorization Bearer header field in order to work.

### Dashboard Summary

Dashboard summary data

<h4 id="proba">General system summary data</h4>

<a id="opIdcreateDashboard_general"></a>

`GET /api/v1/analytics/summary/general`

*Get general system summary data.*

This is info on system wide values of appropriate variables related to a given user. Information about user is read from request jwt token.

<h3 id="opIdcreateDashboard_general_summary-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|timerange_from|query|string|true|start date/datetime in ISO format|
|timerange_to|query|string|true|end date/datetime in ISO format|


<h3 id="opIdcreateDashboard_general_summary-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[GeneralSummaryResponse](#schemageneralsummaryresponse)|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|

> Example responses

```json
{
  "timerange_from": "2017-11-01T00:00:00.0Z",
  "timerange_to": "2018-01-11T23:59:59.1Z",
  "number_of_sales": 84,
  "avg_tx_amount": 0.12657074607143,
  "avg_tx_amount_fiat": 88.72505512713,
  "total_sales": 10.63194267,
  "total_sales_fiat": 7452.9046306789,
  "total_commission_fee_charged": 0.85386515,
  "total_commission_fee_charged_fiat": 602.6705777301
}
```

### Dashboard performance 
#### Location performance

<a id="opIdcreateDashboard_performance_location"></a>

`GET /api/v1/analytics/performance/location`

*Returns top 5 locations in the system.*

<h3 id="opIdcreateDashboard_performance_location-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|currency|query|string|false|which currency result should respond (currently ignored)|
|timerange_from|query|string|true|start date/datetime in ISO format|
|timerange_to|query|string|true|end date/datetime in ISO format|
|page_number|integer|string|true| represents requested page number (currently ignored)|


<h3 id="opIdcreateDashboard_performance_location--responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[LocationPerformanceResponse](#tocLocationPerformanceResponse)|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|

>Example responses

```json
{
  "metadata":{
      "timerangeFrom": "2017-09-01T00:00:00.0Z",
      "timerangeTo": "2018-01-15T23:59:59.1Z",
      "number": 0,
      "size": 2,
      "numberOfElements": 531,
      "totalPages": 54,
      "first": true,
      "last": false
    },
  "data":[
    {
      "location_id": 2432,
      "location_name": "Phoenician",
      "location_address": "6000 E Camelback Rd",
      "item_sales_crypto": 3.03869975,
      "item_sales_fiat": 2213.7153887805,
      "associate_owner": "Demo Merchant",
      "associate_owner_id": 2102
    },
    {
      "location_id": 743,
      "location_name": "Peoria",
      "location_address": "29701 N Sunrise Point",
      "item_sales_crypto": 1.41153177,
      "item_sales_fiat": 936.622608258,
      "associate_owner": "Demo Merchant",
      "associate_owner_id": 2102
    },
    {
      "location_id": 303,
      "location_name": "Phoenix",
      "location_address": "340 N 3rd St",
      "item_sales_crypto": 1.26886494,
      "item_sales_fiat": 767.8435600896,
      "associate_owner": "Demo Merchant",
      "associate_owner_id": 2102
    },
    {
      "location_id": 2427,
      "location_name": "ByMerchant",
      "location_address": "N 7th St",
      "item_sales_crypto": 1.05366415,
      "item_sales_fiat": 720.2720775932,
      "associate_owner": "Demo Merchant",
      "associate_owner_id": 2102
    },
    {
      "location_id": 744,
      "location_name": "Oakland",
      "location_address": "1411 E 31st St",
      "item_sales_crypto": 1.02292684,
      "item_sales_fiat": 690.7045676177,
      "associate_owner": "Demo Merchant",
      "associate_owner_id": 2102
    }
  ]
}
```

####Merchant performance

<a id="opIdcreateDashboard_performance_role"></a>

`GET /api/v1/analytics/performance/merchant`

*Returns top 5 merchants in the system.*

<h3 id="opIdcreateDashboard_performance_location-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|currency|query|string|false|which currency result should respond (currently ignored)|
|timerange_from|query|string|true|start date/datetime in ISO format|
|timerange_to|query|string|true|end date/datetime in ISO format|
|page_number|integer|string|true| represents requested page number (currently ignored)|


<h3 id="opIdcreateDashboard_performance_merchant-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SalesSummaryResponse](#tocSalesSummaryResponse)|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|

>Example responses

```json
{
  "metadata":{
      "timerangeFrom": "2017-09-01T00:00:00.0Z",
      "timerangeTo": "2018-01-15T23:59:59.1Z",
      "number": 0,
      "size": 2,
      "numberOfElements": 531,
      "totalPages": 54,
      "first": true,
      "last": false
    },
  "data":[
    {
      "item_id": 2432,
      "item_name": "Merchant Phoenix",
      "item_sales_crypto": 3.03869975,
      "item_sales_fiat": 2213.7153887805,
      "pos_count": 12
    },
    {
      "item_id": 743,
      "item_name": "Red hat",
      "item_sales_crypto": 1.41153177,
      "item_sales_fiat": 936.622608258,
      "pos_count": 23
    },
    {
      "item_id": 303,
      "item_name": "Merlin",
      "item_sales_crypto": 1.26886494,
      "item_sales_fiat": 767.8435600896,
      "pos_count": 42
    },
    {
      "item_id": 2427,
      "item_name": "Luna",
      "item_sales_crypto": 1.05366415,
      "item_sales_fiat": 720.2720775932,
      "pos_count": 11
    },
    {
      "item_id": 744,
      "item_name": "Venus",
      "item_sales_crypto": 1.02292684,
      "item_sales_fiat": 690.7045676177,
      "pos_count": 35
    }
  ]

}

```

### Sales Summary
#### Total sales by timerange

<a id="opIdcreateDashboard_total_sales_by_timerange"></a>

`GET /api/v1/analytics/summary/sales`

*Total sales by time-range which is further divided on one hour interval. Note that the time intervals are rounded in hours. All values within hour intervals are aggregated. *

<h3 id="opIdcreateDashboard_total_sales_by_timerange-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|currency|query|string|false|which currency result should respond (currently ignored)|
|timerange_from|query|string|true|start date/datetime in ISO format|
|timerange_to|query|string|true|end date/datetime in ISO format|
|page_number|integer|string|true| represents requested page number (currently ignored)|


<h3 id="opIdcreateDashboard_performance_merchant-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RolePerformanceResponse](#tocRolePerformanceResponse)|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|

> Example responses

```json
{
  "metadata":{
      "timerangeFrom": "2017-09-01T00:00:00.0Z",
      "timerangeTo": "2018-01-15T23:59:59.1Z",
      "number": 0,
      "size": 2,
      "numberOfElements": 531,
      "totalPages": 54,
      "first": true,
      "last": false
    },
  "data":[
          {
              "total_amount_of_sales": 0,
              "total_amount_of_sales_fiat":0,
              "time_from": "2017-10-12T13:00:00.000Z",
              "time_to": "2017-10-12T14:00:00.000Z"
          },
          {
              "total_amount_of_sales": 0.01242642,
              "total_amount_of_sales_fiat":24.23,
              "time_from": "2017-10-12T14:00:00.000Z",
              "time_to": "2017-10-12T15:00:00.000Z"
          }
    ]
}
```


#### General
#### Sales
#### Tax

### Sales Summary
#### Associate
#### Location
#### POS
### Reports Merchant
#### Merchant
#### Merchant’s locations
#### POS for Merchant’s locations
### Reports Locations
#### Location
#### POS for Locations
### Reports Point of sale
Point of sale Resource

### Reports Tax

Tax report for period of time

#### Tax report for associate

<a id="opIdcreateTaxReport"></a>

`GET /api/v1/analytics/reports/tax/{associateId}`

<h3 id="opIdcreateDashboard_tax-report-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|timerange_from|query|string|true|start date/datetime in ISO format|
|timerange_to|query|string|true|end date/datetime in ISO format|

<h3 id="opIdcreateDashboard_tax-report-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[TaxReportResponse](#tocTaxReportResponse)|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|

> Example responses

```json
{
    "metadata": {
        "timerangeFrom": "2017-11-11T00:00:00.000Z",
        "timerangeTo": "2017-11-11T23:00:00.000Z"
    },
    "content": {
        "totalTax":  256.23,
        "totalAmountReceived": 0.00223456,
        "totalAmountReceivedFiat": 25.36,
        "totalAmountSent": 0.001232,
        "totalAmountSentFiat": 15.25,
        "totalFee": 0.00012356,
        "totalFeeFiat": 1.0012356,
        "totalNumTxSpent": 52,
        "totalNumTxReceived": 23,
    }
}
```

# Support
In case you have any integration related questions, please contact us at [support@alt36.com](mailto:support@alt36.com). In order to expedite and facilitate the troubleshooting process, please provide us with any relevant information such as your username on the platform, code samples, exact API calls, returned response from our API, error messages, API call date and time, etc.


