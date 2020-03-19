# Application Programming Interface (API)
The API allows you to perform individual, household, email address, postal address, and phone number validations & verifications through multiple interfaces, or through a combined interface.

## Overview
For the latest information on the API, see VerificationPoint https://api.verificationpoint.com/

## Request Data
The request/input data required varies on your application and the validation process

## Payment
You will automatically be charged for each response returned. If you do not have any credits available, the API will not return any results.

## Response Data
All response/output data is returned as JSON.

# Endpoints
The following endpoints are for validation/verification processing.

## Single Endpoints
The following endpoints are for validation/verification of single entity data.

### Email Addresses
#### Request
/emailaddresses?email_address={email address to process}
#### Response


### Phone Numbers
#### Request
/phonenumbers?phone_number={phone number to process}

#### Response
<pre><code>
{
    "RecordId": 0,
    "PartyId": 7,
    "EmailAddress": "email@hotmail.com",
    "Valid": true,
    "Deliverable": true,
    "Role": false,
    "Free": true,
    "Isp": false,
    "Corporate": false,
    "Disposable": false,
    "Suppressed": false,
    "Screamer": false,
    "Global": false,
    "Trap": false,
    "UserName": "email",
    "DisplayName": "",
    "DomainName": "hotmail.com",
    "RootDomainName": "hotmail",
    "TopLevelDomainName": "com"
}
  </code>
