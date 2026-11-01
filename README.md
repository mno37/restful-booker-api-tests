# Restful-Booker API Tests

Automated API test suite for Restful-Booker, a hotel booking API.

## Coverage

- Authentication (token-based login)
- CRUD operations:
  - Create (POST)
  - Read (GET)
  - Update (PUT, PATCH)
  - Delete (DELETE)
- Negative test cases (403 without token, 404 for non-existent booking)
- Query parameters (filtering bookings by name)
- HTML test report generated with Newman

## Tools

- Postman
- Newman
- Git
- GitHub
- VS Code

## How to Run

1. Install [Node.js](https://nodejs.org) (LTS version).
2. Install Newman and the HTML reporter:

   ```bash
   npm install -g newman newman-reporter-htmlextra
   ```

3. Run the tests and generate the report:

   ```bash
   newman run collections/Restful-Booker.postman_collection.json -e environments/Restful-Booker-Env.postman_environment.json -r htmlextra --reporter-htmlextra-export reports/report.html
   ```

4. Open `reports/report.html` in your browser.