
<h3 id="Alt36Dash-API-Merchant-locations">Manage Locations</h3>

Location Resource

#### Get all Locations paginated

<a id="opIdgetAllLocationsUsingGET_1"></a>

> Code samples

```shell
curl -X GET http://example.com/api/locations -H 'Accept: */*'
```

```http
GET http://example.com/api/locations HTTP/1.1
Host: null
Accept: */*
```

```javascript
var headers = {
  'Accept':'*/*'
};

$.ajax({
  url: 'http://example.com/api/locations',
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

fetch('http://example.com/api/locations',
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

result = RestClient.get 'http://example.com/api/locations',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Accept': '*/*'
}

r = requests.get('http://example.com/api/locations',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/locations");
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

`GET /api/locations`

*Get all the locations paginated*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`

<!-- <h3 id="getAllLocationsUsingGET_1-parameters">Parameters</h3> -->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|merchantId|query|integer(int64)|false|merchantId|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc/desc). Default sort order is ascending. Multiple sort criteria are supported.|

> Example responses

```json
{  
   "content":[  
      {  
         "id":303,
         "name":"Phoenix",
         "address":"340 N 3rd St",
         "deletedDate":null,
         "address2":null,
         "city":"Phoenix",
         "file":null,
         "zip":"85004",
         "state":{  
            "id":3,
            "state":"Arizona",
            "abbreviation":"AZ"
         },
         "country":"Alabama",
         "emailAddress":null,
         "phone":"0640272551",
         "note":null,
         "website":"http://www.vizlore.com",
         "geoLocation":"33.4522379,-112.0705419",
         "pointOfSales":[  
            {  
               "id":707,
               "pointOfSaleType":"OTHER",
               "virtualPointOfSalesEnabled":false,
               "active":true,
               "deletedDate":null,
               "inventoryNumber":"POS 5",
               "note":null,
               "name":"POS 5"
            }
         ],
         "parentLocation":null,
         "associate":{  
            "id":2102,
            "enabled":true,
            "canEditOnboarded":false,
            "associateType":"MERCHANT",
            "legalBusinessName":"Demo Merchant",
            "emailAddress":"merchant_AA_1855@021.com",
            "address":"Merchant Address 1855",
            "city":"Novi Sad",
            "zip":"21000",
            "state":{  
               "id":1,
               "state":"Alabama",
               "abbreviation":"AL"
            },
            "phone":"064 5566777",
            "companyEIN":"00-55555",
            "incorporationDate":"2017-09-19",
            "companyWebsite":"http://www.55dsl.com/",
            "beneficiaryPercent":null,
            "commissionFee":0.10,
            "internalFee":0.03,
            "coinaPultApiKey":null,
            "cryptoCapitalApiKey":null,
            "usBankAccount":null,
            "note":null,
            "createdDate":"2017-09-20T10:03:04Z",
            "deletedDate":null,
            "autosell":false,
            "altAutosellInternal":false,
            "partners":0,
            "vendors":31,
            "merchants":0,
            "customers":511,
            "locationsCount":49,
            "posCount":5,
            "enrolledBy":{  
               "id":2054,
               "enabled":true,
               "canEditOnboarded":false,
               "associateType":"PARTNER",
               "legalBusinessName":"Demo Partner",
               "emailAddress":"partner_AA_24306@021.com",
               "address":"Partner Address 24306",
               "city":"Novi Sad",
               "zip":"21000",
               "state":{  
                  "id":1,
                  "state":"Alabama",
                  "abbreviation":"AL"
               },
               "phone":"064 5566776",
               "companyEIN":"00-55555",
               "incorporationDate":"2017-09-03",
               "companyWebsite":"http://www.55dsl.com/",
               "beneficiaryPercent":null,
               "commissionFee":0.10,
               "internalFee":0.03,
               "coinaPultApiKey":null,
               "cryptoCapitalApiKey":null,
               "usBankAccount":null,
               "note":null,
               "createdDate":"2017-09-20T07:11:33Z",
               "deletedDate":null,
               "autosell":false,
               "altAutosellInternal":false,
               "partners":0,
               "vendors":12,
               "merchants":22,
               "customers":477,
               "locationsCount":0,
               "posCount":0,
               "enrolledBy":{  
                  "id":1,
                  "enabled":true,
                  "canEditOnboarded":true,
                  "associateType":"ALT36",
                  "legalBusinessName":"alt thirty six",
                  "emailAddress":"ognjen.miletic@gmail.com",
                  "address":"Kozaracka 12",
                  "city":"Some City",
                  "zip":"81000",
                  "state":{  
                     "id":1,
                     "state":"Alabama",
                     "abbreviation":"AL"
                  },
                  "phone":"+38267246776",
                  "companyEIN":"sdf",
                  "incorporationDate":"2017-07-27",
                  "companyWebsite":"http://alt36.com",
                  "beneficiaryPercent":0,
                  "commissionFee":0.10,
                  "internalFee":0.1,
                  "coinaPultApiKey":"asd",
                  "cryptoCapitalApiKey":"qwe",
                  "usBankAccount":"asd",
                  "note":"note",
                  "createdDate":"2017-08-13T20:29:08Z",
                  "deletedDate":null,
                  "autosell":false,
                  "altAutosellInternal":false,
                  "partners":55,
                  "vendors":60,
                  "merchants":53,
                  "customers":99,
                  "locationsCount":44,
                  "posCount":0,
                  "enrolledBy":null
               }
            }
         }
      }
   ],
   "totalElements":11,
   "last":true,
   "totalPages":1,
   "sort":[  
      {  
         "direction":"DESC",
         "property":"id",
         "ignoreCase":false,
         "nullHandling":"NATIVE",
         "ascending":false,
         "descending":true
      }
   ],
   "size":1,
   "number":0,
   "first":true,
   "numberOfElements":1
}
```

