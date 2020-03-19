# Application Programming Interface (API)
The API allows you to perform individual, household, email address, postal address, and phone number validations & verifications through multiple single interfaces, or through a combined interface.

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
<pre><code>
{
    "Address": "email@hotmail.com",
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
</code></pre>

### Phone Numbers
#### Request
/phonenumbers?phone_number={phone number to process}
#### Response
<pre><code>
{
    "Number": "1234567890",
    "Valid": true,
    "Connected": true,
    "AreaCode": "123",
    "State": "NY",
    "FederalSuppressed": false,
    "StateSuppressed": false,
}
</code></pre>

## Combined Endpoint
The following endpoints are for validation/verification of multiple entity data.

### Validations
#### Request
/validations?email_address={email address to process}&phone_number={phone number to process}
#### Response
The order of responses will always be the same.
<pre><code>
[
{
    "Address": "email@hotmail.com",
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
},
{
    "Number": "1234567890",
    "Valid": true,
    "Connected": true,
    "AreaCode": "123",
    "State": "NY",
    "FederalSuppressed": false,
    "StateSuppressed": false,
}
]
</code></pre>
