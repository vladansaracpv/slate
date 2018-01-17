### Partner Sales Report

#### All Merchants

<a id="opIdcreateAnalyticReports-merchant-list"></a>

`GET /api/v1/analytics/reports/merchant`

*Partner fetch his merchant list with sales summary info*

This endpoint lists all merchants for specified partner (based on jwt token)

**Required user role:**

   * `ROLE_PARTNER_ADMIN`
   * `ROLE_PARTNER_USER`

<!--<h3 id="opIdcreateAnalyticReports-partner-list-parameters">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|timerange_from|query|string|true|start date/datetime in ISO format|
|timerange_to|query|string|true|end date/datetime in ISO format|
|page|query|integer|true|Page of data in “data” section. Note that this is not offset, because server calculates offset based on current page value and sent pageSize. Page counting starts with 0.|
|pageSize|integer|string|true| size of data section ie. maximum number of items shown in data section. Minimum value is 1.|

<h3 id="opIdcreateAnalyticReports-partner-list-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[MerchantReportResponse](#tocMerchantReportResponse)|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|

> Example responses

```json
{
    "metadata": {
        "currency": null,
        "timerangeFrom": "2017-10-21T11:00:26Z",
        "timerangeTo": "2017-10-26T23:00:26Z",
        "pageNumber": 0,
        "itemsPerPage": 2,
        "targetRole": null,
        "totalNumberOfItems": 17
    },
    "summary": {
        "totalSalesVolume": 24064688,
        "totalSalesCount": 2,
        "avgTXAmount": 12032344,
        "totalSalesCommission": 2316468
    },
    "data": [
        {
            "id": 2102,
            "name": "DO_NOT_DELETE_Merchant_19770",
            "email": "ikovico@gmail.com",
            "vendorCnt": 25,
            "locationsCnt": 4,
            "posCnt": 7,
            "customersCnt": 29,
            "totalSalesCommission": 0.02316468,
            "totalSalesCommissionFiat": 568.25 ,
            "totalSales":0.024064688,
            "totalSalesFiat":785.23    
        },
        {
            "id": 2192,
            "name": "Merchant_064",
            "email": "partnermerchant36@gmail.com",
            "vendorCnt": 0,
            "locationsCnt": 1,
            "posCnt": 1,
            "customersCnt": 0,
            "totalSalesCommission": 0,
            "totalSalesCommissionFiat": 568.25 ,
            "totalSales": 0,
            "totalSalesFiat":785.23
        }
   ]
}

```
#### All Locations

<a id="opIdcreateAnalyticReports-location-list"></a>

*Partner fetch list of all locations of his merchants with sales summary info*

`GET /api/v1/analytics/reports/location`

**Required user role:**

   * `ROLE_PARTNER_ADMIN`
   * `ROLE_PARTNER_USER`
   * `ROLE_MERCHANT_ADMIN`
   * `ROLE_MERCHANT_USER`

<!-- <h3 id="opIdcreateAnalyticReports-partner-list-parameters">Parameters</h3> -->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|timerange_from|query|string|true|start date/datetime in ISO format|
|timerange_to|query|string|true|end date/datetime in ISO format|
|page|query|integer|true|Page of data in “data” section. Note that this is not offset, because server calculates offset based on current page value and sent pageSize. Page counting starts with 0.|
|pageSize|integer|string|true| size of data section ie. maximum number of items shown in data section. Minimum value is 1.|

<h3 id="opIdcreateAnalyticReports-partner-list-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[LocationReportResponse](#tocLocationReportResponse)|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|

> Example responses

