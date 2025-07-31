# API Test Plan

## Project Name

**API Testing Portfolio: JSONPlaceholder REST API**

## Prepared By

Jubair Rahman

## Date

[31st July, 2025]

---

## 1. Objective

The objective of this test plan is to validate the functionality, reliability, and behavior of the [JSONPlaceholder](https://jsonplaceholder.typicode.com/) REST API using Postman. The goal is to ensure the API endpoints return correct and expected responses for various request types including GET, POST, PUT, PATCH, and DELETE.

---

## 2. Scope

- Testing of available JSONPlaceholder endpoints related to `/posts`, `/comments`, `/users`
- Functional testing of HTTP methods:
  - GET
  - POST
  - PUT
  - PATCH
  - DELETE
- Request-response structure validation
- Negative testing and edge case handling

---

## 3. Test Items (Endpoints Under Test)

| Endpoint    | Method(s) Tested              |
| ----------- | ----------------------------- |
| /posts      | GET, POST, PUT, PATCH, DELETE |
| /posts/{id} | GET, PUT, PATCH, DELETE       |
| /comments   | GET, POST                     |
| /users      | GET                           |

---

## 4. Features to Be Tested

- Response status codes (200, 201, 404, 500)
- Response body content structure (JSON)
- Response time
- JSON schema validation
- Header verification (Content-Type, etc.)
- Negative testing (invalid IDs, missing fields, incorrect methods)

---

## 5. Approach

- Manual API testing using **Postman**
- Organized test cases per endpoint
- Use of Postman environment variables (if needed)
- Response validation using built-in tests (JavaScript assertions)
- Results captured with screenshots and exported reports

---

## 6. Deliverables

- Postman Collection (`postman_collection/jsonplaceholder_collection.json`)
- Test Cases Document (`docs/API_Test_Cases.md`)
- Test Summary Report (`docs/Test_Summary_Report.md`)
- Bug Report (`docs/Bug_Report.md`)
- Project README

---

## 7. Entry and Exit Criteria

**Entry Criteria**

- API is publicly accessible
- Swagger/API documentation is available
- Postman environment is ready

**Exit Criteria**

- All defined test cases executed
- No critical issues found in tested endpoints
- All deliverables are complete and uploaded to GitHub

---

## 8. Risks and Assumptions

**Risks:**

- Data is not persistent on the server (JSONPlaceholder returns fake success)
- No authentication or authorization layer

**Assumptions:**

- API responses are static
- API downtime is rare

---

## 9. Tools Used

- Postman
- GitHub
- Markdown editor (for documentation)

---

## 10. References

- [JSONPlaceholder Official Website](https://jsonplaceholder.typicode.com/)
- [Postman Docs](https://learning.postman.com/)
