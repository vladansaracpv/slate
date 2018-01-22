### Sales Volume
Summary endpoints are used for sales summary information. These endpoints are user aware, so information is returned only  if specified rules are satisfied.

#### Associate Sales Volume

> Code samples

```shell
curl -X GET http://example.com/api/v1/analytics/salesvolume/associate/<associate_id> -H Authorization: Bearer <token>
```

```php
<?php
$URL = "http://example.com/api/v1/analytics/salesvolume/associate/<associate_id>";

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
  url: 'http://example.com/api/v1/analytics/salesvolume/associate/<associate_id>',
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

result = RestClient.get 'http://example.com/api/v1/analytics/salesvolume/associate/<associate_id>',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/v1/analytics/salesvolume/associate/<associate_id>',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/v1/analytics/salesvolume/associate/<associate_id>");
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

<a id="opIdcreate_merchant_sales_volume"></a>

`GET /api/v1/analytics/salesvolume/associate/<associate_id>`

*Get total sales volume for an associate.*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`

<!--<h3 id="getAllPaginatedUsingGET_4-merchant_sales_volume">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|associate_id|path|integer|false|Associate identifier for whom data is requested|

<h3 id="poscreatenewpaymentrequest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SalesVolume](#tocSalesVolume)|
|401|[Bad request](https://tools.ietf.org/html/rfc7235#section-3.1)|Bad request|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|

#### Location Sales Volume

> Code samples

```shell
curl -X GET http://example.com/api/v1/analytics/salesvolume/location/<location_id> -H Authorization: Bearer <token>
```

```php
<?php
$URL = "http://example.com/api/v1/analytics/salesvolume/location/<location_id>";

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
  url: 'http://example.com/api/v1/analytics/salesvolume/location/<location_id>',
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

result = RestClient.get 'http://example.com/api/v1/analytics/salesvolume/location/<location_id>',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/v1/analytics/salesvolume/location/<location_id>',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/v1/analytics/salesvolume/location/<location_id>");
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
"location_id": 2432,
"sales_crypto": 3.03869975,
"sales_fiat": 2213.7153887805002
}
```

`GET /api/v1/analytics/salesvolume/location/<location_id>`

*Get total sales volume for Location.*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`


<a id="opIdcreate_location_sales_volume"></a>

<!--<h3 id="getAllPaginatedUsingGET_4-location_sales_volume">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|location_id|path|integer|false|Location identifier for whom data is requested|

<h3 id="poscreatenewpaymentrequest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SalesVolume](#tocSalesVolume)|
|401|[Bad request](https://tools.ietf.org/html/rfc7235#section-3.1)|Bad request|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|


#### POS Sales Volume

> Code samples

```shell
curl -X GET http://example.com/api/v1/analytics/salesvolume/location/<location_id>/pos/<pos_id> -H Authorization: Bearer <token>
```

```php
<?php
$URL = "http://example.com/api/v1/analytics/salesvolume/location/<location_id>/pos/<pos_id>";

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
  url: 'http://example.com/api/v1/analytics/salesvolume/location/<location_id>/pos/<pos_id>',
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

result = RestClient.get 'http://example.com/api/v1/analytics/salesvolume/location/<location_id>/pos/<pos_id>',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/v1/analytics/salesvolume/location/<location_id>/pos/<pos_id>',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/v1/analytics/salesvolume/location/<location_id>/pos/<pos_id>");
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
"pos_id": -100,
"sales_crypto": 3.03869975,
"sales_fiat": 2213.7153887805002
}
```

<a id="opIdcreate_pos_sales_volume"></a>

`GET /api/v1/analytics/salesvolume/location/<location_id>/pos/<pos_id>`

*Get total sales volume for POS.*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`

<!--<h3 id="getAllPaginatedUsingGET_4-location_sales_volume">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|location_id|path|integer|false|Location identifier for whom data is requested|
|pos_id|path|integer|false|POS identifier for whom data is requested|

<h3 id="poscreatenewpaymentrequest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SalesVolume](#tocSalesVolume)|
|401|[Bad request](https://tools.ietf.org/html/rfc7235#section-3.1)|Bad request|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