```json
{
    "metadata": {
        "currency": null,
        "timerangeFrom": "2017-10-21T11:00:26Z",
        "timerangeTo": "2017-10-26T23:00:26Z",
        "pageNumber": 0,
        "itemsPerPage": 2,
        "targetRole": null,
        "totalNumberOfItems": 17
    },
    "summary": {
      "totalSalesVolume": 13.4566654,
      "totalSalesVolumeFiat": 94235.0255456,
      "totalSalesCount": 94,
      "avgTXAmount": 0.0955647785212,
      "avgTXAmountFiat": 52.15564556872,
      "totalSalesCommission": 0.9985645,
      "totalSalesCommissionFiat": 1026.25,
      "totalInternalCommissions": 0.22554123,
      "totalInternalCommissionsFiat":1562.1233554
      "income":0.03541,
      "incomeFiat": 180.365
    },
    "data": [
      {
          "id": 363,
          "name": "New location",
          "address": "Test",
          "numberOfPOS": 2,
          "totalSales": 0,
          "totalSalesFiat":0,
          "totalCommission": 0,
          "totalCommissionFiat":0,
          "avgTransaction": 0,
          "avgTransactionFiat":0,
          "totalCount": 0
      },
      {
          "id": 305,
          "name": "Merchant_Location_60438",
          "address": "Miodraga Bulatovica 17",
          "numberOfPOS": 3,
          "totalSales": 0.017231902,
          "totalSalesFiat":175.46,
          "totalCommission": 0.01678190,
          "avgTransaction": 168.123,
          "totalCount": 1
      }

   ]
}
```
#### All POS

<a id="opIdcreateAnalyticReports-pos-list"></a>

*Partner's fetch POS list of all hisMerchants with sales summary info.*

`GET /api/v1/analytics/reports/pos`

**Required user role:**

   * `ROLE_PARTNER_ADMIN`
   * `ROLE_PARTNER_USER`
   * `ROLE_MERCHANT_ADMIN`
   * `ROLE_MERCHANT_USER`


<!--<h3 id="opIdcreateAnalyticReports-pos-list-parameters">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|timerange_from|query|string|true|start date/datetime in ISO format|
|timerange_to|query|string|true|end date/datetime in ISO format|
|page|query|integer|true|Page of data in “data” section. Note that this is not offset, because server calculates offset based on current page value and sent pageSize. Page counting starts with 0.|
|pageSize|integer|string|true| size of data section ie. maximum number of items shown in data section. Minimum value is 1.|

<h3 id="opIdcreateAnalyticReports-partner-list-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[POSReportResponse](#tocPOSReportResponse)|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|

> Example responses

```json
{
    "metadata": {
        "currency": null,
        "timerangeFrom": "2017-10-21T11:00:26Z",
        "timerangeTo": "2017-10-26T23:00:26Z",
        "pageNumber": 0,
        "itemsPerPage": 2,
        "targetRole": null,
        "totalNumberOfItems": 17
    },
    "summary": {
      "totalSalesVolume": 13.4566654,
      "totalSalesVolumeFiat": 94235.0255456,
      "totalSalesCount": 94,
      "avgTXAmount": 0.0955647785212,
      "avgTXAmountFiat": 52.15564556872,
      "totalSalesCommission": 0.9985645,
      "totalSalesCommissionFiat": 1026.25,
      "totalInternalCommissions": 0.22554123,
      "totalInternalCommissionsFiat":1562.1233554
      "income":0.03541,
      "incomeFiat": 180.365
    },
    "data": [
      {
          "id": 363,
          "name": "New location",
          "address": "Test",
          "numberOfPOS": 2,
          "totalSales": 0,
          "totalSalesFiat":0,
          "totalCommission": 0,
          "totalCommissionFiat":0,
          "avgTransaction": 0,
          "avgTransactionFiat":0,
          "totalCount": 0
      },
      {
          "id": 305,
          "name": "Merchant_Location_60438",
          "address": "Miodraga Bulatovica 17",
          "numberOfPOS": 3,
          "totalSales": 0.017231902,
          "totalSalesFiat":175.46,
          "totalCommission": 0.01678190,
          "avgTransaction": 168.123,
          "totalCount": 1
      }

   ]
}
```

#### Locations of single Merchant
<a id="opIdcreateAnalyticReports-location-list"></a>

*Partner fetch list of all locations for a specific merchants with sales summary info*

