### Dashboard Performance
#### Merchant performance

<a id="opIdcreateDashboard_performance_role"></a>


> Code samples

```shell
curl -X GET http://example.com/api/v1/analytics/performance/merchant -H Authorization: Bearer <token>'
```

```php
<?php
$URL = "http://example.com/api/v1/analytics/performance/merchant";

$aHTTP['http']['method']  = 'GET';

$aHTTP['http']['header']  = "Bearer <token>";

$context = stream_context_create($aHTTP);

$response = file_get_contents($URL, false, $context);
?>

```

```javascript
var headers = {
  'Authorization':'Bearer <token>'
};

$.ajax({
  url: 'http://example.com/api/v1/analytics/performance/merchant',
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

result = RestClient.get 'http://example.com/api/v1/analytics/performance/merchant',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/v1/analytics/performance/merchant',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/v1/analytics/performance/merchant");
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

`GET /api/v1/analytics/performance/merchant`

*Returns top 5 merchants in the system.*

**Required user role:**

   * `ROLE_PARTNER_ADMIN`
   * `ROLE_PARTNER_USER`

<!--<h3 id="opIdcreateDashboard_performance_location-parameters">Parameters</h3>-->

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

#### Location performance

> Code samples

```shell
curl -X GET http://example.com/api/v1/analytics/performance/location -H Authorization: Bearer <token>'
```

```php
<?php
$URL = "http://example.com/api/v1/analytics/performance/location";

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
  url: 'http://example.com/api/v1/analytics/performance/location',
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

result = RestClient.get 'http://example.com/api/v1/analytics/performance/location',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/v1/analytics/performance/location',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/v1/analytics/performance/location");
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

<a id="opIdcreateDashboard_performance_location"></a>

`GET /api/v1/analytics/performance/location`

*Returns top 5 locations in the system.*

**Required user role:**

   * `ROLE_PARTNER_ADMIN`
   * `ROLE_PARTNER_USER`
   * `ROLE_MERCHANT_ADMIN`
   * `ROLE_MERCHANT_USER`

<!--<h3 id="opIdcreateDashboard_performance_location-parameters">Parameters</h3>-->

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