<h3 id="getAllLocationsUsingGET_1-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfLocation](#schemapageoflocation)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

#### Get all Locations

<a id="opIdgetAllLocationsForDashboardUsingGET"></a>

> Code samples

```shell
curl -X GET http://example.com/api/dashboard-locations -H 'Accept: */*'
```

```http
GET http://example.com/api/dashboard-locations HTTP/1.1
Host: null
Accept: */*
```

```javascript
var headers = {
  'Accept':'*/*'
};

$.ajax({
  url: 'http://example.com/api/dashboard-locations',
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

fetch('http://example.com/api/dashboard-locations',
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

result = RestClient.get 'http://example.com/api/dashboard-locations',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Accept': '*/*'
}

r = requests.get('http://example.com/api/dashboard-locations',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/dashboard-locations");
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

`GET /api/dashboard-locations`

*Get all the locations*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`

<!-- <h3 id="getAllLocationsForDashboardUsingGET-parameters">Parameters</h3> -->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|merchantId|query|integer(int64)|false|merchantId|

> Example responses

<h3 id="getAllLocationsForDashboardUsingGET-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<h3 id="getAllLocationsForDashboardUsingGET-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[PosForDashboardVm](#schemaposfordashboardvm)]|false|No description|
|» address|string|false|No description|
|» city|string|false|No description|
|» geolocation|string|false|No description|
|» id|integer(int64)|false|No description|
|» name|string|false|No description|
|» noofpos|integer(int64)|false|No description|
|» state|string|false|No description|

#### Get Location by ID

<a id="opIdgetLocationUsingGET_1"></a>

> Code samples

```shell
curl -X GET http://example.com/api/locations/{id} -H 'Accept: */*'
```

```http
GET http://example.com/api/locations/{id} HTTP/1.1
Host: null
Accept: */*
```

```javascript
var headers = {
  'Accept':'*/*'
};

$.ajax({
  url: 'http://example.com/api/locations/{id}',
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

fetch('http://example.com/api/locations/{id}',
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

result = RestClient.get 'http://example.com/api/locations/{id}',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Accept': '*/*'
}

r = requests.get('http://example.com/api/locations/{id}',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/locations/{id}");
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

`GET /api/locations/{id}`

*Get location by ID*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`

<!-- <h3 id="getLocationUsingGET_1-parameters">Parameters</h3> -->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|

> Example responses

```json
{
  "id": 2354,
  "name": "New location",
  "phone": "+18267246776",
  "website": "http://mysite.com",
  "address": "751 S Weir Canyon Rd # 173",
  "city": "Anaheim",
  "zip": "92808",
  "state": {
    "id": 5,
    "state": "California",
    "abbreviation": "CA"
  },
  "geoLocation": "33.8608908,-117.7381407",
  "country": "Alabama",
  "file": "data:image/png;base64,image_in_base_64",
  "fileContentType": "image/png",
  "contact": {
    "firstName": "John",
    "lastName": "Dale",
    "primaryMobilePhone": "+18267246776",
    "primaryEmailAddress": "example@gmail.com",
    "position": "some position",
    "contactType": "LOCATION"
  }
}
```

<h3 id="getLocationUsingGET_1-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[LocationWithTransactionVm](#schemalocationwithtransactionvm)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

#### Create Location

<a id="opIdcreateLocationUsingPOST_1"></a>

> Code samples

```shell
curl -X POST http://example.com/api/locations \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'
```

```http
POST http://example.com/api/locations HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*
```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'
};

