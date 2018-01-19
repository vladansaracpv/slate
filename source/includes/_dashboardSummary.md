
### Dashboard Summary

#### General summary data

> Code samples

```shell
curl -X GET http://example.com/api/v1/analytics/summary/general -H Authorization: Bearer <token>'
```

```php
<?php
$URL = "http://example.com/api/v1/analytics/summary/general";

$aHTTP['http']['method']  = 'GET';

$aHTTP['http']['header']  = "Authorization: YOUR_API_KEY_HERE";

$context = stream_context_create($aHTTP);

$response = file_get_contents($URL, false, $context);
?>

```

```javascript
var headers = {
  'Authorization':'Bearer <token>'
};

$.ajax({
  url: 'http://example.com/api/v1/analytics/summary/general',
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

result = RestClient.get 'http://example.com/api/v1/analytics/summary/general',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/v1/analytics/summary/general',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/v1/analytics/summary/general");
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


<a id="opIdcreateDashboard_general"></a>

`GET /api/v1/analytics/summary/general`

*Get general system summary data. This is info on system wide values of appropriate variables related to a given user. Information about user is read from request JWT token.*

**Required user role:**

   * `Available to all user roles`

<!--<h3 id="opIdcreateDashboard_general_summary-parameters">Parameters</h3>-->

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

#### General sales summary

> Code samples

```shell
curl -X GET http://example.com/api/v1/analytics/summary/sales -H Authorization: Bearer <token>'
```

```php
<?php
$URL = "http://example.com/api/v1/analytics/summary/sales";

$aHTTP['http']['method']  = 'GET';

$aHTTP['http']['header']  = "Authorization: YOUR_API_KEY_HERE";

$context = stream_context_create($aHTTP);

$response = file_get_contents($URL, false, $context);
?>

```

```javascript
var headers = {
  'Authorization':'Bearer <token>'
};

$.ajax({
  url: 'http://example.com/api/v1/analytics/summary/sales',
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

result = RestClient.get 'http://example.com/api/v1/analytics/summary/sales',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/v1/analytics/summary/sales',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/v1/analytics/summary/sales");
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

<a id="opIdcreateDashboard_total_sales_by_timerange"></a>

`GET /api/v1/analytics/summary/sales`

*Total sales by time-range which is further divided on one hour interval. Note that the time intervals are rounded in hours. All values within hour intervals are aggregated.*

**Required user role:**

   * `ROLE_PARTNER_ADMIN`
   * `ROLE_PARTNER_USER`
   * `ROLE_MERCHANT_ADMIN`
   * `ROLE_MERCHANT_USER`

<!--<h3 id="opIdcreateDashboard_total_sales_by_timerange-parameters">Parameters</h3>-->

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


#### General tax summary

> Code samples

```shell
curl -X GET http://example.com/api/v1/analytics/summary/tax -H Authorization: Bearer <token>'
```

```php
<?php
$URL = "http://example.com/api/v1/analytics/summary/tax";

$aHTTP['http']['method']  = 'GET';

$aHTTP['http']['header']  = "Authorization: YOUR_API_KEY_HERE";

$context = stream_context_create($aHTTP);

$response = file_get_contents($URL, false, $context);
?>

```

```javascript
var headers = {
  'Authorization':'Bearer <token>'
};

$.ajax({
  url: 'http://example.com/api/v1/analytics/summary/tax',
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

result = RestClient.get 'http://example.com/api/v1/analytics/summary/tax',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/v1/analytics/summary/tax',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/v1/analytics/summary/tax");
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
              "total_amount_of_tax": 1.22334,
              "total_amount_of_tax_fiat":564.25,
              "time_from": "2017-10-12T00:00:00.000Z",
              "time_to": "2017-10-13T00:00:00.000Z"
          },
          {
              "total_amount_of_tax": 0.99210921,
              "total_amount_of_tax_fiat":458.25,
              "time_from": "2017-10-13T00:00:00.000Z",
              "time_to": "2017-10-14T00:00:00.000Z"
          }
    ]
}
```

<a id="opIdcreateDashboard_total_tax_by_timerange"></a>

`GET /api/v1/analytics/summary/tax`

*Total tax by time-range which is further divided on one day interval. Note that the time intervals are rounded in days. All values within day intervals are aggregated.*

**Required user role:**

   * `Available to all user roles`

<!--<h3 id="opIdcreateDashboard_total_tax_by_timerange-parameters">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|currency|query|string|false|which currency result should respond (currently ignored)|
|timerange_from|query|string|true|start date/datetime in ISO format|
|timerange_to|query|string|true|end date/datetime in ISO format|
|page_number|integer|string|true| represents requested page number (currently ignored)|


<h3 id="opIdcreateDashboard_performance_merchant-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[TaxSummaryResponse](#tocTaxSummaryResponse)|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|
