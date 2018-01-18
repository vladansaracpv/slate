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

<!--<h3 id="getAllPaginatedUsingGET_4-internal_fiat_to_crypto">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[InternalRequest](#tocInternalRequest)|false|InternalRequest object|

>Body parameter

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