`GET /api/v1/analytics/merchant/<merchantid>/location`

**Required user role:**

   * `ROLE_PARTNER_ADMIN`
   * `ROLE_PARTNER_USER`

<!-- <h3 id="opIdcreateAnalyticReports-partner-list-parameters">Parameters</h3> -->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|timerange_from|query|string|true|start date/datetime in ISO format|
|timerange_to|query|string|true|end date/datetime in ISO format|
|page|query|integer|true|Page of data in “data” section. Note that this is not offset, because server calculates offset based on current page value and sent pageSize. Page counting starts with 0.|
|pageSize|integer|string|true| size of data section ie. maximum number of items shown in data section. Minimum value is 1.|

<h3 id="opIdcreateAnalyticReports-partner-list-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[LocationReportResponse](#tocLocationReportResponse)|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|

> Example responses

```json
{
    "metadata": {
        "currency": null,
        "timerangeFrom": "2017-10-21T11:00:26Z",
        "timerangeTo": "2017-10-26T23:00:26Z",
        "pageNumber": 0,
        "itemsPerPage": 2,
        "targetRole": null,
        "totalNumberOfItems": 17
    },
    "summary": {
      "totalSalesVolume": 13.4566654,
      "totalSalesVolumeFiat": 94235.0255456,
      "totalSalesCount": 94,
      "avgTXAmount": 0.0955647785212,
      "avgTXAmountFiat": 52.15564556872,
      "totalSalesCommission": 0.9985645,
      "totalSalesCommissionFiat": 1026.25,
      "totalInternalCommissions": 0.22554123,
      "totalInternalCommissionsFiat":1562.1233554
      "income":0.03541,
      "incomeFiat": 180.365
    },
    "data": [
      {
          "id": 363,
          "name": "New location",
          "address": "Test",
          "numberOfPOS": 2,
          "totalSales": 0,
          "totalSalesFiat":0,
          "totalCommission": 0,
          "totalCommissionFiat":0,
          "avgTransaction": 0,
          "avgTransactionFiat":0,
          "totalCount": 0
      },
      {
          "id": 305,
          "name": "Merchant_Location_60438",
          "address": "Miodraga Bulatovica 17",
          "numberOfPOS": 3,
          "totalSales": 0.017231902,
          "totalSalesFiat":175.46,
          "totalCommission": 0.01678190,
          "avgTransaction": 168.123,
          "totalCount": 1
      }

   ]
}
```

#### POS of single Merchant's Location

<a id="opIdcreateAnalyticReports-pos-list"></a>

*Partner merchant list -> merchant list -> location list->pos list*

`GET /api/v1/analytics/reports/merchant/<merchant_id>/location/<location_id>/pos`

*Lists all POSs drilled down from specific merchant->location.*

**Required user role:**

   * `ROLE_PARTNER_ADMIN`
   * `ROLE_PARTNER_USER`

<!--<h3 id="opIdcreateAnalyticReports-pos-list-parameters">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|timerange_from|query|string|true|start date/datetime in ISO format|
|timerange_to|query|string|true|end date/datetime in ISO format|
|page|query|integer|true|Page of data in “data” section. Note that this is not offset, because server calculates offset based on current page value and sent pageSize. Page counting starts with 0.|
|pageSize|integer|string|true| size of data section ie. maximum number of items shown in data section. Minimum value is 1.|

<h3 id="opIdcreateAnalyticReports-partner-list-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[POSReportResponse](#tocPOSReportResponse)|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|

> Example responses

