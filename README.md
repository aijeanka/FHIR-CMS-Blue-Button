# Project 2.10: CMS Data Access with Blue Button using FHIR

**Author**: Aizhan Uteubayeva (NetID: au198)  
**Published**: June 17, 2024

## Project Overview

This project involves accessing and retrieving patient data from the CMS Blue Button API using FHIR standards. The workflow includes registering a new application, authorizing API calls, and retrieving patient data using tools such as Postman.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Dependencies](#dependencies)
- [License](#license)

## Installation

1. **Register a New Application**
   - Register an account and create a new application at `http://localhost:3000`.

2. **Postman Setup**
   - Create an account with Postman.
   - Set up a new request with the necessary URL and authentication details.

## Usage

1. **New Application Setup**
   - Navigate to `http://localhost:3000` to register a new application.
   - Use the following details:
     - **Client ID** and **Client Secret** obtained during the registration.

2. **Authorization**
   - Navigate to the "Test Client" section.
   - Click on the authorization token to proceed.
   - Login to MyMedicare.gov using the provided credentials:
     - **Username**: BBUser20281
     - **Password**: PW20281!

3. **API Calls**
   - Use the following URL for API calls: `https://sandbox.bluebutton.cms.gov/v1/fhir/Patient/-19990000000001`.
   - Set up the authorization with OAuth 2.0.

4. **Token Information**
   - Use the following parameters to request a new token:
     - **Token Name**: appTestAU
     - **Grant Type**: Authorization Code
     - **Callback URL**: `http://localhost:3000`
     - **Auth URL**: `https://sandbox.bluebutton.cms.gov/v1/o/authorize/`
     - **Access Token URL**: `https://sandbox.bluebutton.cms.gov/v1/o/token/`
     - **Scope**: patient/Patient.read, patient/Coverage.read, patient/ExplanationOfBenefit.read, profile
     - **Client Authentication**: Send as Basic Auth header

5. **Retrieve Patient Data**
   - Use the obtained access token to make API calls and retrieve patient data.

## Features

- Register and set up a new application for accessing CMS Blue Button API.
- Authorize and authenticate API calls using OAuth 2.0.
- Retrieve patient data including demographics, coverage, and benefits.

## Dependencies

- **Postman**: For making API calls and testing endpoints.
- **OAuth 2.0**: For secure authorization and authentication.

## License

This project is licensed under the MIT License.
