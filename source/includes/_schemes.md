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
|companyWebsite|string|true|No description|
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
|reason|string|true|Reason for closing an account|


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
|activated|boolean|false|Is user Activated|
|authorities|[string]|false|User roles|
|createdBy|string|false|User created|
|createdDate|string(date-time)|false|Date created|
|email|string|false|Email address|
|firstName|string|false|First Name|
|id|integer(int64)|false|Last Name|
|imageUrl|string|false|No description|
|langKey|string|false|No description|
|lastLoginDateTime|string(date-time)|false|Last Login datetime|
|lastModifiedBy|string|false|No description|
|lastModifiedDate|string(date-time)|false|No description|
|lastName|string|false|Last Name|
|login|string|true|Username|
|splashscreenEnabled|boolean|false|Is splash screen enabled|
|using2fa|boolean|false|Is 2FA enabled|


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
|splashscreenEnabled|boolean|false|Is splash screen enabled|
|using2fa|boolean|false|Is 2FA enabled|


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

<h2 id="tocSnewcustomervm2">NewCustomerVM2</h2>


<a id="schemanewcustomervm2"></a>


```json
{
  "id": "integer",
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
|id|integer|true|No description|
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
|companyWebsite|string|true|No description|
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

<h2 id="tocSnewmerchantvm2">UpdateMerchantVM</h2>


<a id="schemanewmerchantvm2"></a>


```json
{
  "id": "integer",
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
|id|integer|true|No description|
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
|companyWebsite|string|true|No description|
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
|companyWebsite|string|true|No description|
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


<h2 id="tocSnewvendorvm">NewVendorVM</h2>


<a id="schemanewvendorvm"></a>


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
|companyWebsite|string|true|No description|
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


<h2 id="tocSnewvendorvm2">NewVendorVM2</h2>


<a id="schemanewvendorvm2"></a>


```json
{
  "id": "integer",
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
|id|integer|tru|No description|
|address|string|true|No description|
|address2|string|false|No description|
|altAutosellInternal|boolean|false|No description|
|authorizedSignerContact|[ContactVM](#schemacontactvm)|true|No description|
|autosell|boolean|false|No description|
|canEditOnboarded|boolean|false|No description|
|city|string|true|No description|
|commissionFee|number|false|No description|
|companyEIN|string|true|No description|
|companyWebsite|string|true|No description|
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

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|first|boolean|true|refers to whether the requested page is first page|
|last|boolean|true|refers to whether the requested page is last page|
|number|integer|true|current number of a page, zero index rule is used|
|numberOfElements|integer|true|total number of elements in the requested list of objects|
|size|integer|true|size of the page as requested|
|totalPages|integer|true|total number of pages for the requested list of objects|


<h2 id="tocPOSRequest">POSRequest</h2>

<a id="schemaposrequest"></a>

```json
{
"timestamp_req":integer,
"amount":number,
"currency":string,
"convert_to": string,
"location_id":integer,
"user_id": string
}
```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|timestamp_req|integer|false|Internal transaction id, this is part of internal transaction storage.
|amount|string|true|Amount in currency as defined in currency parameter. Currently only USD is supported.
|currency|string|true|FIAT Currency from which we transfer to DASH (please use USD)
|convert_to|string|true|Cryptocurrency to which conversion is done (please use DASH, or BTC). For sandbox purposes Product36 uses Bitcoin Testnet3 blockchain.
|location_id|integer|optional|Identifier of the location for which POS is registered. It is required for virtual POS, but not for registered POS request
|user_id|integer|true|General purpose value, can be any string. Providers can use this value to put anything inside, for example it can be local user id.

<h2 id="tocPOSRequest">POSResponse</h2>

<a id="schemaposresponse"></a>

```json
{
"tx_id": "TXtbbSjB4HdQ",
"requested_amount": 25,
"requested_currency": "USD",
"converted_amount": 0.06778558065128386,
"converted_currency": "DASH",
"conversion_rate": 368.81,
"timetamp_system": 1504047876,
"pay_to_address": "msJfkM8XmwTxwVVV9EvWLXb4fjCpSvbKWT"
}

```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|tx_id|string|-|Timestamp of the current request moment (used for statistics on server)
|requested_amount|integer|-|FIAT value that sender required
|requested_currency|string|-|FIAT currency that is requested.
|converted_amount|number|-|Amount in cryptocurrency.
|converted_currency|string|-|Currency to which FIAT value is converted.
|conversion_rate|number|-|Conversion rate used for calculation of "converted_amount"
|timetamp_system|integer|-|timestamp when transaction has been created in the system.
|pay_to_address|string|-|Destination address for the transaction.

The values converted_amount and pay_to_address are used as the information for generating customer transaction either directly entered or to generate QR code for payment.
Prior to transaction processing, service endpoint checks that the appropriate data embodied in API key match the values sent in message body.
Important note: There is minimal FIAT value that can be converted, otherwise system will report an error. Minimum value is defined dynamically and it is calculated for every transaction.

<h2 id="tocGeneralSummaryResponse">GeneralSummaryResponse</h2>

<a id="schemageneralsummaryresponse"></a>

```json
{
  "timerange_from": "2017-11-01T00:00:00.0Z",
  "timerange_to": "2018-01-11T23:59:59.1Z",
  "number_of_sales": 84,
  "avg_tx_amount": 0.12657074607143,
  "avg_tx_amount_fiat": 88.72505512713,
  "total_sales": 10.63194267,
  "total_sales_fiat": 7452.9046306789,
  "total_commission_fee_charged": 0.85386515,
  "total_commission_fee_charged_fiat": 602.6705777301
}

```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|timerange_from|string|true|start point in the time range.
|timerange_to|string|true|end point of the time range.
|number_of_sales|integer|true| total number of sales for user
|avg_tx_amount|number|true|average transaction amount of all transactions
|avg_tx_amount_fiat|number|true|average transaction amount converted to FIAT (defaults to USD)
|total_sales|number|total sales sum
|total_sales_fiat|number|true|total sales sum in FIAT (defaults to USD)
|total_commission_fee_charged|number|true|total commission fee.
|total_commission_fee_charged_fiat|number|true|total commission fee converted to FIAT.

<!-- LocationPerformanceItem-->
<h2 id="tocLocationPerformanceItem">LocationPerformanceItem</h2>

<a id="schemareportlocationperformanceitem"></a>

```json
{
  "location_id": 743,
  "location_name": "Peoria",
  "location_address": "29701 N Sunrise Point",
  "item_sales_crypto": 1.41153177,
  "item_sales_fiat": 936.622608258,
  "associate_owner": "Demo Merchant",
  "associate_owner_id": 2102
}
```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|location_id|integer|true|Location identifier
|location_name|string|true|Name of the location
|location_address|string|true|Location postal address
|item_sales_crypto|number|true|Sum of all sales for a given time range
|item_sales_fiat|number|true|Sum of all sales for a given time range in FIAT value
|associate_owner|string|true|Name of location merchant owner
|associate_owner_id|integer|true|Merchant owner identifier

<!-- RolePerformanceItem-->
<h2 id="tocRolePerformanceItem">RolePerformanceItem</h2>

<a id="schemareportroleperformanceitem"></a>

```json
{
  "item_id": 303,
  "item_name": "Merlin",
  "item_sales_crypto": 1.26886494,
  "item_sales_fiat": 767.8435600896,
  "pos_count": 42
}

```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|item_id|integer|true|Merchant identifier
|item_name|string|true|Merchant name as defined in the system
|item_sales_crypto|number|true|Sum of all sales
|item_sales_fiat|number|true|um of all sales in FIAT value
|pos_count|integer|true|Number of POS-es associated with merchant

<!-- SalesItem-->
<h2 id="tocSalesItem">SalesItem</h2>

<a id="schemasalesitem"></a>

```json
{
  "total_amount_of_sales": 0.01242642,
  "total_amount_of_sales_fiat":24.23,
  "time_from": "2017-10-12T14:00:00.000Z",
  "time_to": "2017-10-12T15:00:00.000Z"
}
```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|total_amount_of_sales|number|true|Total amount of sales in cryptocurrency
|item_name|string|true|Total amount of sales in FIAT value
|time_from|number|true|Sum of all sales
|time_to|number|true|Sum of all sales in FIAT value

<!-- TaxItem-->
<h2 id="tocTaxItem">TaxItem</h2>

<a id="schemataxitem"></a>

```json
{
  "total_amount_of_tax": 0.01242642,
  "total_amount_of_tax_fiat":24.23,
  "time_from": "2017-10-12T14:00:00.000Z",
  "time_to": "2017-10-12T15:00:00.000Z"
}
```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|total_amount_of_tax|number|true|Total amount of tax in cryptocurrency
|total_amount_of_tax_fiat|string|true|Total amount of tax in FIAT value
|time_from|string|true|Start of interval (ISO format, timestamp...)
|time_to|string|true|End of interval (ISO format, timestamp ...)

<!-- SummaryItem-->
<h2 id="tocSummaryItem">SummaryItem</h2>

<a id="schemasummaryresponseitem"></a>

```json
{
    "totalSalesVolume": 11.59312777,
    "totalSalesVolumeFiat": 8035.0585505919,
    "totalSalesCount": 105,
    "avgTXAmount": 0.11041074066667,
    "avgTXAmountFiat": 76.524367148494,
    "totalSalesCommission": 0.85508097,
    "totalSalesCommissionFiat": 604.1271665647,
    "totalInternalCommissions": 0.22554123,
    "totalInternalCommissionsFiat":1562.1233554,
    "income":0.0254,
    "incomeFiat": 156.256
  }
```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|totalSalesVolume|number|true|Total sales volume in cryprocurrency
|totalSalesVolumeFiat|number|true|Total sales volume in in FIAT value
|totalSalesCount|integer|true|Total sales count for a given period of time.
|avgTXAmount|number|true|Average transaction value in cryptocurrency
|avgTXAmountFiat|number|true|Average transaction value in FIAT value
|totalSalesCommission|number|true| Total sales commission generated in cryptocurrency
|totalSalesCommissionFiat|number|true|Total income (vendor) in FIAT
|totalInternalCommissions|number|false|Total commissions from internal transactions, omitted for locations and pos
|totalInternalCommissionsFiat|number|false|Total income (vendor). Total commissions from internal transactions, omitted for locations and pos
|income|number|false|Total sales commission generated in cryptocurrency (available only for Patners)
|incomeFiat|number|false|Total sales commission generated in FIAT (available only for Partners)

<!-- PartnerResponseItem-->
<h2 id="tocPartnerResponseItem">PartnerResponseItem</h2>

<a id="schemapartnerresponseitem"></a>

```json
{
  "id": 10656,
  "name": "AdminAddPartner",
  "address": "Neon 47",
  "commissionFee": 0,
  "commissionFeeFiat": 0,
  "totalSales": 0,
  "totalSalesFiat": 0,
  "merchantCnt": 0,
  "locationCnt": 0,
  "posCnt": 0
}
```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|id|integer|true|Merchant identifier
|name|string|true|Merchant Name
|commissionFee|number|true|Commission fee sum for this partner in cryptocurrency
|commissionFeeFiat|number|true|Commission fee sum for this partner in FIAT
|totalSales|number|true|Total sales for this partner in cryptocurrency
|totalSalesFiat|number|true|Total sales for this partner in FIAT
|merchantCnt|integer|true|Total merchant count enrolled by this merchant
|locationCnt|number|true|Total locations number summed for all merchants enrolled by this partner
|posCnt|number|true|Total point of sales number summed for all merchants enrolled by this partner (by locations).


<!-- MerchantResponseItem-->
<h2 id="tocMerchantResponseItem">MerchantResponseItem</h2>

<a id="schemamerchantresponseitem"></a>

```json
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
}