```json
{
    "metadata": {
        "currency": null,
        "timerangeFrom": "2017-10-21T11:00:26Z",
        "timerangeTo": "2017-10-26T23:00:26Z",
        "pageNumber": 0,
        "itemsPerPage": 2,
        "targetRole": null,
        "totalNumberOfItems": 17
    },
    "summary": {
      "totalSalesVolume": 13.4566654,
      "totalSalesVolumeFiat": 94235.0255456,
      "totalSalesCount": 94,
      "avgTXAmount": 0.0955647785212,
      "avgTXAmountFiat": 52.15564556872,
      "totalSalesCommission": 0.9985645,
      "totalSalesCommissionFiat": 1026.25,
      "totalInternalCommissions": 0.22554123,
      "totalInternalCommissionsFiat":1562.1233554
      "income":0.03541,
      "incomeFiat": 180.365
    },
    "data": [
      {
          "id": 363,
          "name": "New location",
          "address": "Test",
          "numberOfPOS": 2,
          "totalSales": 0,
          "totalSalesFiat":0,
          "totalCommission": 0,
          "totalCommissionFiat":0,
          "avgTransaction": 0,
          "avgTransactionFiat":0,
          "totalCount": 0
      },
      {
          "id": 305,
          "name": "Merchant_Location_60438",
          "address": "Miodraga Bulatovica 17",
          "numberOfPOS": 3,
          "totalSales": 0.017231902,
          "totalSalesFiat":175.46,
          "totalCommission": 0.01678190,
          "avgTransaction": 168.123,
          "totalCount": 1
      }

   ]
}
```


#### POS of single Location
<a id="opIdcreateAnalyticReports-pos-list"></a>

*Merchant list -> location list -> pos list*

`GET /api/v1/analytics/reports/location/<location_id>/pos`

*Lists all locations drilled down from*

**Required user role:**

   * `ROLE_PARTNER_ADMIN`
   * `ROLE_PARTNER_USER`
   * `ROLE_MERCHANT_ADMIN`
   * `ROLE_MERCHANT_USER`

<!--<h3 id="opIdcreateAnalyticReports-pos-list-parameters">Parameters</h3>-->

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|timerange_from|query|string|true|start date/datetime in ISO format|
|timerange_to|query|string|true|end date/datetime in ISO format|
|page|query|integer|true|Page of data in “data” section. Note that this is not offset, because server calculates offset based on current page value and sent pageSize. Page counting starts with 0.|
|pageSize|integer|string|true| size of data section ie. maximum number of items shown in data section. Minimum value is 1.|

<h3 id="opIdcreateAnalyticReports-partner-list-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[POSReportResponse](#tocPOSReportResponse)|
|500|Internal server error|Internal server error|[ErrorMessage](#schemareporterrormessage)|
|403|Forbidden|Forbidden|[ErrorMessage](#schemareporterrormessage)|

> Example responses

```json
{
    "metadata": {
        "currency": null,
        "timerangeFrom": "2017-10-21T11:00:26Z",
        "timerangeTo": "2017-10-26T23:00:26Z",
        "pageNumber": 0,
        "itemsPerPage": 2,
        "targetRole": null,
        "totalNumberOfItems": 17
    },
    "summary": {
      "totalSalesVolume": 13.4566654,
      "totalSalesVolumeFiat": 94235.0255456,
      "totalSalesCount": 94,
      "avgTXAmount": 0.0955647785212,
      "avgTXAmountFiat": 52.15564556872,
      "totalSalesCommission": 0.9985645,
      "totalSalesCommissionFiat": 1026.25,
      "totalInternalCommissions": 0.22554123,
      "totalInternalCommissionsFiat":1562.1233554
      "income":0.03541,
      "incomeFiat": 180.365
    },
    "data": [
      {
          "id": 363,
          "name": "New location",
          "address": "Test",
          "numberOfPOS": 2,
          "totalSales": 0,
          "totalSalesFiat":0,
          "totalCommission": 0,
          "totalCommissionFiat":0,
          "avgTransaction": 0,
          "avgTransactionFiat":0,
          "totalCount": 0
      },
      {
          "id": 305,
          "name": "Merchant_Location_60438",
          "address": "Miodraga Bulatovica 17",
          "numberOfPOS": 3,
          "totalSales": 0.017231902,
          "totalSalesFiat":175.46,
          "totalCommission": 0.01678190,
          "avgTransaction": 168.123,
          "totalCount": 1
      }

   ]
}
```
