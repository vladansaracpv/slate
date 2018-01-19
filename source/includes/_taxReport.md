### Tax Report

#### Tax report for associate

> Code samples

```shell
curl -X GET http://example.com/api/v1/analytics/reports/tax/<associate_id> -H Authorization: Bearer <token>'
```

```php
<?php
$URL = "http://example.com/api/v1/analytics/reports/tax/<associate_id>";

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
  url: 'http://example.com/api/v1/analytics/reports/tax/<associate_id>',
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

result = RestClient.get 'http://example.com/api/v1/analytics/reports/tax/<associate_id>',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Authorization': 'Bearer <token>'
}

r = requests.get('http://example.com/api/v1/analytics/reports/tax/<associate_id>',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/v1/analytics/reports/tax/<associate_id>");
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

<a id="opIdcreateTaxReport"></a>

`GET /api/v1/analytics/reports/tax/<associate_id>`

*Get tax report for your associate ID for a period of time.*

**Required user role:**

   * `Available to all user roles`

<!--<h3 id="opIdcreateDashboard_tax-report-parameters">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|associate_id|path|integer|true|Associate identifier for whom data is requested|
|timerange_from|query|string|true|start date/datetime in ISO format|
|timerange_to|query|string|true|end date/datetime in ISO format|

<h3 id="opIdcreateDashboard_tax-report-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[TaxReportResponse](#tocTaxReportResponse)|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|