```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|id|integer|true|Merchant identifier
|name|string|true|Merchant Name
|email|string|true|Merchant email (main email used for registration process)
|vendorCnt|integer|true|Number of vendors connected to this merchant
|locationsCnt|integer|true|Number of location owned by this merchant
|posCnt|integer|true|total number of POSs related to locations related to merchant.
|customersCnt|integer|true|Number of customers related to this merchant
|totalSalesCommission|number|true|Total commission sales from this merchant in cryptocurrency
|totalSalesCommissionFiat|number|true|Total commission sales from this merchant in FIAT (USD default)
|totalSales|number|true|Total sales for this merchant in cryptocurrency
|totalSalesFiat|number|true|Total sales for this merchant in FIAT (USD default)


<!-- LocationResponseItem-->
<h2 id="tocLocationResponseItem">LocationResponseItem</h2>

<a id="schemalocationresponseitem"></a>

```json
{
    "id": 305,
    "name": "Merchant_Location_60438",
    "address": "Miodraga Bulatovica 17",
    "numberOfPOS": 3,
    "totalSales": 0.017231902,
    "totalSalesFiat":175.46,
    "totalCommission": 0.01678190,
    "totalSalesCommissionFiat": 156.26,
    "avgTransaction": 168.123,
    "totalCount": 1
}
```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|id|integer|true|Location identifier
|name|string|true|Location Name
|address|string|true|Location registered address
|numberOfPOS|integer|true|Number of POS devices bound to this location.
|posCnt|integer|true|total number of POSs related to locations.
|customersCnt|integer|true|Number of customers related to this merchant
|totalSales|number|true|Total sales for this merchant in cryptocurrency
|totalSalesFiat|number|true|Total sales for this merchant in FIAT (USD default)
|totalSalesCommission|number|true|Total commission sales from this merchant in cryptocurrency
|totalSalesCommissionFiat|number|true|Total commission sales from this merchant in FIAT (USD default)
|totalCount|number|true|Total sales count

<!-- POSResponseItem-->
<h2 id="tocPOSResponseItem">POSResponseItem</h2>

<a id="schemaPOSresponseitem"></a>

```json
{
  "id": 42,
  "inventoryNumber": "POS 2",
  "name": "POS 2",
  "totalSales": 0,
  "totalSalesFiat": 0,
  "totalCount": 0,
  "avgTransaction": 0,
  "avgTransactionFiat": 0
}
```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|id|integer|true|POS identifier (For virtual POS id is always -100)
|inventoryNumber|string|true|POS inventoryNumber
|name|string|true|POS Name
|totalSales|number|true|Total sales volume for this POS in cryptocurrency
|totalSalesFiat|number|true|Total sales volume for this POS in FIAT (USD default)
|totalCount|integer|true|Total number of sales realized with this POS
|avgTransaction|number|true|Average transaction on this POS in cryprocurrency
|avgTransactionFiat|number|true|Average transaction on this POS in Fiat


<!-- TaxResposeItem-->
<h2 id="tocTaxResposeItemItem">TaxResposeItem</h2>

<a id="schemataxresponseitem"></a>

```json
{
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

```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|totalTax|number|true|the amount of tax reported for received transactions. This is for information reporting only and is not part of any calculations.
|totalAmountReceived|number|true|Total amount received in cryptocurrency
|totalAmountReceivedFiat|number|true|Total amount received in cryptocurrency Fiat
|totalAmountSent|number|true|Total amount sent in cryptocurrency
|totalAmountSentFiat|number|true|Total amount sent in cryptocurrency Fiat
|totalFee|number|true|Total fee applied to transactions in cryptocurrency
|totalFeeFiat|number|true|Total fee applied to transactions in Fiat
|totalNumTxSpent|integer|false|Total number of transactions that spent value
|totalNumTxReceived|integer|fasle|Total bumber of transactions that received value

<!-- CommissionResposeItem-->
<h2 id="tocCommissionResposeItemItem">CommissionResposeItem</h2>

<a id="schemacommissionresponseitem"></a>

```json
{
    "associateId": 2102,
    "name": "John Stockton",
    "role": "CUSTOMER",
    "sales_commission_sum": 123.56,
    "sales_commission_sum_fiat": 35654.23,
    "internal_commission_sum": 20.15,
    "internal_commission_sum_fiat": 6523.12
}

```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|associateId|integer|true|Associate identifier
|name|string|true|Associate name
|role|number|true|Associate role
|sales_commission_sum|number|true|Total commissions from sales in cryptocurrency
|sales_commission_sum_fiat|number|true|Total commissions from sales in Fiat
|internal_commission_sum|number|true|Total commission sum from internal transactions
|internal_commission_sum_fiat|number|true|Total commission sum from internal transactions in Fiat


<!-- ReportMetadata -->
<h2 id="tocReportMetadata">ReportMetadata</h2>

<a id="schemareportmetadata"></a>

```json
{
    "timerangeFrom": "2017-09-01T00:00:00.0Z",
    "timerangeTo": "2018-01-15T23:59:59.1Z",
    "number": 0,
    "size": 2,
    "numberOfElements": 531,
    "totalPages": 54,
    "first": true,
    "last": false
  }
```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|timerange_from|string|true|Start date/datetime in ISO format|
|timerange_to|string|true|End date/datetime in ISO format|
|number|integer|true|Page number|
|size|number|true|Page size|
|numberOfElements|integer|true|Total number of elements|
|totalPages|Integer|true|Total number of pages|
|first|boolean|true|Is this the first page|
|last|Integer|true|Is this the last page|

<!-- LocationPerformanceResponse -->
<h2 id="tocLocationPerformanceResponse">LocationPerformanceResponse</h2>

<a id="schemareportLocationPerformanceResponse"></a>

```json
{
  "metadata":{
      "timerangeFrom": "2017-09-01T00:00:00.0Z",
      "timerangeTo": "2018-01-15T23:59:59.1Z",
      "number": 0,
      "size": 2,
      "numberOfElements": 531,
      "totalPages": 54,
      "first": true,
      "last": false
    },
  "data":[
    {
      "location_id": 2432,
      "location_name": "Phoenician",
      "location_address": "6000 E Camelback Rd",
      "item_sales_crypto": 3.03869975,
      "item_sales_fiat": 2213.7153887805,
      "associate_owner": "Demo Merchant",
      "associate_owner_id": 2102
    },
    {
      "location_id": 743,
      "location_name": "Peoria",
      "location_address": "29701 N Sunrise Point",
      "item_sales_crypto": 1.41153177,
      "item_sales_fiat": 936.622608258,
      "associate_owner": "Demo Merchant",
      "associate_owner_id": 2102
    },
    {
      "location_id": 303,
      "location_name": "Phoenix",
      "location_address": "340 N 3rd St",
      "item_sales_crypto": 1.26886494,
      "item_sales_fiat": 767.8435600896,
      "associate_owner": "Demo Merchant",
      "associate_owner_id": 2102
    },
    {
      "location_id": 2427,
      "location_name": "ByMerchant",
      "location_address": "N 7th St",
      "item_sales_crypto": 1.05366415,
      "item_sales_fiat": 720.2720775932,
      "associate_owner": "Demo Merchant",
      "associate_owner_id": 2102
    },
    {
      "location_id": 744,
      "location_name": "Oakland",
      "location_address": "1411 E 31st St",
      "item_sales_crypto": 1.02292684,
      "item_sales_fiat": 690.7045676177,
      "associate_owner": "Demo Merchant",
      "associate_owner_id": 2102
    }
  ]
}
```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|metadata|[ReportMetadata](#schemareportmetadata)|true|Response metadata
|data|Array([LocationPerformanceItem](#schemarepotlocationperformanceitem))|true|Arary of location performance data


<!-- RolePerformanceResponse -->
<h2 id="tocRolePerformanceResponse">RolePerformanceResponse</h2>

<a id="schemareportRolePerformanceResponse"></a>

```json
{
  "metadata":{
      "timerangeFrom": "2017-09-01T00:00:00.0Z",
      "timerangeTo": "2018-01-15T23:59:59.1Z",
      "number": 0,
      "size": 2,
      "numberOfElements": 531,
      "totalPages": 54,
      "first": true,
      "last": false
    },
  "data":[
    {
      "item_id": 2432,
      "item_name": "Merchant Phoenix",
      "item_sales_crypto": 3.03869975,
      "item_sales_fiat": 2213.7153887805,
      "pos_count": 12
    },
    {
      "item_id": 743,
      "item_name": "Red hat",
      "item_sales_crypto": 1.41153177,
      "item_sales_fiat": 936.622608258,
      "pos_count": 23
    },
    {
      "item_id": 303,
      "item_name": "Merlin",
      "item_sales_crypto": 1.26886494,
      "item_sales_fiat": 767.8435600896,
      "pos_count": 42
    },
    {
      "item_id": 2427,
      "item_name": "Luna",
      "item_sales_crypto": 1.05366415,
      "item_sales_fiat": 720.2720775932,
      "pos_count": 11
    },
    {
      "item_id": 744,
      "item_name": "Venus",
      "item_sales_crypto": 1.02292684,
      "item_sales_fiat": 690.7045676177,
      "pos_count": 35
    }
  ]

}

```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|metadata|[ReportMetadata](#schemareportmetadata)|true|Response metadata
|data|Array([RolePerformanceItem](#schemareportroleperformanceitem))|true|Arary of location performance data

<!-- TaxSummaryResponse -->
<h2 id="tocTaxSummaryResponse">TaxSummaryResponse</h2>

<a id="schemareportTaxSummaryResponse"></a>

```json
{
  "metadata":{
      "timerangeFrom": "2017-09-01T00:00:00.0Z",
      "timerangeTo": "2018-01-15T23:59:59.1Z",
      "number": 0,
      "size": 2,
      "numberOfElements": 531,
      "totalPages": 54,
      "first": true,
      "last": false
    },
    "data":[
      {
        "total_amount_of_tax": 0.01242642,
        "total_amount_of_tax_fiat":24.23,
        "time_from": "2017-10-12T14:00:00.000Z",
        "time_to": "2017-10-12T15:00:00.000Z"
      },
      {
        "total_amount_of_tax": 0.12546585,
        "total_amount_of_tax_fiat":28.15,
        "time_from": "2017-10-12T15:00:00.000Z",
        "time_to": "2017-10-12T16:00:00.000Z"
      }

    ]
}
```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|metadata|[ReportMetadata](#schemareportmetadata)|true|Response metadata
|data|Array([TaxItem](#schemataxitem))|true|Array of tax items


<!-- SalesSummaryResponse -->
<h2 id="tocSalesSummaryResponse">SalesSummaryResponse</h2>

<a id="schemareportSalesSummaryResponse"></a>

```json
{
  "metadata":{
      "timerangeFrom": "2017-09-01T00:00:00.0Z",
      "timerangeTo": "2018-01-15T23:59:59.1Z",
      "number": 0,
      "size": 2,
      "numberOfElements": 531,
      "totalPages": 54,
      "first": true,
      "last": false
    },
  "data":[
          {
              "total_amount_of_sales": 0,
              "total_amount_of_sales_fiat":0,
              "time_from": "2017-10-12T13:00:00.000Z",
              "time_to": "2017-10-12T14:00:00.000Z"
          },
          {
              "total_amount_of_sales": 0.01242642,
              "total_amount_of_sales_fiat":24.23,
              "time_from": "2017-10-12T14:00:00.000Z",
              "time_to": "2017-10-12T15:00:00.000Z"
          }
    ]
}

```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|metadata|[ReportMetadata](#schemareportmetadata)|true|Response metadata
|data|Array([SalesItem](#schemasalesitem))|true|Array of sales items

<!-- ReportResponse -->
<h2 id="tocReportResponse">PartnerReportResponse</h2>

<a id="schemareportPartnerReportResponse"></a>

```json
{
  "metadata":{
      "timerangeFrom": "2017-09-01T00:00:00.0Z",
      "timerangeTo": "2018-01-15T23:59:59.1Z",
      "number": 0,
      "size": 2,
      "numberOfElements": 531,
      "totalPages": 54,
      "first": true,
      "last": false
    },
  "summary":{
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
    }
  "data":[
          {
            "id": 10656,
            "name": "AdminAddPartner",
            "address": "Neon 47",
            "commissionFee": 0,
            "commissionFeeFiat": 0,
            "tootalSales": 0,
            "tootalSalesFiat": 0,
            "merchantCnt": 0,
            "locationCnt": 0,
            "posCnt": 0
          },
          {
            "id": 10664,
            "name": "Bakaja Partner",
            "address": "Neon 47",
            "commissionFee": 0,
            "commissionFeeFiat": 0,
            "tootalSales": 0,
            "tootalSalesFiat": 0,
            "merchantCnt": 0,
            "locationCnt": 0,
            "posCnt": 0
          }
    ]
}

```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|metadata|[ReportMetadata](#schemareportmetadata)|true|Response metadata
|summary|[SummaryItem](#tocSummaryItem)|true|Summary data - ralates to all pages of data.
|data|Array([PartnerResponseItem](#tocPartnerResponseItem))|true|Array of objects

<!-- MerchantReportResponse -->
<h2 id="tocMerchantReportResponse">MerchantReportResponse</h2>

<a id="schemareportMerchantReportResponse"></a>

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
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|metadata|[ReportMetadata](#schemareportmetadata)|true|Response metadata
|summary|[SummaryItem](#tocSummaryItem)|true|Summary data - ralates to all pages of data.
|data|Array([MerchantResponseItem](#tocMerchantResponseItem))|true|Array of objects

<!-- LocationReportResponse -->
<h2 id="tocLocationReportResponse">LocationReportResponse</h2>

<a id="schemareportLocationReportResponse"></a>

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
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|metadata|[ReportMetadata](#schemareportmetadata)|true|Response metadata
|summary|[SummaryItem](#tocSummaryItem)|true|Summary data - ralates to all pages of data.
|data|Array([LocationResponseItem](#tocLocationResponseItem))|true|Array of objects


<!-- PosReportResponse -->
<h2 id="tocPOSReportResponse">POSReportResponse</h2>

<a id="schemareportPOSReportResponse"></a>

```json
{
  "metadata": {
    "timerangeFrom": "2017-09-01T00:00:00.0Z",
    "timerangeTo": "2018-01-15T23:59:59.0Z",
    "number": 0,
    "size": 2,
    "numberOfElements": 6,
    "totalPages": 1,
    "first": true,
    "last": true
  },
  "summary": {
    "totalSalesVolume": 11.52008667,
    "totalSalesVolumeFiat": 7947.5531215589,
    "totalSalesCount": 104,
    "avgTXAmount": 0.11077006413462,
    "avgTXAmountFiat": 76.418780014989,
    "totalSalesCommission": 0.85386515,
    "totalSalesCommissionFiat": 602.6705777301
  },
  "content": [
    {
      "id": -100,
      "inventoryNumber": "N\/A",
      "name": "Virtual POS",
      "totalSales": 4.1240819,
      "totalSalesFiat": 2647.8644134884,
      "totalCount": 41,
      "avgTransaction": 0.10058736341463,
      "avgTransactionFiat": 64.582058865571
    },
    {
      "id": 42,
      "inventoryNumber": "POS 2",
      "name": "POS 2",
      "totalSales": 0,
      "totalSalesFiat": 0,
      "totalCount": 0,
      "avgTransaction": 0,
      "avgTransactionFiat": 0
    }
  ]
}
```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|metadata|[ReportMetadata](#schemareportmetadata)|true|Response metadata
|summary|[SummaryItem](#tocSummaryItem)|true|Summary data - ralates to all pages of data.
|data|Array([POSResponseItem](#tocPOSResponseItem))|true|Array of objects


<!-- TaxReportResponse -->
<h2 id="tocTaxReportResponse">TaxReportResponse</h2>

<a id="schemareportTaxReportResponse"></a>

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
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|metadata|[ReportMetadata](#schemareportmetadata)|true|Response metadata
|content|[TaxResponseItem](#tocTaxResposeItemItem)|true| Tax report item instance

<!-- AltCommissionReportResponse -->
<h2 id="tocAltCommissionReportResponse">AltCommissionReportResponse</h2>

<a id="schemareporAltCommissionReportResponse"></a>

```json
{
    "metadata": {
        "currency": "DASH",
        "timerangeFrom": "2017-11-09T00:00:0.0Z",
        "timerangeTo": "2017-11-10T01:00:00.0Z",
        "size": 2,
        "targetRole": "ROLE_ADMIN",
        "numberOfElements": 2,
        "totalPages": 1,
        "first": true,
        "last": false
    },
    "summaryCommission": {
        "salesCommission": 345.23,
        "salesCommissionFiat": 10234.22,
        "internalCommission": 123.22,
        "internalCommissionFiat": 3523.23
    },
    "content": [
        {
            "associateId": 2102,
            "name": "John Stockton",
            "role": "CUSTOMER",
            "sales_commission_sum": 0.56654,
            "sales_commission_sum_fiat": 2542.25,
            "internal_commission_sum": 0.00235,
            "internal_commission_sum_fiat": 25.56
        },
        {
            "associateId": 2054,
            "name": "Johnatan Doe",
            "role": "PARTNER",
            "sales_commission_sum": 0.85652,
            "sales_commission_sum_fiat": 6854.23,
            "internal_commission_sum": 0.008974,
            "internal_commission_sum_fiat": 175.25
        }
    ]
}

```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|metadata|[ReportMetadata](#schemareportmetadata)|true|Response metadata
|content|Array([CommissionResponseItem])(#tocCommissionResposeItemItem)|true| Array of commission report intems

<!-- ErrorMessage -->
<h2 id="tocErrorMessage">ErrorMessage</h2>

<a id="schemareporterrormessage"></a>

```json
{
  "message":"There was an error processing the request"
}

```
|Parameter|Type|Required|Description|
|---|---|---|---|---|
|message|string|true|Error message returned along with status code


<!-- Notification message -->
<h2 id="tocNotificationMessage">NotificationMessage</h2>

<a id="schemanotificationmessage"></a>

```json
{
 "tx_id":"iw210iw21i0",
 "tx_state":"COMPLETED",
 "requested_amount":25.00,
 "requested_currency":"USD",
 "converted_to_amount": 0.2,
 "converted_to_currency":"DASH",
 "timestamp_resp": 1503007674,
 "pay_to_address": "1xj239s8…js928jswi",
 "warning_msg":{  
        "message":
                "User payed MORE than required, expected_amount_crypto: 0.056 expected_amount_fiat: 25.50, payed_amount_crypto: 0.0571 payed_amount_fiat: 27.25, difference_crypto: 0.0011 difference_fiat: 2.25"
      }
  }
}
```

|Parameter|Type|Required|Description|
|---|---|---|---|---|
|tx_id|string|false|Internal transaction id, this is part of internal transaction storage.
|tx_state|string|true|Current state of the transaction
|requested_amount|number|true|Requested amount that system generated
|requested_currency|string|true|Requested currency
|converted_to_amount|number|true|To which mount value has been converted
|converted_to_currency|string|true|Curency conversion
|timestamp_resp|integer|true|Response timestamp created on server
|pay_to_address|string|true|The address that has been payed to
|warning_msg|[ErrorMessage](#tocErrorMessage)|true|Warning message (could be omitted)


<!-- AssociateAccount -->
<h2 id="tocAssociateAccount">AssociateAccount</h2>

<a id="schemaassociateaccount"></a>

```json
{
  "id":"20",
  "email":"test@example.com"
}
```

|Parameter|Type|Required|Description|
|---|---|---|---|---|
|timestamp_req|integer|false|Internal transaction id, this is part of internal transaction storage.
|id|integer|true|Internal user identifier
|email|string|true|User email address. This address is used for registration with Coinapult and cannot be changed later.

<!-- InternalRequest -->

<h2 id="tocInternalRequest">InternalRequest</h2>

<a id="schemainternalrequest"></a>

```json
{
    "type":"INTERNAL_CRYPTO_TO_INTERNAL_CRYPTO",
    "source_associate_id": 20,
    "destination_associate_id": 100,
    "amount": 1.2,
    "currency_in": "DASH",
    "currency_out": "DASH",
    "timestamp_req":"152345465564",
    "note":"Some transaction note string"
}
```

|Parameter|Type|Required|Description|
|---|---|---|---|---|
|type|string|false| Enumeration (INTERNAL_CRYPTO_TO_INTERNAL_CRYPTO, INTERNAL_CRYPTO_TO_EXTERNAL_CRYPTO, INTERNAL_CRYPTO_TO_FIAT, FIAT_TO_INTERNAL_CRYPTO, INTERNAL_FIAT_TO_EXTERNAL_FIAT).
|source_associate_id|integer|true|Internal associate Id of transaction initiator
|destination_associate_id|integer|true|Internal associate id of transaction destination
|amount|number|true|Amount to transfer
|currency_in|string|true|Currency that is transfered
|currency_out|string|true|Currency to which is transfered
|timestamp_req|integer|true|Timestamp of the request
|note|string|false|General note about transaction


<!-- InternalResponse -->

<h2 id="tocInternalResponse">InternalResponse</h2>

<a id="schemainternalresponse"></a>

```json
{
    "timestamp_accepted": 152345465566,
    "tx_id": "TXtbbSjB4HdQ",
    "destination_address":"myzREJCjMo3peEcvpmPBWdgDpNhvVHTNBZ",
    "status": "PENDING",
    "request_was":{
                "type":"INTERNAL_CRYPTO_TO_INTERNAL_CRYPTO",
                "source_associate_id": 20,
                "destination_associate_id": 100,
                "amount": 1.2,
                "currency_in": "DASH",
                "currency_out": "DASH",
                "timestamp_req":"152345465564",
                "note":"Some transaction note string"
        }
}
```

|Parameter|Type|Required|Description|
|---|---|---|---|---|
|timestamp_accepted|integer|false| timestamp when the transaction is accepted on service
|tx_id|string|string|Internal transaction identifier
|destination_address|string|true| Destination address
|status|string|true|Current transaction status
|request_was|[InternalRequest](#tocInternalRequest)|true|Original request



<h2 id="tocScreateassociateadminuserwithpasswordvm">CreateAssociateAdminUserWithPasswordVM</h2>


<a id="schemacreateassociateadminuserwithpasswordvm"></a>


```json
{
  "email": "string",
  "firstName": "string",
  "lastName": "string",
  "login": "string",
  "password": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|email|string|true|No description|
|firstName|string|true|No description|
|lastName|string|true|No description|
|login|string|true|No description|
|password|string|true|No description|


<h2 id="tocScreateassociateadminuservm">CreateAssociateAdminUserVM</h2>


<a id="schemacreateassociateadminuservm"></a>


```json
{
  "email": "string",
  "firstName": "string",
  "lastName": "string",
  "login": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|email|string|true|No description|
|firstName|string|true|No description|
|lastName|string|true|No description|
|login|string|true|No description|


<h2 id="tocSconversionstransactionsvm">ConversionsTransactionsVM</h2>


<a id="schemaconversionstransactionsvm"></a>


```json
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
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|amountDash|string|false|No description|
|amountFiat|string|false|No description|
|conversionFrom|string|false|No description|
|conversionRate|string|false|No description|
|conversionTo|string|false|No description|
|id|integer(int64)|false|No description|
|status|string|false|No description|
|timeAndDate|string(date-time)|false|No description|
|transactionId|string|false|No description|


<h2 id="tocScommissionfee">CommissionFee</h2>


<a id="schemacommissionfee"></a>


```json
{
  "associateId": 0,
  "commissionFee": 0
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|associateId|integer(int64)|true|No description|
|commissionFee|number|true|No description|


<h2 id="tocScoinfirm">Coinfirm</h2>


<a id="schemacoinfirm"></a>


```json
{
  "address": "string",
  "addressSubtype": "string",
  "addressType": "string",
  "avgCcInflow": 0,
  "avgCcInflowX": "string",
  "avgCcOutflow": 0,
  "avgCcOutflowX": 0,
  "avgTxFee": 0,
  "avgTxSize": 0,
  "balance": 0,
  "ccInflowX": 0,
  "ccOutflowX": 0,
  "clusterSize": 0,
  "cscore": 0,
  "daysWithoutTx": 0,
  "description": "string",
  "flags": "string",
  "id": 0,
  "initialBlockHeight": 0,
  "initialBlockTime": "string",
  "initialTxAmount": 0,
  "initialTxHash": "string",
  "initialTxUsdValue": 0,
  "lastInputTxAmount": 0,
  "lastInputTxBlockHeight": 0,
  "lastInputTxBlockTime": "string",
  "lastInputTxHash": "string",
  "lastInputTxUsdValue": 0,
  "lastOutputTxAmount": 0,
  "lastOutputTxBlockHeight": 0,
  "lastOutputTxBlockTime": "string",
  "lastOutputTxHash": "string",
  "lastOutputTxUsdValue": 0,
  "maxInflow": 0,
  "maxOutflow": 0,
  "minInflow": 0,
  "minOutflow": 0,
  "multisig": true,
  "profiles": "string",
  "receiveCount": 0,
  "receivePeak": 0,
  "recommendation": 0,
  "reportId": "string",
  "reportType": "string",
  "sentCount": 0,
  "time": "string",
  "totalInflow": 0,
  "totalOutflow": 0,
  "txCount": 0,
  "usdBalance": 0,
  "usdExchangeRate": 0,
  "whitelist": true
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|address|string|false|No description|
|addressSubtype|string|false|No description|
|addressType|string|false|No description|
|avgCcInflow|number(double)|false|No description|
|avgCcInflowX|string|false|No description|
|avgCcOutflow|number(double)|false|No description|
|avgCcOutflowX|number(double)|false|No description|
|avgTxFee|number(double)|false|No description|
|avgTxSize|number(double)|false|No description|
|balance|number(double)|false|No description|
|ccInflowX|integer(int64)|false|No description|
|ccOutflowX|integer(int64)|false|No description|
|clusterSize|integer(int64)|false|No description|
|cscore|integer(int64)|false|No description|
|daysWithoutTx|integer(int64)|false|No description|
|description|string|false|No description|
|flags|string|false|No description|
|id|integer(int64)|false|No description|
|initialBlockHeight|integer(int64)|false|No description|
|initialBlockTime|string|false|No description|
|initialTxAmount|integer(int64)|false|No description|
|initialTxHash|string|false|No description|
|initialTxUsdValue|number(double)|false|No description|
|lastInputTxAmount|integer(int64)|false|No description|
|lastInputTxBlockHeight|integer(int64)|false|No description|
|lastInputTxBlockTime|string|false|No description|
|lastInputTxHash|string|false|No description|
|lastInputTxUsdValue|number(double)|false|No description|
|lastOutputTxAmount|integer(int64)|false|No description|
|lastOutputTxBlockHeight|integer(int64)|false|No description|
|lastOutputTxBlockTime|string|false|No description|
|lastOutputTxHash|string|false|No description|
|lastOutputTxUsdValue|number(double)|false|No description|
|maxInflow|integer(int64)|false|No description|
|maxOutflow|integer(int64)|false|No description|
|minInflow|integer(int64)|false|No description|
|minOutflow|integer(int64)|false|No description|
|multisig|boolean|false|No description|
|profiles|string|false|No description|
|receiveCount|integer(int64)|false|No description|
|receivePeak|integer(int64)|false|No description|
|recommendation|integer(int64)|false|No description|
|reportId|string|false|No description|
|reportType|string|false|No description|
|sentCount|integer(int64)|false|No description|
|time|string|false|No description|
|totalInflow|integer(int64)|false|No description|
|totalOutflow|integer(int64)|false|No description|
|txCount|integer(int64)|false|No description|
|usdBalance|integer(int64)|false|No description|
|usdExchangeRate|number(double)|false|No description|
|whitelist|boolean|false|No description|


<h2 id="tocSchangepasswordvm">ChangePasswordVM</h2>


<a id="schemachangepasswordvm"></a>


```json
{
  "password": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|password|string|true|No description|


<h2 id="tocSassociate">Associate</h2>


<a id="schemaassociate"></a>


```json
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
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|address|string|true|No description|
|altAutosellInternal|boolean|false|No description|
|associateType|string|true|No description|
|autosell|boolean|false|No description|
|beneficiaryPercent|integer(int64)|false|No description|
|canEditOnboarded|boolean|false|No description|
|city|string|true|No description|
|coinaPultApiKey|string|false|No description|
|commissionFee|number|false|No description|
|companyEIN|string|false|No description|
|companyWebsite|string|true|No description|
|createdDate|string(date-time)|false|No description|
|cryptoCapitalApiKey|string|false|No description|
|customers|integer(int32)|false|No description|
|deletedDate|string(date-time)|false|No description|
|emailAddress|string|true|No description|
|enabled|boolean|false|No description|
|enrolledBy|[Associate](#schemaassociate)|false|No description|
|id|integer(int64)|false|No description|
|incorporationDate|string(date)|false|No description|
|internalFee|number(double)|false|No description|
|legalBusinessName|string|true|No description|
|locationsCount|integer(int32)|false|No description|
|merchants|integer(int32)|false|No description|
|note|string|false|No description|
|partners|integer(int32)|false|No description|
|phone|string|true|No description|
|posCount|integer(int32)|false|No description|
|state|[CountryState](#schemacountrystate)|true|No description|
|usBankAccount|string|false|No description|
|vendors|integer(int32)|false|No description|
|zip|string|true|No description|


#### Enumerated Values


|Property|Value|
|---|---|
|associateType|ALT36|
|associateType|PARTNER|
|associateType|MERCHANT|
|associateType|VENDOR|
|associateType|CUSTOMER|

<h2 id="tocSapikeyapisecretvm">ApiKeyApiSecretVM</h2>


<a id="schemaapikeyapisecretvm"></a>


```json
{
  "apiKey": "string",
  "apiSecret": "string",
  "registeredEmail": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|apiKey|string|true|No description|
|apiSecret|string|true|No description|
|registeredEmail|string|true|No description|

<!-- SalesVolume -->

<h2 id="tocSalesVolume">SalesVolume</h2>

<a id="schemasalesvolume"></a>
Note that the given example is only for associate SalesVolume object

```json
{
  "associate_id": 2102,
  "sales_crypto": 11.52008667,
  "sales_fiat": 7947.5531215589
}
```

|Parameter|Type|Required|Description|
|---|---|---|---|---|
|associate_id|integer|false| Associate identifier (used with associate sales volume)
|location_id|integer|false|Location idenfifier (used with location sales volume)
|pos_id|integer|false|POS identifier (used with pos sales volume)
|sales_crypto|number|true|Total sales in cryptocurrency
|sales_fiat|string|true|Total sales in FIAT currency (USD)
