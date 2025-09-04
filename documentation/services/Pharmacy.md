# Pharmacy

A list of all methods in the `Pharmacy` service. Click on the method name to view detailed information about that method.

| Methods | Description |
| :------ | :---------- |
|[Pharmacy_ReEnqueuePrescription](#pharmacy_reenqueueprescription)|  |
|[Pharmacy_GetCurrentAgentClinicians](#pharmacy_getcurrentagentclinicians)|  |
|[Pharmacy_GetAgents](#pharmacy_getagents)|  |
|[Pharmacy_GetAgentClinicians](#pharmacy_getagentclinicians)|  |
|[Pharmacy_LinkClinicToAgent](#pharmacy_linkclinictoagent)| links an agent to a clinic by agent_id and clinic_id agents have to be linked in order to be able to prescribe prescriptions |
|[Pharmacy_UnlinkClinicFromAgent](#pharmacy_unlinkclinicfromagent)| unlinks an agent from a clinic by agent_id and clinic_id |
|[Pharmacy_GetClinic](#pharmacy_getclinic)|  |
|[Pharmacy_GetCurrentClinician](#pharmacy_getcurrentclinician)| Returns the currently logged in clinician. This endpoint only works for  sessions authenticated using a careconnect.id account. |
|[Pharmacy_GetClinicians](#pharmacy_getclinicians)|  |
|[Pharmacy_CreateClinician](#pharmacy_createclinician)|  |
|[Pharmacy_GetClinician](#pharmacy_getclinician)|  |
|[Pharmacy_UpdateClinician](#pharmacy_updateclinician)|  |
|[Pharmacy_DeleteClinician](#pharmacy_deleteclinician)|  |
|[Pharmacy_LinkAgentToClinician](#pharmacy_linkagenttoclinician)|  |
|[Pharmacy_UnlinkAgentFromClinician](#pharmacy_unlinkagentfromclinician)|  |
|[Pharmacy_LinkClinicClinician](#pharmacy_linkclinicclinician)| links a clinician to a clinic by clinician_id and clinic_id clinicians have to be linked in order to be able to prescribe prescriptions |
|[Pharmacy_UnlinkClinicClinician](#pharmacy_unlinkclinicclinician)| unlinks a clinician from a clinic by clinician_id and clinic_id |
|[Pharmacy_GetClinicianIdentityRecoveryLink](#pharmacy_getclinicianidentityrecoverylink)| TODO: Deprecate this endpoint in favor of GetUserIdentityRecoveryLink |
|[Pharmacy_GetClinics](#pharmacy_getclinics)|  |
|[Pharmacy_CreateClinic](#pharmacy_createclinic)|  |
|[Pharmacy_UpdateClinic](#pharmacy_updateclinic)|  |
|[Pharmacy_DeleteClinic](#pharmacy_deleteclinic)|  |
|[Pharmacy_GetClinicClinicians](#pharmacy_getclinicclinicians)|  |
|[Pharmacy_GetAllowedOrderShippingMethods](#pharmacy_getallowedordershippingmethods)|  |
|[Pharmacy_PreviewOrderSummary](#pharmacy_previewordersummary)|  |
|[Pharmacy_SubmitExternalOrder](#pharmacy_submitexternalorder)| SubmitExternalOrder submits an order for a patient using the given data. All objects are identified by their external_id. |
|[Pharmacy_SubmitClinicianOrder](#pharmacy_submitclinicianorder)|  |
|[Pharmacy_GetOrder](#pharmacy_getorder)|  |
|[Pharmacy_GetPharmacyByDrug](#pharmacy_getpharmacybydrug)|  |
|[Pharmacy_GetPatientPrescriptions](#pharmacy_getpatientprescriptions)|  |
|[Pharmacy_SubmitPrescription](#pharmacy_submitprescription)|  |
|[Pharmacy_GetPrescriptionItems](#pharmacy_getprescriptionitems)|  |
|[Pharmacy_GetPrescriptionItem](#pharmacy_getprescriptionitem)|  |
|[Pharmacy_GetPrescriptions](#pharmacy_getprescriptions)|  |
|[Pharmacy_GetAllDosageForms](#pharmacy_getalldosageforms)|  |
|[Pharmacy_GetAllDrugsAndDosages](#pharmacy_getalldrugsanddosages)|  |
|[Pharmacy_GetDrugs](#pharmacy_getdrugs)|  |
|[Pharmacy_GetPharmacies](#pharmacy_getpharmacies)|  |
|[Pharmacy_GetPharmacyByID](#pharmacy_getpharmacybyid)|  |
|[Pharmacy_GetCurrentUser](#pharmacy_getcurrentuser)| Returns the currently logged in user. This endpoint only works for  sessions authenticated using a careconnect.id account. |
|[Pharmacy_SetUserPrivateKey](#pharmacy_setuserprivatekey)| SetUserPrivateKey sets the private key for current user |
|[Pharmacy_GetUsers](#pharmacy_getusers)|  |
|[Pharmacy_AddUser](#pharmacy_adduser)| Add a user adds a user with mentioned roles  this can not be used to create clinicians but  once a user is created they converted to clinician |
|[Pharmacy_GetUser](#pharmacy_getuser)|  |
|[Pharmacy_UpdateUser](#pharmacy_updateuser)|  |
|[Pharmacy_GetUserClinics](#pharmacy_getuserclinics)|  |
|[Pharmacy_AddClinicMembership](#pharmacy_addclinicmembership)| AddClinicMembership adds a user to a clinic with the specified role. |
|[Pharmacy_RemoveClinicMembership](#pharmacy_removeclinicmembership)| RemoveClinicMembership removes a user from a clinic with the specified role. |
|[Pharmacy_GetUserIdentityRecoveryLink](#pharmacy_getuseridentityrecoverylink)|  |
|[Pharmacy_GetPublicKeys](#pharmacy_getpublickeys)| AddPublicKey adds a public key to a clinician |
|[Pharmacy_AddPublicKey](#pharmacy_addpublickey)| AddPublicKey adds a public key to a clinician |
|[Pharmacy_AddUserRoles](#pharmacy_adduserroles)|  |
|[Pharmacy_RemoveUserRole](#pharmacy_removeuserrole)|  |

## Pharmacy_ReEnqueuePrescription


- HTTP Method: `POST`
- Endpoint: `/v1/admin/re-enqueue-prescription`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $prescriptionId | string | ❌ |  |

**Return Type**

`array`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyReEnqueuePrescription(
  prescriptionId: "prescriptionId"
);

print_r($response);
```

## Pharmacy_GetCurrentAgentClinicians


- HTTP Method: `GET`
- Endpoint: `/v1/agent/clinicians`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $clinicId | string | ❌ |  |

**Return Type**

`Models\GetCurrentAgentCliniciansResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetCurrentAgentClinicians(
  clinicId: "clinicId"
);

print_r($response);
```

## Pharmacy_GetAgents


- HTTP Method: `GET`
- Endpoint: `/v1/agents`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $paginationSize | int | ❌ |  |
| $paginationPage | int | ❌ |  |
| $agentName | string | ❌ |  |
| $assignableTo | string | ❌ |  |

**Return Type**

`Models\GetAgentsResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetAgents(
  paginationSize: 8,
  paginationPage: 2,
  agentName: "agentName",
  assignableTo: "assignableTo"
);

print_r($response);
```

## Pharmacy_GetAgentClinicians


- HTTP Method: `GET`
- Endpoint: `/v1/agents/{agentId}/clinicians`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $agentId | string | ✅ |  |

**Return Type**

`Models\GetAgentCliniciansResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetAgentClinicians(
  agentId: "agentId"
);

print_r($response);
```

## Pharmacy_LinkClinicToAgent

links an agent to a clinic by agent_id and clinic_id agents have to be linked in order to be able to prescribe prescriptions


- HTTP Method: `PUT`
- Endpoint: `/v1/agents/{agentId}/clinics/{clinicId}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $agentId | string | ✅ | agent uuid |
| $clinicId | string | ✅ | clinic uuid |

**Return Type**

`mixed`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyLinkClinicToAgent(
  agentId: "agentId",
  clinicId: "clinicId"
);

print_r($response);
```

## Pharmacy_UnlinkClinicFromAgent

unlinks an agent from a clinic by agent_id and clinic_id


- HTTP Method: `DELETE`
- Endpoint: `/v1/agents/{agentId}/clinics/{clinicId}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $agentId | string | ✅ | agent uuid |
| $clinicId | string | ✅ | clinic uuid |

**Return Type**

`mixed`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyUnlinkClinicFromAgent(
  agentId: "agentId",
  clinicId: "clinicId"
);

print_r($response);
```

## Pharmacy_GetClinic


- HTTP Method: `GET`
- Endpoint: `/v1/clinic/{clinicId}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $clinicId | string | ✅ |  |

**Return Type**

`Models\GetClinicResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetClinic(
  clinicId: "clinicId"
);

print_r($response);
```

## Pharmacy_GetCurrentClinician

Returns the currently logged in clinician. This endpoint only works for  sessions authenticated using a careconnect.id account.


- HTTP Method: `GET`
- Endpoint: `/v1/clinician`


**Return Type**

`Models\GetCurrentClinicianResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetCurrentClinician();

print_r($response);
```

## Pharmacy_GetClinicians


- HTTP Method: `GET`
- Endpoint: `/v1/clinicians`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $query | string | ❌ |  |
| $externalId | string | ❌ | external_id is used to search for clinicians by their external id |
| $filterIsNpiSet | bool | ❌ |  |
| $filterIsPrivateKeySet | bool | ❌ |  |

**Return Type**

`Models\GetCliniciansResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetClinicians(
  query: "query",
  externalId: "externalId",
  filterIsNpiSet: true,
  filterIsPrivateKeySet: true
);

print_r($response);
```

## Pharmacy_CreateClinician


- HTTP Method: `POST`
- Endpoint: `/v1/clinicians`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| input | Models\CreateClinicianRequest | ✅ |  |

**Return Type**

`Models\CreateClinicianResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;
use WellSyncServicesCareConnect\Models\Clinician;
use WellSyncServicesCareConnect\Models\CreateClinicianRequest;

$sdk = new Client(accessToken: 'YOUR_TOKEN');


$input = new Models\CreateClinicianRequest(
  clinician: $clinician,
  clinicIds: [],
  createIdentity: true
);

$response = $sdk->pharmacy->pharmacyCreateClinician(
  input: $input
);

print_r($response);
```

## Pharmacy_GetClinician


- HTTP Method: `GET`
- Endpoint: `/v1/clinicians/{clinicianId}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $clinicianId | string | ✅ |  |

**Return Type**

`Models\GetClinicianResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetClinician(
  clinicianId: "clinicianId"
);

print_r($response);
```

## Pharmacy_UpdateClinician


- HTTP Method: `PUT`
- Endpoint: `/v1/clinicians/{clinicianId}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| input | Models\PharmacyUpdateClinicianRequest | ✅ |  |
| $clinicianId | string | ✅ |  |

**Return Type**

`Models\UpdateClinicianResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;
use WellSyncServicesCareConnect\Models\PharmacyUpdateClinicianRequest;

$sdk = new Client(accessToken: 'YOUR_TOKEN');


$input = new Models\PharmacyUpdateClinicianRequest(
  firstName: "firstName",
  lastName: "lastName",
  npi: "npi",
  dea: "dea"
);

$response = $sdk->pharmacy->pharmacyUpdateClinician(
  input: $input,
  clinicianId: "clinicianId"
);

print_r($response);
```

## Pharmacy_DeleteClinician


- HTTP Method: `DELETE`
- Endpoint: `/v1/clinicians/{clinicianId}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $clinicianId | string | ✅ | clinician uuid |

**Return Type**

`mixed`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyDeleteClinician(
  clinicianId: "clinicianId"
);

print_r($response);
```

## Pharmacy_LinkAgentToClinician


- HTTP Method: `POST`
- Endpoint: `/v1/clinicians/{clinicianId}/agent`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| input | Models\PharmacyLinkAgentToClinicianRequest | ✅ |  |
| $clinicianId | string | ✅ |  |

**Return Type**

`array`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;
use WellSyncServicesCareConnect\Models\PharmacyLinkAgentToClinicianRequest;

$sdk = new Client(accessToken: 'YOUR_TOKEN');


$input = new Models\PharmacyLinkAgentToClinicianRequest(
  agentId: "agentId"
);

$response = $sdk->pharmacy->pharmacyLinkAgentToClinician(
  input: $input,
  clinicianId: "clinicianId"
);

print_r($response);
```

## Pharmacy_UnlinkAgentFromClinician


- HTTP Method: `DELETE`
- Endpoint: `/v1/clinicians/{clinicianId}/agent/{agentId}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $clinicianId | string | ✅ |  |
| $agentId | string | ✅ |  |

**Return Type**

`array`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyUnlinkAgentFromClinician(
  clinicianId: "clinicianId",
  agentId: "agentId"
);

print_r($response);
```

## Pharmacy_LinkClinicClinician

links a clinician to a clinic by clinician_id and clinic_id clinicians have to be linked in order to be able to prescribe prescriptions


- HTTP Method: `PUT`
- Endpoint: `/v1/clinicians/{clinicianId}/clinic/{clinicId}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $clinicianId | string | ✅ | clinician uuid |
| $clinicId | string | ✅ | clinic uuid |

**Return Type**

`mixed`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyLinkClinicClinician(
  clinicianId: "clinicianId",
  clinicId: "clinicId"
);

print_r($response);
```

## Pharmacy_UnlinkClinicClinician

unlinks a clinician from a clinic by clinician_id and clinic_id


- HTTP Method: `DELETE`
- Endpoint: `/v1/clinicians/{clinicianId}/clinic/{clinicId}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $clinicianId | string | ✅ | clinician uuid |
| $clinicId | string | ✅ | clinic uuid |

**Return Type**

`mixed`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyUnlinkClinicClinician(
  clinicianId: "clinicianId",
  clinicId: "clinicId"
);

print_r($response);
```

## Pharmacy_GetClinicianIdentityRecoveryLink

TODO: Deprecate this endpoint in favor of GetUserIdentityRecoveryLink


- HTTP Method: `GET`
- Endpoint: `/v1/clinicians/{clinicianId}/identity/recovery`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $clinicianId | string | ✅ |  |

**Return Type**

`Models\GetClinicianIdentityRecoveryLinkResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetClinicianIdentityRecoveryLink(
  clinicianId: "clinicianId"
);

print_r($response);
```

## Pharmacy_GetClinics


- HTTP Method: `GET`
- Endpoint: `/v1/clinics`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $query | string | ❌ |  |
| $externalId | string | ❌ |  |

**Return Type**

`Models\GetClinicsResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetClinics(
  query: "query",
  externalId: "externalId"
);

print_r($response);
```

## Pharmacy_CreateClinic


- HTTP Method: `POST`
- Endpoint: `/v1/clinics`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| input | Models\CreateClinicRequest | ✅ |  |

**Return Type**

`Models\CreateClinicResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;
use WellSyncServicesCareConnect\Models\Clinic;
use WellSyncServicesCareConnect\Models\CreateClinicRequest;

$sdk = new Client(accessToken: 'YOUR_TOKEN');


$input = new Models\CreateClinicRequest(
  clinic: $clinic
);

$response = $sdk->pharmacy->pharmacyCreateClinic(
  input: $input
);

print_r($response);
```

## Pharmacy_UpdateClinic


- HTTP Method: `PUT`
- Endpoint: `/v1/clinics/{clinicId}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| input | Models\PharmacyUpdateClinicRequest | ✅ |  |
| $clinicId | string | ✅ |  |

**Return Type**

`Models\UpdateClinicResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;
use WellSyncServicesCareConnect\Models\PharmacyUpdateClinicRequest;

$sdk = new Client(accessToken: 'YOUR_TOKEN');


$input = new Models\PharmacyUpdateClinicRequest(
  addressLineOne: "123 Main St",
  addressLineTwo: "Apt 1",
  city: "Tampa",
  zip: "12345",
  administrativeArea: "FL",
  country: "US",
  phone: "1234567890",
  name: "Tampa General Hospital",
  salesRep: "Jane Doe"
);

$response = $sdk->pharmacy->pharmacyUpdateClinic(
  input: $input,
  clinicId: "clinicId"
);

print_r($response);
```

## Pharmacy_DeleteClinic


- HTTP Method: `DELETE`
- Endpoint: `/v1/clinics/{clinicId}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $clinicId | string | ✅ | clinic uuid |

**Return Type**

`mixed`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyDeleteClinic(
  clinicId: "clinicId"
);

print_r($response);
```

## Pharmacy_GetClinicClinicians


- HTTP Method: `GET`
- Endpoint: `/v1/clinics/{clinicId}/clinicians`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $clinicId | string | ✅ |  |
| $query | string | ❌ |  |

**Return Type**

`Models\GetClinicCliniciansResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetClinicClinicians(
  query: "query",
  clinicId: "clinicId"
);

print_r($response);
```

## Pharmacy_GetAllowedOrderShippingMethods


- HTTP Method: `GET`
- Endpoint: `/v1/clinics/{clinicId}/order/shipping-methods`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $clinicId | string | ✅ |  |
| $pharmacyIds | array | ❌ |  |

**Return Type**

`Models\GetAllowedOrderShippingMethodsResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetAllowedOrderShippingMethods(
  pharmacyIds: [],
  clinicId: "clinicId"
);

print_r($response);
```

## Pharmacy_PreviewOrderSummary


- HTTP Method: `POST`
- Endpoint: `/v1/clinics/{clinicId}/order/summary/preview`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| input | Models\PharmacyPreviewOrderSummaryRequest | ✅ |  |
| $clinicId | string | ✅ |  |

**Return Type**

`Models\PreviewOrderSummaryResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;
use WellSyncServicesCareConnect\Models\LineItem;
use WellSyncServicesCareConnect\Models\PharmacyPreviewOrderSummaryRequest;

$sdk = new Client(accessToken: 'YOUR_TOKEN');


$input = new Models\PharmacyPreviewOrderSummaryRequest(
  state: "state",
  lineItems: [],
  shippingMethod: $pharmacyPreviewOrderSummaryRequestShippingMethod
);

$response = $sdk->pharmacy->pharmacyPreviewOrderSummary(
  input: $input,
  clinicId: "clinicId"
);

print_r($response);
```

## Pharmacy_SubmitExternalOrder

SubmitExternalOrder submits an order for a patient using the given data. All objects are identified by their external_id.


- HTTP Method: `POST`
- Endpoint: `/v1/clinics/{clinicId}/orders`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| input | Models\PharmacySubmitExternalOrderRequest | ✅ | SubmitExternalOrder submits an order for a patient using the given data. All objects are identified by their external_id. |
| $clinicId | string | ✅ |  |

**Return Type**

`Models\SubmitExternalOrderResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;
use WellSyncServicesCareConnect\Models\Patient;
use WellSyncServicesCareConnect\Models\Clinician;
use WellSyncServicesCareConnect\Models\Address;
use WellSyncServicesCareConnect\Models\PrescriptionItem;
use WellSyncServicesCareConnect\Models\PharmacySubmitExternalOrderRequest;

$sdk = new Client(accessToken: 'YOUR_TOKEN');


$input = new Models\PharmacySubmitExternalOrderRequest(
  externalCaseId: "ext-12345",
  symmetricalSigningKey: "symmetricalSigningKey",
  patient: $patient,
  clinician: $clinician,
  shippingMethod: $pharmacySubmitExternalOrderRequestShippingMethod,
  shippingAddress: $address,
  prescriptionItems: []
);

$response = $sdk->pharmacy->pharmacySubmitExternalOrder(
  input: $input,
  clinicId: "clinicId"
);

print_r($response);
```

## Pharmacy_SubmitClinicianOrder


- HTTP Method: `POST`
- Endpoint: `/v1/clinics/{clinicId}/patients/{patientId}/orders`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| input | Models\PharmacySubmitClinicianOrderRequest | ✅ |  |
| $clinicId | string | ✅ |  |
| $patientId | string | ✅ |  |

**Return Type**

`Models\SubmitClinicianOrderResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;
use WellSyncServicesCareConnect\Models\Address;
use WellSyncServicesCareConnect\Models\PrescriptionItem;
use WellSyncServicesCareConnect\Models\PharmacySubmitClinicianOrderRequest;

$sdk = new Client(accessToken: 'YOUR_TOKEN');


$input = new Models\PharmacySubmitClinicianOrderRequest(
  id: "id",
  externalCaseId: "externalCaseId",
  clinicianId: "clinicianId",
  agentId: "agentId",
  shippingMethod: $pharmacySubmitClinicianOrderRequestShippingMethod,
  shippingAddress: $address,
  prescriptionItems: [],
  signedMessage: "signedMessage"
);

$response = $sdk->pharmacy->pharmacySubmitClinicianOrder(
  input: $input,
  clinicId: "clinicId",
  patientId: "patientId"
);

print_r($response);
```

## Pharmacy_GetOrder


- HTTP Method: `GET`
- Endpoint: `/v1/clinics/{clinicId}/patients/{patientId}/orders/{orderId}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $clinicId | string | ✅ |  |
| $patientId | string | ✅ |  |
| $orderId | string | ✅ |  |

**Return Type**

`Models\GetOrderResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetOrder(
  clinicId: "clinicId",
  patientId: "patientId",
  orderId: "orderId"
);

print_r($response);
```

## Pharmacy_GetPharmacyByDrug


- HTTP Method: `GET`
- Endpoint: `/v1/clinics/{clinicId}/patients/{patientId}/pharmacy`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $clinicId | string | ✅ |  |
| $patientId | string | ✅ |  |
| $drugId | string | ❌ |  |
| $dosageId | string | ❌ |  |

**Return Type**

`Models\GetPharmacyByDrugResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetPharmacyByDrug(
  drugId: "drugId",
  dosageId: "dosageId",
  clinicId: "clinicId",
  patientId: "patientId"
);

print_r($response);
```

## Pharmacy_GetPatientPrescriptions


- HTTP Method: `GET`
- Endpoint: `/v1/clinics/{clinicId}/patients/{patientId}/prescriptions`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $clinicId | string | ✅ |  |
| $patientId | string | ✅ |  |
| $externalCaseId | string | ❌ |  |
| $withDetails | bool | ❌ | with_details will return the full prescription details  including patient and drug details |
| $paginationSize | int | ❌ |  |
| $paginationPage | int | ❌ |  |
| $orderId | string | ❌ |  |

**Return Type**

`Models\GetPatientPrescriptionsResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetPatientPrescriptions(
  externalCaseId: "externalCaseId",
  withDetails: true,
  paginationSize: 3,
  paginationPage: 9,
  orderId: "orderId",
  clinicId: "clinicId",
  patientId: "patientId"
);

print_r($response);
```

## Pharmacy_SubmitPrescription


- HTTP Method: `POST`
- Endpoint: `/v1/clinics/{clinicId}/patients/{patientId}/prescriptions`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| input | Models\PharmacySubmitPrescriptionRequest | ✅ |  |
| $clinicId | string | ✅ |  |
| $patientId | string | ✅ |  |

**Return Type**

`Models\SubmitPrescriptionResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;
use WellSyncServicesCareConnect\Models\Prescription;
use WellSyncServicesCareConnect\Models\PharmacySubmitPrescriptionRequest;

$sdk = new Client(accessToken: 'YOUR_TOKEN');


$input = new Models\PharmacySubmitPrescriptionRequest(
  externalCaseId: "externalCaseId",
  prescription: $prescription
);

$response = $sdk->pharmacy->pharmacySubmitPrescription(
  input: $input,
  clinicId: "clinicId",
  patientId: "patientId"
);

print_r($response);
```

## Pharmacy_GetPrescriptionItems


- HTTP Method: `GET`
- Endpoint: `/v1/clinics/{clinicId}/prescription-items`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $clinicId | string | ✅ |  |
| $patientId | string | ❌ |  |
| $externalCaseId | string | ❌ |  |
| $paginationSize | int | ❌ |  |
| $paginationPage | int | ❌ |  |
| $orderId | string | ❌ |  |
| $withDetails | bool | ❌ |  |

**Return Type**

`Models\GetPrescriptionItemsResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetPrescriptionItems(
  patientId: "patientId",
  externalCaseId: "externalCaseId",
  paginationSize: 7,
  paginationPage: 123,
  orderId: "orderId",
  withDetails: true,
  clinicId: "clinicId"
);

print_r($response);
```

## Pharmacy_GetPrescriptionItem


- HTTP Method: `GET`
- Endpoint: `/v1/clinics/{clinicId}/prescription-items/{prescriptionItemId}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $clinicId | string | ✅ |  |
| $prescriptionItemId | string | ✅ |  |

**Return Type**

`Models\GetPrescriptionItemResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetPrescriptionItem(
  clinicId: "clinicId",
  prescriptionItemId: "prescriptionItemId"
);

print_r($response);
```

## Pharmacy_GetPrescriptions


- HTTP Method: `GET`
- Endpoint: `/v1/clinics/{clinicId}/prescriptions`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $clinicId | string | ✅ |  |
| $externalPatientId | string | ❌ |  |
| $externalCaseId | string | ❌ |  |
| $withDetails | bool | ❌ | with_details will return the full prescription details  including patient and drug details |
| $paginationSize | int | ❌ |  |
| $paginationPage | int | ❌ |  |
| $orderId | string | ❌ |  |

**Return Type**

`Models\GetPrescriptionsResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetPrescriptions(
  externalPatientId: "externalPatientId",
  externalCaseId: "externalCaseId",
  withDetails: true,
  paginationSize: 5,
  paginationPage: 2,
  orderId: "orderId",
  clinicId: "clinicId"
);

print_r($response);
```

## Pharmacy_GetAllDosageForms


- HTTP Method: `GET`
- Endpoint: `/v1/dosage-forms`


**Return Type**

`Models\GetAllDosageFormsResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetAllDosageForms();

print_r($response);
```

## Pharmacy_GetAllDrugsAndDosages


- HTTP Method: `GET`
- Endpoint: `/v1/drugs`


**Return Type**

`Models\GetAllDrugsAndDosagesResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetAllDrugsAndDosages();

print_r($response);
```

## Pharmacy_GetDrugs


- HTTP Method: `GET`
- Endpoint: `/v1/patients/{patientId}/drugs`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $patientId | string | ✅ |  |

**Return Type**

`Models\GetDrugsResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetDrugs(
  patientId: "patientId"
);

print_r($response);
```

## Pharmacy_GetPharmacies


- HTTP Method: `GET`
- Endpoint: `/v1/pharmacies`


**Return Type**

`Models\GetPharmaciesResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetPharmacies();

print_r($response);
```

## Pharmacy_GetPharmacyByID


- HTTP Method: `GET`
- Endpoint: `/v1/pharmacies/{pharmacyId}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $pharmacyId | string | ✅ |  |

**Return Type**

`Models\GetPharmacyByIdResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetPharmacyById(
  pharmacyId: "pharmacyId"
);

print_r($response);
```

## Pharmacy_GetCurrentUser

Returns the currently logged in user. This endpoint only works for  sessions authenticated using a careconnect.id account.


- HTTP Method: `GET`
- Endpoint: `/v1/user`


**Return Type**

`Models\GetCurrentUserResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetCurrentUser();

print_r($response);
```

## Pharmacy_SetUserPrivateKey

SetUserPrivateKey sets the private key for current user


- HTTP Method: `POST`
- Endpoint: `/v1/user/private-key`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| input | Models\SetUserPrivateKeyRequest | ✅ | SetUserPrivateKey sets the private key for current user |

**Return Type**

`array`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;
use WellSyncServicesCareConnect\Models\SetUserPrivateKeyRequest;

$sdk = new Client(accessToken: 'YOUR_TOKEN');


$input = new Models\SetUserPrivateKeyRequest(
  encryptedPrivateKey: "encryptedPrivateKey",
  encryptedWrapperKey: "encryptedWrapperKey",
  encryptedRecoveryKeys: [],
  publicKey: "publicKey"
);

$response = $sdk->pharmacy->pharmacySetUserPrivateKey(
  input: $input
);

print_r($response);
```

## Pharmacy_GetUsers


- HTTP Method: `GET`
- Endpoint: `/v1/users`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $query | string | ❌ |  |
| $paginationSize | int | ❌ |  |
| $paginationPage | int | ❌ |  |

**Return Type**

`Models\GetUsersResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetUsers(
  query: "query",
  paginationSize: 6,
  paginationPage: 2
);

print_r($response);
```

## Pharmacy_AddUser

Add a user adds a user with mentioned roles  this can not be used to create clinicians but  once a user is created they converted to clinician


- HTTP Method: `POST`
- Endpoint: `/v1/users`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| input | Models\AddUserRequest | ✅ | Add a user adds a user with mentioned roles  this can not be used to create clinicians but  once a user is created they converted to clinician |

**Return Type**

`Models\AddUserResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;
use WellSyncServicesCareConnect\Models\ClinicMembership;
use WellSyncServicesCareConnect\Models\AddUserRequest;

$sdk = new Client(accessToken: 'YOUR_TOKEN');


$input = new Models\AddUserRequest(
  firstName: "firstName",
  lastName: "lastName",
  email: "email",
  phone: "phone",
  roles: [],
  clinicMemberships: []
);

$response = $sdk->pharmacy->pharmacyAddUser(
  input: $input
);

print_r($response);
```

## Pharmacy_GetUser


- HTTP Method: `GET`
- Endpoint: `/v1/users/{userId}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $userId | string | ✅ |  |

**Return Type**

`Models\GetUserResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetUser(
  userId: "userId"
);

print_r($response);
```

## Pharmacy_UpdateUser


- HTTP Method: `PUT`
- Endpoint: `/v1/users/{userId}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| input | Models\PharmacyUpdateUserRequest | ✅ |  |
| $userId | string | ✅ |  |

**Return Type**

`Models\UpdateUserResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;
use WellSyncServicesCareConnect\Models\PharmacyUpdateUserRequest;

$sdk = new Client(accessToken: 'YOUR_TOKEN');


$input = new Models\PharmacyUpdateUserRequest(
  firstName: "firstName",
  lastName: "lastName"
);

$response = $sdk->pharmacy->pharmacyUpdateUser(
  input: $input,
  userId: "userId"
);

print_r($response);
```

## Pharmacy_GetUserClinics


- HTTP Method: `GET`
- Endpoint: `/v1/users/{userId}/clinics`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $userId | string | ✅ |  |
| $query | string | ❌ |  |

**Return Type**

`Models\GetUserClinicsResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetUserClinics(
  query: "query",
  userId: "userId"
);

print_r($response);
```

## Pharmacy_AddClinicMembership

AddClinicMembership adds a user to a clinic with the specified role.


- HTTP Method: `PUT`
- Endpoint: `/v1/users/{userId}/clinics/{clinicId}/role/{role}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| input | array | ✅ | AddClinicMembership adds a user to a clinic with the specified role. |
| $userId | string | ✅ |  |
| $clinicId | string | ✅ |  |
| $role | string | ✅ |  |

**Return Type**

`array`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyAddClinicMembership(
  input: $input,
  userId: "userId",
  clinicId: "clinicId",
  role: "role"
);

print_r($response);
```

## Pharmacy_RemoveClinicMembership

RemoveClinicMembership removes a user from a clinic with the specified role.


- HTTP Method: `DELETE`
- Endpoint: `/v1/users/{userId}/clinics/{clinicId}/role/{role}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $userId | string | ✅ |  |
| $clinicId | string | ✅ |  |
| $role | string | ✅ |  |

**Return Type**

`array`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyRemoveClinicMembership(
  userId: "userId",
  clinicId: "clinicId",
  role: "role"
);

print_r($response);
```

## Pharmacy_GetUserIdentityRecoveryLink


- HTTP Method: `GET`
- Endpoint: `/v1/users/{userId}/identity/recovery`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $userId | string | ✅ |  |

**Return Type**

`Models\GetUserIdentityRecoveryLinkResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetUserIdentityRecoveryLink(
  userId: "userId"
);

print_r($response);
```

## Pharmacy_GetPublicKeys

AddPublicKey adds a public key to a clinician


- HTTP Method: `GET`
- Endpoint: `/v1/users/{userId}/public-keys`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $userId | string | ✅ |  |
| $activeOnly | bool | ❌ |  |

**Return Type**

`Models\GetPublicKeysResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyGetPublicKeys(
  activeOnly: true,
  userId: "userId"
);

print_r($response);
```

## Pharmacy_AddPublicKey

AddPublicKey adds a public key to a clinician


- HTTP Method: `POST`
- Endpoint: `/v1/users/{userId}/public-keys`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| input | Models\PharmacyAddPublicKeyRequest | ✅ | AddPublicKey adds a public key to a clinician |
| $userId | string | ✅ |  |

**Return Type**

`Models\AddPublicKeyResponse`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;
use WellSyncServicesCareConnect\Models\PharmacyAddPublicKeyRequest;

$sdk = new Client(accessToken: 'YOUR_TOKEN');


$input = new Models\PharmacyAddPublicKeyRequest(
  pem: "pem",
  alias: "alias"
);

$response = $sdk->pharmacy->pharmacyAddPublicKey(
  input: $input,
  userId: "userId"
);

print_r($response);
```

## Pharmacy_AddUserRoles


- HTTP Method: `POST`
- Endpoint: `/v1/users/{userId}/roles`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| input | Models\PharmacyAddUserRolesRequest | ✅ |  |
| $userId | string | ✅ |  |

**Return Type**

`array`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;
use WellSyncServicesCareConnect\Models\PharmacyAddUserRolesRequest;

$sdk = new Client(accessToken: 'YOUR_TOKEN');


$input = new Models\PharmacyAddUserRolesRequest(
  roles: []
);

$response = $sdk->pharmacy->pharmacyAddUserRoles(
  input: $input,
  userId: "userId"
);

print_r($response);
```

## Pharmacy_RemoveUserRole


- HTTP Method: `DELETE`
- Endpoint: `/v1/users/{userId}/roles/{role}`

**Parameters**

| Name    | Type| Required | Description |
| :-------- | :----------| :----------| :----------|
| $userId | string | ✅ |  |
| $role | string | ✅ |  |

**Return Type**

`mixed`

**Example Usage Code Snippet**
```php
<?php

use WellSyncServicesCareConnect\Client;

$sdk = new Client(accessToken: 'YOUR_TOKEN');

$response = $sdk->pharmacy->pharmacyRemoveUserRole(
  userId: "userId",
  role: "role"
);

print_r($response);
```




<!-- This file was generated by liblab | https://liblab.com/ -->