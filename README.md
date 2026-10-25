Banking Payment API Lab
Hands-on API testing portfolio applying banking payment knowledge to REST API quality engineering.

The project uses a synthetic Oracle database exposed through Oracle REST Data Services (ORDS).

What This Project Demonstrates
REST API testing with Postman
OAuth 2.0 Client Credentials authentication
Role-protected ORDS endpoints
Positive and negative payment scenarios
JavaScript assertions using pm.test
Automatic access-token extraction and reuse
Reusable Postman environment variables
Authentication Flow
Postman sends Client ID and Client Secret to the ORDS OAuth endpoint.
Oracle ORDS returns an access token.
Postman saves the token in {{access_token}}.
Protected requests use Bearer {{access_token}}.
Expected results:

No token: 401 Unauthorized
Invalid token: 401 Unauthorized
Valid token: 200 OK
Covered Scenarios
OAuth access-token request
Protected endpoint without authorization
Payment-list inquiry
SEPA Credit Transfer
SEPA Instant Payment
Direct Debit
Invalid IBAN
Missing required field
Invalid SEPA currency
Payment status inquiry
Payment return
Repository Files
Payment-API-Quality-Portfolio.postman_collection.json
Oracle Payment API - Local.postman_environment.json
How to Run
Import the collection and environment into Postman.
Select the Oracle payment environment.
Add the required test credentials.
Run Get ORDS OAuth Token.
Run the protected payment requests.
Current Status
Implemented
Synthetic Oracle payment database
Oracle ORDS REST endpoints
Postman API collection
OAuth Client Credentials flow
Role-protected API
Automatic token handling
Positive and negative scenarios
In Progress
JavaScript assertions for all requests
Newman command-line execution
GitHub Actions CI pipeline
Automated test reports
Disclaimer
This is an independent portfolio project using synthetic data only. It contains no employer information, customer data or real banking records.
