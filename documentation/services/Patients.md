# Patients

A list of all methods in the `Patients` service. Click on the method name to view detailed information about that method.

| Methods | Description |
| :------ | :---------- |
|[Services_GetPatients](#services_getpatients)|  |
|[Services_Create](#services_create)|  |
|[Services_Get](#services_get)|  |
|[Services_Update](#services_update)|  |
|[Services_CreateAddressForTenant](#services_createaddressfortenant)|  |
|[Services_UpdateAddressForTenant](#services_updateaddressfortenant)|  |
|[Services_ArchiveAddressForTenant](#services_archiveaddressfortenant)|  |

## Services_GetPatients


- HTTP Method: `GET`
- Endpoint: `/v1/patients`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $externalId | string | ❌ |  |
| $subTenantId | string | ❌ |  |
| $id | string | ❌ |  |
| $paginationSize | int | ❌ |  |
| $paginationPage | int | ❌ |  |
| $query | string | ❌ |  |

**Return Type**

`Models\GetPatientsResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->patients->servicesGetPatients(
  externalId: "externalId",
  subTenantId: "subTenantId",
  id: "id",
  paginationSize: 4,
  paginationPage: 2,
  query: "query"
);

print_r($response);
```

## Services_Create


- HTTP Method: `POST`
- Endpoint: `/v1/patients`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| input | Models\CreatePatientRequest | ✅ |  |

**Return Type**

`Models\CreatePatientResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;
use WellSyncServicesCareConnect\Models\Patient;
use WellSyncServicesCareConnect\Models\CreatePatientRequest;

$sdk = new Client(accessToken: 'YOUR_TOKEN');


$input = new Models\CreatePatientRequest(
  patient: $patient
);

$response = $sdk->patients->servicesCreate(
  input: $input
);

print_r($response);
```

## Services_Get


- HTTP Method: `GET`
- Endpoint: `/v1/patients/{patientId}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $patientId | string | ✅ |  |

**Return Type**

`Models\GetResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->patients->servicesGet(
  patientId: "patientId"
);

print_r($response);
```

## Services_Update


- HTTP Method: `PUT`
- Endpoint: `/v1/patients/{patientId}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| input | Models\ServicesUpdateRequest | ✅ |  |
| $patientId | string | ✅ |  |

**Return Type**

`Models\UpdatePatientForTenantResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;
use WellSyncServicesCareConnect\Models\Patient;
use WellSyncServicesCareConnect\Models\ServicesUpdateRequest;

$sdk = new Client(accessToken: 'YOUR_TOKEN');


$input = new Models\ServicesUpdateRequest(
  patient: $patient
);

$response = $sdk->patients->servicesUpdate(
  input: $input,
  patientId: "patientId"
);

print_r($response);
```

## Services_CreateAddressForTenant


- HTTP Method: `POST`
- Endpoint: `/v1/patients/{patientId}/addresses`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| input | Models\ServicesCreateAddressForTenantRequest | ✅ |  |
| $patientId | string | ✅ |  |

**Return Type**

`Models\CreateAddressForTenantResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;
use WellSyncServicesCareConnect\Models\Address;
use WellSyncServicesCareConnect\Models\ServicesCreateAddressForTenantRequest;

$sdk = new Client(accessToken: 'YOUR_TOKEN');


$input = new Models\ServicesCreateAddressForTenantRequest(
  address: $address
);

$response = $sdk->patients->servicesCreateAddressForTenant(
  input: $input,
  patientId: "patientId"
);

print_r($response);
```

## Services_UpdateAddressForTenant


- HTTP Method: `PATCH`
- Endpoint: `/v1/patients/{patientId}/addresses/{addressId}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| input | Models\ServicesUpdateAddressForTenantRequest | ✅ |  |
| $patientId | string | ✅ |  |
| $addressId | string | ✅ |  |

**Return Type**

`array`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;
use WellSyncServicesCareConnect\Models\Address;
use WellSyncServicesCareConnect\Models\ServicesUpdateAddressForTenantRequest;

$sdk = new Client(accessToken: 'YOUR_TOKEN');


$input = new Models\ServicesUpdateAddressForTenantRequest(
  address: $address
);

$response = $sdk->patients->servicesUpdateAddressForTenant(
  input: $input,
  patientId: "patientId",
  addressId: "addressId"
);

print_r($response);
```

## Services_ArchiveAddressForTenant


- HTTP Method: `DELETE`
- Endpoint: `/v1/patients/{patientId}/addresses/{addressId}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $patientId | string | ✅ |  |
| $addressId | string | ✅ |  |

**Return Type**

`array`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->patients->servicesArchiveAddressForTenant(
  patientId: "patientId",
  addressId: "addressId"
);

print_r($response);
```




<!-- This file was generated by liblab | https://liblab.com/ -->