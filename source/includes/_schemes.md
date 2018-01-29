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

|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|address|string|true|Address of the company|input|
|authorizedSignerContact|[AuthorizedSignerVM](#schemaauthorizedsignervm)|true|Object containing info regarding authorized signer in the company|input|
|city|string|true|City where company is located|input|
|companyEIN|string|true|Employer Identification Number of the company|input|
|companyWebsite|string|true|Website of the company|input|
|emailAddress|string|true|Email address for creating account|input|
|incorporationDate|string(date)|false|Company incorporation date with format YYYY-MM-DD|input|
|legalBusinessName|string|true|Company legal business name|input|
|mainContact|[ContactVM](#schemacontactvm)|true|Object containig info regarding main contact in the company|input|
|note|string|false|Any additional note|input|
|phone|string|true|Business phone|input|
|state|[CountryState](#schemacountrystate)|true|Object containing info about the state where company is located|input|
|usBankAccount|string|false|A bank account of the company|input|
|user|[CreateAssociateAdminUserWithPasswordVM](#schemacreateassociateadminuserwithpasswordvm)|false|Object containing info regarding user account.|input|
|zip|string|true|Zip code as part of company's address|input|


<h2 id="tocSshutdownaccountrequestvm">ShutDownAccountRequestVM</h2>


<a id="schemashutdownaccountrequestvm"></a>


```json
{
  "reason": "string"
}
```


### Properties


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|reason|string|true|Reason for closing an account|input|


<h2 id="tocSsort">Sort</h2>


<a id="schemasort"></a>

### Values

|Name|In|Required|Description|
|---|---|---|---|
|id|query|false|Sort list by id|
|asc|query|false|Sort list in ascending order|
|desc|query|true|Sort list in descending order|

Example

`http//example.com/api/exampleResource?sort=id,asc`

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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|accountNonExpired|boolean|false|No description|output|
|accountNonLocked|boolean|false|No description|output|
|activated|boolean|true|No description|output|
|associate|[Associate](#schemaassociate)|true|No description|output|
|credentialsNonExpired|boolean|false|No description|output|
|email|string|false|No description|both|
|enabled|boolean|false|No description|output|
|firstName|string|false|No description|both|
|id|integer(int64)|false|No description|both|
|imageUrl|string|false|No description|both|
|langKey|string|false|No description|both|
|lastLoginDateTime|string(date-time)|false|No description|output|
|lastName|string|false|No description|both|
|location|[Location](#schemalocation)|false|No description|both|
|login|string|true|No description|both|
|resetDate|string(date-time)|false|No description|output|
|splashscreenEnabled|boolean|false|No description|both|
|using2fa|boolean|false|Is two step authentication enabled for this user - read-only|output|


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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|activated|boolean|false|Is user account verified|output|
|authorities|Array[string]|false|User authorization roles|both|
|createdBy|string|false|Who created the user account|output|
|createdDate|string(date-time)|false|The date when user account has been created|output|
|email|string|false|Email address of the account|both|
|firstName|string|false|First name|both|
|lastName|string|false|Last Name|both|
|id|integer(int64)|false|User account id, read-only|both|
|login|string|true|Username|both|
|imageUrl|string|false|Image URL - not used at the moment|both|
|langKey|string|false|Language - not used at the moment|both|
|lastLoginDateTime|string(date-time)|false|Datetime when user has logged in last time|output|
|lastModifiedBy|string|false|Who modified the user account last time (not used at the moment)|output|
|lastModifiedDate|string(date-time)|false|When was the user account modified last time (not used at the moment)|output|
|splashscreenEnabled|boolean|false|Is splash screen for web app enabled|both|
|using2fa|boolean|false|Is two step authentication enabled for this user - read-only|output|


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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|activated|boolean|false|Is user account verified|output|
|authorities|Array[string]|false|User authorization roles|both|
|createdBy|string|false|Who created the user account|output|
|createdDate|string(date-time)|false|The date when user account has been created|output|
|email|string|false|Email address of the account|both|
|firstName|string|false|First name|both|
|lastName|string|false|Last Name|both|
|id|integer(int64)|false|User account id, read-only|both|
|login|string|true|Username|both|
|imageUrl|string|false|Image URL - not used at the moment|both|
|langKey|string|false|Language - not used at the moment|both|
|lastLoginDateTime|string(date-time)|false|Datetime when user has logged in last time|output|
|lastModifiedBy|string|false|Who modified the user account last time (not used at the moment)|output|
|lastModifiedDate|string(date-time)|false|When was the user account modified last time (not used at the moment)|output|
|splashscreenEnabled|boolean|false|Is splash screen for web app enabled|both|
|using2fa|boolean|false|Is two step authentication enabled for this user - read-only|output|


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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|amount|string|false|Withdrawal amount in USD|output|
|id|integer(int64)|false|Database id for transaction|output|
|status|string|false|Transaction status|output|
|timeAndDate|string(date-time)|false|Date and time of the transaction YYYY-MM-DDTHH:MM:SSZ|output|
|transactionId|string|false|Internal transaction id|output|


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
|content|[[UserDTO](#schemauserdto)]|false|UserDTO object|
|first|boolean|false|Is the current page first page - read-only|
|last|boolean|false|Is the current page last page - read-only|
|number|integer(int32)|false|Page index (starts from 0)|
|numberOfElements|integer(int32)|false|Number of elements on current page - read-only|
|size|integer(int32)|false|Number of elements to be returned |
|sort|[Sort](#schemasort)|false|Sorting parameters|
|totalElements|integer(int64)|false|Total number of available elements - read-only|
|totalPages|integer(int32)|false|Total number of pages - read-only|


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
|content|[[WithdrawalsTransactionsVm](#schemawithdrawalstransactionsvm)]|false|WithdrawlsTransactionsVm object|
|first|boolean|false|Is the current page first page - read-only|
|last|boolean|false|Is the current page last page - read-only|
|number|integer(int32)|false|Page index (starts from 0)|
|numberOfElements|integer(int32)|false|Number of elements on current page - read-only|
|size|integer(int32)|false|Number of elements to be returned |
|sort|[Sort](#schemasort)|false|Sorting parameters|
|totalElements|integer(int64)|false|Total number of available elements - read-only|
|totalPages|integer(int32)|false|Total number of pages - read-only|


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
|approved|integer(int64)|false|Number of approved entities|
|content|[[NewPartnerVM](#schemanewpartnervm)]|false|NewPartnerVM object|
|first|boolean|false|Is the current page first page - read-only|
|last|boolean|false|Is the current page last page - read-only|
|number|integer(int32)|false|Page index (starts from 0)|
|numberOfElements|integer(int32)|false|Number of elements on current page - read-only|
|size|integer(int32)|false|Number of elements to be returned |
|totalElements|integer(int64)|false|Total number of available elements - read-only|
|totalPages|integer(int32)|false|Total number of pages - read-only|
|pending|integer(int64)|false|Number of pending entities|

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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|amount|string|false|Amount in DASH|output|
|id|integer(int64)|false|Database ID of the transaction|output|
|receiver|string|false|Receiver business name|output|
|receiverType|string|false|Receiver type {PARTNER, MERCHANT, VENDOR, CUSTOMER, ALT36}|output|
|sender|string|false|Sender business name|output|
|senderType|string|false|Sender type {PARTNER, MERCHANT, VENDOR, CUSTOMER, ALT36}|output|
|status|string|false|Transaction status|output|
|timeAndDate|string(date-time)|false|Date and time of the transaction YYYY-MM-DDTHH:MM:SSZ|output|
|transactionId|string|false|Internal transaction ID|output|


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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|accompliceAssociate|[Associate](#schemaassociate)|false|No description|output|
|commissionFee|integer(int64)|false|No description|output|
|dateTime|string(date-time)|false|No description|output|
|destinationAddress|string|false|No description|output|
|direction|string|false|No description|output|
|externalWallet|[ExternalWallet](#schemaexternalwallet)|false|No description|output|
|id|integer(int64)|false|No description|output|
|location|[Location](#schemalocation)|false|No description|output|
|note|string|false|No description|output|
|originalAmount|integer(int64)|false|No description|output|
|ownerAssociate|[Associate](#schemaassociate)|false|No description|output|
|pointOfSale|[PointOfSale](#schemapointofsale)|false|No description|output|
|rawTransaction|string|false|No description|output|
|rawTxId|string|false|No description|output|
|type|string|false|No description|output|
|user|[User](#schemauser)|false|No description|output|


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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|active|boolean|false|No description|output|
|deletedDate|string(date-time)|false|No description|output|
|id|integer(int64)|false|Mandatory on update|both|
|inventoryNumber|string|false|No description|both|
|location|[LocationPOS](#schemalocationpos)|true|No description|both|
|name|string|false|No description|both|
|note|string|false|No description|both|
|pointOfSaleType|string|true|No description|both|
|virtualPointOfSalesEnabled|boolean|true|No description|both|


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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|address|string|false|No description|output|
|city|string|false|No description|output|
|geolocation|string|false|No description|output|
|id|integer(int64)|false|No description|output|
|name|string|false|No description|output|
|noofpos|integer(int64)|false|No description|output|
|state|string|false|No description|output|


<h2 id="tocSrequestfordeleteassociate">RequestForDeleteAssociate</h2>


<a id="schemarequestfordeleteassociate"></a>


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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|associateDelete|[Associate](#schemaassociate)|true|Associate object - for which the request was sent|both|
|dateRequested|string(date-time)|false|Date when request was made. |output|
|id|integer(int64)|false|ID of the request|both|
|reason|string|true|Reason for delete|output|
|requestedBy|[Associate](#schemaassociate)|false|Associate object - who has sent the request|output|


<h2 id="tocSresetpasswordvm">ResetPasswordVM</h2>


<a id="schemaresetpasswordvm"></a>


```json
{
  "email": "john.doe@example.com"
}
```


### Properties


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|email|string|true|Email for password reset init.|input|


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
|body|object|false|Empty body|
|statusCode|string|false|Status code|
|statusCodeValue|integer(int32)|false|Status code value (HTTP codes)|


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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|amountInDash|string|false|Amount in DASH|output|
|amountInUSD|string|false|Amount in USD|output|
|commisionFeeinDash|string|false|Commission fee charged in DASH|output|
|commisionFeeinUSD|string|false|Commission fee charged in USD|output|
|id|integer(int64)|false|Database transaction ID|output|
|location|string|false|Location name|output|
|pointOfSale|string|false|Point of sale name|output|
|status|string|false|status {Pending, Succeded, Failed}|output|
|timeAndDate|string(date-time)|false|Date and time of the transaction YYY-MM-DDTHH:MM:SSZ|output|
|transactionId|string|false|Internal transaction ID|output|


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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|emailAddress|string|true|Customer's email address|input|
|legalBusinessName|string|true|Please populate with "CUSTOMER"|input|
|phone|string|true|Phone number of a customer|input|
|user|[CreateAssociateAdminUserWithPasswordVM](#schemacreateassociateadminuserwithpasswordvm)|true|User object|input|

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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|password|string|true|Password for login|input|
|rememberMe|boolean|false|If enabled, authorization token will last for 30 days. If not token will last for 24 hours|input|
|username|string|true|Username/email for login|input|


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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|id|integer(int64)|false|No description|output|
|merchant|[Associate](#schemaassociate)|true|No description|input|
|note|string|false|No description|both|
|vendor|[Associate](#schemaassociate)|true|No description|input|


<h2 id="tocSnewcustomervm">NewCustomerVM</h2>


<a id="schemanewcustomervm"></a>


```json
{
  "emailAddress": "string",
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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|emailAddress|string|true|Customer's email|input|
|legalBusinessName|string|true|Please populate with "CUSTOMER"|input|
|phone|string|true|Customer's phone number|input|
|user|[CreateAssociateAdminUserVM](#schemacreateassociateadminuservm)|true|CreateAssociateAdminUserVM object|input|

<h2 id="tocSnewcustomervm2">NewCustomerVM2</h2>


<a id="schemanewcustomervm2"></a>


```json
{
  "id": 1,
  "emailAddress": "string",
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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|id|integer(int64)|true|ID of the customer - read-only|input|
|emailAddress|string|true|Email address of the customer.|input|
|legalBusinessName|string|true|Please populate with "CUSTOMER"|input|
|phone|string|true|Customer's phone number|input|
|user|[CreateAssociateAdminUserVM](#schemacreateassociateadminuservm)|true|CreateAssociateAdminUserVM object|input|

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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|address|string|true|Address of the company|both|
|address2|string|false|Address of the company (line2)|both|
|altAutosellInternal|boolean|false|For internal use - read-only|output|
|authorizedSignerContact|[AuthorizedSignerVM](#schemaauthorizedsignervm)|true|Object containing info regarding authorized signer in the company|both|
|autosell|boolean|false|Enable/disable autosell feature for merchants. Enabled means funds will be converted in USD immediately|output|
|canEditOnboarded|boolean|false|Provides info if a partner can edit his merchants and vendors - read-only|output|
|city|string|true|City where company is located|both|
|commissionFee|number(double)|false|Commission fee for the company - read-only (0,1)|output|
|companyEIN|string|true|Employer Identification Number of the company|both|
|companyWebsite|string|true|Website of the company|both|
|createdDate|string(date-time)|false|Provides info when the entity has been created - read-only|output|
|customers|integer(int32)|false|Number of customers - read-only|output|
|emailAddress|string|true|Email address for creating account|both|
|enabled|boolean|false|Provides info if the entity has been approved by AltThirtySix Admin - read-only|output|
|enroledBy|[Associate](#schemaassociate)|false|Provides info about the parent of an entity - read-only|output|
|id|integer(int64)|false|ID of the entity assigned by system - read-only|both|
|incorporationDate|string(date)|true|Company incorporation date with format YYYY-MM-DD|both|
|legalBusinessName|string|true|Company legal business name|both|
|locationsCount|integer(int32)|false|Number of locations - read-only|output|
|mainContact|[ContactVM](#schemacontactvm)|true|Object containing info regarding main contact in the company|output|
|merchants|integer(int32)|false|Number of merchants - read-only|output|
|note|string|false|Any additional note|both|
|partners|integer(int32)|false|Number of partners - read-only|output|
|phone|string|true|Company's business phone|both|
|posCount|integer(int32)|false|Number of pos - read-only|output|
|saleVolume|number(double)|false|Sales volume of an entity|output|
|state|[CountryState](#schemacountrystate)|true|Object containing info about the state where company is located|both|
|usBankAccount|string|false|A bank account of the company|both|
|user|[CreateAssociateAdminUserVM](#schemacreateassociateadminuservm)|true|Object containing info regarding user account.|both|
|vendors|integer(int32)|false|Number of vendors - read-only|output|
|zip|string|true|Zip code as part of company's address|both|

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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|id|integer(int64)|true|ID of the entity assigned by system - read-only|both|
|address|string|true|Address of the company|both|
|address2|string|false|Address of the company (line2)|both|
|altAutosellInternal|boolean|false|For internal use - read-only|output|
|authorizedSignerContact|[AuthorizedSignerVM](#schemaauthorizedsignervm)|true|Object containing info regarding authorized signer in the company|both|
|autosell|boolean|false|Enable/disable autosell feature for merchants. Enabled means funds will be converted in USD immediately|
|canEditOnboarded|boolean|false|Provides info if a partner can edit his merchants and vendors - read-only|output|
|city|string|true|City where company is located|both|
|commissionFee|number(double)|false|Commission fee for the company - read-only (0,1)|output|
|companyEIN|string|true|Employer Identification Number of the company|both|
|companyWebsite|string|true|Website of the company|both|
|createdDate|string(date-time)|false|Provides info when the entity has been created - read-only|output|
|customers|integer(int32)|false|Number of customers - read-only|output|
|emailAddress|string|true|Email address for creating account|both|
|enabled|boolean|false|Provides info if the entity has been approved by AltThirtySix Admin - read-only|output|
|enroledBy|[Associate](#schemaassociate)|false|Provides info about the parent of an entity - read-only|output|
|incorporationDate|string(date)|true|Company incorporation date with format YYYY-MM-DD|both|
|legalBusinessName|string|true|Company legal business name|both|
|locationsCount|integer(int32)|false|Number of locations - read-only|output|
|mainContact|[ContactVM](#schemacontactvm)|true|Object containing info regarding main contact in the company|both|
|merchants|integer(int32)|false|Number of merchants - read-only|output|
|note|string|false|Any additional note|both|
|partners|integer(int32)|false|Number of partners - read-only|output|
|phone|string|true|Company's business phone|both|
|posCount|integer(int32)|false|Number of pos - read-only|output|
|saleVolume|number(double)|false|Sales volume of an entity|output|
|state|[CountryState](#schemacountrystate)|true|Object containing info about the state where company is located|both|
|usBankAccount|string|false|A bank account of the company|both|
|user|[CreateAssociateAdminUserVM](#schemacreateassociateadminuservm)|false|Object containing info regarding user account.|both|
|vendors|integer(int32)|false|Number of vendors - read-only|output|
|zip|string|true|Zip code as part of company's address|both|

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
    "email": "string",
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
|id|integer(int64)|true|ID of the entity - assigned by system|
|address|string|true|Address of the company|
|address2|string|false|Address of the company (line2)|
|altAutosellInternal|boolean|false|For internal use - read-only|
|authorizedSignerContact|[AuthorizedSignerVM](#schemaauthorizedsignervm)|true|Object containing info regarding authorized signer in the company|
|autosell|boolean|false|Enable/disable autosell feature for merchants. Enabled means funds will be converted in USD immediately|
|canEditOnboarded|boolean|false|Provides info if a partner can edit his merchants and vendors - read-only|
|city|string|true|City where company is located|
|commissionFee|number(double)|false|Commission fee for the company - read-only (0,1)|
|companyEIN|string|true|Employer Identification Number of the company|
|companyWebsite|string|true|Website of the company|
|createdDate|string(date-time)|false|Provides info when the entity has been created - read-only|
|customers|integer(int32)|false|Number of customers - read-only|
|emailAddress|string|true|Email address for creating account|
|enabled|boolean|false|Provides info if the entity has been approved by AltThirtySix Admin - read-only|
|enroledBy|[Associate](#schemaassociate)|false|Provides info about the parent of an entity - read-only|
|incorporationDate|string(date)|true|Company incorporation date with format YYYY-MM-DD|
|legalBusinessName|string|true|Company legal business name|
|locationsCount|integer(int32)|false|Number of locations|
|mainContact|[ContactVM](#schemacontactvm)|true|Object containing info regarding main contact in the company|
|merchants|integer(int32)|false|Number of merchants - read-only|
|note|string|false|Any additional note|
|partners|integer(int32)|false|Number of partners - read-only|
|phone|string|true|Company's business phone|
|posCount|integer(int32)|false|Number of pos - read-only|
|saleVolume|number(double)|false|Sales volume of an entity|
|state|[CountryState](#schemacountrystate)|true|Object containing info about the state where company is located|
|usBankAccount|string|false|A bank account of the company|
|user|[CreateAssociateAdminUserVM](#schemacreateassociateadminuservm)|false|Object containing info regarding user account.|
|vendors|integer(int32)|false|Number of vendors - read-only|
|zip|string|true|Zip code as part of company's address|


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
|address|string|true|Address of the company|
|address2|string|false|Address of the company (line2)|
|altAutosellInternal|boolean|false|For internal use - read-only|
|authorizedSignerContact|[AuthorizedSignerVM](#schemaauthorizedsignervm)|true|Object containing info regarding authorized signer in the company|
|autosell|boolean|false|Enable/disable autosell feature for merchants. Enabled means funds will be converted in USD immediately|
|canEditOnboarded|boolean|false|Provides info if a partner can edit his merchants and vendors - read-only|
|city|string|true|City where company is located|
|commissionFee|number(double)|false|Commission fee for the company - read-only (0,1)|
|companyEIN|string|true|Employer Identification Number of the company|
|companyWebsite|string|true|Website of the company|
|createdDate|string(date-time)|false|Provides info when the entity has been created - read-only|
|customers|integer(int32)|false|Number of customers - read-only|
|emailAddress|string|true|Email address for creating account|
|enabled|boolean|false|Provides info if the entity has been approved by AltThirtySix Admin - read-only|
|enroledBy|[Associate](#schemaassociate)|false|Provides info about the parent of an entity - read-only|
|id|integer(int64)|false|ID of the entity assigned by system - read-only|
|incorporationDate|string(date)|true|Company incorporation date with format YYYY-MM-DD|
|legalBusinessName|string|true|Company legal business name|
|locationsCount|integer(int32)|false|Number of locations - read-only|
|mainContact|[ContactVM](#schemacontactvm)|true|Object containing info regarding main contact in the company|
|merchants|integer(int32)|false|Number of merchants - read-only|
|note|string|false|Any additional note|
|partners|integer(int32)|false|Number of partners - read-only|
|phone|string|true|Company's business phone|
|posCount|integer(int32)|false|Number of pos - read-only|
|saleVolume|number(double)|false|Sales volume of an entity|
|state|[CountryState](#schemacountrystate)|true|Object containing info about the state where company is located|
|usBankAccount|string|false|A bank account of the company|
|user|[CreateAssociateAdminUserVM](#schemacreateassociateadminuservm)|true|Object containing info regarding user account.|
|vendors|integer(int32)|false|Number of vendors - read-only|
|zip|string|true|Zip code as part of company's address|


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
|id|integer(int64)|true|ID of the entity assigned by system - read-only|
|address|string|true|Address of the company|
|address2|string|false|Address of the company (line2)|
|altAutosellInternal|boolean|false|For internal use - read-only|
|authorizedSignerContact|[AuthorizedSignerVM](#schemaauthorizedsignervm)|true|Object containing info regarding authorized signer in the company|
|autosell|boolean|false|Enable/disable autosell feature for merchants. Enabled means funds will be converted in USD immediately|
|canEditOnboarded|boolean|false|Provides info if a partner can edit his merchants and vendors - read-only|
|city|string|true|City where company is located|
|commissionFee|number(double)|false|Commission fee for the company - read-only (0,1)|
|companyEIN|string|true|Employer Identification Number of the company|
|companyWebsite|string|true|Website of the company|
|createdDate|string(date-time)|false|Provides info when the entity has been created - read-only|
|customers|integer(int32)|false|Number of customers - read-only|
|emailAddress|string|true|Email address for creating account|
|enabled|boolean|false|Provides info if the entity has been approved by AltThirtySix Admin - read-only|
|enroledBy|[Associate](#schemaassociate)|false|Provides info about the parent of an entity - read-only|
|incorporationDate|string(date)|true|Company incorporation date with format YYYY-MM-DD|
|legalBusinessName|string|true|Company legal business name|
|locationsCount|integer(int32)|false|Number of locations - read-only|
|mainContact|[ContactVM](#schemacontactvm)|true|Object containing info regarding main contact in the company|
|merchants|integer(int32)|false|Number of merchants - read-only|
|note|string|false|Any additional note|
|partners|integer(int32)|false|Number of partners - read-only|
|phone|string|true|Company's business phone|
|posCount|integer(int32)|false|Number of pos - read-only|
|saleVolume|number(double)|false|Sales volume of an entity|
|state|[CountryState](#schemacountrystate)|true|Object containing info about the state where company is located|
|usBankAccount|string|false|A bank account of the company|
|user|[CreateAssociateAdminUserVM](#schemacreateassociateadminuservm)|false|Object containing info regarding user account.|
|vendors|integer(int32)|false|Number of vendors - read-only|
|zip|string|true|Zip code as part of company's address|

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
|content|[[Associate](#schemaassociate)]|false|Associate object|
|first|boolean|false|Is the current page first page - read-only|
|last|boolean|false|Is the current page last page - read-only|
|number|integer(int32)|false|Page index (starts from 0)|
|numberOfElements|integer(int32)|false|Number of elements on current page - read-only|
|size|integer(int32)|false|Number of elements to be returned |
|sort|[Sort](#schemasort)|false|Sorting parameters|
|totalElements|integer(int64)|false|Total number of available elements - read-only|
|totalPages|integer(int32)|false|Total number of pages - read-only|


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
|content|[[ConversionsTransactionsVM](#schemaconversionstransactionsvm)]|false|ConversionTransaction Object|
|first|boolean|false|Is the current page first page - read-only|
|last|boolean|false|Is the current page last page - read-only|
|number|integer(int32)|false|Page index (starts from 0)|
|numberOfElements|integer(int32)|false|Number of elements on current page - read-only|
|size|integer(int32)|false|Number of elements to be returned |
|sort|[Sort](#schemasort)|false|Sorting parameters|
|totalElements|integer(int64)|false|Total number of available elements - read-only|
|totalPages|integer(int32)|false|Total number of pages - read-only|


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
|content|[[Invitation](#schemainvitation)]|false|Invitation object|
|first|boolean|false|Is the current page first page - read-only|
|last|boolean|false|Is the current page last page - read-only|
|number|integer(int32)|false|Page index (starts from 0)|
|numberOfElements|integer(int32)|false|Number of elements on current page - read-only|
|size|integer(int32)|false|Number of elements to be returned |
|sort|[Sort](#schemasort)|false|Sorting parameters|
|totalElements|integer(int64)|false|Total number of available elements - read-only|
|totalPages|integer(int32)|false|Total number of pages - read-only|


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
|content|[[Location](#schemalocation)]|false|Location object|
|first|boolean|false|Is the current page first page - read-only|
|last|boolean|false|Is the current page last page - read-only|
|number|integer(int32)|false|Page index (starts from 0)|
|numberOfElements|integer(int32)|false|Number of elements on current page - read-only|
|size|integer(int32)|false|Number of elements to be returned |
|sort|[Sort](#schemasort)|false|Sorting parameters|
|totalElements|integer(int64)|false|Total number of available elements - read-only|
|totalPages|integer(int32)|false|Total number of pages - read-only|


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
|content|[[MerchantVendor](#schemamerchantvendor)]|false|Merchant's favorite Vendor object|
|first|boolean|false|Is the current page first page - read-only|
|last|boolean|false|Is the current page last page - read-only|
|number|integer(int32)|false|Page index (starts from 0)|
|numberOfElements|integer(int32)|false|Number of elements on current page - read-only|
|size|integer(int32)|false|Number of elements to be returned |
|sort|[Sort](#schemasort)|false|Sorting parameters|
|totalElements|integer(int64)|false|Total number of available elements - read-only|
|totalPages|integer(int32)|false|Total number of pages - read-only|


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
|content|[[NewPartnerVM](#schemanewpartnervm)]|false|NewPartnerVM object|
|first|boolean|false|Is the current page first page - read-only|
|last|boolean|false|Is the current page last page - read-only|
|number|integer(int32)|false|Page index (starts from 0)|
|numberOfElements|integer(int32)|false|Number of elements on current page - read-only|
|size|integer(int32)|false|Number of elements to be returned |
|sort|[Sort](#schemasort)|false|Sorting parameters|
|totalElements|integer(int64)|false|Total number of available elements - read-only|
|totalPages|integer(int32)|false|Total number of pages - read-only|


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
|content|[[PaymentsTransactionVm](#schemapaymentstransactionvm)]|false|PaymentTransaction object|
|first|boolean|false|Is the current page first page - read-only|
|last|boolean|false|Is the current page last page - read-only|
|number|integer(int32)|false|Page index (starts from 0)|
|numberOfElements|integer(int32)|false|Number of elements on current page - read-only|
|size|integer(int32)|false|Number of elements to be returned |
|sort|[Sort](#schemasort)|false|Sorting parameters|
|totalElements|integer(int64)|false|Total number of available elements - read-only|
|totalPages|integer(int32)|false|Total number of pages - read-only|


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
|content|[[PendingTransaction](#schemapendingtransaction)]|false|PendingTransaction object|
|first|boolean|false|Is the current page first page - read-only|
|last|boolean|false|Is the current page last page - read-only|
|number|integer(int32)|false|Page index (starts from 0)|
|numberOfElements|integer(int32)|false|Number of elements on current page - read-only|
|size|integer(int32)|false|Number of elements to be returned |
|sort|[Sort](#schemasort)|false|Sorting parameters|
|totalElements|integer(int64)|false|Total number of available elements - read-only|
|totalPages|integer(int32)|false|Total number of pages - read-only|


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
|content|[[PointOfSale](#schemapointofsale)]|false|Point of Sale object|
|first|boolean|false|Is the current page first page - read-only|
|last|boolean|false|Is the current page last page - read-only|
|number|integer(int32)|false|Page index (starts from 0)|
|numberOfElements|integer(int32)|false|Number of elements on current page - read-only|
|size|integer(int32)|false|Number of elements to be returned |
|sort|[Sort](#schemasort)|false|Sorting parameters|
|totalElements|integer(int64)|false|Total number of available elements - read-only|
|totalPages|integer(int32)|false|Total number of pages - read-only|


<h2 id="tocSpageofrequestfordeleteassociate">PageOfRequestForDeleteAssociate</h2>


<a id="schemapageofrequestfordeleteassociate"></a>


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
|content|[[RequestForDeleteAssociate](#schemarequestfordeleteassociate)]|false|RequestForDeleteAssociate object|
|first|boolean|false|Is the current page first page - read-only|
|last|boolean|false|Is the current page last page - read-only|
|number|integer(int32)|false|Page index (starts from 0)|
|numberOfElements|integer(int32)|false|Number of elements on current page - read-only|
|size|integer(int32)|false|Number of elements to be returned |
|sort|[Sort](#schemasort)|false|Sorting parameters|
|totalElements|integer(int64)|false|Total number of available elements - read-only|
|totalPages|integer(int32)|false|Total number of pages - read-only|


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
|content|[[SalesTransactionVM](#schemasalestransactionvm)]|false|SalesTransaction object|
|first|boolean|false|Is the current page first page - read-only|
|last|boolean|false|Is the current page last page - read-only|
|number|integer(int32)|false|Page index (starts from 0)|
|numberOfElements|integer(int32)|false|Number of elements on current page - read-only|
|size|integer(int32)|false|Number of elements to be returned |
|sort|[Sort](#schemasort)|false|Sorting parameters|
|totalElements|integer(int64)|false|Total number of available elements - read-only|
|totalPages|integer(int32)|false|Total number of pages - read-only|


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
|email|string|true|Email to which the invitation will be sent|


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
|key|string|true|Key for password reset - read-only|
|newPassword|string|true|New password, min 8 characters long, min one uppercase letter one lowercase letter one digit|


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
|amountInDASH|number(double)|false|Last transaction amount in DASH - read-only|
|amountInUSD|number(double)|false|Last transaction amount in USD - read-only|
|dateTime|string(date-time)|false|Last transaction date and time YYY-MM-DDTHH:MM:SSZ- read-only|


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
|website|string|false|website URL|
|zip|string|true|Zip code|


<h2 id="tocSlocationpos">LocationPOS</h2>


<a id="schemalocationpos"></a>


```json
{
  "id": 1
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|id|integer(int64)|false|No description|

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
|file|string|true|Location license with format: data:image/png;base64,image_in_base_64|
|fileContentType|string|true|[FileContentType](#tocFileContentType)|
|geoLocation|string|true|Example 33.8608908,-117.7381407|
|id|integer(int64)|false|Mandatory on update|
|merchantId|integer(int64)|true|ID of a merchant for which location needs to be created|
|name|string|true|No description|
|noOfPos|integer(int32)|false|No description|
|note|string|false|No description|
|parentLocationId|integer(int64)|false|For future use|
|phone|string|true|No description|
|state|[CountryState](#schemacountrystate)|true|No description|
|website|string|true|No description|
|zip|string|true|Zip code|


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
|file|string|true|Location license with format: data:image/png;base64,image_in_base_64|
|fileContentType|string|true|[FileContentType](#tocFileContentType)|
|geoLocation|string|true|Example 33.8608908,-117.7381407|
|id|integer(int64)|false|Mandatory on update|
|name|string|true|No description|
|noOfPos|integer(int32)|false|No description|
|note|string|false|No description|
|parentLocationId|integer(int64)|false|For future use|
|phone|string|true|No description|
|state|[CountryState](#schemacountrystate)|true|No description|
|website|string|true|No description|
|zip|string|true|Zip code|


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
|parentLocationId|integer(int64)|false|For future use|
|phone|string|false|No description|
|state|[CountryState](#schemacountrystate)|true|No description|
|website|string|false|website URL|
|zip|string|true|Zip code|


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

<h2 id="tocScountrystate">CountryState</h2>


<a id="schemacountrystate"></a>


```json
{
  "abbreviation": "string",
  "id": 1,
  "state": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|abbreviation|string|false|No description|
|id|integer(int64)|true|[Get all states](#opIdgetAllCountryStatesUsingGET)|
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
|birthDate|string(date)|false|YYYY-MM-DD|
|city|string|false|No description|
|file|string|false|No description|
|fileBytes|string(byte)|false|No description|
|fileContentType|string|false|No description|
|firstName|string|true|No description|
|gender|string|false|No description|
|id|integer(int64)|false|No description|
|lastName|string|true|No description|
|nationality|string|false|No description|
|note|string|false|No description|
|passportExpiryDate|string(date)|false|YYYY-MM-DD|
|passportIssueDate|string(date)|false|YYYY-MM-DD|
|passportNumber|string|false|No description|
|position|string|true|No description|
|primaryEmailAddress|string|true|No description|
|primaryMobilePhone|string|true|No description|
|secondaryEmailAddress|string|false|No description|
|secondaryMobilePhone|string|false|No description|
|state|[CountryState](#schemacountrystate)|false|No description|
|zip|string|false|No description|

<h2 id="tocSchemaAuthorizedSignervm">AuthorizedSignerVM</h2>


<a id="schemaauthorizedsignervm"></a>


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
|birthDate|string(date)|true|YYYY-MM-DD|
|city|string|false|No description|
|file|string|false|UUID of the file once it's uploaded. Provided only within GET method.|
|fileBytes|string(byte)|true|Base64 encoded file content Max 5.000.000 bytes|
|fileContentType|string|true|[Allowed types](#tocFileContentType)|
|firstName|string|true|No description|
|gender|string|false|No description|
|id|integer(int64)|false|No description|
|lastName|string|true|No description|
|nationality|string|true|No description|
|note|string|false|No description|
|passportExpiryDate|string(date)|true|YYYY-MM-DD|
|passportIssueDate|string(date)|true|YYYY-MM-DD|
|passportNumber|string|true|No description|
|position|string|false|No description|
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


<h2 id="tocFileContentType">FileContentType</h2>


<a id="schemafilecontenttype"></a>

|Property|Value|
|---|---|
|fileContentType|image/jpeg|
|fileContentType|image/png|
|fileContentType|application/pdf|
|fileContentType|application/msword|
|fileContentType|text/csv|


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
|contactType|string|true|[Enumerated Values](#tocenumeratedvalues)|
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

<h3 id="tocenumeratedvalues">Enumerated Values</h3>

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
|Parameter|Type|Required|Description|input/output parameter|
|---|---|---|---|---|---|
|timerange_from|string|true|Start date/datetime in ISO format|output|
|timerange_to|string|true|End date/datetime in ISO format|output|
|number|integer|true|Page number|output|
|size|number|true|Page size|output|
|numberOfElements|integer|true|Total number of elements|output|
|totalPages|Integer|true|Total number of pages|output|
|first|boolean|true|Is this the first page|output|
|last|Integer|true|Is this the last page|output|

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
|Parameter|Type|Required|Description|input/output parameter|
|---|---|---|---|---|---|
|metadata|[ReportMetadata](#schemareportmetadata)|true|Response metadata|output|
|data|Array([LocationPerformanceItem](#schemarepotlocationperformanceitem))|true|Arary of location performance data|output|


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
|Parameter|Type|Required|Description|input/output parameter|
|---|---|---|---|---|---|
|metadata|[ReportMetadata](#schemareportmetadata)|true|Response metadata|output|
|data|Array([RolePerformanceItem](#schemareportroleperformanceitem))|true|Arary of location performance data|output|

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
|Parameter|Type|Required|Description|input/output parameter|
|---|---|---|---|---|---|
|metadata|[ReportMetadata](#schemareportmetadata)|true|Response metadata|output|
|data|Array([TaxItem](#schemataxitem))|true|Array of tax items|output|


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
|Parameter|Type|Required|Description|input/output parameter|
|---|---|---|---|---|---|
|metadata|[ReportMetadata](#schemareportmetadata)|true|Response metadata|output|
|data|Array([SalesItem](#schemasalesitem))|true|Array of sales items|output|

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
|Parameter|Type|Required|Description|input/output parameter|
|---|---|---|---|---|---|
|metadata|[ReportMetadata](#schemareportmetadata)|true|Response metadata|output|
|summary|[SummaryItem](#tocSummaryItem)|true|Summary data - ralates to all pages of data.|output|
|data|Array([PartnerResponseItem](#tocPartnerResponseItem))|true|Array of objects|output|

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
|Parameter|Type|Required|Description|input/output parameter|
|---|---|---|---|---|---|
|metadata|[ReportMetadata](#schemareportmetadata)|true|Response metadata|output|
|summary|[SummaryItem](#tocSummaryItem)|true|Summary data - ralates to all pages of data.|output|
|data|Array([MerchantResponseItem](#tocMerchantResponseItem))|true|Array of objects|output|

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
|Parameter|Type|Required|Description|input/output parameter|
|---|---|---|---|---|---|
|metadata|[ReportMetadata](#schemareportmetadata)|true|Response metadata|output|
|summary|[SummaryItem](#tocSummaryItem)|true|Summary data - ralates to all pages of data.|output|
|data|Array([LocationResponseItem](#tocLocationResponseItem))|true|Array of objects|output|


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
|Parameter|Type|Required|Description|input/output parameter|
|---|---|---|---|---|---|
|metadata|[ReportMetadata](#schemareportmetadata)|true|Response metadata|output|
|summary|[SummaryItem](#tocSummaryItem)|true|Summary data - ralates to all pages of data.|output|
|data|Array([POSResponseItem](#tocPOSResponseItem))|true|Array of objects|output|


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
|Parameter|Type|Required|Description|input/output parameter|
|---|---|---|---|---|---|
|metadata|[ReportMetadata](#schemareportmetadata)|true|Response metadata|output|
|content|[TaxResponseItem](#tocTaxResposeItemItem)|true| Tax report item instance|output|

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
|Parameter|Type|Required|Description|input/output parameter|
|---|---|---|---|---|---|
|metadata|[ReportMetadata](#schemareportmetadata)|true|Response metadata|output|
|content|Array([CommissionResponseItem])(#tocCommissionResposeItemItem)|true| Array of commission report intems|output|

<!-- ErrorMessage -->
<h2 id="tocErrorMessage">ErrorMessage</h2>

<a id="schemareporterrormessage"></a>

```json
{
  "message":"There was an error processing the request"
}

```
|Parameter|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|message|string|true|Error message returned along with status code|output|


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

|Parameter|Type|Required|Description|input/output parameter|
|---|---|---|---|---|---|
|tx_id|string|false|Internal transaction id, this is part of internal transaction storage.|output|
|tx_state|string|true|Current state of the transaction|output|
|requested_amount|number|true|Requested amount that system generated|output|
|requested_currency|string|true|Requested currency|output|
|converted_to_amount|number|true|To which mount value has been converted|output|
|converted_to_currency|string|true|Curency conversion|output|
|timestamp_resp|integer|true|Response timestamp created on server|output|
|pay_to_address|string|true|The address that has been payed to|output|
|warning_msg|[ErrorMessage](#tocErrorMessage)|true|Warning message (could be omitted)|output|


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

|Parameter|Type|Required|Description|input/output parameter|
|---|---|---|---|---|---|
|type|string|false| Enumeration (INTERNAL_CRYPTO_TO_INTERNAL_CRYPTO, INTERNAL_CRYPTO_TO_EXTERNAL_CRYPTO, INTERNAL_CRYPTO_TO_FIAT, FIAT_TO_INTERNAL_CRYPTO, INTERNAL_FIAT_TO_EXTERNAL_FIAT).|input|
|source_associate_id|integer|true|Internal associate Id of transaction initiator|input|
|destination_associate_id|integer|true|Internal associate id of transaction destination|input|
|amount|number|true|Amount to transfer|input|
|currency_in|string|true|Currency that is transfered|input|
|currency_out|string|true|Currency to which is transfered|input|
|timestamp_req|integer|true|Timestamp of the request|input|
|note|string|false|General note about transaction|input|


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

|Parameter|Type|Required|Description|input/output parameter|
|---|---|---|---|---|---|
|timestamp_accepted|integer|false| timestamp when the transaction is accepted on service| output|
|tx_id|string|string|Internal transaction identifier| output|
|destination_address|string|true| Destination address| output|
|status|string|true|Current transaction status| output|
|request_was|[InternalRequest](#tocInternalRequest)|true|Original request| output|



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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|email|string|true|Account | input|
|firstName|string|true|First name|input|
|lastName|string|true|Last name|input|
|login|string|true|Login|input|
|password|string|true|Min requirements: 8 characters long, uppercase, digits and lower case letters|input|

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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|email|string|true|valid Email|both|
|firstName|string|true|First name|both|
|lastName|string|true|Last name|both|
|login|string|true|Login|both|


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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|amountDash|string|false|No description|output|
|amountFiat|string|false|No description|output|
|conversionFrom|string|false|No description|output|
|conversionRate|string|false|No description|output|
|conversionTo|string|false|No description|output|
|id|integer(int64)|false|No description|output|
|status|string|false|No description|output|
|timeAndDate|string(date-time)|false|No description|output|
|transactionId|string|false|No description|output|


<h2 id="tocScommissionfee">CommissionFee</h2>


<a id="schemacommissionfee"></a>


```json
{
  "associateId": 0,
  "commissionFee": 0
}
```


### Properties


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|associateId|integer(int64)|true|No description|both|
|commissionFee|number|true|No description|both|


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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|address|string|false|No description|output|
|addressSubtype|string|false|No description|output|
|addressType|string|false|No description|output|
|avgCcInflow|number(double)|false|No description|output|
|avgCcInflowX|string|false|No description|output|
|avgCcOutflow|number(double)|false|No description|output|
|avgCcOutflowX|number(double)|false|No description|output|
|avgTxFee|number(double)|false|No description|output|
|avgTxSize|number(double)|false|No description|output|
|balance|number(double)|false|No description|output|
|ccInflowX|integer(int64)|false|No description|output|
|ccOutflowX|integer(int64)|false|No description|output|
|clusterSize|integer(int64)|false|No description|output|
|cscore|integer(int64)|false|No description|output|
|daysWithoutTx|integer(int64)|false|No description|output|
|description|string|false|No description|output|
|flags|string|false|No description|output|
|id|integer(int64)|false|No description|output|
|initialBlockHeight|integer(int64)|false|No description|output|
|initialBlockTime|string|false|No description|output|
|initialTxAmount|integer(int64)|false|No description|output|
|initialTxHash|string|false|No description|output|
|initialTxUsdValue|number(double)|false|No description|output|
|lastInputTxAmount|integer(int64)|false|No description|output|
|lastInputTxBlockHeight|integer(int64)|false|No description|output|
|lastInputTxBlockTime|string|false|No description|output|
|lastInputTxHash|string|false|No description|output|
|lastInputTxUsdValue|number(double)|false|No description|output|
|lastOutputTxAmount|integer(int64)|false|No description|output|
|lastOutputTxBlockHeight|integer(int64)|false|No description|output|
|lastOutputTxBlockTime|string|false|No description|output|
|lastOutputTxHash|string|false|No description|output|
|lastOutputTxUsdValue|number(double)|false|No description|output|
|maxInflow|integer(int64)|false|No description|output|
|maxOutflow|integer(int64)|false|No description|output|
|minInflow|integer(int64)|false|No description|output|
|minOutflow|integer(int64)|false|No description|output|
|multisig|boolean|false|No description|output|
|profiles|string|false|No description|output|
|receiveCount|integer(int64)|false|No description|output|
|receivePeak|integer(int64)|false|No description|output|
|recommendation|integer(int64)|false|No description|output|
|reportId|string|false|No description|output|
|reportType|string|false|No description|output|
|sentCount|integer(int64)|false|No description|output|
|time|string|false|No description|output|
|totalInflow|integer(int64)|false|No description|output|
|totalOutflow|integer(int64)|false|No description|output|
|txCount|integer(int64)|false|No description|output|
|usdBalance|integer(int64)|false|No description|output|
|usdExchangeRate|number(double)|false|No description|output|
|whitelist|boolean|false|No description|output|


<h2 id="tocSchangepasswordvm">ChangePasswordVM</h2>


<a id="schemachangepasswordvm"></a>


```json
{
  "password": "string"
}
```


### Properties


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|
|password|string|true|New password|input|


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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|address|string|true|No description|output|
|altAutosellInternal|boolean|false|No description|output|
|associateType|string|true|No description|output|
|autosell|boolean|false|No description|output|
|beneficiaryPercent|integer(int64)|false|No description|output|
|canEditOnboarded|boolean|false|No description|output|
|city|string|true|No description|output|
|coinaPultApiKey|string|false|No description|output|
|commissionFee|number|false|No description|output|
|companyEIN|string|false|No description|output|
|companyWebsite|string|true|No description|output|
|createdDate|string(date-time)|false|No description|output|
|cryptoCapitalApiKey|string|false|No description|output|
|customers|integer(int32)|false|Number of associated customers|output|
|deletedDate|string(date-time)|false|No description|output|
|emailAddress|string|true|No description|output|
|enabled|boolean|false|No description|output|
|enrolledBy|[Associate](#schemaassociate)|false|No description|output|
|id|integer(int64)|false|No description|output|
|incorporationDate|string(date)|false|No description|output|
|internalFee|number(double)|false|No description|output|
|legalBusinessName|string|true|No description|output|
|locationsCount|integer(int32)|false|No description|output|
|merchants|integer(int32)|false|Number of associated merchants|output|
|note|string|false|No description|output|
|partners|integer(int32)|false|Number of associated partners|output|
|phone|string|true|No description|output|
|posCount|integer(int32)|false|Number of POS|output|
|state|[CountryState](#schemacountrystate)|true|No description|output|
|usBankAccount|string|false|No description|output|
|vendors|integer(int32)|false|Number of associated vendors|output|
|zip|string|true|Zip code|output|


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


|Name|Type|Required|Description|input/output parameter|
|---|---|---|---|---|
|apiKey|string|true|No description|both|
|apiSecret|string|true|No description|input|
|registeredEmail|string|true|No description|both|

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

|Parameter|Type|Required|Description|input/output parameter|
|---|---|---|---|---|---|
|associate_id|integer|false| Associate identifier (used with associate sales volume)|output|
|location_id|integer|false|Location idenfifier (used with location sales volume)|output|
|pos_id|integer|false|POS identifier (used with pos sales volume)|output|
|sales_crypto|number|true|Total sales in cryptocurrency|output|
|sales_fiat|string|true|Total sales in FIAT currency (USD)|output|
