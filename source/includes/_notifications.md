## Notifications

Notification service uses EventSource capability of HTTP protocol. That is a variant of standard GET request, but conformed to long pulling use case. The notification service is used to get notifications on transaction status updates. The notification is provided for PoS related transactions and transactions of DASH digital currency to an external or internal wallet.

The base URL for Production environment is:

* `https:/notifier-dot-altthirtysixproduct36.appspot.com`

The base URL for Sandbox environment is:

* `https://notifier-dot-sandboxaltthirtysixproduct36.appspot.com`

### Payment Notification

`GET /api/pos/payment/notification/<internal_tx_id>`

**Important**: This is not simple GET request, event source object has to be used as specified [here](https://developer.mozilla.org/en-US/docs/Web/API/EventSource). For other clients there are appropriate libraries provided.

**Required authentication:**

   * `No authentication is required`

**Important usage notice**

A user may pay more or less than the amount requested simply by altering the amount to be paid from their mobile wallet after they scan the presented QR code. Therefore an addition parameter `warning_msg` is provided which includes a message with the exact difference. If the amount paid is equal as the requested amount, this parameter is omitted or empty.

> Code samples

```shell
curl -X GET http://example.com/api/pos/payment/notification/<internal_tx_id>
```

```php

```

```javascript
var evtSource = new EventSource("http://example.com/api/pos/payment/notification/<internal_tx_id>", { withCredentials: true } );

evtSource.onmessage = function(e) {
  var newElement = document.createElement("li");

  newElement.innerHTML = "message: " + e.data;
  eventList.appendChild(newElement);
}

evtSource.onerror = function(e) {
  console.log("EventSource failed.");
};
```

```ruby
require "em-eventsource"
EM.run do
  source = EventMachine::EventSource.new("http://example.com/api/pos/payment/notification/<internal_tx_id>")
  source.message do |message|
    puts "new message #{message}"
  end
  source.start # Start listening
end
```

```python
from sseclient import SSEClient

messages = SSEClient('http://example.com/api/pos/payment/notification/<internal_tx_id>')
for msg in messages:
    do_something_useful(msg)
```

```java
   URI streamdataUri = new URI("http://example.com/api/pos/payment/notification/<internal_tx_id>");  
   ResolvableType type = forClassWithGenerics(ServerSentEvent.class, JsonNode.class);
   WebClient client = WebClient.create();
   Flux<ServerSentEvent<JsonNode>> events =
             client.get()
                   .uri(streamdataUri)
                   .accept(TEXT_EVENT_STREAM)
                   .exchange()
             .flatMapMany(response -> response.body(toFlux(type)));

    events.subscribe(System.out::println,Throwable::printStackTrace);
```


> Example response

```json
{
 "tx_id":"iw210iw21i0",
 "tx_state":"COMPLETED",
 "requested_amount":25.00,
 "requested_currency":"USD",
 "converted_to_amount": 0.2,
 "converted_to_currency":"DASH",
 "timestamp_resp": "1503007674",
 "pay_to_address": "1xj239s8…js928jswi",
 "warning_msg":{  
        "message":
                "User payed MORE than required, expected_amount_crypto: 0.056 expected_amount_fiat: 25.50, payed_amount_crypto: 0.0571 payed_amount_fiat: 27.25, difference_crypto: 0.0011 difference_fiat: 2.25"
      }
  }
}
```
<!--<h3 id="getAllPaginatedUsingGET_4-internal_fiat_to_crypto">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|internal_tx_id|path|string|true|Internal transaction identifier for which data is requested|

<h3 id="poscreatenewpaymentrequest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[NotificationMessage](#tocNotificationMessage)|
|401|[Bad request](https://tools.ietf.org/html/rfc7235#section-3.1)|Bad request|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
