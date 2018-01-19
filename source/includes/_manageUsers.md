###User Resource


#### Get Authorities


<a id="opIdgetAuthoritiesUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/roles \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/roles HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/roles',
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


fetch('http://example.com/api/roles',
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


result = RestClient.get 'http://example.com/api/roles',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/roles', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/roles");
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


`GET /api/roles`


*Get all roles*


String list of the all possible roles for Associate type


**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_VENDOR_ADMIN`


> Example responses
```json

```


<h3 id="getAuthoritiesUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<h3 id="getAuthoritiesUsingGET-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|



#### Get All Users


<a id="opIdgetAllUsersUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/users \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/users HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/users',
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


fetch('http://example.com/api/users',
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


result = RestClient.get 'http://example.com/api/users',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/users', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/users");
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


`GET /api/users`


*Get All Users*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`
  * `ROLE_VENDOR_ADMIN`
  * `ROLE_VENDOR_USER`


<!-- <h3 id="getAllUsersUsingGET-parameters">Parameters</h3> -->


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer(int32)|false|Page number of the requested page|
|size|query|integer(int32)|false|Size of a page|
|sort|query|array[string]|false|Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported.|


> Example responses

```json

{  
   "content":[  
      {  
         "id":15140,
         "login":"merchantuser",
         "firstName":"Merchant",
         "lastName":"User",
         "email":"ikov.ico@gmail.com",
         "imageUrl":null,
         "activated":true,
         "langKey":"en",
         "createdBy":"partner",
         "createdDate":"2017-09-21T21:16:49Z",
         "lastModifiedBy":"merchantuser",
         "lastModifiedDate":"2017-12-22T09:10:49Z",
         "lastLoginDateTime":"2017-12-22T09:10:49Z",
         "authorities":[  
            "ROLE_MERCHANT_USER"
         ],
         "splashscreenEnabled":true,
         "using2fa":false
      },
      {  
         "id":3544,
         "login":"merchant",
         "firstName":"Merchant",
         "lastName":"Admin",
         "email":"ikovico@gmail.com",
         "imageUrl":"",
         "activated":true,
         "langKey":"en",
         "createdBy":"partner",
         "createdDate":"2017-09-21T21:16:49Z",
         "lastModifiedBy":"merchant",
         "lastModifiedDate":"2018-01-19T00:04:11Z",
         "lastLoginDateTime":"2018-01-19T00:04:11Z",
         "authorities":[  
            "ROLE_MERCHANT_ADMIN"
         ],
         "splashscreenEnabled":true,
         "using2fa":false
      }
   ],
   "totalElements":2,
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
   "size":25,
   "number":0,
   "first":true,
   "numberOfElements":2
}
```


<h3 id="getAllUsersUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[PageOfUserDTO](#schemapageofuserdto)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|




#### Create User


<a id="opIdcreateUserUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST http://example.com/api/users \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
POST http://example.com/api/users HTTP/1.1
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
  url: 'http://example.com/api/users',
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
  "activated": true,
  "authorities": [
    "string"
  ],
  "createdBy": "string",
  "createdDate": "2018-01-08T16:57:23Z",
  "email": "string",
  "firstName": "string",
  "id": 0,
  "imageUrl": "string",
  "langKey": "strin",
  "lastLoginDateTime": "2018-01-08T16:57:23Z",
  "lastModifiedBy": "string",
  "lastModifiedDate": "2018-01-08T16:57:23Z",
  "lastName": "string",
  "login": "string",
  "splashscreenEnabled": true,
  "using2fa": true
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('http://example.com/api/users',
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


result = RestClient.post 'http://example.com/api/users',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.post('http://example.com/api/users', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/users");
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


`POST /api/users`


*Create User*


**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_VENDOR_ADMIN`


> Body parameter


```json
{
  "activated": true,
  "authorities": [
    "string"
  ],
  "createdBy": "string",
  "createdDate": "2018-01-08T16:57:23Z",
  "email": "string",
  "firstName": "string",
  "id": 0,
  "imageUrl": "string",
  "langKey": "strin",
  "lastLoginDateTime": "2018-01-08T16:57:23Z",
  "lastModifiedBy": "string",
  "lastModifiedDate": "2018-01-08T16:57:23Z",
  "lastName": "string",
  "login": "string",
  "splashscreenEnabled": true,
  "using2fa": true
}
```


<!-- <h3 id="createUserUsingPOST-parameters">Parameters</h3> -->


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UserDTO](#schemauserdto)|true|managedUserVM|


> Example responses

```json

{  
         "id":3544,
         "login":"merchant",
         "firstName":"Merchant",
         "lastName":"Admin",
         "email":"ikovico@gmail.com",
         "imageUrl":"",
         "activated":true,
         "langKey":"en",
         "createdBy":"partner",
         "createdDate":"2017-09-21T21:16:49Z",
         "lastModifiedBy":"merchant",
         "lastModifiedDate":"2018-01-19T00:04:11Z",
         "lastLoginDateTime":"2018-01-19T00:04:11Z",
         "authorities":[  
            "ROLE_MERCHANT_ADMIN"
         ],
         "splashscreenEnabled":true,
         "using2fa":false
      }

```


<h3 id="createUserUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|



#### Update User



<a id="opIdupdateUserUsingPUT"></a>


> Code samples


```shell
# You can also use wget
curl -X PUT http://example.com/api/users \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
PUT http://example.com/api/users HTTP/1.1
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
  url: 'http://example.com/api/users',
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
  "activated": true,
  "authorities": [
    "string"
  ],
  "createdBy": "string",
  "createdDate": "2018-01-08T16:57:23Z",
  "email": "string",
  "firstName": "string",
  "id": 0,
  "imageUrl": "string",
  "langKey": "strin",
  "lastLoginDateTime": "2018-01-08T16:57:23Z",
  "lastModifiedBy": "string",
  "lastModifiedDate": "2018-01-08T16:57:23Z",
  "lastName": "string",
  "login": "string",
  "splashscreenEnabled": true,
  "using2fa": true
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('http://example.com/api/users',
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


result = RestClient.put 'http://example.com/api/users',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.put('http://example.com/api/users', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/users");
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


`PUT /api/users`


*Update existing User*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_VENDOR_ADMIN`

> Body parameter


```json
{  
         "id":3544,
         "login":"merchant",
         "firstName":"Merchant",
         "lastName":"Admin",
         "email":"ikovico@gmail.com",
         "langKey":"en",
         "authorities":[  
            "ROLE_MERCHANT_ADMIN"
         ],
         "splashscreenEnabled":true,
         "using2fa":false
      }
```


<!-- <h3 id="updateUserUsingPUT-parameters">Parameters</h3> -->


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UserDTO](#schemauserdto)|true|managedUserVM|


> Example responses

```json

{  
         "id":3544,
         "login":"merchant",
         "firstName":"Merchant",
         "lastName":"Admin",
         "email":"ikovico@gmail.com",
         "imageUrl":"",
         "activated":true,
         "langKey":"en",
         "createdBy":"partner",
         "createdDate":"2017-09-21T21:16:49Z",
         "lastModifiedBy":"merchant",
         "lastModifiedDate":"2018-01-19T00:04:11Z",
         "lastLoginDateTime":"2018-01-19T00:04:11Z",
         "authorities":[  
            "ROLE_MERCHANT_ADMIN"
         ],
         "splashscreenEnabled":true,
         "using2fa":false
      }
```


<h3 id="updateUserUsingPUT-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[UserDTO](#schemauserdto)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|







#### Get User


<a id="opIdgetUserUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/users/{login} \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/users/{login} HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/users/{login}',
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


fetch('http://example.com/api/users/{login}',
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


result = RestClient.get 'http://example.com/api/users/{login}',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/users/{login}', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/users/{login}");
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


`GET /api/users/{login}`


*Get User*

**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_PARTNER_USER`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_MERCHANT_USER`
  * `ROLE_VENDOR_ADMIN`
  * `ROLE_VENDOR_USER`

<!-- <h3 id="getUserUsingGET-parameters">Parameters</h3> -->


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|login|path|string|true|login|


> Example responses


<h3 id="getUserUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[UserDTO](#schemauserdto)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|



#### Delete User


<a id="opIddeleteUserUsingDELETE"></a>


> Code samples


```shell
# You can also use wget
curl -X DELETE http://example.com/api/users/{login}


```


```http
DELETE http://example.com/api/users/{login} HTTP/1.1
Host: null


```


```javascript


$.ajax({
  url: 'http://example.com/api/users/{login}',
  method: 'delete',


  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


fetch('http://example.com/api/users/{login}',
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


result = RestClient.delete 'http://example.com/api/users/{login}',
  params: {
  }


p JSON.parse(result)


```


```python
import requests


r = requests.delete('http://example.com/api/users/{login}', params={


)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/users/{login}");
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


`DELETE /api/users/{login}`


*Delete user*


delete the User by username


**Required user role:**

  * `ROLE_PARTNER_ADMIN`
  * `ROLE_MERCHANT_ADMIN`
  * `ROLE_VENDOR_ADMIN`


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|login|path|string|true|login|


<h3 id="deleteUserUsingDELETE-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|

