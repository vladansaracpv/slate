#Objects
<h2 id="tocSselfregistervm">SelfRegisterVM</h2>


<a id="schemaselfregistervm"></a>


```json
{
  "address": "string",
  "address2": "string",
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "city": "string",
  "companyEIN": "string",
  "companyWebsite": "string",
  "emailAddress": "string",
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "note": "string",
  "phone": "string",
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "john.doe@example.com",
    "firstName": "john",
    "lastName": "doe",
    "login": "john.doe@example.com",
    "password": "mySecretPassword"
  },
  "zip": "81000"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|address|string|true|No description|
|address2|string|false|No description|
|authorizedSignerContact|[ContactVM](#schemacontactvm)|true|No description|
|city|string|true|No description|
|companyEIN|string|true|No description|
|companyWebsite|string|false|No description|
|emailAddress|string|true|No description|
|incorporationDate|string(date)|false|No description|
|legalBusinessName|string|true|No description|
|mainContact|[ContactVM](#schemacontactvm)|true|No description|
|note|string|false|No description|
|phone|string|true|No description|
|state|[CountryState](#schemacountrystate)|true|No description|
|usBankAccount|string|false|No description|
|user|[CreateAssociateAdminUserWithPasswordVM](#schemacreateassociateadminuserwithpasswordvm)|false|No description|
|zip|string|true|No description|


<h2 id="tocSshutdownaccountrequestvm">ShutDownAccountRequestVM</h2>


<a id="schemashutdownaccountrequestvm"></a>


```json
{
  "reason": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|reason|string|true|No description|


<h2 id="tocSsort">Sort</h2>


<a id="schemasort"></a>


```json
{}
```


### Properties


*None*


<h2 id="tocSuser">User</h2>


<a id="schemauser"></a>


```json
{
  "accountNonExpired": true,
  "accountNonLocked": true,
  "activated": true,
  "associate": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "credentialsNonExpired": true,
  "email": "john.doe@example.com",
  "enabled": true,
  "firstName": "string",
  "id": 0,
  "imageUrl": "string",
  "langKey": "strin",
  "lastLoginDateTime": "2018-01-08T16:57:23Z",
  "lastName": "string",
  "location": {
    "address": "string",
    "address2": "string",
    "associate": {
      "address": "string",
      "altAutosellInternal": true,
      "associateType": "ALT36",
      "autosell": true,
      "beneficiaryPercent": 0,
      "canEditOnboarded": true,
      "city": "string",
      "coinaPultApiKey": "string",
      "commissionFee": 0,
      "companyEIN": "string",
      "companyWebsite": "string",
      "createdDate": "2018-01-08T16:57:23Z",
      "cryptoCapitalApiKey": "string",
      "customers": 0,
      "deletedDate": "2018-01-08T16:57:23Z",
      "emailAddress": "string",
      "enabled": true,
      "enrolledBy": null,
      "id": 0,
      "incorporationDate": "2018-01-08",
      "internalFee": 0,
      "legalBusinessName": "string",
      "locationsCount": 0,
      "merchants": 0,
      "note": "string",
      "partners": 0,
      "phone": "string",
      "posCount": 0,
      "state": {
        "abbreviation": "string",
        "id": 0,
        "state": "string"
      },
      "usBankAccount": "string",
      "vendors": 0,
      "zip": "string"
    },
    "city": "string",
    "country": "string",
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "file": "string",
    "geoLocation": "string",
    "id": 0,
    "name": "string",
    "note": "string",
    "parentLocation": null,
    "phone": "string",
    "pointOfSales": [
      {
        "active": true,
        "deletedDate": "2018-01-08T16:57:23Z",
        "id": 0,
        "inventoryNumber": "string",
        "location": null,
        "name": "string",
        "note": "string",
        "pointOfSaleType": "GREENBITS",
        "virtualPointOfSalesEnabled": true
      }
    ],
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "website": "string",
    "zip": "string"
  },
  "login": "string",
  "resetDate": "2018-01-08T16:57:23Z",
  "splashscreenEnabled": true,
  "using2fa": true
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|accountNonExpired|boolean|false|No description|
|accountNonLocked|boolean|false|No description|
|activated|boolean|true|No description|
|associate|[Associate](#schemaassociate)|true|No description|
|credentialsNonExpired|boolean|false|No description|
|email|string|false|No description|
|enabled|boolean|false|No description|
|firstName|string|false|No description|
|id|integer(int64)|false|No description|
|imageUrl|string|false|No description|
|langKey|string|false|No description|
|lastLoginDateTime|string(date-time)|false|No description|
|lastName|string|false|No description|
|location|[Location](#schemalocation)|false|No description|
|login|string|true|No description|
|resetDate|string(date-time)|false|No description|
|splashscreenEnabled|boolean|false|No description|
|using2fa|boolean|false|No description|


<h2 id="tocSuserdto">UserDTO</h2>


<a id="schemauserdto"></a>


```json
{
  "activated": true,
  "authorities": [
    "string"
  ],
  "createdBy": "string",
  "createdDate": "2018-01-08T16:57:23Z",
  "email": "john.doe@example.com",
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


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|activated|boolean|false|No description|
|authorities|[string]|false|No description|
|createdBy|string|false|No description|
|createdDate|string(date-time)|false|No description|
|email|string|false|No description|
|firstName|string|false|No description|
|id|integer(int64)|false|No description|
|imageUrl|string|false|No description|
|langKey|string|false|No description|
|lastLoginDateTime|string(date-time)|false|No description|
|lastModifiedBy|string|false|No description|
|lastModifiedDate|string(date-time)|false|No description|
|lastName|string|false|No description|
|login|string|true|No description|
|splashscreenEnabled|boolean|false|No description|
|using2fa|boolean|false|No description|


<h2 id="tocSuserdtoextended">UserDTOExtended</h2>


<a id="schemauserdtoextended"></a>


```json
{
  "activated": true,
  "associateActive": true,
  "authorities": [
    "string"
  ],
  "createdBy": "string",
  "createdDate": "2018-01-08T16:57:23Z",
  "email": "john.doe@example.com",
  "firstName": "string",
  "id": 0,
  "imageUrl": "string",
  "langKey": "strin",
  "lastModifiedBy": "string",
  "lastModifiedDate": "2018-01-08T16:57:23Z",
  "lastName": "string",
  "login": "string",
  "splashscreenEnabled": true,
  "using2fa": true
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|activated|boolean|false|No description|
|associateActive|boolean|false|No description|
|authorities|[string]|false|No description|
|createdBy|string|false|No description|
|createdDate|string(date-time)|false|No description|
|email|string|false|No description|
|firstName|string|false|No description|
|id|integer(int64)|false|No description|
|imageUrl|string|false|No description|
|langKey|string|false|No description|
|lastModifiedBy|string|false|No description|
|lastModifiedDate|string(date-time)|false|No description|
|lastName|string|false|No description|
|login|string|true|No description|
|splashscreenEnabled|boolean|false|No description|
|using2fa|boolean|false|No description|


<h2 id="tocSwithdrawalstransactionsvm">WithdrawalsTransactionsVm</h2>


<a id="schemawithdrawalstransactionsvm"></a>


```json
{
  "amount": "string",
  "id": 0,
  "status": "string",
  "timeAndDate": "2018-01-08T16:57:23Z",
  "transactionId": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|amount|string|false|No description|
|id|integer(int64)|false|No description|
|status|string|false|No description|
|timeAndDate|string(date-time)|false|No description|
|transactionId|string|false|No description|


<h2 id="tocSpageofuserdto">PageOfUserDTO</h2>


<a id="schemapageofuserdto"></a>


```json
{
  "content": [
    {
      "activated": true,
      "authorities": [
        "string"
      ],
      "createdBy": "string",
      "createdDate": "2018-01-08T16:57:23Z",
      "email": "john.doe@example.com",
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
  ],
  "first": true,
  "last": true,
  "number": 0,
  "numberOfElements": 0,
  "size": 0,
  "sort": {},
  "totalElements": 0,
  "totalPages": 0
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|content|[[UserDTO](#schemauserdto)]|false|No description|
|first|boolean|false|No description|
|last|boolean|false|No description|
|number|integer(int32)|false|No description|
|numberOfElements|integer(int32)|false|No description|
|size|integer(int32)|false|No description|
|sort|[Sort](#schemasort)|false|No description|
|totalElements|integer(int64)|false|No description|
|totalPages|integer(int32)|false|No description|


<h2 id="tocSpageofwithdrawalstransactionsvm">PageOfWithdrawalsTransactionsVm</h2>


<a id="schemapageofwithdrawalstransactionsvm"></a>


```json
{
  "content": [
    {
      "amount": "string",
      "id": 0,
      "status": "string",
      "timeAndDate": "2018-01-08T16:57:23Z",
      "transactionId": "string"
    }
  ],
  "first": true,
  "last": true,
  "number": 0,
  "numberOfElements": 0,
  "size": 0,
  "sort": {},
  "totalElements": 0,
  "totalPages": 0
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|content|[[WithdrawalsTransactionsVm](#schemawithdrawalstransactionsvm)]|false|No description|
|first|boolean|false|No description|
|last|boolean|false|No description|
|number|integer(int32)|false|No description|
|numberOfElements|integer(int32)|false|No description|
|size|integer(int32)|false|No description|
|sort|[Sort](#schemasort)|false|No description|
|totalElements|integer(int64)|false|No description|
|totalPages|integer(int32)|false|No description|


<h2 id="tocSpartnerpage">PartnerPage</h2>


<a id="schemapartnerpage"></a>


```json
{
  "approved": 0,
  "content": [
    {
      "address": "string",
      "address2": "string",
      "altAutosellInternal": true,
      "authorizedSignerContact": {
        "address": "string",
        "address2": "string",
        "beneficiaryPercent": 0,
        "birthDate": "2018-01-08",
        "city": "string",
        "file": "string",
        "fileBytes": "string",
        "fileContentType": "string",
        "firstName": "string",
        "gender": "MALE",
        "id": 0,
        "lastName": "string",
        "nationality": "string",
        "note": "string",
        "passportExpiryDate": "2018-01-08",
        "passportIssueDate": "2018-01-08",
        "passportNumber": "string",
        "position": "string",
        "primaryEmailAddress": "string",
        "primaryMobilePhone": "string",
        "secondaryEmailAddress": "string",
        "secondaryMobilePhone": "string",
        "state": {
          "abbreviation": "string",
          "id": 0,
          "state": "string"
        },
        "zip": "string"
      },
      "autosell": true,
      "canEditOnboarded": true,
      "city": "string",
      "commissionFee": 0,
      "companyEIN": "string",
      "companyWebsite": "string",
      "createdDate": "2018-01-08T16:57:23Z",
      "customers": 0,
      "emailAddress": "string",
      "enabled": true,
      "enroledBy": {
        "address": "string",
        "altAutosellInternal": true,
        "associateType": "ALT36",
        "autosell": true,
        "beneficiaryPercent": 0,
        "canEditOnboarded": true,
        "city": "string",
        "coinaPultApiKey": "string",
        "commissionFee": 0,
        "companyEIN": "string",
        "companyWebsite": "string",
        "createdDate": "2018-01-08T16:57:23Z",
        "cryptoCapitalApiKey": "string",
        "customers": 0,
        "deletedDate": "2018-01-08T16:57:23Z",
        "emailAddress": "string",
        "enabled": true,
        "enrolledBy": null,
        "id": 0,
        "incorporationDate": "2018-01-08",
        "internalFee": 0,
        "legalBusinessName": "string",
        "locationsCount": 0,
        "merchants": 0,
        "note": "string",
        "partners": 0,
        "phone": "string",
        "posCount": 0,
        "state": {
          "abbreviation": "string",
          "id": 0,
          "state": "string"
        },
        "usBankAccount": "string",
        "vendors": 0,
        "zip": "string"
      },
      "id": 0,
      "incorporationDate": "2018-01-08",
      "legalBusinessName": "string",
      "locationsCount": 0,
      "mainContact": {
        "address": "string",
        "address2": "string",
        "beneficiaryPercent": 0,
        "birthDate": "2018-01-08",
        "city": "string",
        "file": "string",
        "fileBytes": "string",
        "fileContentType": "string",
        "firstName": "string",
        "gender": "MALE",
        "id": 0,
        "lastName": "string",
        "nationality": "string",
        "note": "string",
        "passportExpiryDate": "2018-01-08",
        "passportIssueDate": "2018-01-08",
        "passportNumber": "string",
        "position": "string",
        "primaryEmailAddress": "string",
        "primaryMobilePhone": "string",
        "secondaryEmailAddress": "string",
        "secondaryMobilePhone": "string",
        "state": {
          "abbreviation": "string",
          "id": 0,
          "state": "string"
        },
        "zip": "string"
      },
      "merchants": 0,
      "note": "string",
      "partners": 0,
      "phone": "string",
      "posCount": 0,
      "saleVolume": 0,
      "state": {
        "abbreviation": "string",
        "id": 0,
        "state": "string"
      },
      "usBankAccount": "string",
      "user": {
        "email": "john.doe@example.com",
        "firstName": "string",
        "lastName": "string",
        "login": "string"
      },
      "vendors": 0,
      "zip": "string"
    }
  ],
  "first": true,
  "last": true,
  "number": 0,
  "numberOfElements": 0,
  "pending": 0,
  "size": 0,
  "totalElements": 0,
  "totalPages": 0
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|approved|integer(int64)|false|No description|
|content|[[NewPartnerVM](#schemanewpartnervm)]|false|No description|
|first|boolean|false|No description|
|last|boolean|false|No description|
|number|integer(int32)|false|No description|
|numberOfElements|integer(int32)|false|No description|
|pending|integer(int64)|false|No description|
|size|integer(int32)|false|No description|
|totalElements|integer(int64)|false|No description|
|totalPages|integer(int32)|false|No description|


<h2 id="tocSpaymentstransactionvm">PaymentsTransactionVm</h2>


<a id="schemapaymentstransactionvm"></a>


```json
{
  "amount": "string",
  "id": 0,
  "receiver": "string",
  "receiverType": "string",
  "sender": "string",
  "senderType": "string",
  "status": "string",
  "timeAndDate": "2018-01-08T16:57:23Z",
  "transactionId": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|amount|string|false|No description|
|id|integer(int64)|false|No description|
|receiver|string|false|No description|
|receiverType|string|false|No description|
|sender|string|false|No description|
|senderType|string|false|No description|
|status|string|false|No description|
|timeAndDate|string(date-time)|false|No description|
|transactionId|string|false|No description|


<h2 id="tocSpendingtransaction">PendingTransaction</h2>


<a id="schemapendingtransaction"></a>


```json
{
  "accompliceAssociate": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "commissionFee": 0,
  "dateTime": "2018-01-08T16:57:23Z",
  "destinationAddress": "string",
  "direction": "IN",
  "externalWallet": {
    "address": "string",
    "associate": {
      "address": "string",
      "altAutosellInternal": true,
      "associateType": "ALT36",
      "autosell": true,
      "beneficiaryPercent": 0,
      "canEditOnboarded": true,
      "city": "string",
      "coinaPultApiKey": "string",
      "commissionFee": 0,
      "companyEIN": "string",
      "companyWebsite": "string",
      "createdDate": "2018-01-08T16:57:23Z",
      "cryptoCapitalApiKey": "string",
      "customers": 0,
      "deletedDate": "2018-01-08T16:57:23Z",
      "emailAddress": "string",
      "enabled": true,
      "enrolledBy": null,
      "id": 0,
      "incorporationDate": "2018-01-08",
      "internalFee": 0,
      "legalBusinessName": "string",
      "locationsCount": 0,
      "merchants": 0,
      "note": "string",
      "partners": 0,
      "phone": "string",
      "posCount": 0,
      "state": {
        "abbreviation": "string",
        "id": 0,
        "state": "string"
      },
      "usBankAccount": "string",
      "vendors": 0,
      "zip": "string"
    },
    "id": 0,
    "name": "string",
    "note": "string",
    "walletType": "JAXX"
  },
  "id": 0,
  "location": {
    "address": "string",
    "address2": "string",
    "associate": {
      "address": "string",
      "altAutosellInternal": true,
      "associateType": "ALT36",
      "autosell": true,
      "beneficiaryPercent": 0,
      "canEditOnboarded": true,
      "city": "string",
      "coinaPultApiKey": "string",
      "commissionFee": 0,
      "companyEIN": "string",
      "companyWebsite": "string",
      "createdDate": "2018-01-08T16:57:23Z",
      "cryptoCapitalApiKey": "string",
      "customers": 0,
      "deletedDate": "2018-01-08T16:57:23Z",
      "emailAddress": "string",
      "enabled": true,
      "enrolledBy": null,
      "id": 0,
      "incorporationDate": "2018-01-08",
      "internalFee": 0,
      "legalBusinessName": "string",
      "locationsCount": 0,
      "merchants": 0,
      "note": "string",
      "partners": 0,
      "phone": "string",
      "posCount": 0,
      "state": {
        "abbreviation": "string",
        "id": 0,
        "state": "string"
      },
      "usBankAccount": "string",
      "vendors": 0,
      "zip": "string"
    },
    "city": "string",
    "country": "string",
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "file": "string",
    "geoLocation": "string",
    "id": 0,
    "name": "string",
    "note": "string",
    "parentLocation": null,
    "phone": "string",
    "pointOfSales": [
      {
        "active": true,
        "deletedDate": "2018-01-08T16:57:23Z",
        "id": 0,
        "inventoryNumber": "string",
        "location": null,
        "name": "string",
        "note": "string",
        "pointOfSaleType": "GREENBITS",
        "virtualPointOfSalesEnabled": true
      }
    ],
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "website": "string",
    "zip": "string"
  },
  "note": "string",
  "originalAmount": 0,
  "ownerAssociate": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "pointOfSale": {
    "active": true,
    "deletedDate": "2018-01-08T16:57:23Z",
    "id": 0,
    "inventoryNumber": "string",
    "location": {
      "address": "string",
      "address2": "string",
      "associate": {
        "address": "string",
        "altAutosellInternal": true,
        "associateType": "ALT36",
        "autosell": true,
        "beneficiaryPercent": 0,
        "canEditOnboarded": true,
        "city": "string",
        "coinaPultApiKey": "string",
        "commissionFee": 0,
        "companyEIN": "string",
        "companyWebsite": "string",
        "createdDate": "2018-01-08T16:57:23Z",
        "cryptoCapitalApiKey": "string",
        "customers": 0,
        "deletedDate": "2018-01-08T16:57:23Z",
        "emailAddress": "string",
        "enabled": true,
        "enrolledBy": null,
        "id": 0,
        "incorporationDate": "2018-01-08",
        "internalFee": 0,
        "legalBusinessName": "string",
        "locationsCount": 0,
        "merchants": 0,
        "note": "string",
        "partners": 0,
        "phone": "string",
        "posCount": 0,
        "state": {
          "abbreviation": "string",
          "id": 0,
          "state": "string"
        },
        "usBankAccount": "string",
        "vendors": 0,
        "zip": "string"
      },
      "city": "string",
      "country": "string",
      "deletedDate": "2018-01-08T16:57:23Z",
      "emailAddress": "string",
      "file": "string",
      "geoLocation": "string",
      "id": 0,
      "name": "string",
      "note": "string",
      "parentLocation": null,
      "phone": "string",
      "pointOfSales": [
        null
      ],
      "state": {
        "abbreviation": "string",
        "id": 0,
        "state": "string"
      },
      "website": "string",
      "zip": "string"
    },
    "name": "string",
    "note": "string",
    "pointOfSaleType": "GREENBITS",
    "virtualPointOfSalesEnabled": true
  },
  "rawTransaction": "string",
  "rawTxId": "string",
  "type": "string",
  "user": {
    "accountNonExpired": true,
    "accountNonLocked": true,
    "activated": true,
    "associate": {
      "address": "string",
      "altAutosellInternal": true,
      "associateType": "ALT36",
      "autosell": true,
      "beneficiaryPercent": 0,
      "canEditOnboarded": true,
      "city": "string",
      "coinaPultApiKey": "string",
      "commissionFee": 0,
      "companyEIN": "string",
      "companyWebsite": "string",
      "createdDate": "2018-01-08T16:57:23Z",
      "cryptoCapitalApiKey": "string",
      "customers": 0,
      "deletedDate": "2018-01-08T16:57:23Z",
      "emailAddress": "string",
      "enabled": true,
      "enrolledBy": null,
      "id": 0,
      "incorporationDate": "2018-01-08",
      "internalFee": 0,
      "legalBusinessName": "string",
      "locationsCount": 0,
      "merchants": 0,
      "note": "string",
      "partners": 0,
      "phone": "string",
      "posCount": 0,
      "state": {
        "abbreviation": "string",
        "id": 0,
        "state": "string"
      },
      "usBankAccount": "string",
      "vendors": 0,
      "zip": "string"
    },
    "credentialsNonExpired": true,
    "email": "john.doe@example.com",
    "enabled": true,
    "firstName": "string",
    "id": 0,
    "imageUrl": "string",
    "langKey": "strin",
    "lastLoginDateTime": "2018-01-08T16:57:23Z",
    "lastName": "string",
    "location": {
      "address": "string",
      "address2": "string",
      "associate": {
        "address": "string",
        "altAutosellInternal": true,
        "associateType": "ALT36",
        "autosell": true,
        "beneficiaryPercent": 0,
        "canEditOnboarded": true,
        "city": "string",
        "coinaPultApiKey": "string",
        "commissionFee": 0,
        "companyEIN": "string",
        "companyWebsite": "string",
        "createdDate": "2018-01-08T16:57:23Z",
        "cryptoCapitalApiKey": "string",
        "customers": 0,
        "deletedDate": "2018-01-08T16:57:23Z",
        "emailAddress": "string",
        "enabled": true,
        "enrolledBy": null,
        "id": 0,
        "incorporationDate": "2018-01-08",
        "internalFee": 0,
        "legalBusinessName": "string",
        "locationsCount": 0,
        "merchants": 0,
        "note": "string",
        "partners": 0,
        "phone": "string",
        "posCount": 0,
        "state": {
          "abbreviation": "string",
          "id": 0,
          "state": "string"
        },
        "usBankAccount": "string",
        "vendors": 0,
        "zip": "string"
      },
      "city": "string",
      "country": "string",
      "deletedDate": "2018-01-08T16:57:23Z",
      "emailAddress": "string",
      "file": "string",
      "geoLocation": "string",
      "id": 0,
      "name": "string",
      "note": "string",
      "parentLocation": null,
      "phone": "string",
      "pointOfSales": [
        {
          "active": true,
          "deletedDate": "2018-01-08T16:57:23Z",
          "id": 0,
          "inventoryNumber": "string",
          "location": null,
          "name": "string",
          "note": "string",
          "pointOfSaleType": "GREENBITS",
          "virtualPointOfSalesEnabled": true
        }
      ],
      "state": {
        "abbreviation": "string",
        "id": 0,
        "state": "string"
      },
      "website": "string",
      "zip": "string"
    },
    "login": "string",
    "resetDate": "2018-01-08T16:57:23Z",
    "splashscreenEnabled": true,
    "using2fa": true
  }
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|accompliceAssociate|[Associate](#schemaassociate)|false|No description|
|commissionFee|integer(int64)|false|No description|
|dateTime|string(date-time)|false|No description|
|destinationAddress|string|false|No description|
|direction|string|false|No description|
|externalWallet|[ExternalWallet](#schemaexternalwallet)|false|No description|
|id|integer(int64)|false|No description|
|location|[Location](#schemalocation)|false|No description|
|note|string|false|No description|
|originalAmount|integer(int64)|false|No description|
|ownerAssociate|[Associate](#schemaassociate)|false|No description|
|pointOfSale|[PointOfSale](#schemapointofsale)|false|No description|
|rawTransaction|string|false|No description|
|rawTxId|string|false|No description|
|type|string|false|No description|
|user|[User](#schemauser)|false|No description|


#### Enumerated Values


|Property|Value|
|---|---|
|direction|IN|
|direction|OUT|


<h2 id="tocSpointofsale">PointOfSale</h2>


<a id="schemapointofsale"></a>


```json
{
  "active": true,
  "deletedDate": "2018-01-08T16:57:23Z",
  "id": 0,
  "inventoryNumber": "string",
  "location": {
    "address": "string",
    "address2": "string",
    "associate": {
      "address": "string",
      "altAutosellInternal": true,
      "associateType": "ALT36",
      "autosell": true,
      "beneficiaryPercent": 0,
      "canEditOnboarded": true,
      "city": "string",
      "coinaPultApiKey": "string",
      "commissionFee": 0,
      "companyEIN": "string",
      "companyWebsite": "string",
      "createdDate": "2018-01-08T16:57:23Z",
      "cryptoCapitalApiKey": "string",
      "customers": 0,
      "deletedDate": "2018-01-08T16:57:23Z",
      "emailAddress": "string",
      "enabled": true,
      "enrolledBy": null,
      "id": 0,
      "incorporationDate": "2018-01-08",
      "internalFee": 0,
      "legalBusinessName": "string",
      "locationsCount": 0,
      "merchants": 0,
      "note": "string",
      "partners": 0,
      "phone": "string",
      "posCount": 0,
      "state": {
        "abbreviation": "string",
        "id": 0,
        "state": "string"
      },
      "usBankAccount": "string",
      "vendors": 0,
      "zip": "string"
    },
    "city": "string",
    "country": "string",
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "file": "string",
    "geoLocation": "string",
    "id": 0,
    "name": "string",
    "note": "string",
    "parentLocation": null,
    "phone": "string",
    "pointOfSales": [
      null
    ],
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "website": "string",
    "zip": "string"
  },
  "name": "string",
  "note": "string",
  "pointOfSaleType": "GREENBITS",
  "virtualPointOfSalesEnabled": true
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|active|boolean|false|No description|
|deletedDate|string(date-time)|false|No description|
|id|integer(int64)|false|No description|
|inventoryNumber|string|false|No description|
|location|[Location](#schemalocation)|true|No description|
|name|string|false|No description|
|note|string|false|No description|
|pointOfSaleType|string|true|No description|
|virtualPointOfSalesEnabled|boolean|true|No description|


#### Enumerated Values


|Property|Value|
|---|---|
|pointOfSaleType|GREENBITS|
|pointOfSaleType|OTHER|
|pointOfSaleType|VIRTUAL|


<h2 id="tocSposfordashboardvm">PosForDashboardVm</h2>


<a id="schemaposfordashboardvm"></a>


```json
{
  "address": "string",
  "city": "string",
  "geolocation": "string",
  "id": 0,
  "name": "string",
  "noofpos": 0,
  "state": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|address|string|false|No description|
|city|string|false|No description|
|geolocation|string|false|No description|
|id|integer(int64)|false|No description|
|name|string|false|No description|
|noofpos|integer(int64)|false|No description|
|state|string|false|No description|


<h2 id="tocSrequestfordeleteacssociate">RequestForDeleteAcssociate</h2>


<a id="schemarequestfordeleteacssociate"></a>


```json
{
  "associateDelete": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "dateRequested": "2018-01-08T16:57:23Z",
  "id": 0,
  "reason": "stringstri",
  "requestedBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  }
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|associateDelete|[Associate](#schemaassociate)|true|No description|
|dateRequested|string(date-time)|false|No description|
|id|integer(int64)|false|No description|
|reason|string|true|No description|
|requestedBy|[Associate](#schemaassociate)|false|No description|


<h2 id="tocSresetpasswordvm">ResetPasswordVM</h2>


<a id="schemaresetpasswordvm"></a>


```json
{
  "email": "john.doe@example.com"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|email|string|true|No description|


<h2 id="tocSresponseentity">ResponseEntity</h2>


<a id="schemaresponseentity"></a>


```json
{
  "body": {},
  "statusCode": "100",
  "statusCodeValue": 0
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|body|object|false|No description|
|statusCode|string|false|No description|
|statusCodeValue|integer(int32)|false|No description|


#### Enumerated Values


|Property|Value|
|---|---|
|statusCode|100|
|statusCode|101|
|statusCode|102|
|statusCode|103|
|statusCode|200|
|statusCode|201|
|statusCode|202|
|statusCode|203|
|statusCode|204|
|statusCode|205|
|statusCode|206|
|statusCode|207|
|statusCode|208|
|statusCode|226|
|statusCode|300|
|statusCode|301|
|statusCode|302|
|statusCode|303|
|statusCode|304|
|statusCode|305|
|statusCode|307|
|statusCode|308|
|statusCode|400|
|statusCode|401|
|statusCode|402|
|statusCode|403|
|statusCode|404|
|statusCode|405|
|statusCode|406|
|statusCode|407|
|statusCode|408|
|statusCode|409|
|statusCode|410|
|statusCode|411|
|statusCode|412|
|statusCode|413|
|statusCode|414|
|statusCode|415|
|statusCode|416|
|statusCode|417|
|statusCode|418|
|statusCode|419|
|statusCode|420|
|statusCode|421|
|statusCode|422|
|statusCode|423|
|statusCode|424|
|statusCode|426|
|statusCode|428|
|statusCode|429|
|statusCode|431|
|statusCode|451|
|statusCode|500|
|statusCode|501|
|statusCode|502|
|statusCode|503|
|statusCode|504|
|statusCode|505|
|statusCode|506|
|statusCode|507|
|statusCode|508|
|statusCode|509|
|statusCode|510|
|statusCode|511|


<h2 id="tocSsalestransactionvm">SalesTransactionVM</h2>


<a id="schemasalestransactionvm"></a>


```json
{
  "amountInDash": "string",
  "amountInUSD": "string",
  "commisionFeeinDash": "string",
  "commisionFeeinUSD": "string",
  "id": 0,
  "location": "string",
  "pointOfSale": "string",
  "status": "string",
  "timeAndDate": "2018-01-08T16:57:23Z",
  "transactionId": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|amountInDash|string|false|No description|
|amountInUSD|string|false|No description|
|commisionFeeinDash|string|false|No description|
|commisionFeeinUSD|string|false|No description|
|id|integer(int64)|false|No description|
|location|string|false|No description|
|pointOfSale|string|false|No description|
|status|string|false|No description|
|timeAndDate|string(date-time)|false|No description|
|transactionId|string|false|No description|


<h2 id="tocSselfregistercustomervm">SelfRegisterCustomerVM</h2>


<a id="schemaselfregistercustomervm"></a>


```json
{
  "emailAddress": "string",
  "legalBusinessName": "string",
  "phone": "string",
  "user": {
    "email": "john.doe@example.com",
    "firstName": "string",
    "lastName": "string",
    "login": "string",
    "password": "string"
  }
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|emailAddress|string|true|No description|
|legalBusinessName|string|true|No description|
|phone|string|true|No description|
|user|[CreateAssociateAdminUserWithPasswordVM](#schemacreateassociateadminuserwithpasswordvm)|true|No description|

<h2 id="tocSloginvm">LoginVM</h2>


<a id="schemaloginvm"></a>


```json
{
  "password": "string",
  "rememberMe": true,
  "username": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|password|string|false|No description|
|rememberMe|boolean|false|No description|
|username|string|true|No description|


<h2 id="tocSmerchantvendor">MerchantVendor</h2>


<a id="schemamerchantvendor"></a>


```json
{
  "id": 0,
  "merchant": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "note": "string",
  "vendor": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  }
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|id|integer(int64)|false|No description|
|merchant|[Associate](#schemaassociate)|true|No description|
|note|string|false|No description|
|vendor|[Associate](#schemaassociate)|true|No description|


<h2 id="tocSnewcustomervm">NewCustomerVM</h2>


<a id="schemanewcustomervm"></a>


```json
{
  "emailAddress": "string",
  "id": 0,
  "legalBusinessName": "string",
  "phone": "string",
  "user": {
    "email": "john.doe@example.com",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  }
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|emailAddress|string|true|No description|
|id|integer(int64)|false|No description|
|legalBusinessName|string|true|No description|
|phone|string|true|No description|
|user|[CreateAssociateAdminUserVM](#schemacreateassociateadminuservm)|true|No description|


<h2 id="tocSnewmerchantvm">NewMerchantVM</h2>


<a id="schemanewmerchantvm"></a>


```json
{
  "address": "string",
  "address2": "string",
  "altAutosellInternal": true,
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "autosell": true,
  "beneficiaryPercent": 0,
  "canEditOnboarded": true,
  "city": "string",
  "commissionFee": 0,
  "companyEIN": "string",
  "companyWebsite": "string",
  "createdDate": "2018-01-08T16:57:23Z",
  "customers": 0,
  "emailAddress": "string",
  "enabled": true,
  "enroledBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "id": 0,
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "locationsCount": 0,
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "merchants": 0,
  "note": "string",
  "partners": 0,
  "phone": "string",
  "posCount": 0,
  "saleVolume": 0,
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "john.doe@example.com",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  },
  "vendors": 0,
  "zip": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|address|string|true|No description|
|address2|string|false|No description|
|altAutosellInternal|boolean|false|No description|
|authorizedSignerContact|[ContactVM](#schemacontactvm)|true|No description|
|autosell|boolean|false|No description|
|beneficiaryPercent|integer(int64)|false|No description|
|canEditOnboarded|boolean|false|No description|
|city|string|true|No description|
|commissionFee|number|false|No description|
|companyEIN|string|true|No description|
|companyWebsite|string|false|No description|
|createdDate|string(date-time)|false|No description|
|customers|integer(int32)|false|No description|
|emailAddress|string|true|No description|
|enabled|boolean|false|No description|
|enroledBy|[Associate](#schemaassociate)|false|No description|
|id|integer(int64)|false|No description|
|incorporationDate|string(date)|true|No description|
|legalBusinessName|string|true|No description|
|locationsCount|integer(int32)|false|No description|
|mainContact|[ContactVM](#schemacontactvm)|true|No description|
|merchants|integer(int32)|false|No description|
|note|string|false|No description|
|partners|integer(int32)|false|No description|
|phone|string|true|No description|
|posCount|integer(int32)|false|No description|
|saleVolume|number(double)|false|No description|
|state|[CountryState](#schemacountrystate)|true|No description|
|usBankAccount|string|false|No description|
|user|[CreateAssociateAdminUserVM](#schemacreateassociateadminuservm)|false|No description|
|vendors|integer(int32)|false|No description|
|zip|string|true|No description|


<h2 id="tocSnewpartnervm">NewPartnerVM</h2>


<a id="schemanewpartnervm"></a>


```json
{
  "address": "string",
  "address2": "string",
  "altAutosellInternal": true,
  "authorizedSignerContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "autosell": true,
  "canEditOnboarded": true,
  "city": "string",
  "commissionFee": 0,
  "companyEIN": "string",
  "companyWebsite": "string",
  "createdDate": "2018-01-08T16:57:23Z",
  "customers": 0,
  "emailAddress": "string",
  "enabled": true,
  "enroledBy": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "id": 0,
  "incorporationDate": "2018-01-08",
  "legalBusinessName": "string",
  "locationsCount": 0,
  "mainContact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "file": "string",
    "fileBytes": "string",
    "fileContentType": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "zip": "string"
  },
  "merchants": 0,
  "note": "string",
  "partners": 0,
  "phone": "string",
  "posCount": 0,
  "saleVolume": 0,
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "usBankAccount": "string",
  "user": {
    "email": "john.doe@example.com",
    "firstName": "string",
    "lastName": "string",
    "login": "string"
  },
  "vendors": 0,
  "zip": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|address|string|true|No description|
|address2|string|false|No description|
|altAutosellInternal|boolean|false|No description|
|authorizedSignerContact|[ContactVM](#schemacontactvm)|true|No description|
|autosell|boolean|false|No description|
|canEditOnboarded|boolean|false|No description|
|city|string|true|No description|
|commissionFee|number|false|No description|
|companyEIN|string|true|No description|
|companyWebsite|string|false|No description|
|createdDate|string(date-time)|false|No description|
|customers|integer(int32)|false|No description|
|emailAddress|string|true|No description|
|enabled|boolean|false|No description|
|enroledBy|[Associate](#schemaassociate)|false|No description|
|id|integer(int64)|false|No description|
|incorporationDate|string(date)|false|No description|
|legalBusinessName|string|true|No description|
|locationsCount|integer(int32)|false|No description|
|mainContact|[ContactVM](#schemacontactvm)|true|No description|
|merchants|integer(int32)|false|No description|
|note|string|false|No description|
|partners|integer(int32)|false|No description|
|phone|string|true|No description|
|posCount|integer(int32)|false|No description|
|saleVolume|number(double)|false|No description|
|state|[CountryState](#schemacountrystate)|true|No description|
|usBankAccount|string|false|No description|
|user|[CreateAssociateAdminUserVM](#schemacreateassociateadminuservm)|false|No description|
|vendors|integer(int32)|false|No description|
|zip|string|true|No description|


<h2 id="tocSpageofassociate">PageOfAssociate</h2>


<a id="schemapageofassociate"></a>


```json
{
  "content": [
    {
      "address": "string",
      "altAutosellInternal": true,
      "associateType": "ALT36",
      "autosell": true,
      "beneficiaryPercent": 0,
      "canEditOnboarded": true,
      "city": "string",
      "coinaPultApiKey": "string",
      "commissionFee": 0,
      "companyEIN": "string",
      "companyWebsite": "string",
      "createdDate": "2018-01-08T16:57:23Z",
      "cryptoCapitalApiKey": "string",
      "customers": 0,
      "deletedDate": "2018-01-08T16:57:23Z",
      "emailAddress": "string",
      "enabled": true,
      "enrolledBy": null,
      "id": 0,
      "incorporationDate": "2018-01-08",
      "internalFee": 0,
      "legalBusinessName": "string",
      "locationsCount": 0,
      "merchants": 0,
      "note": "string",
      "partners": 0,
      "phone": "string",
      "posCount": 0,
      "state": {
        "abbreviation": "string",
        "id": 0,
        "state": "string"
      },
      "usBankAccount": "string",
      "vendors": 0,
      "zip": "string"
    }
  ],
  "first": true,
  "last": true,
  "number": 0,
  "numberOfElements": 0,
  "size": 0,
  "sort": {},
  "totalElements": 0,
  "totalPages": 0
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|content|[[Associate](#schemaassociate)]|false|No description|
|first|boolean|false|No description|
|last|boolean|false|No description|
|number|integer(int32)|false|No description|
|numberOfElements|integer(int32)|false|No description|
|size|integer(int32)|false|No description|
|sort|[Sort](#schemasort)|false|No description|
|totalElements|integer(int64)|false|No description|
|totalPages|integer(int32)|false|No description|


<h2 id="tocSpageofconversionstransactionsvm">PageOfConversionsTransactionsVM</h2>


<a id="schemapageofconversionstransactionsvm"></a>


```json
{
  "content": [
    {
      "amountDash": "string",
      "amountFiat": "string",
      "conversionFrom": "string",
      "conversionRate": "string",
      "conversionTo": "string",
      "id": 0,
      "status": "string",
      "timeAndDate": "2018-01-08T16:57:23Z",
      "transactionId": "string"
    }
  ],
  "first": true,
  "last": true,
  "number": 0,
  "numberOfElements": 0,
  "size": 0,
  "sort": {},
  "totalElements": 0,
  "totalPages": 0
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|content|[[ConversionsTransactionsVM](#schemaconversionstransactionsvm)]|false|No description|
|first|boolean|false|No description|
|last|boolean|false|No description|
|number|integer(int32)|false|No description|
|numberOfElements|integer(int32)|false|No description|
|size|integer(int32)|false|No description|
|sort|[Sort](#schemasort)|false|No description|
|totalElements|integer(int64)|false|No description|
|totalPages|integer(int32)|false|No description|


<h2 id="tocSpageofinvitation">PageOfInvitation</h2>


<a id="schemapageofinvitation"></a>


```json
{
  "content": [
    {
      "acceptedDateTime": "2018-01-08T16:57:23Z",
      "associateType": "ALT36",
      "id": 0,
      "inviteKey": "string",
      "invitedMail": "string",
      "ivitationDateTime": "2018-01-08T16:57:23Z",
      "mailSent": true
    }
  ],
  "first": true,
  "last": true,
  "number": 0,
  "numberOfElements": 0,
  "size": 0,
  "sort": {},
  "totalElements": 0,
  "totalPages": 0
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|content|[[Invitation](#schemainvitation)]|false|No description|
|first|boolean|false|No description|
|last|boolean|false|No description|
|number|integer(int32)|false|No description|
|numberOfElements|integer(int32)|false|No description|
|size|integer(int32)|false|No description|
|sort|[Sort](#schemasort)|false|No description|
|totalElements|integer(int64)|false|No description|
|totalPages|integer(int32)|false|No description|


<h2 id="tocSpageoflocation">PageOfLocation</h2>


<a id="schemapageoflocation"></a>


```json
{
  "content": [
    {
      "address": "string",
      "address2": "string",
      "associate": {
        "address": "string",
        "altAutosellInternal": true,
        "associateType": "ALT36",
        "autosell": true,
        "beneficiaryPercent": 0,
        "canEditOnboarded": true,
        "city": "string",
        "coinaPultApiKey": "string",
        "commissionFee": 0,
        "companyEIN": "string",
        "companyWebsite": "string",
        "createdDate": "2018-01-08T16:57:23Z",
        "cryptoCapitalApiKey": "string",
        "customers": 0,
        "deletedDate": "2018-01-08T16:57:23Z",
        "emailAddress": "string",
        "enabled": true,
        "enrolledBy": null,
        "id": 0,
        "incorporationDate": "2018-01-08",
        "internalFee": 0,
        "legalBusinessName": "string",
        "locationsCount": 0,
        "merchants": 0,
        "note": "string",
        "partners": 0,
        "phone": "string",
        "posCount": 0,
        "state": {
          "abbreviation": "string",
          "id": 0,
          "state": "string"
        },
        "usBankAccount": "string",
        "vendors": 0,
        "zip": "string"
      },
      "city": "string",
      "country": "string",
      "deletedDate": "2018-01-08T16:57:23Z",
      "emailAddress": "string",
      "file": "string",
      "geoLocation": "string",
      "id": 0,
      "name": "string",
      "note": "string",
      "parentLocation": null,
      "phone": "string",
      "pointOfSales": [
        {
          "active": true,
          "deletedDate": "2018-01-08T16:57:23Z",
          "id": 0,
          "inventoryNumber": "string",
          "location": null,
          "name": "string",
          "note": "string",
          "pointOfSaleType": "GREENBITS",
          "virtualPointOfSalesEnabled": true
        }
      ],
      "state": {
        "abbreviation": "string",
        "id": 0,
        "state": "string"
      },
      "website": "string",
      "zip": "string"
    }
  ],
  "first": true,
  "last": true,
  "number": 0,
  "numberOfElements": 0,
  "size": 0,
  "sort": {},
  "totalElements": 0,
  "totalPages": 0
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|content|[[Location](#schemalocation)]|false|No description|
|first|boolean|false|No description|
|last|boolean|false|No description|
|number|integer(int32)|false|No description|
|numberOfElements|integer(int32)|false|No description|
|size|integer(int32)|false|No description|
|sort|[Sort](#schemasort)|false|No description|
|totalElements|integer(int64)|false|No description|
|totalPages|integer(int32)|false|No description|


<h2 id="tocSpageofmerchantvendor">PageOfMerchantVendor</h2>


<a id="schemapageofmerchantvendor"></a>


```json
{
  "content": [
    {
      "id": 0,
      "merchant": {
        "address": "string",
        "altAutosellInternal": true,
        "associateType": "ALT36",
        "autosell": true,
        "beneficiaryPercent": 0,
        "canEditOnboarded": true,
        "city": "string",
        "coinaPultApiKey": "string",
        "commissionFee": 0,
        "companyEIN": "string",
        "companyWebsite": "string",
        "createdDate": "2018-01-08T16:57:23Z",
        "cryptoCapitalApiKey": "string",
        "customers": 0,
        "deletedDate": "2018-01-08T16:57:23Z",
        "emailAddress": "string",
        "enabled": true,
        "enrolledBy": null,
        "id": 0,
        "incorporationDate": "2018-01-08",
        "internalFee": 0,
        "legalBusinessName": "string",
        "locationsCount": 0,
        "merchants": 0,
        "note": "string",
        "partners": 0,
        "phone": "string",
        "posCount": 0,
        "state": {
          "abbreviation": "string",
          "id": 0,
          "state": "string"
        },
        "usBankAccount": "string",
        "vendors": 0,
        "zip": "string"
      },
      "note": "string",
      "vendor": {
        "address": "string",
        "altAutosellInternal": true,
        "associateType": "ALT36",
        "autosell": true,
        "beneficiaryPercent": 0,
        "canEditOnboarded": true,
        "city": "string",
        "coinaPultApiKey": "string",
        "commissionFee": 0,
        "companyEIN": "string",
        "companyWebsite": "string",
        "createdDate": "2018-01-08T16:57:23Z",
        "cryptoCapitalApiKey": "string",
        "customers": 0,
        "deletedDate": "2018-01-08T16:57:23Z",
        "emailAddress": "string",
        "enabled": true,
        "enrolledBy": null,
        "id": 0,
        "incorporationDate": "2018-01-08",
        "internalFee": 0,
        "legalBusinessName": "string",
        "locationsCount": 0,
        "merchants": 0,
        "note": "string",
        "partners": 0,
        "phone": "string",
        "posCount": 0,
        "state": {
          "abbreviation": "string",
          "id": 0,
          "state": "string"
        },
        "usBankAccount": "string",
        "vendors": 0,
        "zip": "string"
      }
    }
  ],
  "first": true,
  "last": true,
  "number": 0,
  "numberOfElements": 0,
  "size": 0,
  "sort": {},
  "totalElements": 0,
  "totalPages": 0
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|content|[[MerchantVendor](#schemamerchantvendor)]|false|No description|
|first|boolean|false|No description|
|last|boolean|false|No description|
|number|integer(int32)|false|No description|
|numberOfElements|integer(int32)|false|No description|
|size|integer(int32)|false|No description|
|sort|[Sort](#schemasort)|false|No description|
|totalElements|integer(int64)|false|No description|
|totalPages|integer(int32)|false|No description|


<h2 id="tocSpageofnewpartnervm">PageOfNewPartnerVM</h2>


<a id="schemapageofnewpartnervm"></a>


```json
{
  "content": [
    {
      "address": "string",
      "address2": "string",
      "altAutosellInternal": true,
      "authorizedSignerContact": {
        "address": "string",
        "address2": "string",
        "beneficiaryPercent": 0,
        "birthDate": "2018-01-08",
        "city": "string",
        "file": "string",
        "fileBytes": "string",
        "fileContentType": "string",
        "firstName": "string",
        "gender": "MALE",
        "id": 0,
        "lastName": "string",
        "nationality": "string",
        "note": "string",
        "passportExpiryDate": "2018-01-08",
        "passportIssueDate": "2018-01-08",
        "passportNumber": "string",
        "position": "string",
        "primaryEmailAddress": "string",
        "primaryMobilePhone": "string",
        "secondaryEmailAddress": "string",
        "secondaryMobilePhone": "string",
        "state": {
          "abbreviation": "string",
          "id": 0,
          "state": "string"
        },
        "zip": "string"
      },
      "autosell": true,
      "canEditOnboarded": true,
      "city": "string",
      "commissionFee": 0,
      "companyEIN": "string",
      "companyWebsite": "string",
      "createdDate": "2018-01-08T16:57:23Z",
      "customers": 0,
      "emailAddress": "string",
      "enabled": true,
      "enroledBy": {
        "address": "string",
        "altAutosellInternal": true,
        "associateType": "ALT36",
        "autosell": true,
        "beneficiaryPercent": 0,
        "canEditOnboarded": true,
        "city": "string",
        "coinaPultApiKey": "string",
        "commissionFee": 0,
        "companyEIN": "string",
        "companyWebsite": "string",
        "createdDate": "2018-01-08T16:57:23Z",
        "cryptoCapitalApiKey": "string",
        "customers": 0,
        "deletedDate": "2018-01-08T16:57:23Z",
        "emailAddress": "string",
        "enabled": true,
        "enrolledBy": null,
        "id": 0,
        "incorporationDate": "2018-01-08",
        "internalFee": 0,
        "legalBusinessName": "string",
        "locationsCount": 0,
        "merchants": 0,
        "note": "string",
        "partners": 0,
        "phone": "string",
        "posCount": 0,
        "state": {
          "abbreviation": "string",
          "id": 0,
          "state": "string"
        },
        "usBankAccount": "string",
        "vendors": 0,
        "zip": "string"
      },
      "id": 0,
      "incorporationDate": "2018-01-08",
      "legalBusinessName": "string",
      "locationsCount": 0,
      "mainContact": {
        "address": "string",
        "address2": "string",
        "beneficiaryPercent": 0,
        "birthDate": "2018-01-08",
        "city": "string",
        "file": "string",
        "fileBytes": "string",
        "fileContentType": "string",
        "firstName": "string",
        "gender": "MALE",
        "id": 0,
        "lastName": "string",
        "nationality": "string",
        "note": "string",
        "passportExpiryDate": "2018-01-08",
        "passportIssueDate": "2018-01-08",
        "passportNumber": "string",
        "position": "string",
        "primaryEmailAddress": "string",
        "primaryMobilePhone": "string",
        "secondaryEmailAddress": "string",
        "secondaryMobilePhone": "string",
        "state": {
          "abbreviation": "string",
          "id": 0,
          "state": "string"
        },
        "zip": "string"
      },
      "merchants": 0,
      "note": "string",
      "partners": 0,
      "phone": "string",
      "posCount": 0,
      "saleVolume": 0,
      "state": {
        "abbreviation": "string",
        "id": 0,
        "state": "string"
      },
      "usBankAccount": "string",
      "user": {
        "email": "john.doe@example.com",
        "firstName": "string",
        "lastName": "string",
        "login": "string"
      },
      "vendors": 0,
      "zip": "string"
    }
  ],
  "first": true,
  "last": true,
  "number": 0,
  "numberOfElements": 0,
  "size": 0,
  "sort": {},
  "totalElements": 0,
  "totalPages": 0
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|content|[[NewPartnerVM](#schemanewpartnervm)]|false|No description|
|first|boolean|false|No description|
|last|boolean|false|No description|
|number|integer(int32)|false|No description|
|numberOfElements|integer(int32)|false|No description|
|size|integer(int32)|false|No description|
|sort|[Sort](#schemasort)|false|No description|
|totalElements|integer(int64)|false|No description|
|totalPages|integer(int32)|false|No description|


<h2 id="tocSpageofpaymentstransactionvm">PageOfPaymentsTransactionVm</h2>


<a id="schemapageofpaymentstransactionvm"></a>


```json
{
  "content": [
    {
      "amount": "string",
      "id": 0,
      "receiver": "string",
      "receiverType": "string",
      "sender": "string",
      "senderType": "string",
      "status": "string",
      "timeAndDate": "2018-01-08T16:57:23Z",
      "transactionId": "string"
    }
  ],
  "first": true,
  "last": true,
  "number": 0,
  "numberOfElements": 0,
  "size": 0,
  "sort": {},
  "totalElements": 0,
  "totalPages": 0
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|content|[[PaymentsTransactionVm](#schemapaymentstransactionvm)]|false|No description|
|first|boolean|false|No description|
|last|boolean|false|No description|
|number|integer(int32)|false|No description|
|numberOfElements|integer(int32)|false|No description|
|size|integer(int32)|false|No description|
|sort|[Sort](#schemasort)|false|No description|
|totalElements|integer(int64)|false|No description|
|totalPages|integer(int32)|false|No description|


<h2 id="tocSpageofpendingtransaction">PageOfPendingTransaction</h2>


<a id="schemapageofpendingtransaction"></a>


```json
{
  "content": [
    {
      "accompliceAssociate": {
        "address": "string",
        "altAutosellInternal": true,
        "associateType": "ALT36",
        "autosell": true,
        "beneficiaryPercent": 0,
        "canEditOnboarded": true,
        "city": "string",
        "coinaPultApiKey": "string",
        "commissionFee": 0,
        "companyEIN": "string",
        "companyWebsite": "string",
        "createdDate": "2018-01-08T16:57:23Z",
        "cryptoCapitalApiKey": "string",
        "customers": 0,
        "deletedDate": "2018-01-08T16:57:23Z",
        "emailAddress": "string",
        "enabled": true,
        "enrolledBy": null,
        "id": 0,
        "incorporationDate": "2018-01-08",
        "internalFee": 0,
        "legalBusinessName": "string",
        "locationsCount": 0,
        "merchants": 0,
        "note": "string",
        "partners": 0,
        "phone": "string",
        "posCount": 0,
        "state": {
          "abbreviation": "string",
          "id": 0,
          "state": "string"
        },
        "usBankAccount": "string",
        "vendors": 0,
        "zip": "string"
      },
      "commissionFee": 0,
      "dateTime": "2018-01-08T16:57:23Z",
      "destinationAddress": "string",
      "direction": "IN",
      "externalWallet": {
        "address": "string",
        "associate": {
          "address": "string",
          "altAutosellInternal": true,
          "associateType": "ALT36",
          "autosell": true,
          "beneficiaryPercent": 0,
          "canEditOnboarded": true,
          "city": "string",
          "coinaPultApiKey": "string",
          "commissionFee": 0,
          "companyEIN": "string",
          "companyWebsite": "string",
          "createdDate": "2018-01-08T16:57:23Z",
          "cryptoCapitalApiKey": "string",
          "customers": 0,
          "deletedDate": "2018-01-08T16:57:23Z",
          "emailAddress": "string",
          "enabled": true,
          "enrolledBy": null,
          "id": 0,
          "incorporationDate": "2018-01-08",
          "internalFee": 0,
          "legalBusinessName": "string",
          "locationsCount": 0,
          "merchants": 0,
          "note": "string",
          "partners": 0,
          "phone": "string",
          "posCount": 0,
          "state": {
            "abbreviation": "string",
            "id": 0,
            "state": "string"
          },
          "usBankAccount": "string",
          "vendors": 0,
          "zip": "string"
        },
        "id": 0,
        "name": "string",
        "note": "string",
        "walletType": "JAXX"
      },
      "id": 0,
      "location": {
        "address": "string",
        "address2": "string",
        "associate": {
          "address": "string",
          "altAutosellInternal": true,
          "associateType": "ALT36",
          "autosell": true,
          "beneficiaryPercent": 0,
          "canEditOnboarded": true,
          "city": "string",
          "coinaPultApiKey": "string",
          "commissionFee": 0,
          "companyEIN": "string",
          "companyWebsite": "string",
          "createdDate": "2018-01-08T16:57:23Z",
          "cryptoCapitalApiKey": "string",
          "customers": 0,
          "deletedDate": "2018-01-08T16:57:23Z",
          "emailAddress": "string",
          "enabled": true,
          "enrolledBy": null,
          "id": 0,
          "incorporationDate": "2018-01-08",
          "internalFee": 0,
          "legalBusinessName": "string",
          "locationsCount": 0,
          "merchants": 0,
          "note": "string",
          "partners": 0,
          "phone": "string",
          "posCount": 0,
          "state": {
            "abbreviation": "string",
            "id": 0,
            "state": "string"
          },
          "usBankAccount": "string",
          "vendors": 0,
          "zip": "string"
        },
        "city": "string",
        "country": "string",
        "deletedDate": "2018-01-08T16:57:23Z",
        "emailAddress": "string",
        "file": "string",
        "geoLocation": "string",
        "id": 0,
        "name": "string",
        "note": "string",
        "parentLocation": null,
        "phone": "string",
        "pointOfSales": [
          {
            "active": true,
            "deletedDate": "2018-01-08T16:57:23Z",
            "id": 0,
            "inventoryNumber": "string",
            "location": null,
            "name": "string",
            "note": "string",
            "pointOfSaleType": "GREENBITS",
            "virtualPointOfSalesEnabled": true
          }
        ],
        "state": {
          "abbreviation": "string",
          "id": 0,
          "state": "string"
        },
        "website": "string",
        "zip": "string"
      },
      "note": "string",
      "originalAmount": 0,
      "ownerAssociate": {
        "address": "string",
        "altAutosellInternal": true,
        "associateType": "ALT36",
        "autosell": true,
        "beneficiaryPercent": 0,
        "canEditOnboarded": true,
        "city": "string",
        "coinaPultApiKey": "string",
        "commissionFee": 0,
        "companyEIN": "string",
        "companyWebsite": "string",
        "createdDate": "2018-01-08T16:57:23Z",
        "cryptoCapitalApiKey": "string",
        "customers": 0,
        "deletedDate": "2018-01-08T16:57:23Z",
        "emailAddress": "string",
        "enabled": true,
        "enrolledBy": null,
        "id": 0,
        "incorporationDate": "2018-01-08",
        "internalFee": 0,
        "legalBusinessName": "string",
        "locationsCount": 0,
        "merchants": 0,
        "note": "string",
        "partners": 0,
        "phone": "string",
        "posCount": 0,
        "state": {
          "abbreviation": "string",
          "id": 0,
          "state": "string"
        },
        "usBankAccount": "string",
        "vendors": 0,
        "zip": "string"
      },
      "pointOfSale": {
        "active": true,
        "deletedDate": "2018-01-08T16:57:23Z",
        "id": 0,
        "inventoryNumber": "string",
        "location": {
          "address": "string",
          "address2": "string",
          "associate": {
            "address": "string",
            "altAutosellInternal": true,
            "associateType": "ALT36",
            "autosell": true,
            "beneficiaryPercent": 0,
            "canEditOnboarded": true,
            "city": "string",
            "coinaPultApiKey": "string",
            "commissionFee": 0,
            "companyEIN": "string",
            "companyWebsite": "string",
            "createdDate": "2018-01-08T16:57:23Z",
            "cryptoCapitalApiKey": "string",
            "customers": 0,
            "deletedDate": "2018-01-08T16:57:23Z",
            "emailAddress": "string",
            "enabled": true,
            "enrolledBy": null,
            "id": 0,
            "incorporationDate": "2018-01-08",
            "internalFee": 0,
            "legalBusinessName": "string",
            "locationsCount": 0,
            "merchants": 0,
            "note": "string",
            "partners": 0,
            "phone": "string",
            "posCount": 0,
            "state": {
              "abbreviation": "string",
              "id": 0,
              "state": "string"
            },
            "usBankAccount": "string",
            "vendors": 0,
            "zip": "string"
          },
          "city": "string",
          "country": "string",
          "deletedDate": "2018-01-08T16:57:23Z",
          "emailAddress": "string",
          "file": "string",
          "geoLocation": "string",
          "id": 0,
          "name": "string",
          "note": "string",
          "parentLocation": null,
          "phone": "string",
          "pointOfSales": [
            null
          ],
          "state": {
            "abbreviation": "string",
            "id": 0,
            "state": "string"
          },
          "website": "string",
          "zip": "string"
        },
        "name": "string",
        "note": "string",
        "pointOfSaleType": "GREENBITS",
        "virtualPointOfSalesEnabled": true
      },
      "rawTransaction": "string",
      "rawTxId": "string",
      "type": "string",
      "user": {
        "accountNonExpired": true,
        "accountNonLocked": true,
        "activated": true,
        "associate": {
          "address": "string",
          "altAutosellInternal": true,
          "associateType": "ALT36",
          "autosell": true,
          "beneficiaryPercent": 0,
          "canEditOnboarded": true,
          "city": "string",
          "coinaPultApiKey": "string",
          "commissionFee": 0,
          "companyEIN": "string",
          "companyWebsite": "string",
          "createdDate": "2018-01-08T16:57:23Z",
          "cryptoCapitalApiKey": "string",
          "customers": 0,
          "deletedDate": "2018-01-08T16:57:23Z",
          "emailAddress": "string",
          "enabled": true,
          "enrolledBy": null,
          "id": 0,
          "incorporationDate": "2018-01-08",
          "internalFee": 0,
          "legalBusinessName": "string",
          "locationsCount": 0,
          "merchants": 0,
          "note": "string",
          "partners": 0,
          "phone": "string",
          "posCount": 0,
          "state": {
            "abbreviation": "string",
            "id": 0,
            "state": "string"
          },
          "usBankAccount": "string",
          "vendors": 0,
          "zip": "string"
        },
        "credentialsNonExpired": true,
        "email": "john.doe@example.com",
        "enabled": true,
        "firstName": "string",
        "id": 0,
        "imageUrl": "string",
        "langKey": "strin",
        "lastLoginDateTime": "2018-01-08T16:57:23Z",
        "lastName": "string",
        "location": {
          "address": "string",
          "address2": "string",
          "associate": {
            "address": "string",
            "altAutosellInternal": true,
            "associateType": "ALT36",
            "autosell": true,
            "beneficiaryPercent": 0,
            "canEditOnboarded": true,
            "city": "string",
            "coinaPultApiKey": "string",
            "commissionFee": 0,
            "companyEIN": "string",
            "companyWebsite": "string",
            "createdDate": "2018-01-08T16:57:23Z",
            "cryptoCapitalApiKey": "string",
            "customers": 0,
            "deletedDate": "2018-01-08T16:57:23Z",
            "emailAddress": "string",
            "enabled": true,
            "enrolledBy": null,
            "id": 0,
            "incorporationDate": "2018-01-08",
            "internalFee": 0,
            "legalBusinessName": "string",
            "locationsCount": 0,
            "merchants": 0,
            "note": "string",
            "partners": 0,
            "phone": "string",
            "posCount": 0,
            "state": {
              "abbreviation": "string",
              "id": 0,
              "state": "string"
            },
            "usBankAccount": "string",
            "vendors": 0,
            "zip": "string"
          },
          "city": "string",
          "country": "string",
          "deletedDate": "2018-01-08T16:57:23Z",
          "emailAddress": "string",
          "file": "string",
          "geoLocation": "string",
          "id": 0,
          "name": "string",
          "note": "string",
          "parentLocation": null,
          "phone": "string",
          "pointOfSales": [
            {
              "active": true,
              "deletedDate": "2018-01-08T16:57:23Z",
              "id": 0,
              "inventoryNumber": "string",
              "location": null,
              "name": "string",
              "note": "string",
              "pointOfSaleType": "GREENBITS",
              "virtualPointOfSalesEnabled": true
            }
          ],
          "state": {
            "abbreviation": "string",
            "id": 0,
            "state": "string"
          },
          "website": "string",
          "zip": "string"
        },
        "login": "string",
        "resetDate": "2018-01-08T16:57:23Z",
        "splashscreenEnabled": true,
        "using2fa": true
      }
    }
  ],
  "first": true,
  "last": true,
  "number": 0,
  "numberOfElements": 0,
  "size": 0,
  "sort": {},
  "totalElements": 0,
  "totalPages": 0
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|content|[[PendingTransaction](#schemapendingtransaction)]|false|No description|
|first|boolean|false|No description|
|last|boolean|false|No description|
|number|integer(int32)|false|No description|
|numberOfElements|integer(int32)|false|No description|
|size|integer(int32)|false|No description|
|sort|[Sort](#schemasort)|false|No description|
|totalElements|integer(int64)|false|No description|
|totalPages|integer(int32)|false|No description|


<h2 id="tocSpageofpointofsale">PageOfPointOfSale</h2>


<a id="schemapageofpointofsale"></a>


```json
{
  "content": [
    {
      "active": true,
      "deletedDate": "2018-01-08T16:57:23Z",
      "id": 0,
      "inventoryNumber": "string",
      "location": {
        "address": "string",
        "address2": "string",
        "associate": {
          "address": "string",
          "altAutosellInternal": true,
          "associateType": "ALT36",
          "autosell": true,
          "beneficiaryPercent": 0,
          "canEditOnboarded": true,
          "city": "string",
          "coinaPultApiKey": "string",
          "commissionFee": 0,
          "companyEIN": "string",
          "companyWebsite": "string",
          "createdDate": "2018-01-08T16:57:23Z",
          "cryptoCapitalApiKey": "string",
          "customers": 0,
          "deletedDate": "2018-01-08T16:57:23Z",
          "emailAddress": "string",
          "enabled": true,
          "enrolledBy": null,
          "id": 0,
          "incorporationDate": "2018-01-08",
          "internalFee": 0,
          "legalBusinessName": "string",
          "locationsCount": 0,
          "merchants": 0,
          "note": "string",
          "partners": 0,
          "phone": "string",
          "posCount": 0,
          "state": {
            "abbreviation": "string",
            "id": 0,
            "state": "string"
          },
          "usBankAccount": "string",
          "vendors": 0,
          "zip": "string"
        },
        "city": "string",
        "country": "string",
        "deletedDate": "2018-01-08T16:57:23Z",
        "emailAddress": "string",
        "file": "string",
        "geoLocation": "string",
        "id": 0,
        "name": "string",
        "note": "string",
        "parentLocation": null,
        "phone": "string",
        "pointOfSales": [
          null
        ],
        "state": {
          "abbreviation": "string",
          "id": 0,
          "state": "string"
        },
        "website": "string",
        "zip": "string"
      },
      "name": "string",
      "note": "string",
      "pointOfSaleType": "GREENBITS",
      "virtualPointOfSalesEnabled": true
    }
  ],
  "first": true,
  "last": true,
  "number": 0,
  "numberOfElements": 0,
  "size": 0,
  "sort": {},
  "totalElements": 0,
  "totalPages": 0
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|content|[[PointOfSale](#schemapointofsale)]|false|No description|
|first|boolean|false|No description|
|last|boolean|false|No description|
|number|integer(int32)|false|No description|
|numberOfElements|integer(int32)|false|No description|
|size|integer(int32)|false|No description|
|sort|[Sort](#schemasort)|false|No description|
|totalElements|integer(int64)|false|No description|
|totalPages|integer(int32)|false|No description|


<h2 id="tocSpageofrequestfordeleteacssociate">PageOfRequestForDeleteAcssociate</h2>


<a id="schemapageofrequestfordeleteacssociate"></a>


```json
{
  "content": [
    {
      "associateDelete": {
        "address": "string",
        "altAutosellInternal": true,
        "associateType": "ALT36",
        "autosell": true,
        "beneficiaryPercent": 0,
        "canEditOnboarded": true,
        "city": "string",
        "coinaPultApiKey": "string",
        "commissionFee": 0,
        "companyEIN": "string",
        "companyWebsite": "string",
        "createdDate": "2018-01-08T16:57:23Z",
        "cryptoCapitalApiKey": "string",
        "customers": 0,
        "deletedDate": "2018-01-08T16:57:23Z",
        "emailAddress": "string",
        "enabled": true,
        "enrolledBy": null,
        "id": 0,
        "incorporationDate": "2018-01-08",
        "internalFee": 0,
        "legalBusinessName": "string",
        "locationsCount": 0,
        "merchants": 0,
        "note": "string",
        "partners": 0,
        "phone": "string",
        "posCount": 0,
        "state": {
          "abbreviation": "string",
          "id": 0,
          "state": "string"
        },
        "usBankAccount": "string",
        "vendors": 0,
        "zip": "string"
      },
      "dateRequested": "2018-01-08T16:57:23Z",
      "id": 0,
      "reason": "stringstri",
      "requestedBy": {
        "address": "string",
        "altAutosellInternal": true,
        "associateType": "ALT36",
        "autosell": true,
        "beneficiaryPercent": 0,
        "canEditOnboarded": true,
        "city": "string",
        "coinaPultApiKey": "string",
        "commissionFee": 0,
        "companyEIN": "string",
        "companyWebsite": "string",
        "createdDate": "2018-01-08T16:57:23Z",
        "cryptoCapitalApiKey": "string",
        "customers": 0,
        "deletedDate": "2018-01-08T16:57:23Z",
        "emailAddress": "string",
        "enabled": true,
        "enrolledBy": null,
        "id": 0,
        "incorporationDate": "2018-01-08",
        "internalFee": 0,
        "legalBusinessName": "string",
        "locationsCount": 0,
        "merchants": 0,
        "note": "string",
        "partners": 0,
        "phone": "string",
        "posCount": 0,
        "state": {
          "abbreviation": "string",
          "id": 0,
          "state": "string"
        },
        "usBankAccount": "string",
        "vendors": 0,
        "zip": "string"
      }
    }
  ],
  "first": true,
  "last": true,
  "number": 0,
  "numberOfElements": 0,
  "size": 0,
  "sort": {},
  "totalElements": 0,
  "totalPages": 0
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|content|[[RequestForDeleteAcssociate](#schemarequestfordeleteacssociate)]|false|No description|
|first|boolean|false|No description|
|last|boolean|false|No description|
|number|integer(int32)|false|No description|
|numberOfElements|integer(int32)|false|No description|
|size|integer(int32)|false|No description|
|sort|[Sort](#schemasort)|false|No description|
|totalElements|integer(int64)|false|No description|
|totalPages|integer(int32)|false|No description|


<h2 id="tocSpageofsalestransactionvm">PageOfSalesTransactionVM</h2>


<a id="schemapageofsalestransactionvm"></a>


```json
{
  "content": [
    {
      "amountInDash": "string",
      "amountInUSD": "string",
      "commisionFeeinDash": "string",
      "commisionFeeinUSD": "string",
      "id": 0,
      "location": "string",
      "pointOfSale": "string",
      "status": "string",
      "timeAndDate": "2018-01-08T16:57:23Z",
      "transactionId": "string"
    }
  ],
  "first": true,
  "last": true,
  "number": 0,
  "numberOfElements": 0,
  "size": 0,
  "sort": {},
  "totalElements": 0,
  "totalPages": 0
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|content|[[SalesTransactionVM](#schemasalestransactionvm)]|false|No description|
|first|boolean|false|No description|
|last|boolean|false|No description|
|number|integer(int32)|false|No description|
|numberOfElements|integer(int32)|false|No description|
|size|integer(int32)|false|No description|
|sort|[Sort](#schemasort)|false|No description|
|totalElements|integer(int64)|false|No description|
|totalPages|integer(int32)|false|No description|


<h2 id="tocSinviteassociateviaemail">InviteAssociateViaEmail</h2>


<a id="schemainviteassociateviaemail"></a>


```json
{
  "email": "john.doe@example.com"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|email|string|true|No description|


<h2 id="tocSkeyandpasswordvm">KeyAndPasswordVM</h2>


<a id="schemakeyandpasswordvm"></a>


```json
{
  "key": "string",
  "newPassword": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|key|string|true|No description|
|newPassword|string|false|No description|


<h2 id="tocSlasttransactionvm">LastTransactionVm</h2>


<a id="schemalasttransactionvm"></a>


```json
{
  "amountInDASH": 0,
  "amountInUSD": 0,
  "dateTime": "2018-01-08T16:57:23Z"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|amountInDASH|number(double)|false|No description|
|amountInUSD|number(double)|false|No description|
|dateTime|string(date-time)|false|No description|


<h2 id="tocSlocation">Location</h2>


<a id="schemalocation"></a>


```json
{
  "address": "string",
  "address2": "string",
  "associate": {
    "address": "string",
    "altAutosellInternal": true,
    "associateType": "ALT36",
    "autosell": true,
    "beneficiaryPercent": 0,
    "canEditOnboarded": true,
    "city": "string",
    "coinaPultApiKey": "string",
    "commissionFee": 0,
    "companyEIN": "string",
    "companyWebsite": "string",
    "createdDate": "2018-01-08T16:57:23Z",
    "cryptoCapitalApiKey": "string",
    "customers": 0,
    "deletedDate": "2018-01-08T16:57:23Z",
    "emailAddress": "string",
    "enabled": true,
    "enrolledBy": null,
    "id": 0,
    "incorporationDate": "2018-01-08",
    "internalFee": 0,
    "legalBusinessName": "string",
    "locationsCount": 0,
    "merchants": 0,
    "note": "string",
    "partners": 0,
    "phone": "string",
    "posCount": 0,
    "state": {
      "abbreviation": "string",
      "id": 0,
      "state": "string"
    },
    "usBankAccount": "string",
    "vendors": 0,
    "zip": "string"
  },
  "city": "string",
  "country": "string",
  "deletedDate": "2018-01-08T16:57:23Z",
  "emailAddress": "string",
  "file": "string",
  "geoLocation": "string",
  "id": 0,
  "name": "string",
  "note": "string",
  "parentLocation": null,
  "phone": "string",
  "pointOfSales": [
    {
      "active": true,
      "deletedDate": "2018-01-08T16:57:23Z",
      "id": 0,
      "inventoryNumber": "string",
      "location": null,
      "name": "string",
      "note": "string",
      "pointOfSaleType": "GREENBITS",
      "virtualPointOfSalesEnabled": true
    }
  ],
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "website": "string",
  "zip": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|address|string|true|No description|
|address2|string|false|No description|
|associate|[Associate](#schemaassociate)|false|No description|
|city|string|true|No description|
|country|string|true|No description|
|deletedDate|string(date-time)|false|No description|
|emailAddress|string|false|No description|
|file|string|false|No description|
|geoLocation|string|false|No description|
|id|integer(int64)|false|No description|
|name|string|true|No description|
|note|string|false|No description|
|parentLocation|[Location](#schemalocation)|false|No description|
|phone|string|false|No description|
|pointOfSales|[[PointOfSale](#schemapointofsale)]|false|No description|
|state|[CountryState](#schemacountrystate)|true|No description|
|website|string|false|No description|
|zip|string|true|No description|


<h2 id="tocSlocationexternalvm">LocationExternalVm</h2>


<a id="schemalocationexternalvm"></a>


```json
{
  "address": "string",
  "address2": "string",
  "city": "string",
  "contact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "contactType": "MAIN",
    "file": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "notificationCronSchedule": "string",
    "notificationEvent": "INBOUND_TRANSACTION",
    "notifyByEmail": true,
    "notifyByTextMessage": true,
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "zip": "string"
  },
  "country": "string",
  "emailAddress": "string",
  "file": "string",
  "fileBytes": "string",
  "fileContentType": "string",
  "geoLocation": "string",
  "id": 0,
  "merchantId": 0,
  "name": "string",
  "noOfPos": 0,
  "note": "string",
  "parentLocationId": 0,
  "phone": "string",
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "website": "string",
  "zip": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|address|string|true|No description|
|address2|string|false|No description|
|city|string|true|No description|
|contact|[Contact](#schemacontact)|true|No description|
|country|string|true|No description|
|emailAddress|string|false|No description|
|file|string|false|No description|
|fileBytes|string(byte)|false|No description|
|fileContentType|string|false|No description|
|geoLocation|string|true|No description|
|id|integer(int64)|false|No description|
|merchantId|integer(int64)|true|No description|
|name|string|true|No description|
|noOfPos|integer(int32)|false|No description|
|note|string|false|No description|
|parentLocationId|integer(int64)|false|No description|
|phone|string|false|No description|
|state|[CountryState](#schemacountrystate)|true|No description|
|website|string|false|No description|
|zip|string|true|No description|


<h2 id="tocSlocationvm">LocationVm</h2>


<a id="schemalocationvm"></a>


```json
{
  "address": "string",
  "address2": "string",
  "city": "string",
  "contact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "contactType": "MAIN",
    "file": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "notificationCronSchedule": "string",
    "notificationEvent": "INBOUND_TRANSACTION",
    "notifyByEmail": true,
    "notifyByTextMessage": true,
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "zip": "string"
  },
  "country": "string",
  "emailAddress": "string",
  "file": "string",
  "fileBytes": "string",
  "fileContentType": "string",
  "geoLocation": "string",
  "id": 0,
  "name": "string",
  "noOfPos": 0,
  "note": "string",
  "parentLocationId": 0,
  "phone": "string",
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "website": "string",
  "zip": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|address|string|true|No description|
|address2|string|false|No description|
|city|string|true|No description|
|contact|[Contact](#schemacontact)|true|No description|
|country|string|true|No description|
|emailAddress|string|false|No description|
|file|string|false|No description|
|fileBytes|string(byte)|false|No description|
|fileContentType|string|false|No description|
|geoLocation|string|false|No description|
|id|integer(int64)|false|No description|
|name|string|true|No description|
|noOfPos|integer(int32)|false|No description|
|note|string|false|No description|
|parentLocationId|integer(int64)|false|No description|
|phone|string|false|No description|
|state|[CountryState](#schemacountrystate)|true|No description|
|website|string|false|No description|
|zip|string|true|No description|


<h2 id="tocSlocationwithtransactionvm">LocationWithTransactionVm</h2>


<a id="schemalocationwithtransactionvm"></a>


```json
{
  "address": "string",
  "address2": "string",
  "city": "string",
  "contact": {
    "address": "string",
    "address2": "string",
    "beneficiaryPercent": 0,
    "birthDate": "2018-01-08",
    "city": "string",
    "contactType": "MAIN",
    "file": "string",
    "firstName": "string",
    "gender": "MALE",
    "id": 0,
    "lastName": "string",
    "nationality": "string",
    "note": "string",
    "notificationCronSchedule": "string",
    "notificationEvent": "INBOUND_TRANSACTION",
    "notifyByEmail": true,
    "notifyByTextMessage": true,
    "passportExpiryDate": "2018-01-08",
    "passportIssueDate": "2018-01-08",
    "passportNumber": "string",
    "position": "string",
    "primaryEmailAddress": "string",
    "primaryMobilePhone": "string",
    "secondaryEmailAddress": "string",
    "secondaryMobilePhone": "string",
    "zip": "string"
  },
  "country": "string",
  "emailAddress": "string",
  "file": "string",
  "fileBytes": "string",
  "fileContentType": "string",
  "geoLocation": "string",
  "id": 0,
  "lastTransaction": {
    "amountInDASH": 0,
    "amountInUSD": 0,
    "dateTime": "2018-01-08T16:57:23Z"
  },
  "name": "string",
  "noOfPos": 0,
  "note": "string",
  "parentLocationId": 0,
  "phone": "string",
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "website": "string",
  "zip": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|address|string|true|No description|
|address2|string|false|No description|
|city|string|true|No description|
|contact|[Contact](#schemacontact)|true|No description|
|country|string|true|No description|
|emailAddress|string|false|No description|
|file|string|false|No description|
|fileBytes|string(byte)|false|No description|
|fileContentType|string|false|No description|
|geoLocation|string|false|No description|
|id|integer(int64)|false|No description|
|lastTransaction|[LastTransactionVm](#schemalasttransactionvm)|false|No description|
|name|string|true|No description|
|noOfPos|integer(int32)|false|No description|
|note|string|false|No description|
|parentLocationId|integer(int64)|false|No description|
|phone|string|false|No description|
|state|[CountryState](#schemacountrystate)|true|No description|
|website|string|false|No description|
|zip|string|true|No description|


<h2 id="tocSinvitation">Invitation</h2>


<a id="schemainvitation"></a>


```json
{
  "acceptedDateTime": "2018-01-08T16:57:23Z",
  "associateType": "ALT36",
  "id": 0,
  "inviteKey": "string",
  "invitedMail": "string",
  "ivitationDateTime": "2018-01-08T16:57:23Z",
  "mailSent": true
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|acceptedDateTime|string(date-time)|false|No description|
|associateType|string|false|No description|
|id|integer(int64)|false|No description|
|inviteKey|string|false|No description|
|invitedMail|string|true|No description|
|ivitationDateTime|string(date-time)|false|No description|
|mailSent|boolean|false|No description|


#### Enumerated Values


|Property|Value|
|---|---|
|associateType|ALT36|
|associateType|PARTNER|
|associateType|MERCHANT|
|associateType|VENDOR|
|associateType|CUSTOMER|

<h2 id="tocSdeactivateassociate">DeactivateAssociate</h2>


<a id="schemadeactivateassociate"></a>


```json
{
  "id": 0,
  "reason": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|id|integer(int64)|true|No description|
|reason|string|false|No description|

<h2 id="tocScountrystatedto">CountryStateDTO</h2>


<a id="schemacountrystatedto"></a>


```json
{
  "abbreviation": "string",
  "id": 0,
  "state": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|abbreviation|string|false|No description|
|id|integer(int64)|false|No description|
|state|string|false|No description|

<h2 id="tocScountrystate">CountryState</h2>


<a id="schemacountrystate"></a>


```json
{
  "abbreviation": "string",
  "id": 0,
  "state": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|abbreviation|string|false|No description|
|id|integer(int64)|false|No description|
|state|string|false|No description|


<h2 id="tocScontactvm">ContactVM</h2>


<a id="schemacontactvm"></a>


```json
{
  "address": "string",
  "address2": "string",
  "beneficiaryPercent": 0,
  "birthDate": "2018-01-08",
  "city": "string",
  "file": "string",
  "fileBytes": "string",
  "fileContentType": "string",
  "firstName": "string",
  "gender": "MALE",
  "id": 0,
  "lastName": "string",
  "nationality": "string",
  "note": "string",
  "passportExpiryDate": "2018-01-08",
  "passportIssueDate": "2018-01-08",
  "passportNumber": "string",
  "position": "string",
  "primaryEmailAddress": "string",
  "primaryMobilePhone": "string",
  "secondaryEmailAddress": "string",
  "secondaryMobilePhone": "string",
  "state": {
    "abbreviation": "string",
    "id": 0,
    "state": "string"
  },
  "zip": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|address|string|false|No description|
|address2|string|false|No description|
|beneficiaryPercent|integer(int64)|false|No description|
|birthDate|string(date)|false|No description|
|city|string|false|No description|
|file|string|false|No description|
|fileBytes|string(byte)|true|No description|
|fileContentType|string|true|No description|
|firstName|string|true|No description|
|gender|string|false|No description|
|id|integer(int64)|false|No description|
|lastName|string|true|No description|
|nationality|string|false|No description|
|note|string|false|No description|
|passportExpiryDate|string(date)|false|No description|
|passportIssueDate|string(date)|false|No description|
|passportNumber|string|false|No description|
|position|string|true|No description|
|primaryEmailAddress|string|true|No description|
|primaryMobilePhone|string|true|No description|
|secondaryEmailAddress|string|false|No description|
|secondaryMobilePhone|string|false|No description|
|state|[CountryState](#schemacountrystate)|false|No description|
|zip|string|false|No description|


#### Enumerated Values


|Property|Value|
|---|---|
|gender|MALE|
|gender|FEMALE|
|gender|OTHER|

<h2 id="tocScontact">Contact</h2>


<a id="schemacontact"></a>


```json
{
  "address": "string",
  "address2": "string",
  "beneficiaryPercent": 0,
  "birthDate": "2018-01-08",
  "city": "string",
  "contactType": "MAIN",
  "file": "string",
  "firstName": "string",
  "gender": "MALE",
  "id": 0,
  "lastName": "string",
  "nationality": "string",
  "note": "string",
  "notificationCronSchedule": "string",
  "notificationEvent": "INBOUND_TRANSACTION",
  "notifyByEmail": true,
  "notifyByTextMessage": true,
  "passportExpiryDate": "2018-01-08",
  "passportIssueDate": "2018-01-08",
  "passportNumber": "string",
  "position": "string",
  "primaryEmailAddress": "string",
  "primaryMobilePhone": "string",
  "secondaryEmailAddress": "string",
  "secondaryMobilePhone": "string",
  "zip": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|address|string|false|No description|
|address2|string|false|No description|
|beneficiaryPercent|integer(int64)|false|No description|
|birthDate|string(date)|false|No description|
|city|string|false|No description|
|contactType|string|true|No description|
|file|string|false|No description|
|firstName|string|true|No description|
|gender|string|false|No description|
|id|integer(int64)|false|No description|
|lastName|string|true|No description|
|nationality|string|false|No description|
|note|string|false|No description|
|notificationCronSchedule|string|false|No description|
|notificationEvent|string|false|No description|
|notifyByEmail|boolean|false|No description|
|notifyByTextMessage|boolean|false|No description|
|passportExpiryDate|string(date)|false|No description|
|passportIssueDate|string(date)|false|No description|
|passportNumber|string|false|No description|
|position|string|false|No description|
|primaryEmailAddress|string|true|No description|
|primaryMobilePhone|string|false|No description|
|secondaryEmailAddress|string|false|No description|
|secondaryMobilePhone|string|false|No description|
|zip|string|false|No description|


#### Enumerated Values


|Property|Value|
|---|---|
|contactType|MAIN|
|contactType|SIGNATORY|
|contactType|OTHER|
|contactType|LOCATION|
|gender|MALE|
|gender|FEMALE|
|gender|OTHER|
|notificationEvent|INBOUND_TRANSACTION|
|notificationEvent|OUTBOUND_TRANSACTION|
|notificationEvent|DAILY_TRANSACTION_SUMMARY|
|notificationEvent|WEEKLY_TRANSACTION_SUMMARY|
|notificationEvent|MONTHLY_TRANSACTION_SUMMARY|



<h2 id="backendPaginationObject">Backend pagination object</h2>

```json
{
  "content": [

  ],
  "first": true,
  "last": false,
  "number": 0,
  "numberOfElements": 25,
  "size": 25,
  "sort": {},
  "totalElements": 250,
  "totalPages": 10
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|content|Paginated content|false|No description|
|first|boolean|false|is Current page first page|
|last|boolean|false|is Current page last page|
|number|integer(int32)|false|page index (start from 0)|
|numberOfElements|integer(int32)|false|number Of Elements on current page|
|size|integer(int32)|false|number of items to be returned|
|sort|[Sort](#schemasort)|false|sorting parameters|
|totalElements|integer(int64)|false|total number of elements|
|totalPages|integer(int32)|false|total number of pages|


<h2 id="reportingPaginationObject">Reporting pagination object</h2>

first (Boolean) - refers to whether the requested page is first page
last (Boolean) - refers to whether the requested page is last page
number (Integer) - current number of a page, zero index rule is used
numberOfElements (Integer) - total number of elements in the requested list of objects 
size (Integer)- size of the page as requested  
totalPages (Integer)- total number of pages for the requested list of objects
As one may notice, totalElements parameter is omitted here. instead numberOfElements is used to represent that value.