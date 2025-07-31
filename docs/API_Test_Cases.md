# API Test Cases – JSONPlaceholder

This document contains detailed test cases for the JSONPlaceholder REST API endpoints.

---

## 📌 Endpoint: GET /posts

| TC ID | Test Scenario                      | Test Steps                        | Expected Result                      | Status |
| ----- | ---------------------------------- | --------------------------------- | ------------------------------------ | ------ |
| TC001 | Retrieve all posts                 | Send GET request to `/posts`      | Status 200, returns list of posts    | ✅     |
| TC002 | Retrieve a single post by valid ID | Send GET request to `/posts/1`    | Status 200, returns post with id = 1 | ✅     |
| TC003 | Retrieve post with invalid ID      | Send GET request to `/posts/9999` | Status 404 or empty object           | ✅     |

---

## 📌 Endpoint: POST /posts

| TC ID | Test Scenario                    | Test Steps                                             | Expected Result                              | Status |
| ----- | -------------------------------- | ------------------------------------------------------ | -------------------------------------------- | ------ |
| TC004 | Create a post with valid data    | Send POST request to `/posts` with valid JSON body     | Status 201, returns created post             | ✅     |
| TC005 | Create a post with missing title | Send POST request with only `body` and `userId` fields | Status 201, default/fake data returned       | ✅     |
| TC006 | Create a post with empty body    | Send POST request with `{}` as body                    | Status 201, server returns default/fake post | ✅     |

---

## 📌 Endpoint: PUT /posts/1

| TC ID | Test Scenario                     | Test Steps                                           | Expected Result                        | Status |
| ----- | --------------------------------- | ---------------------------------------------------- | -------------------------------------- | ------ |
| TC007 | Fully update a post               | Send PUT request to `/posts/1` with full JSON object | Status 200, updated post data returned | ✅     |
| TC008 | Update a post with missing fields | Send PUT request with only title or partial data     | Status 200, fields may be set to null  | ✅     |

---

## 📌 Endpoint: PATCH /posts/1

| TC ID | Test Scenario                 | Test Steps                                             | Expected Result                   | Status |
| ----- | ----------------------------- | ------------------------------------------------------ | --------------------------------- | ------ |
| TC009 | Partially update a post title | Send PATCH request with `{ "title": "Updated Title" }` | Status 200, returns updated title | ✅     |
| TC010 | Patch with invalid ID         | Send PATCH request to `/posts/9999`                    | Status 200 or empty response      | ✅     |

---

## 📌 Endpoint: DELETE /posts/1

| TC ID | Test Scenario           | Test Steps                           | Expected Result               | Status |
| ----- | ----------------------- | ------------------------------------ | ----------------------------- | ------ |
| TC011 | Delete an existing post | Send DELETE request to `/posts/1`    | Status 200 or 204, no content | ✅     |
| TC012 | Delete with invalid ID  | Send DELETE request to `/posts/9999` | Status 200 or empty response  | ✅     |

---

## ✅ Notes

- JSONPlaceholder is a **mock API**, so POST, PUT, PATCH, DELETE requests return fake responses.
- The data is not stored — testing is for request/response validation only.
- All expected results are based on observed default behaviors.

---

## 🧪 Future Coverage

- `/comments`
- `/users`
- Negative test cases with invalid methods (e.g., PUT on `/users`)

---

## 👨‍💻 Author

Jubair Rahman
