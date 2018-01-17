### Common API

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

**Required user role:**

 * `No authentication is required`

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

**Required user role:**

 * `Available to all user roles`

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

**Required user role:**

 * `No authentication is required`

<!--
<h3 id="getAllInvitationsUsingGET-parameters">Parameters</h3>
-->

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
