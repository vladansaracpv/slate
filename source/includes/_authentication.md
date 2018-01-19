
#Authentication

The Product36 platform uses [JSON Web Tokens](https://jwt.io/) for authentication.

The first step for authentication is to get a Bearer token by using [Authenticate](#authenticate) API. The token received in the response should be used to access all other resources. In order to use the token please include it in the request headers:

`Authorization: Bearer <token>`

The URL examples throughout this documentation use `<token>` as a placeholder. For these examples to work, you need to substitute the value with your own access token. The token expires after 24 hours. If `rememberMe` parameter is set to `true`, the token expires after 30 days. Once expired, a new token should be obtained.

##Authenticate

`POST /api/authenticate`

Access tokens are required to access nearly all endpoints of this API.

> Body parameter


```json
{
  "password": "string",
  "rememberMe": true,
  "username": "string"
}
```


<!-- <h3 id="authorizeUsingPOST-parameters">Parameters</h3> -->


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[LoginVM](#schemaloginvm)|true|loginVM|


> Example responses

```json
{ "id_token":"eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJtZXJjaGFudCIsImF1dGgiOiJST0xFX01FUkNIQU5UX0FETUlOIiwiYXNzb2NpYXRlIjoiMjEwMiIsInVzZXJfaW2iOiIzNTQ0IiwiZXhwIjoxNTE2MTM5MDI3fQ.P5mwh63sMSYw8JXxf7KIwJZbvmI-j8SHIsZE4ACY670dxYsfpWxYUJYJNDHJBkTFaXEIC9a7ayXcbvPW9va3fw" }
```


<h3 id="authorizeUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResponseEntity](#schemaresponseentity)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


## Is Authenticated

`GET /api/authenticate`

*Is Authenticated*

**Parameters**

None

> Code samples


```shell
# You can also use wget
curl -X GET http://example.com/api/authenticate \
  -H 'Accept: */*'


```


```http
GET http://example.com/api/authenticate HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: 'http://example.com/api/authenticate',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```



```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get 'http://example.com/api/authenticate',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('http://example.com/api/authenticate', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("http://example.com/api/authenticate");
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

> Example responses


<h3 id="isAuthenticatedUsingGET-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|