$.ajax({
  url: 'http://example.com/api/locations',
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
  "name": "New location",
  "phone": "+18267246776",
  "website": "http://mysite.com",
  "address": "751 S Weir Canyon Rd # 173",
  "city": "Anaheim",
  "zip": "92808",
  "state": {
    "id": 5,
    "state": "California",
    "abbreviation": "CA"
  },
  "geoLocation": "33.8608908,-117.7381407",
  "country": "Alabama",
  "file": "data:image/png;base64,image_in_base_64",
  "fileContentType": "image/png",
  "contact": {
    "firstName": "John",
    "lastName": "Dale",
    "primaryMobilePhone": "+18267246776",
    "primaryEmailAddress": "example@gmail.com",
    "position": "some position",
    "contactType": "LOCATION"
  }
}';

const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'
};

fetch('http://example.com/api/locations',
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
  'Accept' => '*/*'
}

result = RestClient.post 'http://example.com/api/locations',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}

r = requests.post('http://example.com/api/locations',
                   params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/locations");
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

`POST /api/locations`

*Create a new location*

**Required user role:**

  * `ROLE_MERCHANT_ADMIN`

> Body parameter

```json
{
  "name": "New location",
  "phone": "+18267246776",
  "website": "http://mysite.com",
  "address": "751 S Weir Canyon Rd # 173",
  "city": "Anaheim",
  "zip": "92808",
  "state": {
    "id": 5,
    "state": "California",
    "abbreviation": "CA"
  },
  "geoLocation": "33.8608908,-117.7381407",
  "country": "Alabama",
  "file": "data:image/png;base64,image_in_base_64",
  "fileContentType": "image/png",
  "contact": {
    "firstName": "John",
    "lastName": "Dale",
    "primaryMobilePhone": "+18267246776",
    "primaryEmailAddress": "example@gmail.com",
    "position": "some position",
    "contactType": "LOCATION"
  }
}
```

<!-- <h3 id="createLocationUsingPOST_1-parameters">Parameters</h3> -->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|merchantId|query|integer(int64)|false|merchantId|
|body|body|[LocationVm](#schemalocationvm)|true|locationVm|

> Example responses

<h3 id="createLocationUsingPOST_1-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[Location](#schemalocation)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

```json
{  
   "id":2498,
   "name":"New location",
   "address":"751 S Weir Canyon Rd # 173",
   "deletedDate":null,
   "address2":null,
   "city":"Anaheim",
   "file":"d6fb5ec0-33fe-492d-a663-80e95beba983",
   "zip":"92808",
   "state":{  
      "id":5,
      "state":"California",
      "abbreviation":"CA"
   },
   "country":"Alabama",
   "emailAddress":null,
   "phone":"+18267246776",
   "note":null,
   "website":"http://mysite.com",
   "geoLocation":"33.8608908,-117.7381407",
   "pointOfSales":[  

   ],
   "parentLocation":null,
   "associate":{  
      "id":2102,
      "enabled":true,
      "canEditOnboarded":false,
      "associateType":"MERCHANT",
      "legalBusinessName":"Demo Merchant",
      "emailAddress":"merchant_AA_1855@021.com",
      "address":"Merchant Address 1855",
      "city":"Novi Sad",
      "zip":"21000",
      "state":{  
         "id":1,
         "state":"Alabama",
         "abbreviation":"AL"
      },
      "phone":"064 5566777",
      "companyEIN":"00-55555",
      "incorporationDate":"2017-09-19",
      "companyWebsite":"http://www.55dsl.com/",
      "beneficiaryPercent":null,
      "commissionFee":0.10,
      "internalFee":0.03,
      "coinaPultApiKey":null,
      "cryptoCapitalApiKey":null,
      "usBankAccount":null,
      "note":null,
      "createdDate":"2017-09-20T10:03:04Z",
      "deletedDate":null,
      "autosell":false,
      "altAutosellInternal":false,
      "partners":0,
      "vendors":31,
      "merchants":0,
      "customers":511,
      "locationsCount":49,
      "posCount":5

   }
}
```

#### Update Location

<a id="opIdupdateLocationUsingPUT_1"></a>

> Code samples

```shell
curl -X PUT http://example.com/api/locations \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'
```

```http
PUT http://example.com/api/locations HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*
```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'
};

$.ajax({
  url: 'http://example.com/api/locations',
  method: 'put',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})
```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "id": 2354,
  "name": "New location",
  "phone": "+18267246776",
  "website": "http://mysite.com",
  "address": "751 S Weir Canyon Rd # 173",
  "city": "Anaheim",
  "zip": "92808",
  "state": {
    "id": 5,
    "state": "California",
    "abbreviation": "CA"
  },
  "geoLocation": "33.8608908,-117.7381407",
  "country": "Alabama",
  "file": "data:image/png;base64,image_in_base_64",
  "fileContentType": "image/png",
  "contact": {
    "firstName": "John",
    "lastName": "Dale",
    "primaryMobilePhone": "+18267246776",
    "primaryEmailAddress": "example@gmail.com",
    "position": "some position",
    "contactType": "LOCATION"
  }
}';

const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'
};


fetch('http://example.com/api/locations',
{
  method: 'PUT',
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
  'Accept' => '*/*'
}

result = RestClient.put 'http://example.com/api/locations',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}

r = requests.put('http://example.com/api/locations',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/locations");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
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

`PUT /api/locations`

*Updates an existing location*

**Required user role:**

  * `ROLE_MERCHANT_ADMIN`

> Body parameter

```json
{
  "id": 2354,
  "name": "New location",
  "phone": "+18267246776",
  "website": "http://mysite.com",
  "address": "751 S Weir Canyon Rd # 173",
  "city": "Anaheim",
  "zip": "92808",
  "state": {
    "id": 5,
    "state": "California",
    "abbreviation": "CA"
  },
  "geoLocation": "33.8608908,-117.7381407",
  "country": "Alabama",
  "file": "data:image/png;base64,image_in_base_64",
  "fileContentType": "image/png",
  "contact": {
    "firstName": "John",
    "lastName": "Dale",
    "primaryMobilePhone": "+18267246776",
    "primaryEmailAddress": "example@gmail.com",
    "position": "some position",
    "contactType": "LOCATION"
  }
}
```

<!-- <h3 id="updateLocationUsingPUT_1-parameters">Parameters</h3> -->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[LocationVm](#schemalocationvm)|true|locationVm|

> Example responses

<h3 id="updateLocationUsingPUT_1-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[Location](#schemalocation)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

#### Delete Location

<a id="opIddeleteLocationUsingDELETE_1"></a>

> Code samples

```shell
curl -X DELETE http://example.com/api/locations/{id}
```

```http
DELETE http://example.com/api/locations/{id} HTTP/1.1
Host: null
```

```javascript
$.ajax({
  url: 'http://example.com/api/locations/{id}',
  method: 'delete',
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})
```


```javascript--nodejs
const request = require('node-fetch');

fetch('http://example.com/api/locations/{id}',
{
  method: 'DELETE'
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

result = RestClient.delete 'http://example.com/api/locations/{id}',
         params: {}

p JSON.parse(result)
```

```python
import requests

r = requests.delete('http://example.com/api/locations/{id}',
                     params={})

print r.json()
```

```java
URL obj = new URL("http://example.com/api/locations/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
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

`DELETE /api/locations/{id}`

*Delete location by ID*

**Required user role:**

  * `ROLE_MERCHANT_ADMIN`

<!-- <h3 id="deleteLocationUsingDELETE_1-parameters">Parameters</h3> -->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|id|

<h3 id="deleteLocationUsingDELETE_1-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|

#### Search Locations

<a id="opIdsearchUsingGET_1"></a>

> Code samples

```shell
curl -X GET http://example.com/api/location/search -H 'Accept: */*'
```

```http
GET http://example.com/api/location/search HTTP/1.1
Host: null
Accept: */*
```

```javascript
var headers = {
  'Accept':'*/*'
};

$.ajax({
  url: 'http://example.com/api/location/search',
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

fetch('http://example.com/api/location/search',
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

result = RestClient.get 'http://example.com/api/location/search',
         params: {}, headers: headers

p JSON.parse(result)
```

```python
import requests

headers = {
  'Accept': '*/*'
}

r = requests.get('http://example.com/api/location/search',
                  params={}, headers = headers)

print r.json()
```

```java
URL obj = new URL("http://example.com/api/location/search");
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

`GET /api/location/search`

*search locations*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`

<!-- <h3 id="searchUsingGET_1-parameters">Parameters</h3> -->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|q|query|string|false|q|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc/desc). Default sort order is ascending. Multiple sort criteria are supported.|

> Example responses

```json
{  
   "content":[  
      {  
         "id":303,
         "name":"Phoenix",
         "address":"340 N 3rd St",
         "deletedDate":null,
         "address2":null,
         "city":"Phoenix",
         "file":null,
         "zip":"85004",
         "state":{  
            "id":3,
            "state":"Arizona",
            "abbreviation":"AZ"
         },
         "country":"Alabama",
         "emailAddress":null,
         "phone":"0640272551",
         "note":null,
         "website":"http://www.vizlore.com",
         "geoLocation":"33.4522379,-112.0705419",
         "pointOfSales":[  
            {  
               "id":707,
               "pointOfSaleType":"OTHER",
               "virtualPointOfSalesEnabled":false,
               "active":true,
               "deletedDate":null,
               "inventoryNumber":"POS 5",
               "note":null,
               "name":"POS 5"
            }
         ],
         "parentLocation":null,
         "associate":{  
            "id":2102,
            "enabled":true,
            "canEditOnboarded":false,
            "associateType":"MERCHANT",
            "legalBusinessName":"Demo Merchant",
            "emailAddress":"merchant_AA_1855@021.com",
            "address":"Merchant Address 1855",
            "city":"Novi Sad",
            "zip":"21000",
            "state":{  
               "id":1,
               "state":"Alabama",
               "abbreviation":"AL"
            },
            "phone":"064 5566777",
            "companyEIN":"00-55555",
            "incorporationDate":"2017-09-19",
            "companyWebsite":"http://www.55dsl.com/",
            "beneficiaryPercent":null,
            "commissionFee":0.10,
            "internalFee":0.03,
            "coinaPultApiKey":null,
            "cryptoCapitalApiKey":null,
            "usBankAccount":null,
            "note":null,
            "createdDate":"2017-09-20T10:03:04Z",
            "deletedDate":null,
            "autosell":false,
            "altAutosellInternal":false,
            "partners":0,
            "vendors":31,
            "merchants":0,
            "customers":511,
            "locationsCount":49,
            "posCount":5,
            "enrolledBy":{  
               "id":2054,
               "enabled":true,
               "canEditOnboarded":false,
               "associateType":"PARTNER",
               "legalBusinessName":"Demo Partner",
               "emailAddress":"partner_AA_24306@021.com",
               "address":"Partner Address 24306",
               "city":"Novi Sad",
               "zip":"21000",
               "state":{  
                  "id":1,
                  "state":"Alabama",
                  "abbreviation":"AL"
               },
               "phone":"064 5566776",
               "companyEIN":"00-55555",
               "incorporationDate":"2017-09-03",
               "companyWebsite":"http://www.55dsl.com/",
               "beneficiaryPercent":null,
               "commissionFee":0.10,
               "internalFee":0.03,
               "coinaPultApiKey":null,
               "cryptoCapitalApiKey":null,
               "usBankAccount":null,
               "note":null,
               "createdDate":"2017-09-20T07:11:33Z",
               "deletedDate":null,
               "autosell":false,
               "altAutosellInternal":false,
               "partners":0,
               "vendors":12,
               "merchants":22,
               "customers":477,
               "locationsCount":0,
               "posCount":0,
               "enrolledBy":{  
                  "id":1,
                  "enabled":true,
                  "canEditOnboarded":true,
                  "associateType":"ALT36",
                  "legalBusinessName":"alt thirty six",
                  "emailAddress":"ognjen.miletic@gmail.com",
                  "address":"Kozaracka 12",
                  "city":"Some City",
                  "zip":"81000",
                  "state":{  
                     "id":1,
                     "state":"Alabama",
                     "abbreviation":"AL"
                  },
                  "phone":"+38267246776",
                  "companyEIN":"sdf",
                  "incorporationDate":"2017-07-27",
                  "companyWebsite":"http://alt36.com",
                  "beneficiaryPercent":0,
                  "commissionFee":0.10,
                  "internalFee":0.1,
                  "coinaPultApiKey":"asd",
                  "cryptoCapitalApiKey":"qwe",
                  "usBankAccount":"asd",
                  "note":"note",
                  "createdDate":"2017-08-13T20:29:08Z",
                  "deletedDate":null,
                  "autosell":false,
                  "altAutosellInternal":false,
                  "partners":55,
                  "vendors":60,
                  "merchants":53,
                  "customers":99,
                  "locationsCount":44,
                  "posCount":0,
                  "enrolledBy":null
               }
            }
         }
      }
   ],
   "totalElements":11,
   "last":true,
   "totalPages":1,
   "sort":[  
      {  
         "direction":"DESC",
         "property":"id",
         "ignoreCase":false,
         "nullHandling":"NATIVE",
         "ascending":false,
         "descending":true
      }
   ],
   "size":1,
   "number":0,
   "first":true,
   "numberOfElements":1
}
```

<h3 id="searchUsingGET_1-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfLocation](#schemapageoflocation)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|
